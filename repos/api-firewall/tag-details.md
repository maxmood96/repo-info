<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.6.14`](#api-firewall0614)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.6.14`

```console
$ docker pull api-firewall@sha256:dcf2cdf39bfd3519e389bd00836622f567bc50e293b103b168e176272d54a1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.14` - linux; amd64

```console
$ docker pull api-firewall@sha256:a61a72d941ee48fcaaf4005a58cc5f21c024b1f1676a17448721481f10da8bce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13745440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b45d10c801467ace93e32c3b57b5eca3eb9e1a3b17be19f8fe51ca54dceb39c`
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
# Sat, 27 Jan 2024 03:33:14 GMT
ENV APIFIREWALL_VERSION=v0.6.14
# Sat, 27 Jan 2024 03:33:16 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='d42c2350217da3831e227f5d9e20adbace1a262fc7f94fb46d9de1b8bf5e5548';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='83716032269cf05ba916c0a91c384527ea23f527f5cfb1cde61b0687d41145e5';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ccfb44e9cfd06a9a21c3b7c283e95890e94b5f0011b73b7e64f86638475efd97';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Sat, 27 Jan 2024 03:33:17 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Sat, 27 Jan 2024 03:33:17 GMT
USER api-firewall
# Sat, 27 Jan 2024 03:33:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:33:17 GMT
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
	-	`sha256:1806772afc43fa7b57eee68a7227d6b5305fbed8f465cbd8eb9e8d27c2a691df`  
		Last Modified: Sat, 27 Jan 2024 03:33:27 GMT  
		Size: 10.3 MB (10341340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a55cf8c5ea1950ed8c54f89269eb5d9bdba3674e51a0d288395568f44c3a7d`  
		Last Modified: Sat, 27 Jan 2024 03:33:25 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.14` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:48df05bd0e7a66758bb971d03bab42dce1a7c5b3a246cc01774f19964e4ddb88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12932447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61a0994f1b88b6f4049f9c2beb96a1d19f37093570c7ded6ad75a961bcd41bf`
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
# Sat, 27 Jan 2024 00:38:38 GMT
ENV APIFIREWALL_VERSION=v0.6.14
# Sat, 27 Jan 2024 00:38:40 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='d42c2350217da3831e227f5d9e20adbace1a262fc7f94fb46d9de1b8bf5e5548';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='83716032269cf05ba916c0a91c384527ea23f527f5cfb1cde61b0687d41145e5';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ccfb44e9cfd06a9a21c3b7c283e95890e94b5f0011b73b7e64f86638475efd97';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Sat, 27 Jan 2024 00:38:40 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Sat, 27 Jan 2024 00:38:41 GMT
USER api-firewall
# Sat, 27 Jan 2024 00:38:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:38:41 GMT
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
	-	`sha256:0ee88421fa1b69cd999a8880ad15f0990b31124893374b818c26d8355b8462c6`  
		Last Modified: Sat, 27 Jan 2024 00:38:49 GMT  
		Size: 9.6 MB (9597533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acdb78322b5634ae43eb2662c7bd60701243ab85950b1b95fa580aa733a498c`  
		Last Modified: Sat, 27 Jan 2024 00:38:48 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.14` - linux; 386

```console
$ docker pull api-firewall@sha256:a54201dbf09f242d10810f6a8ddd1a797bf940c1bfc4a052a8f9b3366da841a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12243578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316960d09f21195f6aa074b6a80366b422e1081089d5167adce8df666b9c2b4b`
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
# Sat, 27 Jan 2024 04:24:21 GMT
ENV APIFIREWALL_VERSION=v0.6.14
# Sat, 27 Jan 2024 04:24:23 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='d42c2350217da3831e227f5d9e20adbace1a262fc7f94fb46d9de1b8bf5e5548';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='83716032269cf05ba916c0a91c384527ea23f527f5cfb1cde61b0687d41145e5';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ccfb44e9cfd06a9a21c3b7c283e95890e94b5f0011b73b7e64f86638475efd97';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Sat, 27 Jan 2024 04:24:23 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Sat, 27 Jan 2024 04:24:24 GMT
USER api-firewall
# Sat, 27 Jan 2024 04:24:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 04:24:24 GMT
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
	-	`sha256:a9286a66641e316b159bb4f0d6c17806b20033d317f41f9c2c0c0993d0427aad`  
		Last Modified: Sat, 27 Jan 2024 04:24:32 GMT  
		Size: 9.0 MB (9002953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2475e8ea618303a37021eec2ed28311574be0ee899eb95aae255c94bf1f8f31`  
		Last Modified: Sat, 27 Jan 2024 04:24:30 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:dcf2cdf39bfd3519e389bd00836622f567bc50e293b103b168e176272d54a1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:a61a72d941ee48fcaaf4005a58cc5f21c024b1f1676a17448721481f10da8bce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13745440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b45d10c801467ace93e32c3b57b5eca3eb9e1a3b17be19f8fe51ca54dceb39c`
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
# Sat, 27 Jan 2024 03:33:14 GMT
ENV APIFIREWALL_VERSION=v0.6.14
# Sat, 27 Jan 2024 03:33:16 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='d42c2350217da3831e227f5d9e20adbace1a262fc7f94fb46d9de1b8bf5e5548';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='83716032269cf05ba916c0a91c384527ea23f527f5cfb1cde61b0687d41145e5';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ccfb44e9cfd06a9a21c3b7c283e95890e94b5f0011b73b7e64f86638475efd97';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Sat, 27 Jan 2024 03:33:17 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Sat, 27 Jan 2024 03:33:17 GMT
USER api-firewall
# Sat, 27 Jan 2024 03:33:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:33:17 GMT
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
	-	`sha256:1806772afc43fa7b57eee68a7227d6b5305fbed8f465cbd8eb9e8d27c2a691df`  
		Last Modified: Sat, 27 Jan 2024 03:33:27 GMT  
		Size: 10.3 MB (10341340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a55cf8c5ea1950ed8c54f89269eb5d9bdba3674e51a0d288395568f44c3a7d`  
		Last Modified: Sat, 27 Jan 2024 03:33:25 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:48df05bd0e7a66758bb971d03bab42dce1a7c5b3a246cc01774f19964e4ddb88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12932447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61a0994f1b88b6f4049f9c2beb96a1d19f37093570c7ded6ad75a961bcd41bf`
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
# Sat, 27 Jan 2024 00:38:38 GMT
ENV APIFIREWALL_VERSION=v0.6.14
# Sat, 27 Jan 2024 00:38:40 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='d42c2350217da3831e227f5d9e20adbace1a262fc7f94fb46d9de1b8bf5e5548';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='83716032269cf05ba916c0a91c384527ea23f527f5cfb1cde61b0687d41145e5';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ccfb44e9cfd06a9a21c3b7c283e95890e94b5f0011b73b7e64f86638475efd97';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Sat, 27 Jan 2024 00:38:40 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Sat, 27 Jan 2024 00:38:41 GMT
USER api-firewall
# Sat, 27 Jan 2024 00:38:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:38:41 GMT
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
	-	`sha256:0ee88421fa1b69cd999a8880ad15f0990b31124893374b818c26d8355b8462c6`  
		Last Modified: Sat, 27 Jan 2024 00:38:49 GMT  
		Size: 9.6 MB (9597533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acdb78322b5634ae43eb2662c7bd60701243ab85950b1b95fa580aa733a498c`  
		Last Modified: Sat, 27 Jan 2024 00:38:48 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:a54201dbf09f242d10810f6a8ddd1a797bf940c1bfc4a052a8f9b3366da841a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12243578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316960d09f21195f6aa074b6a80366b422e1081089d5167adce8df666b9c2b4b`
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
# Sat, 27 Jan 2024 04:24:21 GMT
ENV APIFIREWALL_VERSION=v0.6.14
# Sat, 27 Jan 2024 04:24:23 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='d42c2350217da3831e227f5d9e20adbace1a262fc7f94fb46d9de1b8bf5e5548';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='83716032269cf05ba916c0a91c384527ea23f527f5cfb1cde61b0687d41145e5';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ccfb44e9cfd06a9a21c3b7c283e95890e94b5f0011b73b7e64f86638475efd97';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Sat, 27 Jan 2024 04:24:23 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Sat, 27 Jan 2024 04:24:24 GMT
USER api-firewall
# Sat, 27 Jan 2024 04:24:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 04:24:24 GMT
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
	-	`sha256:a9286a66641e316b159bb4f0d6c17806b20033d317f41f9c2c0c0993d0427aad`  
		Last Modified: Sat, 27 Jan 2024 04:24:32 GMT  
		Size: 9.0 MB (9002953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2475e8ea618303a37021eec2ed28311574be0ee899eb95aae255c94bf1f8f31`  
		Last Modified: Sat, 27 Jan 2024 04:24:30 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
