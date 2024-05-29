<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-1809`](#caddy2-builder-windowsservercore-1809)
-	[`caddy:2-builder-windowsservercore-ltsc2022`](#caddy2-builder-windowsservercore-ltsc2022)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-1809`](#caddy2-windowsservercore-1809)
-	[`caddy:2-windowsservercore-ltsc2022`](#caddy2-windowsservercore-ltsc2022)
-	[`caddy:2.8`](#caddy28)
-	[`caddy:2.8-alpine`](#caddy28-alpine)
-	[`caddy:2.8-builder`](#caddy28-builder)
-	[`caddy:2.8-builder-alpine`](#caddy28-builder-alpine)
-	[`caddy:2.8-builder-windowsservercore-1809`](#caddy28-builder-windowsservercore-1809)
-	[`caddy:2.8-builder-windowsservercore-ltsc2022`](#caddy28-builder-windowsservercore-ltsc2022)
-	[`caddy:2.8-windowsservercore`](#caddy28-windowsservercore)
-	[`caddy:2.8-windowsservercore-1809`](#caddy28-windowsservercore-1809)
-	[`caddy:2.8-windowsservercore-ltsc2022`](#caddy28-windowsservercore-ltsc2022)
-	[`caddy:2.8.0`](#caddy280)
-	[`caddy:2.8.0-alpine`](#caddy280-alpine)
-	[`caddy:2.8.0-builder`](#caddy280-builder)
-	[`caddy:2.8.0-builder-alpine`](#caddy280-builder-alpine)
-	[`caddy:2.8.0-builder-windowsservercore-1809`](#caddy280-builder-windowsservercore-1809)
-	[`caddy:2.8.0-builder-windowsservercore-ltsc2022`](#caddy280-builder-windowsservercore-ltsc2022)
-	[`caddy:2.8.0-windowsservercore`](#caddy280-windowsservercore)
-	[`caddy:2.8.0-windowsservercore-1809`](#caddy280-windowsservercore-1809)
-	[`caddy:2.8.0-windowsservercore-ltsc2022`](#caddy280-windowsservercore-ltsc2022)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:builder-alpine`](#caddybuilder-alpine)
-	[`caddy:builder-windowsservercore-1809`](#caddybuilder-windowsservercore-1809)
-	[`caddy:builder-windowsservercore-ltsc2022`](#caddybuilder-windowsservercore-ltsc2022)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-1809`](#caddywindowsservercore-1809)
-	[`caddy:windowsservercore-ltsc2022`](#caddywindowsservercore-ltsc2022)

## `caddy:2`

```console
$ docker pull caddy@sha256:236c6a30ccb84fa412a5360ca8b586d804faba0621ea182fb45902608cd8a563
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:7b51768d110708c44179dc299884e9ee73d243a37abccce2dc796abc36371a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18476986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e21ce508b7f91169630895a0fe9a9f58288e5eb6e899c3462f168229c84193`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88463a31d6d2c104349aaaaae3b5a60c2a63ba0ac2712ba190211e9cd15d4cc`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 360.6 KB (360570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de93e10dd6701c976a78596c69babad750fc3957060c758b8859daab7fd2dd27`  
		Last Modified: Thu, 02 May 2024 00:51:57 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae96b49a2d955ff25ddc1858d84596c16d525d531d2342bd372945ccf5e410`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 14.7 MB (14706390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:666c65a5f3beaff567eaca64d4f307c64b81695485a64ad5d33ac192c1b299e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfba4fe57beaf0920d15623535056bcc81e42e1ac5eacec9827a7932a15bc94b`

```dockerfile
```

-	Layers:
	-	`sha256:0f942a2c6c2e9440173dadc3211a6cecf73e846edcdcb423bffad328d9c8727e`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 268.9 KB (268899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f88d335506cc1ae671b94135d1dff65cbb966f39e5145fe171d82377ea601c1`  
		Last Modified: Thu, 02 May 2024 00:51:57 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a37e44b94565539d082d85ceab947792effbecc9d7db223ea6abca196ee05a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17432782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b5570c733ff428231e40e91550787c9f5ddc4bb728f09cb7effb937964fa7d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320944b9d89ce73b5dbd09f5e7a6041004d85f4bef04eb1417a27e8a24f13f5b`  
		Last Modified: Wed, 01 May 2024 21:56:04 GMT  
		Size: 357.3 KB (357340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe068432b49975aecbf4e69d7736019056ee4d62a52931a724ff06f70e86c25`  
		Last Modified: Thu, 02 May 2024 00:56:31 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb925eb8f3d094c61b238fe90aca158009b859c95c7e87ff0cad1f810e65aa9`  
		Last Modified: Thu, 02 May 2024 00:56:32 GMT  
		Size: 13.9 MB (13920901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:29db70769c20c963daa30568350c31fc72970c036d8e8a0d7a7a8a47d275300e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58dc3b1df0157f859652c398af09ae3a777bb2fb92015e0f62436f9e993a7e54`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb7c30b377cc96f8036dbe70e0f8d249776fdbc6cac9bf32c4ba0e42eaa843`  
		Last Modified: Thu, 02 May 2024 00:56:31 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:3d1e889eda417007d88637f9adca7509e5bb547492e555d4a758ce2df850a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17156262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3523597ee5af2fd110570a00e504f5e22dd8704d65c7c8778bc0c9ef96ae269`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b527911aa0f8852117f57452d522fb961c184d105b0818cb4a87109b08272643`  
		Last Modified: Wed, 01 May 2024 22:05:53 GMT  
		Size: 353.7 KB (353705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ab12f0e1a27e1224e11b4fc25b25dc760337a04bb0883175300b1a8842aff2`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fa49870fc1f8bcbe7983ca022544c47da797299179b3287255e96b1254a28d`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 13.9 MB (13893683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:1f74bd28526188e78a3ee7ac25ba3de34683b3251d1e0b495cc33270910d6d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060e4e44fb56999c235e64a72bcb39cc3db4a016d5e7307bb82c1a31106afb75`

```dockerfile
```

-	Layers:
	-	`sha256:eeda73bc8fa144234fa52e9915e531709e0b3d01b8aa6ed8dabfbeaa03d8ec52`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 269.0 KB (268967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039dd7674e2f60b9d2f360db16a7759fb38a2b8153fda85eff01c915c1da050e`  
		Last Modified: Thu, 02 May 2024 01:08:17 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:578dcc962eb6776e3e6ed964d11a13d40983f294e590f0040fc9febce144fa3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17278610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220a025aa536c6d9e845318ec54c7969a55f365311b36886f0eed8b3a218012`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f50788699932589070b139144f3b1440a2948fa84be4ca81ecdc1d1a54e4e69`  
		Last Modified: Wed, 01 May 2024 22:12:04 GMT  
		Size: 368.8 KB (368765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b07f03c61a8e689485aedd78191737c91a5f2f23e95122ca9de2af436c14c`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef67f47d4ab395e9c3fa86967774f6a1f31b10e560ad19c1a48b64db88bb6ee0`  
		Last Modified: Thu, 02 May 2024 04:53:38 GMT  
		Size: 13.6 MB (13569000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:38001a08c78526af0f51525a1f82a25923b94559287782c232932bff2c9a6682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b174326e15ad188a5fc078e50318dbccac12850ef07b98ac27e0ccdf2b05e9`

```dockerfile
```

-	Layers:
	-	`sha256:93cfedcf72234e144ba3ae74894f78ff082dc5b8330cbd00229c9377c80c9d93`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 268.9 KB (268918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a58d69a87e8d3b310715fe89231c5f8d7a4d5d6ee5add7d9a97ea9273937afa`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 17.6 KB (17552 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:2c0050449fe45c8df3fa0b90fa1621dd8fb2de864d8154aa379c73b71d1ee769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17060083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913f3ac3d369a2d5a24e332dec6da8cbca6f9d6c570768127927ee62e7aa7770`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0550c488b324bf74512534b8af77dc0690e94dd12f1286c76669cb03c733692`  
		Last Modified: Wed, 01 May 2024 22:06:02 GMT  
		Size: 370.3 KB (370278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f53ff24ab7a11bdbef2dbc4774bd8c9241c60f282247607ac7401ec586a681`  
		Last Modified: Thu, 02 May 2024 01:07:51 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30849c5c1ec8a58215a8ad6e5f79db3be0b1d9c9f843dcd81c42748732a39917`  
		Last Modified: Thu, 02 May 2024 01:07:52 GMT  
		Size: 13.3 MB (13333836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:09f14bafcec41acaf23fa3fbfcb3542d754279ff9bcd6994883dd551a91d9118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 KB (284603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e3abe481d46e34ec2db9e2960600548a2a65472765919c636e793baecc365e`

```dockerfile
```

-	Layers:
	-	`sha256:d8a5956a258ed188944c638c13de5928c93ec3795de1dbc3881214c0ddb98063`  
		Last Modified: Thu, 02 May 2024 01:07:52 GMT  
		Size: 267.0 KB (267003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24c13f8f699644b031a10dbed52d9ed326c7dde29529b70a82bb603d2677989`  
		Last Modified: Thu, 02 May 2024 01:07:51 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:faab60dc3a1acc475e2d0f12c86d9f31290b49896611d5cd61feb631ea7b0b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17828011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6446726caf9ff49671c1b47b04ff608cc10c783fd3dbf2a2d79d816140cb2ea`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7649425a6a944a0c8c4f452b8bc1e2874e0e99c7e097d2aec191fb8ac784fd6d`  
		Last Modified: Wed, 01 May 2024 22:05:37 GMT  
		Size: 364.7 KB (364696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df358d50a949fe6c09ee403e747cafa7b4bcdac928dbb75cee120ea25330f4`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc640f077739a0d0aa11a1722064f9f3d5dfc31ffc720787fe16c78e49d827`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 14.2 MB (14238300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:a941d2a34e67bad02c9ee6d9cb55c09fccf5ae73670d0c5cf653ba2457ae8cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 KB (284475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76679ae3672baef460ec34615d3960669d3d95e73990aeddf0e2d5bd8573af8`

```dockerfile
```

-	Layers:
	-	`sha256:144c0dfb68c151b0a1b0c92da22a910fb7b8e8cc63389ab9b7e180d746bbf9c2`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 266.9 KB (266941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958b331e0cf47b7621d5c63aafb1753bf1abd52d632a23dd19e986657b53c310`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e2f8b997d964717694810a581f3548bb7c88de368a40ad9de4f8ed414fa2c8bc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128741780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48489f36ce94641f6ce5703ea4babbd5e2e2ec4dbffc55809b7eb8c1c1508cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:03:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:03:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 22:04:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:04:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 22:04:09 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 22:04:10 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 22:04:10 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 22:04:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 22:04:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 22:04:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 80
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 443
# Wed, 15 May 2024 22:04:17 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 22:04:18 GMT
EXPOSE 2019
# Wed, 15 May 2024 22:04:22 GMT
RUN caddy version
# Wed, 15 May 2024 22:04:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cabe3592a5a508b32120c2f3f50485ce2af3e5b977d817fa71bff28061336aa`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7474cb4a8c303c68700f525e09e3bd29bb30d75dc33c01ea4a44732e7e7423f7`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 364.6 KB (364646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6d09183adf4d940c7dac96cc9d75af33bcb47d7d1811a7a296ad60e0d1b1c`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ce5e1d365ba13fb9103a5020b6644b3ae71e76d5e4d159b2f58914673cf2bf`  
		Last Modified: Wed, 15 May 2024 22:04:31 GMT  
		Size: 15.3 MB (15344884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aded66dd078b571ebb532e084c4af4f6beb685bd8a5b7524468e97c168f1a5`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37260cc3f9937e208886001176fd42c7113d3d49bdfd01a29d269126dc8538b4`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c851cec2c829abe440fde3ba79f95ec4728dfa01da5cb2b09e817e7581dc6b`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358cdf5957564add30758b73811ebe0f230cea2692cbb624fb5e8c369dcacc32`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b6a2684656992e4dbd6e42d4dd8ee988d00626cd55d362075a3a9243af3b54`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccb203e5de222a30a89c733e9964e55090c4ff8911cd1ccd005de5e27d7523`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097f79242227f6445dd34eaf655c51b48ce991b72a1ff5589b72787ee42f0fee`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e44fe3122406544397fc58d026c1cbeea8aec0444aaa6d12a759f86d4714c4`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401e6d173f17fd472a9adf0f3ce231ed4fa53e327b3fbd222c6900a64dc1573`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571e94ebd3fc2965298bc42c3810c16d0f6f6c9743a4b5aea94dc66e91aad8e2`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484373c77dd756bb7eb292a32b21c4039a936fdd0871ca3bc6c7467fcf29c77f`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9921976cbc4a4e3222ce034a2dbd34e498f4bc4fc93f52173e5339e8fb9571`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca02ad3a0dd4ff383e5fe8cef81201aa747f513bd724391e69d4272e441fb1c3`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0fb2e91e46705b26409f246c0bf3647718c5187bb6ffa4c5dafddfc2a2edd`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca09518406089c86c645aa571b37a75799b274b772b04a8fef6703ffbf76ef3b`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 338.9 KB (338919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd845c75155a3609f78ca6b64788a35f72e73fb0c060ee22b4dd7b4be922372f`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:39ca8d38bb88e8ba8d04cd6eeeff4530e4db12daa30aa37e9a0c216a3e2bcfcd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195917858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d1ee2064b2ba3276dc02e0d45d90e35c36d900905b3034b07989d7ed715418`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:53:10 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 21:53:11 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 21:53:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 21:53:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 21:53:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 21:53:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 21:53:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 21:53:47 GMT
EXPOSE 80
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 21:53:49 GMT
EXPOSE 2019
# Wed, 15 May 2024 21:54:15 GMT
RUN caddy version
# Wed, 15 May 2024 21:54:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf806c2d672572084312cc8aa494c8cec9af9daeed5057140149ccdd78dfb80`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b711793313f153495eabe6635f5e8f65dc570d25985f5f6f5ef8c5c0a553b3`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 490.6 KB (490620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d512e0e145af2eec1bd2d32a9b70d48703e256b6d9f9d9199a3a7f36a6c9ff`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4f52645186abe39ac028b27c3e9ffdd710c940ddd12cbbf6d0d29065a18491`  
		Last Modified: Wed, 15 May 2024 21:54:23 GMT  
		Size: 15.3 MB (15345743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa23f4c47c349e446197c7316ed9a453a261ab1fdd2c0e3f6d97d0992d65bdef`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97aa1e7097461ea94ece8afce1dd51ee1513ef285e26743e89614b29a473ed`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576b04f13aae77f986a510a286ba44a00cca8d03b5fffdd0cd881ff59ace8a29`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e02a14a1675118d3895f8691bae0b4c39b9fb31f41a7cee00b3ee9d5d4c6c88`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029ead0bd0493b4a27aca7d5c7dca9fd26f0cc230fe67e95131782faf30b3c7`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be7a0a749e1ab96c5b49167c6b4740f6dc3bd739e58052f848e479c157bbf16`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dc01200272cf83484b850657355cb0afd45801fd642b0e293ddd0a66f5bc6e`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff9d61cc398e1efd41ad219b45a7b7954fdca6b77c3641a047a7d3bba2d24ca`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdefed17ab78afabf07e8a0de1c83420d9eb0a05a6a13b1bd7c6e4f42b785ff`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a28a34a28f7595618aa6579263ace412ec6492a68f265fb56920fb0f52e98e`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e3072da47a79873523ce57465acf158d0f749d150dc2c354873ef27355441a`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709eb7f911c45eec7a80d9be6b73eb9c5b76c363f768c6b678b5e5ec589fb7e0`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118c06d85763da95dd5181f248564978ab3507b219ffb98f85c7473509bec42`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec0cdeef31f251bce3d39ed741232e9eb28b233af8a7373cf3c706afbfbbab4`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb36f279201594c9a4f90cc70e1669eb98c980e9582e2bb7b53fd70ec5071dda`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 348.0 KB (348008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a72e74ca019379f2a07ba0eaa7e4164da0d80823fab977d9182936d89dcf225`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:2e1d4592f1718bb47645da5a83a846fe19094f18e6c921fdf56d174f05c63213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:7b51768d110708c44179dc299884e9ee73d243a37abccce2dc796abc36371a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18476986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e21ce508b7f91169630895a0fe9a9f58288e5eb6e899c3462f168229c84193`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88463a31d6d2c104349aaaaae3b5a60c2a63ba0ac2712ba190211e9cd15d4cc`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 360.6 KB (360570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de93e10dd6701c976a78596c69babad750fc3957060c758b8859daab7fd2dd27`  
		Last Modified: Thu, 02 May 2024 00:51:57 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae96b49a2d955ff25ddc1858d84596c16d525d531d2342bd372945ccf5e410`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 14.7 MB (14706390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:666c65a5f3beaff567eaca64d4f307c64b81695485a64ad5d33ac192c1b299e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfba4fe57beaf0920d15623535056bcc81e42e1ac5eacec9827a7932a15bc94b`

```dockerfile
```

-	Layers:
	-	`sha256:0f942a2c6c2e9440173dadc3211a6cecf73e846edcdcb423bffad328d9c8727e`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 268.9 KB (268899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f88d335506cc1ae671b94135d1dff65cbb966f39e5145fe171d82377ea601c1`  
		Last Modified: Thu, 02 May 2024 00:51:57 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a37e44b94565539d082d85ceab947792effbecc9d7db223ea6abca196ee05a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17432782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b5570c733ff428231e40e91550787c9f5ddc4bb728f09cb7effb937964fa7d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320944b9d89ce73b5dbd09f5e7a6041004d85f4bef04eb1417a27e8a24f13f5b`  
		Last Modified: Wed, 01 May 2024 21:56:04 GMT  
		Size: 357.3 KB (357340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe068432b49975aecbf4e69d7736019056ee4d62a52931a724ff06f70e86c25`  
		Last Modified: Thu, 02 May 2024 00:56:31 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb925eb8f3d094c61b238fe90aca158009b859c95c7e87ff0cad1f810e65aa9`  
		Last Modified: Thu, 02 May 2024 00:56:32 GMT  
		Size: 13.9 MB (13920901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:29db70769c20c963daa30568350c31fc72970c036d8e8a0d7a7a8a47d275300e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58dc3b1df0157f859652c398af09ae3a777bb2fb92015e0f62436f9e993a7e54`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb7c30b377cc96f8036dbe70e0f8d249776fdbc6cac9bf32c4ba0e42eaa843`  
		Last Modified: Thu, 02 May 2024 00:56:31 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:3d1e889eda417007d88637f9adca7509e5bb547492e555d4a758ce2df850a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17156262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3523597ee5af2fd110570a00e504f5e22dd8704d65c7c8778bc0c9ef96ae269`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b527911aa0f8852117f57452d522fb961c184d105b0818cb4a87109b08272643`  
		Last Modified: Wed, 01 May 2024 22:05:53 GMT  
		Size: 353.7 KB (353705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ab12f0e1a27e1224e11b4fc25b25dc760337a04bb0883175300b1a8842aff2`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fa49870fc1f8bcbe7983ca022544c47da797299179b3287255e96b1254a28d`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 13.9 MB (13893683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1f74bd28526188e78a3ee7ac25ba3de34683b3251d1e0b495cc33270910d6d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060e4e44fb56999c235e64a72bcb39cc3db4a016d5e7307bb82c1a31106afb75`

```dockerfile
```

-	Layers:
	-	`sha256:eeda73bc8fa144234fa52e9915e531709e0b3d01b8aa6ed8dabfbeaa03d8ec52`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 269.0 KB (268967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039dd7674e2f60b9d2f360db16a7759fb38a2b8153fda85eff01c915c1da050e`  
		Last Modified: Thu, 02 May 2024 01:08:17 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:578dcc962eb6776e3e6ed964d11a13d40983f294e590f0040fc9febce144fa3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17278610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220a025aa536c6d9e845318ec54c7969a55f365311b36886f0eed8b3a218012`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f50788699932589070b139144f3b1440a2948fa84be4ca81ecdc1d1a54e4e69`  
		Last Modified: Wed, 01 May 2024 22:12:04 GMT  
		Size: 368.8 KB (368765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b07f03c61a8e689485aedd78191737c91a5f2f23e95122ca9de2af436c14c`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef67f47d4ab395e9c3fa86967774f6a1f31b10e560ad19c1a48b64db88bb6ee0`  
		Last Modified: Thu, 02 May 2024 04:53:38 GMT  
		Size: 13.6 MB (13569000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:38001a08c78526af0f51525a1f82a25923b94559287782c232932bff2c9a6682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b174326e15ad188a5fc078e50318dbccac12850ef07b98ac27e0ccdf2b05e9`

```dockerfile
```

-	Layers:
	-	`sha256:93cfedcf72234e144ba3ae74894f78ff082dc5b8330cbd00229c9377c80c9d93`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 268.9 KB (268918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a58d69a87e8d3b310715fe89231c5f8d7a4d5d6ee5add7d9a97ea9273937afa`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 17.6 KB (17552 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:2c0050449fe45c8df3fa0b90fa1621dd8fb2de864d8154aa379c73b71d1ee769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17060083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913f3ac3d369a2d5a24e332dec6da8cbca6f9d6c570768127927ee62e7aa7770`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0550c488b324bf74512534b8af77dc0690e94dd12f1286c76669cb03c733692`  
		Last Modified: Wed, 01 May 2024 22:06:02 GMT  
		Size: 370.3 KB (370278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f53ff24ab7a11bdbef2dbc4774bd8c9241c60f282247607ac7401ec586a681`  
		Last Modified: Thu, 02 May 2024 01:07:51 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30849c5c1ec8a58215a8ad6e5f79db3be0b1d9c9f843dcd81c42748732a39917`  
		Last Modified: Thu, 02 May 2024 01:07:52 GMT  
		Size: 13.3 MB (13333836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:09f14bafcec41acaf23fa3fbfcb3542d754279ff9bcd6994883dd551a91d9118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 KB (284603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e3abe481d46e34ec2db9e2960600548a2a65472765919c636e793baecc365e`

```dockerfile
```

-	Layers:
	-	`sha256:d8a5956a258ed188944c638c13de5928c93ec3795de1dbc3881214c0ddb98063`  
		Last Modified: Thu, 02 May 2024 01:07:52 GMT  
		Size: 267.0 KB (267003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24c13f8f699644b031a10dbed52d9ed326c7dde29529b70a82bb603d2677989`  
		Last Modified: Thu, 02 May 2024 01:07:51 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:faab60dc3a1acc475e2d0f12c86d9f31290b49896611d5cd61feb631ea7b0b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17828011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6446726caf9ff49671c1b47b04ff608cc10c783fd3dbf2a2d79d816140cb2ea`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7649425a6a944a0c8c4f452b8bc1e2874e0e99c7e097d2aec191fb8ac784fd6d`  
		Last Modified: Wed, 01 May 2024 22:05:37 GMT  
		Size: 364.7 KB (364696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df358d50a949fe6c09ee403e747cafa7b4bcdac928dbb75cee120ea25330f4`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc640f077739a0d0aa11a1722064f9f3d5dfc31ffc720787fe16c78e49d827`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 14.2 MB (14238300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a941d2a34e67bad02c9ee6d9cb55c09fccf5ae73670d0c5cf653ba2457ae8cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 KB (284475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76679ae3672baef460ec34615d3960669d3d95e73990aeddf0e2d5bd8573af8`

```dockerfile
```

-	Layers:
	-	`sha256:144c0dfb68c151b0a1b0c92da22a910fb7b8e8cc63389ab9b7e180d746bbf9c2`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 266.9 KB (266941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958b331e0cf47b7621d5c63aafb1753bf1abd52d632a23dd19e986657b53c310`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:c4ca919a359a82291778345c9886a9cf948d4e4613aee402066f0be8819179ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:2d0f98ee37151fac228829512d71cd60683bcca714b42a2accfd5b2ed0eef309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77076844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da2caebf0c82328df2582d2154aea90549512f5f8075a1d211888861edc36d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ea3408117e6ad5da2610d98c7aaaa6ab17d9280a7f00e54b78f4a8af1a13e6`  
		Last Modified: Tue, 14 May 2024 22:57:18 GMT  
		Size: 293.4 KB (293394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91320369b822ebdafa53385de29218150ed2e0c9432c803ae9ab0917b1c13e05`  
		Last Modified: Tue, 14 May 2024 22:57:19 GMT  
		Size: 67.0 MB (67007431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0406650e82959e8bef670a6825ebc6caab141ed9ad0670923af9d5998de85b1b`  
		Last Modified: Tue, 14 May 2024 22:57:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54b29b355af23f51f47454c3e17573db8b78d7b52ce85f0455a2e39d7fa074`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 5.0 MB (4973399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbee18c299cb69dbccc6437fb935315abe5ea1a53244f52a8ef81bf71b3ec7c`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 1.4 MB (1399486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3962e3b1e39ca0549762f19fbf5ce97673a3c8e25e572443e99130f629becf`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:6f76e9858ca4547fe58ff97bd2ffc98029feb869b1dfc98633fd6f628b314292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 KB (288373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d01d8efed7000405f724e82795e9cc915343e431cc02e71f7cb5c25dc349bc`

```dockerfile
```

-	Layers:
	-	`sha256:746b0306cd3cb1912a3fc855ffc1003e09c16f75c165c8632bfe6eb00f877847`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 268.0 KB (268019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8416aff5ff51dc4e8fe28c6decdd0e3d91752160f7da7909a202850f8bd690`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ac7c2575373554f84061a11c48e068678edf889b364d17fc18cae4e80ce71e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75488808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48147857ead25ab7ee7a77aa74a59e293fa9eca878fe8afdd536d5f143675028`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c253e1ccd740370512ac16dc1198d4cc7e5f79502d830e914be781d2a53ef`  
		Last Modified: Tue, 14 May 2024 23:02:34 GMT  
		Size: 294.1 KB (294052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d6f1f07c341f159f464047d7dfc24c2fe15b8492e49ca6864e4bb242a3ec8`  
		Last Modified: Tue, 14 May 2024 23:03:32 GMT  
		Size: 65.8 MB (65766197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ab3f344a28c5c3a77d5b42ed139c704c1a62bb86a51a6d424570cbeddca4f3`  
		Last Modified: Tue, 14 May 2024 23:04:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b167340b71c005d807677fbbfbac662cedcb4fec7ccda3d644fa2d7cd2160000`  
		Last Modified: Tue, 14 May 2024 23:59:49 GMT  
		Size: 5.0 MB (4959292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db00701b53c1d5eee7ae5f0370ad0e2bf8c7624155e1ccd2197c482e47a9b928`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 1.3 MB (1321618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3610115cc7dedfcb5e2e244108591d41fbe0430d9c192503193a6f2a0e0c62`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:65e3693b278d4ef7c1c71f462d35e072feb067d47d882a6357051558d5f46278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 KB (20292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883db6588355f9fff45c61143a3c184d6b5360f70087363d292d63c4ffd73363`

```dockerfile
```

-	Layers:
	-	`sha256:f9d8b3568f220dfd1bdb1ddf4e41df2a13ced2a403b7245c9a18e0b60d52fd7b`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 20.3 KB (20292 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:09a6c1b0e1bd5044d5c064715c0aa03b90e6940ba650cf16faef929b3f79fa04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74794769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a0acea946d5a81787cb9fe18c7071c5aa68a591344d13571c0ce51a5e470d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1e32b4becad7a3ff9750dab0a6195a4136fe3417839cd5d6ced26f77c37d79`  
		Last Modified: Wed, 15 May 2024 08:39:33 GMT  
		Size: 293.0 KB (292954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab304151744566becd5140e866f02946274de2d4d2a228bdba72a0e4dddfa248`  
		Last Modified: Wed, 15 May 2024 08:40:52 GMT  
		Size: 65.8 MB (65766163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ceb4452378bf5d66c4470fe48fe8427a79ec5fdc8ddb8ea1c7fc02a13ce65b`  
		Last Modified: Wed, 15 May 2024 08:43:33 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270f12d361d5c63e9937439d8ff8f1080a9e9af98e31682da7f8d67a613c759`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 4.5 MB (4515403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058f91ac0045b9c67e0b445141195571ad95b6f59a25eb681889ad831b1498dd`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 1.3 MB (1318268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4d6b7782ec5dfb52798f8e6b9b9ab819fa68f6eb20afac4a297ba01be2efae`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:7642ba203742b9113008f284cfdf3548460cbae2ee69ecb2454eb8c735b96da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 KB (291146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94a8f15a57f45b959c2c2fc76cdd718d5ad776676b941690a80ec419f5487c6`

```dockerfile
```

-	Layers:
	-	`sha256:d711709c34958acee3c07ef7e1919d12e4928a2ca18487dd1819cbe2b91d6ae5`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 270.6 KB (270635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bcb88e50c5a338a29305fce33e34c339529ad379da7ba7d1cd2088bf08e935`  
		Last Modified: Wed, 15 May 2024 09:20:10 GMT  
		Size: 20.5 KB (20511 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:022c416ba80bd913b0d16582f1065f5c4b8ad34f219855b8a021c94d106524c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74098271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d00e35d265158288ca2a81ad2fdfbedc5b7035f13ab9cd1b998d4991d8fa37`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84613e011ca8867fd82ad1a4602a9c5ca1629a8c52b91548ba0a8ce39bc63bd6`  
		Last Modified: Wed, 15 May 2024 10:25:13 GMT  
		Size: 295.8 KB (295843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a7eb7dd16a3cb705d643f2c1b3ccb0cce9120eef39b1b1844864195af6c32`  
		Last Modified: Wed, 15 May 2024 10:28:17 GMT  
		Size: 64.1 MB (64106287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788e89ea89d463b8bcafc4d5b552bddaa08b72930505c3e5b6917da512bca47c`  
		Last Modified: Wed, 15 May 2024 10:29:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119b2251effb8f032617ef72426ede6300a48b24df3322f8180c5112fcb1488`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 5.1 MB (5063898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab86c9ac1c04673c91199de9df55b222aeb76d630df93b84c38cabab987ca9b`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 1.3 MB (1298290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e12372ead2b5522c0b9d32638dcec3d9780a4b4495fe0327787759f670419`  
		Last Modified: Wed, 15 May 2024 17:32:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e620ba0bef62789334c010b7cacf7a13de0927228fc5d74634b118f93d8a5ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 KB (288452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988be65311a6efef34a6bdac2f8dcba490cc5ae7a90c13a7b4b72cd68956fd79`

```dockerfile
```

-	Layers:
	-	`sha256:b860d1f348c1e8c34388faf32ca1f31601f367503a56b8482f22e27d112f725c`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 268.0 KB (268038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0144585ac3a8859d627186fb46c2dc5e2e025006a8801d6718aca937f207427`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 20.4 KB (20414 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ed5114faaef7109c9b6d09463fe6cd92b3012e1b89d7d4881ba567e2215f37c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa437d1d5649dee8d678ada0475d1bf336545ad8ffa4a692c19bba4fe496c25f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b2216e014970a83beea11c197a24ccf7f0027acc0d35a08b3a3b2c976b5eff`  
		Last Modified: Wed, 15 May 2024 04:47:32 GMT  
		Size: 296.3 KB (296270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b672324861585f05676c004287c9eeb3ec624b063c08e6689139af3a2f1ed3df`  
		Last Modified: Wed, 15 May 2024 05:01:36 GMT  
		Size: 64.1 MB (64129414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4969b1c1838dc52cc8a18a048524a037b980febaecd9563210c4df1a96604b42`  
		Last Modified: Wed, 15 May 2024 05:23:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abcaf0a32c421ab0105f8a6eb25fa2862e92a57fe5c68c0de96702a1496789d`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 5.3 MB (5270859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14972492f5cb274941b32172d5bccee08aba0eb45858ff97fe6fb9f45719fed`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 1.3 MB (1293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad16cdba266ead2ca15865cafeddfa415df7136a8ea60d18e820ce12c1407b61`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:2b40a03abefdfce61a9c05a652fbccf303ce8b02a57d74d4a4e0b3faebc448e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7793b7cdf8a3c9fe0b5515824960473b044a9be5b121a8763e7f63d45e27617e`

```dockerfile
```

-	Layers:
	-	`sha256:a992b851d066d8fb1da7d613d1d07540e1edd799d4b99a7da6d8c73629f8982c`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 266.2 KB (266157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b35b875bfd977ef42a74ac4b84ec1b6d05e4daea22d2a52db56fab59e5a6663`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 20.5 KB (20460 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:a47a2a03f9a9b7816a7a1113d57cd13a6291da16c23508710b0ca70debbb86d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76203648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e88c1f13b847682609243dade2de8bb68fc2643f3ef6c50cf558e301e6f05f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1a1d4bba7fb363f0ef2f025a4c6c441c7026445c4b9c955c509893576ea917`  
		Last Modified: Wed, 15 May 2024 02:47:56 GMT  
		Size: 293.9 KB (293929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109cf0320d2fb40b9f56e4b0b8249d43214d262e3aaa145e939c8d7354258d89`  
		Last Modified: Wed, 15 May 2024 02:49:19 GMT  
		Size: 66.2 MB (66221838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f36caa761931318dec5fb4c6712ab1ab66f9992473dd4c5bd890ad223c3ddd`  
		Last Modified: Wed, 15 May 2024 03:08:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c238da3c7fff1913d7b837e4c0413d72ec94e770a03bf0abcdd03ee7f233c6`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 5.1 MB (5117490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4576d2e047b1a8655a7d7395721fa5506df982c1b78ffc068954ec28445a9b7`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 1.4 MB (1352270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56b016932ac8f843faffdd88108c80fcd9b38b5ac893706dc6780d4777eb88d`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:51196241f4bb937ea188f006f7ce0120d183680a55447da6b30b27c68f3d44d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03069f12e51484e13fcfe4b6c7d03806f5efafe115a28c761003f672133cde4e`

```dockerfile
```

-	Layers:
	-	`sha256:074231774abc16fdbd7854582de2bfed128864d0fdabc7f75ee0b1cb2c153ebb`  
		Last Modified: Wed, 15 May 2024 04:14:19 GMT  
		Size: 266.1 KB (266063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77307ab5bd56ac3f136ed6992239aa495abc11b377b0e06d0fc98228b8c830bb`  
		Last Modified: Wed, 15 May 2024 04:14:19 GMT  
		Size: 20.4 KB (20390 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:ad54c78bb3d28e3aed3b194e44c2cef16277742c48cbdd5b62f57cff882294c7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2209668109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95a5f06a80f188aa7801df8ddf2e4cd69fd4686d0a68e51b8c04895fb4bd333`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:00:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:00:07 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:00:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:00:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:00:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:00:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:44 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:00:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:00:52 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 15 May 2024 22:02:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:02:03 GMT
WORKDIR C:\go
# Wed, 15 May 2024 22:54:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:54:20 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 15 May 2024 22:54:21 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:54:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 May 2024 22:55:43 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 May 2024 22:55:43 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff17c3a20dffac1d58c01594126216783c6f2f9b6c28a3a59f03a8ee906e2b`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a094f0476df4af0d71317b871f0fff1466fcb871824ba980d7746c7c7e19b4a`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e701d4f2f41ad4fc9ba76dec4fe56953399cd0f2f75d73d787daac52f5d01d42`  
		Last Modified: Wed, 15 May 2024 22:02:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf8bc44f874f9876c9d4e2d6081d14f0f7cae294108bd970a95a338c78e0267`  
		Last Modified: Wed, 15 May 2024 22:02:11 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0977a400b67989adcaa14e29549e6b7cf2016f2d293c6e0ad8c7e5131d6df`  
		Last Modified: Wed, 15 May 2024 22:02:10 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7ce095d7b4c8673e3da44be3d164160077fe5ceb1277aa402a7967f956ba12`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 25.4 MB (25431934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f74875c2cc73da758ccf48534c4447970abf1ca82506c5faac57fd7387bd95`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459ecbda0c5ac4cbd3edf97e00cc0f627e4a814ef2f3ce681bc4fe3a7240782f`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 329.6 KB (329556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1542fa949c26e34cf1b1b0142a0e23a25d2081c6735416c29aab51eb11a35e92`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac01d339a495506ea26c9903ee836493dd37f673f7861ff487d34fbad8dbe3a`  
		Last Modified: Wed, 15 May 2024 22:02:18 GMT  
		Size: 69.4 MB (69376703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018e748194263b3beeeee7e77a560e00f492435701dab2bccf109bed0f9b1fa5`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72448ba01254027acfd81714f262f5a929dfcae70bdce747d1b5d32febcadc3f`  
		Last Modified: Wed, 15 May 2024 22:55:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677ff24892a40528aaf057d88da31eaeae8979c187d0ec9d3a700b10eb9c0139`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b11f0b0a347b93aa95dcd56d43ffd423093f9baf73e3160778dbaf72f5b6ba`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f42c29fd8b1472cd668f410cae0b1e058865e8cfba4dc4afbba72139a3c73d`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5db520771c4c59ce4e205c4cb1527364a5242234c8c7ccd3aa8de0921b40fc`  
		Last Modified: Wed, 15 May 2024 22:55:48 GMT  
		Size: 1.8 MB (1841438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b63369b487f355d1be166f1cb0c1daaa037fbe80ce6e867e1f5f66a42dc8f4c`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:5a908c8e961d324c5675ab4c2ab96d32fa02aa4f5989320b06753099bd224455
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2276876401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c05c04fbdab0842c80fc8d1fc925f4ffca4f1ca02e89371883ffc6d7ce887b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:51:55 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:51:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:51:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:51:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:52:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:52:47 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:53:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:53:20 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 15 May 2024 21:56:21 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:56:23 GMT
WORKDIR C:\go
# Wed, 15 May 2024 22:53:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:53:36 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 15 May 2024 22:53:37 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:53:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 May 2024 22:55:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 May 2024 22:55:09 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896e983a0a4309b805accb8ae63327cc1f3b8f992e0d75b555a5c61d02fed986`  
		Last Modified: Wed, 15 May 2024 21:56:31 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c7744622a8e10412cfb393caef5a301667c3db556da9fd3857c72be60fcdc`  
		Last Modified: Wed, 15 May 2024 21:56:31 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b652aa3eb2aa15638a8e9f572497cfd1fb6884ebeeb6ecdc9074aad63f79a69`  
		Last Modified: Wed, 15 May 2024 21:56:30 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148c74e800af547d1d14d91f5b9c167f17c75e65d02f875b5ae130c570d83299`  
		Last Modified: Wed, 15 May 2024 21:56:29 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bccf2db4b47631e2d74d6e6ad17ebb28e6387c6e6c884011fdde2bf29fac7e`  
		Last Modified: Wed, 15 May 2024 21:56:29 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d4419852279e679aaa47097723ddfa68affbce518a5f31fe47caabc8b251d`  
		Last Modified: Wed, 15 May 2024 21:56:32 GMT  
		Size: 25.6 MB (25575407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8509005ef5150522ee2b4ded57557935baf2a14c34cc5d25b2241d935a81284a`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1477c6f08b1aaca7cf172e0b0e9b08c945114f3cfca719b6d9479d28377627da`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 346.4 KB (346387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd971ba008fee57e5da9f3e4bc2084142f53a330c099ed32492c660baebc4af`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3866e6ca6d2695e04b9a5fdb00612bf63b2a25f82548a42a0e9ea44defcc619`  
		Last Modified: Wed, 15 May 2024 21:56:38 GMT  
		Size: 69.4 MB (69400042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063360e32b8a7b88e36a87b59c4cdb689ee9bce85fff56da69f8a0953db6a9c3`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517e5d69bc86420b8e423d4fd9afd5e4138c87c06149927fb1ada38053147657`  
		Last Modified: Wed, 15 May 2024 22:55:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c1d817dc7c4f2d1ed65b8ebe3020056e330b2880f3ad70d0802de6684feb54`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf22c592153e6d7c1e0037379a2ec28694088ec9e283ef66024397d93249165c`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46c8b9479856498dc80f87da766924b2bbb9fcd9f7ecaf9e84245241ac743a5`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e3a07a3c56d5582fc71b9183eadde4dc83368be6d164ae5c95c4a9f4522234`  
		Last Modified: Wed, 15 May 2024 22:55:14 GMT  
		Size: 1.8 MB (1826095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677fb13fe6786ac8f8b9f709a8cfe6db6074ad603b3a45efe55fa8c478e22766`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:1bd8cac07af2bd33d70ca237e3fa5324af77ff08d2868e890ef971eb2c9222b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:2d0f98ee37151fac228829512d71cd60683bcca714b42a2accfd5b2ed0eef309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77076844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da2caebf0c82328df2582d2154aea90549512f5f8075a1d211888861edc36d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ea3408117e6ad5da2610d98c7aaaa6ab17d9280a7f00e54b78f4a8af1a13e6`  
		Last Modified: Tue, 14 May 2024 22:57:18 GMT  
		Size: 293.4 KB (293394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91320369b822ebdafa53385de29218150ed2e0c9432c803ae9ab0917b1c13e05`  
		Last Modified: Tue, 14 May 2024 22:57:19 GMT  
		Size: 67.0 MB (67007431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0406650e82959e8bef670a6825ebc6caab141ed9ad0670923af9d5998de85b1b`  
		Last Modified: Tue, 14 May 2024 22:57:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54b29b355af23f51f47454c3e17573db8b78d7b52ce85f0455a2e39d7fa074`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 5.0 MB (4973399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbee18c299cb69dbccc6437fb935315abe5ea1a53244f52a8ef81bf71b3ec7c`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 1.4 MB (1399486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3962e3b1e39ca0549762f19fbf5ce97673a3c8e25e572443e99130f629becf`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:6f76e9858ca4547fe58ff97bd2ffc98029feb869b1dfc98633fd6f628b314292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 KB (288373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d01d8efed7000405f724e82795e9cc915343e431cc02e71f7cb5c25dc349bc`

```dockerfile
```

-	Layers:
	-	`sha256:746b0306cd3cb1912a3fc855ffc1003e09c16f75c165c8632bfe6eb00f877847`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 268.0 KB (268019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8416aff5ff51dc4e8fe28c6decdd0e3d91752160f7da7909a202850f8bd690`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ac7c2575373554f84061a11c48e068678edf889b364d17fc18cae4e80ce71e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75488808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48147857ead25ab7ee7a77aa74a59e293fa9eca878fe8afdd536d5f143675028`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c253e1ccd740370512ac16dc1198d4cc7e5f79502d830e914be781d2a53ef`  
		Last Modified: Tue, 14 May 2024 23:02:34 GMT  
		Size: 294.1 KB (294052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d6f1f07c341f159f464047d7dfc24c2fe15b8492e49ca6864e4bb242a3ec8`  
		Last Modified: Tue, 14 May 2024 23:03:32 GMT  
		Size: 65.8 MB (65766197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ab3f344a28c5c3a77d5b42ed139c704c1a62bb86a51a6d424570cbeddca4f3`  
		Last Modified: Tue, 14 May 2024 23:04:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b167340b71c005d807677fbbfbac662cedcb4fec7ccda3d644fa2d7cd2160000`  
		Last Modified: Tue, 14 May 2024 23:59:49 GMT  
		Size: 5.0 MB (4959292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db00701b53c1d5eee7ae5f0370ad0e2bf8c7624155e1ccd2197c482e47a9b928`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 1.3 MB (1321618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3610115cc7dedfcb5e2e244108591d41fbe0430d9c192503193a6f2a0e0c62`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:65e3693b278d4ef7c1c71f462d35e072feb067d47d882a6357051558d5f46278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 KB (20292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883db6588355f9fff45c61143a3c184d6b5360f70087363d292d63c4ffd73363`

```dockerfile
```

-	Layers:
	-	`sha256:f9d8b3568f220dfd1bdb1ddf4e41df2a13ced2a403b7245c9a18e0b60d52fd7b`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 20.3 KB (20292 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:09a6c1b0e1bd5044d5c064715c0aa03b90e6940ba650cf16faef929b3f79fa04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74794769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a0acea946d5a81787cb9fe18c7071c5aa68a591344d13571c0ce51a5e470d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1e32b4becad7a3ff9750dab0a6195a4136fe3417839cd5d6ced26f77c37d79`  
		Last Modified: Wed, 15 May 2024 08:39:33 GMT  
		Size: 293.0 KB (292954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab304151744566becd5140e866f02946274de2d4d2a228bdba72a0e4dddfa248`  
		Last Modified: Wed, 15 May 2024 08:40:52 GMT  
		Size: 65.8 MB (65766163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ceb4452378bf5d66c4470fe48fe8427a79ec5fdc8ddb8ea1c7fc02a13ce65b`  
		Last Modified: Wed, 15 May 2024 08:43:33 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270f12d361d5c63e9937439d8ff8f1080a9e9af98e31682da7f8d67a613c759`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 4.5 MB (4515403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058f91ac0045b9c67e0b445141195571ad95b6f59a25eb681889ad831b1498dd`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 1.3 MB (1318268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4d6b7782ec5dfb52798f8e6b9b9ab819fa68f6eb20afac4a297ba01be2efae`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7642ba203742b9113008f284cfdf3548460cbae2ee69ecb2454eb8c735b96da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 KB (291146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94a8f15a57f45b959c2c2fc76cdd718d5ad776676b941690a80ec419f5487c6`

```dockerfile
```

-	Layers:
	-	`sha256:d711709c34958acee3c07ef7e1919d12e4928a2ca18487dd1819cbe2b91d6ae5`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 270.6 KB (270635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bcb88e50c5a338a29305fce33e34c339529ad379da7ba7d1cd2088bf08e935`  
		Last Modified: Wed, 15 May 2024 09:20:10 GMT  
		Size: 20.5 KB (20511 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:022c416ba80bd913b0d16582f1065f5c4b8ad34f219855b8a021c94d106524c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74098271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d00e35d265158288ca2a81ad2fdfbedc5b7035f13ab9cd1b998d4991d8fa37`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84613e011ca8867fd82ad1a4602a9c5ca1629a8c52b91548ba0a8ce39bc63bd6`  
		Last Modified: Wed, 15 May 2024 10:25:13 GMT  
		Size: 295.8 KB (295843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a7eb7dd16a3cb705d643f2c1b3ccb0cce9120eef39b1b1844864195af6c32`  
		Last Modified: Wed, 15 May 2024 10:28:17 GMT  
		Size: 64.1 MB (64106287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788e89ea89d463b8bcafc4d5b552bddaa08b72930505c3e5b6917da512bca47c`  
		Last Modified: Wed, 15 May 2024 10:29:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119b2251effb8f032617ef72426ede6300a48b24df3322f8180c5112fcb1488`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 5.1 MB (5063898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab86c9ac1c04673c91199de9df55b222aeb76d630df93b84c38cabab987ca9b`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 1.3 MB (1298290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e12372ead2b5522c0b9d32638dcec3d9780a4b4495fe0327787759f670419`  
		Last Modified: Wed, 15 May 2024 17:32:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e620ba0bef62789334c010b7cacf7a13de0927228fc5d74634b118f93d8a5ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 KB (288452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988be65311a6efef34a6bdac2f8dcba490cc5ae7a90c13a7b4b72cd68956fd79`

```dockerfile
```

-	Layers:
	-	`sha256:b860d1f348c1e8c34388faf32ca1f31601f367503a56b8482f22e27d112f725c`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 268.0 KB (268038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0144585ac3a8859d627186fb46c2dc5e2e025006a8801d6718aca937f207427`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 20.4 KB (20414 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ed5114faaef7109c9b6d09463fe6cd92b3012e1b89d7d4881ba567e2215f37c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa437d1d5649dee8d678ada0475d1bf336545ad8ffa4a692c19bba4fe496c25f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b2216e014970a83beea11c197a24ccf7f0027acc0d35a08b3a3b2c976b5eff`  
		Last Modified: Wed, 15 May 2024 04:47:32 GMT  
		Size: 296.3 KB (296270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b672324861585f05676c004287c9eeb3ec624b063c08e6689139af3a2f1ed3df`  
		Last Modified: Wed, 15 May 2024 05:01:36 GMT  
		Size: 64.1 MB (64129414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4969b1c1838dc52cc8a18a048524a037b980febaecd9563210c4df1a96604b42`  
		Last Modified: Wed, 15 May 2024 05:23:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abcaf0a32c421ab0105f8a6eb25fa2862e92a57fe5c68c0de96702a1496789d`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 5.3 MB (5270859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14972492f5cb274941b32172d5bccee08aba0eb45858ff97fe6fb9f45719fed`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 1.3 MB (1293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad16cdba266ead2ca15865cafeddfa415df7136a8ea60d18e820ce12c1407b61`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2b40a03abefdfce61a9c05a652fbccf303ce8b02a57d74d4a4e0b3faebc448e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7793b7cdf8a3c9fe0b5515824960473b044a9be5b121a8763e7f63d45e27617e`

```dockerfile
```

-	Layers:
	-	`sha256:a992b851d066d8fb1da7d613d1d07540e1edd799d4b99a7da6d8c73629f8982c`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 266.2 KB (266157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b35b875bfd977ef42a74ac4b84ec1b6d05e4daea22d2a52db56fab59e5a6663`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 20.5 KB (20460 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:a47a2a03f9a9b7816a7a1113d57cd13a6291da16c23508710b0ca70debbb86d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76203648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e88c1f13b847682609243dade2de8bb68fc2643f3ef6c50cf558e301e6f05f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1a1d4bba7fb363f0ef2f025a4c6c441c7026445c4b9c955c509893576ea917`  
		Last Modified: Wed, 15 May 2024 02:47:56 GMT  
		Size: 293.9 KB (293929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109cf0320d2fb40b9f56e4b0b8249d43214d262e3aaa145e939c8d7354258d89`  
		Last Modified: Wed, 15 May 2024 02:49:19 GMT  
		Size: 66.2 MB (66221838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f36caa761931318dec5fb4c6712ab1ab66f9992473dd4c5bd890ad223c3ddd`  
		Last Modified: Wed, 15 May 2024 03:08:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c238da3c7fff1913d7b837e4c0413d72ec94e770a03bf0abcdd03ee7f233c6`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 5.1 MB (5117490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4576d2e047b1a8655a7d7395721fa5506df982c1b78ffc068954ec28445a9b7`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 1.4 MB (1352270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56b016932ac8f843faffdd88108c80fcd9b38b5ac893706dc6780d4777eb88d`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:51196241f4bb937ea188f006f7ce0120d183680a55447da6b30b27c68f3d44d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03069f12e51484e13fcfe4b6c7d03806f5efafe115a28c761003f672133cde4e`

```dockerfile
```

-	Layers:
	-	`sha256:074231774abc16fdbd7854582de2bfed128864d0fdabc7f75ee0b1cb2c153ebb`  
		Last Modified: Wed, 15 May 2024 04:14:19 GMT  
		Size: 266.1 KB (266063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77307ab5bd56ac3f136ed6992239aa495abc11b377b0e06d0fc98228b8c830bb`  
		Last Modified: Wed, 15 May 2024 04:14:19 GMT  
		Size: 20.4 KB (20390 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:d9056f7c8ccc04e12cf3daf31698cdcf5f083170891372f94d61c8da6db21187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:5a908c8e961d324c5675ab4c2ab96d32fa02aa4f5989320b06753099bd224455
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2276876401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c05c04fbdab0842c80fc8d1fc925f4ffca4f1ca02e89371883ffc6d7ce887b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:51:55 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:51:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:51:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:51:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:52:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:52:47 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:53:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:53:20 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 15 May 2024 21:56:21 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:56:23 GMT
WORKDIR C:\go
# Wed, 15 May 2024 22:53:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:53:36 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 15 May 2024 22:53:37 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:53:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 May 2024 22:55:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 May 2024 22:55:09 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896e983a0a4309b805accb8ae63327cc1f3b8f992e0d75b555a5c61d02fed986`  
		Last Modified: Wed, 15 May 2024 21:56:31 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c7744622a8e10412cfb393caef5a301667c3db556da9fd3857c72be60fcdc`  
		Last Modified: Wed, 15 May 2024 21:56:31 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b652aa3eb2aa15638a8e9f572497cfd1fb6884ebeeb6ecdc9074aad63f79a69`  
		Last Modified: Wed, 15 May 2024 21:56:30 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148c74e800af547d1d14d91f5b9c167f17c75e65d02f875b5ae130c570d83299`  
		Last Modified: Wed, 15 May 2024 21:56:29 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bccf2db4b47631e2d74d6e6ad17ebb28e6387c6e6c884011fdde2bf29fac7e`  
		Last Modified: Wed, 15 May 2024 21:56:29 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d4419852279e679aaa47097723ddfa68affbce518a5f31fe47caabc8b251d`  
		Last Modified: Wed, 15 May 2024 21:56:32 GMT  
		Size: 25.6 MB (25575407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8509005ef5150522ee2b4ded57557935baf2a14c34cc5d25b2241d935a81284a`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1477c6f08b1aaca7cf172e0b0e9b08c945114f3cfca719b6d9479d28377627da`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 346.4 KB (346387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd971ba008fee57e5da9f3e4bc2084142f53a330c099ed32492c660baebc4af`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3866e6ca6d2695e04b9a5fdb00612bf63b2a25f82548a42a0e9ea44defcc619`  
		Last Modified: Wed, 15 May 2024 21:56:38 GMT  
		Size: 69.4 MB (69400042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063360e32b8a7b88e36a87b59c4cdb689ee9bce85fff56da69f8a0953db6a9c3`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517e5d69bc86420b8e423d4fd9afd5e4138c87c06149927fb1ada38053147657`  
		Last Modified: Wed, 15 May 2024 22:55:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c1d817dc7c4f2d1ed65b8ebe3020056e330b2880f3ad70d0802de6684feb54`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf22c592153e6d7c1e0037379a2ec28694088ec9e283ef66024397d93249165c`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46c8b9479856498dc80f87da766924b2bbb9fcd9f7ecaf9e84245241ac743a5`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e3a07a3c56d5582fc71b9183eadde4dc83368be6d164ae5c95c4a9f4522234`  
		Last Modified: Wed, 15 May 2024 22:55:14 GMT  
		Size: 1.8 MB (1826095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677fb13fe6786ac8f8b9f709a8cfe6db6074ad603b3a45efe55fa8c478e22766`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:556e1cdffb3884bd3e44b4b252bd2886642eb4470ca6a9612f027f00f3f6a366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:ad54c78bb3d28e3aed3b194e44c2cef16277742c48cbdd5b62f57cff882294c7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2209668109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95a5f06a80f188aa7801df8ddf2e4cd69fd4686d0a68e51b8c04895fb4bd333`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:00:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:00:07 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:00:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:00:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:00:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:00:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:44 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:00:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:00:52 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 15 May 2024 22:02:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:02:03 GMT
WORKDIR C:\go
# Wed, 15 May 2024 22:54:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:54:20 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 15 May 2024 22:54:21 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:54:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 May 2024 22:55:43 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 May 2024 22:55:43 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff17c3a20dffac1d58c01594126216783c6f2f9b6c28a3a59f03a8ee906e2b`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a094f0476df4af0d71317b871f0fff1466fcb871824ba980d7746c7c7e19b4a`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e701d4f2f41ad4fc9ba76dec4fe56953399cd0f2f75d73d787daac52f5d01d42`  
		Last Modified: Wed, 15 May 2024 22:02:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf8bc44f874f9876c9d4e2d6081d14f0f7cae294108bd970a95a338c78e0267`  
		Last Modified: Wed, 15 May 2024 22:02:11 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0977a400b67989adcaa14e29549e6b7cf2016f2d293c6e0ad8c7e5131d6df`  
		Last Modified: Wed, 15 May 2024 22:02:10 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7ce095d7b4c8673e3da44be3d164160077fe5ceb1277aa402a7967f956ba12`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 25.4 MB (25431934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f74875c2cc73da758ccf48534c4447970abf1ca82506c5faac57fd7387bd95`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459ecbda0c5ac4cbd3edf97e00cc0f627e4a814ef2f3ce681bc4fe3a7240782f`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 329.6 KB (329556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1542fa949c26e34cf1b1b0142a0e23a25d2081c6735416c29aab51eb11a35e92`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac01d339a495506ea26c9903ee836493dd37f673f7861ff487d34fbad8dbe3a`  
		Last Modified: Wed, 15 May 2024 22:02:18 GMT  
		Size: 69.4 MB (69376703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018e748194263b3beeeee7e77a560e00f492435701dab2bccf109bed0f9b1fa5`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72448ba01254027acfd81714f262f5a929dfcae70bdce747d1b5d32febcadc3f`  
		Last Modified: Wed, 15 May 2024 22:55:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677ff24892a40528aaf057d88da31eaeae8979c187d0ec9d3a700b10eb9c0139`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b11f0b0a347b93aa95dcd56d43ffd423093f9baf73e3160778dbaf72f5b6ba`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f42c29fd8b1472cd668f410cae0b1e058865e8cfba4dc4afbba72139a3c73d`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5db520771c4c59ce4e205c4cb1527364a5242234c8c7ccd3aa8de0921b40fc`  
		Last Modified: Wed, 15 May 2024 22:55:48 GMT  
		Size: 1.8 MB (1841438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b63369b487f355d1be166f1cb0c1daaa037fbe80ce6e867e1f5f66a42dc8f4c`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:a5b412c8ac820da3d8ce408bc4bcb2fbc19a99c67fd16ff5c2c4ecce76276fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e2f8b997d964717694810a581f3548bb7c88de368a40ad9de4f8ed414fa2c8bc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128741780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48489f36ce94641f6ce5703ea4babbd5e2e2ec4dbffc55809b7eb8c1c1508cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:03:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:03:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 22:04:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:04:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 22:04:09 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 22:04:10 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 22:04:10 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 22:04:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 22:04:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 22:04:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 80
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 443
# Wed, 15 May 2024 22:04:17 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 22:04:18 GMT
EXPOSE 2019
# Wed, 15 May 2024 22:04:22 GMT
RUN caddy version
# Wed, 15 May 2024 22:04:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cabe3592a5a508b32120c2f3f50485ce2af3e5b977d817fa71bff28061336aa`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7474cb4a8c303c68700f525e09e3bd29bb30d75dc33c01ea4a44732e7e7423f7`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 364.6 KB (364646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6d09183adf4d940c7dac96cc9d75af33bcb47d7d1811a7a296ad60e0d1b1c`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ce5e1d365ba13fb9103a5020b6644b3ae71e76d5e4d159b2f58914673cf2bf`  
		Last Modified: Wed, 15 May 2024 22:04:31 GMT  
		Size: 15.3 MB (15344884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aded66dd078b571ebb532e084c4af4f6beb685bd8a5b7524468e97c168f1a5`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37260cc3f9937e208886001176fd42c7113d3d49bdfd01a29d269126dc8538b4`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c851cec2c829abe440fde3ba79f95ec4728dfa01da5cb2b09e817e7581dc6b`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358cdf5957564add30758b73811ebe0f230cea2692cbb624fb5e8c369dcacc32`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b6a2684656992e4dbd6e42d4dd8ee988d00626cd55d362075a3a9243af3b54`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccb203e5de222a30a89c733e9964e55090c4ff8911cd1ccd005de5e27d7523`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097f79242227f6445dd34eaf655c51b48ce991b72a1ff5589b72787ee42f0fee`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e44fe3122406544397fc58d026c1cbeea8aec0444aaa6d12a759f86d4714c4`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401e6d173f17fd472a9adf0f3ce231ed4fa53e327b3fbd222c6900a64dc1573`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571e94ebd3fc2965298bc42c3810c16d0f6f6c9743a4b5aea94dc66e91aad8e2`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484373c77dd756bb7eb292a32b21c4039a936fdd0871ca3bc6c7467fcf29c77f`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9921976cbc4a4e3222ce034a2dbd34e498f4bc4fc93f52173e5339e8fb9571`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca02ad3a0dd4ff383e5fe8cef81201aa747f513bd724391e69d4272e441fb1c3`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0fb2e91e46705b26409f246c0bf3647718c5187bb6ffa4c5dafddfc2a2edd`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca09518406089c86c645aa571b37a75799b274b772b04a8fef6703ffbf76ef3b`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 338.9 KB (338919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd845c75155a3609f78ca6b64788a35f72e73fb0c060ee22b4dd7b4be922372f`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:39ca8d38bb88e8ba8d04cd6eeeff4530e4db12daa30aa37e9a0c216a3e2bcfcd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195917858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d1ee2064b2ba3276dc02e0d45d90e35c36d900905b3034b07989d7ed715418`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:53:10 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 21:53:11 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 21:53:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 21:53:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 21:53:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 21:53:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 21:53:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 21:53:47 GMT
EXPOSE 80
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 21:53:49 GMT
EXPOSE 2019
# Wed, 15 May 2024 21:54:15 GMT
RUN caddy version
# Wed, 15 May 2024 21:54:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf806c2d672572084312cc8aa494c8cec9af9daeed5057140149ccdd78dfb80`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b711793313f153495eabe6635f5e8f65dc570d25985f5f6f5ef8c5c0a553b3`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 490.6 KB (490620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d512e0e145af2eec1bd2d32a9b70d48703e256b6d9f9d9199a3a7f36a6c9ff`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4f52645186abe39ac028b27c3e9ffdd710c940ddd12cbbf6d0d29065a18491`  
		Last Modified: Wed, 15 May 2024 21:54:23 GMT  
		Size: 15.3 MB (15345743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa23f4c47c349e446197c7316ed9a453a261ab1fdd2c0e3f6d97d0992d65bdef`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97aa1e7097461ea94ece8afce1dd51ee1513ef285e26743e89614b29a473ed`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576b04f13aae77f986a510a286ba44a00cca8d03b5fffdd0cd881ff59ace8a29`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e02a14a1675118d3895f8691bae0b4c39b9fb31f41a7cee00b3ee9d5d4c6c88`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029ead0bd0493b4a27aca7d5c7dca9fd26f0cc230fe67e95131782faf30b3c7`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be7a0a749e1ab96c5b49167c6b4740f6dc3bd739e58052f848e479c157bbf16`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dc01200272cf83484b850657355cb0afd45801fd642b0e293ddd0a66f5bc6e`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff9d61cc398e1efd41ad219b45a7b7954fdca6b77c3641a047a7d3bba2d24ca`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdefed17ab78afabf07e8a0de1c83420d9eb0a05a6a13b1bd7c6e4f42b785ff`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a28a34a28f7595618aa6579263ace412ec6492a68f265fb56920fb0f52e98e`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e3072da47a79873523ce57465acf158d0f749d150dc2c354873ef27355441a`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709eb7f911c45eec7a80d9be6b73eb9c5b76c363f768c6b678b5e5ec589fb7e0`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118c06d85763da95dd5181f248564978ab3507b219ffb98f85c7473509bec42`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec0cdeef31f251bce3d39ed741232e9eb28b233af8a7373cf3c706afbfbbab4`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb36f279201594c9a4f90cc70e1669eb98c980e9582e2bb7b53fd70ec5071dda`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 348.0 KB (348008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a72e74ca019379f2a07ba0eaa7e4164da0d80823fab977d9182936d89dcf225`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:719e7a5b787e20985b0cdeec13fd4a3fba6b6c86a9b79341a5aaa6c2a3bab316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:39ca8d38bb88e8ba8d04cd6eeeff4530e4db12daa30aa37e9a0c216a3e2bcfcd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195917858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d1ee2064b2ba3276dc02e0d45d90e35c36d900905b3034b07989d7ed715418`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:53:10 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 21:53:11 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 21:53:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 21:53:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 21:53:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 21:53:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 21:53:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 21:53:47 GMT
EXPOSE 80
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 21:53:49 GMT
EXPOSE 2019
# Wed, 15 May 2024 21:54:15 GMT
RUN caddy version
# Wed, 15 May 2024 21:54:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf806c2d672572084312cc8aa494c8cec9af9daeed5057140149ccdd78dfb80`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b711793313f153495eabe6635f5e8f65dc570d25985f5f6f5ef8c5c0a553b3`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 490.6 KB (490620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d512e0e145af2eec1bd2d32a9b70d48703e256b6d9f9d9199a3a7f36a6c9ff`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4f52645186abe39ac028b27c3e9ffdd710c940ddd12cbbf6d0d29065a18491`  
		Last Modified: Wed, 15 May 2024 21:54:23 GMT  
		Size: 15.3 MB (15345743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa23f4c47c349e446197c7316ed9a453a261ab1fdd2c0e3f6d97d0992d65bdef`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97aa1e7097461ea94ece8afce1dd51ee1513ef285e26743e89614b29a473ed`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576b04f13aae77f986a510a286ba44a00cca8d03b5fffdd0cd881ff59ace8a29`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e02a14a1675118d3895f8691bae0b4c39b9fb31f41a7cee00b3ee9d5d4c6c88`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029ead0bd0493b4a27aca7d5c7dca9fd26f0cc230fe67e95131782faf30b3c7`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be7a0a749e1ab96c5b49167c6b4740f6dc3bd739e58052f848e479c157bbf16`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dc01200272cf83484b850657355cb0afd45801fd642b0e293ddd0a66f5bc6e`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff9d61cc398e1efd41ad219b45a7b7954fdca6b77c3641a047a7d3bba2d24ca`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdefed17ab78afabf07e8a0de1c83420d9eb0a05a6a13b1bd7c6e4f42b785ff`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a28a34a28f7595618aa6579263ace412ec6492a68f265fb56920fb0f52e98e`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e3072da47a79873523ce57465acf158d0f749d150dc2c354873ef27355441a`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709eb7f911c45eec7a80d9be6b73eb9c5b76c363f768c6b678b5e5ec589fb7e0`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118c06d85763da95dd5181f248564978ab3507b219ffb98f85c7473509bec42`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec0cdeef31f251bce3d39ed741232e9eb28b233af8a7373cf3c706afbfbbab4`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb36f279201594c9a4f90cc70e1669eb98c980e9582e2bb7b53fd70ec5071dda`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 348.0 KB (348008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a72e74ca019379f2a07ba0eaa7e4164da0d80823fab977d9182936d89dcf225`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:d5b364dd26bbab8a208d93d622f59091ff21942823dea37c1fcf16137353d746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e2f8b997d964717694810a581f3548bb7c88de368a40ad9de4f8ed414fa2c8bc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128741780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48489f36ce94641f6ce5703ea4babbd5e2e2ec4dbffc55809b7eb8c1c1508cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:03:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:03:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 22:04:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:04:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 22:04:09 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 22:04:10 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 22:04:10 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 22:04:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 22:04:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 22:04:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 80
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 443
# Wed, 15 May 2024 22:04:17 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 22:04:18 GMT
EXPOSE 2019
# Wed, 15 May 2024 22:04:22 GMT
RUN caddy version
# Wed, 15 May 2024 22:04:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cabe3592a5a508b32120c2f3f50485ce2af3e5b977d817fa71bff28061336aa`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7474cb4a8c303c68700f525e09e3bd29bb30d75dc33c01ea4a44732e7e7423f7`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 364.6 KB (364646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6d09183adf4d940c7dac96cc9d75af33bcb47d7d1811a7a296ad60e0d1b1c`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ce5e1d365ba13fb9103a5020b6644b3ae71e76d5e4d159b2f58914673cf2bf`  
		Last Modified: Wed, 15 May 2024 22:04:31 GMT  
		Size: 15.3 MB (15344884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aded66dd078b571ebb532e084c4af4f6beb685bd8a5b7524468e97c168f1a5`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37260cc3f9937e208886001176fd42c7113d3d49bdfd01a29d269126dc8538b4`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c851cec2c829abe440fde3ba79f95ec4728dfa01da5cb2b09e817e7581dc6b`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358cdf5957564add30758b73811ebe0f230cea2692cbb624fb5e8c369dcacc32`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b6a2684656992e4dbd6e42d4dd8ee988d00626cd55d362075a3a9243af3b54`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccb203e5de222a30a89c733e9964e55090c4ff8911cd1ccd005de5e27d7523`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097f79242227f6445dd34eaf655c51b48ce991b72a1ff5589b72787ee42f0fee`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e44fe3122406544397fc58d026c1cbeea8aec0444aaa6d12a759f86d4714c4`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401e6d173f17fd472a9adf0f3ce231ed4fa53e327b3fbd222c6900a64dc1573`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571e94ebd3fc2965298bc42c3810c16d0f6f6c9743a4b5aea94dc66e91aad8e2`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484373c77dd756bb7eb292a32b21c4039a936fdd0871ca3bc6c7467fcf29c77f`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9921976cbc4a4e3222ce034a2dbd34e498f4bc4fc93f52173e5339e8fb9571`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca02ad3a0dd4ff383e5fe8cef81201aa747f513bd724391e69d4272e441fb1c3`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0fb2e91e46705b26409f246c0bf3647718c5187bb6ffa4c5dafddfc2a2edd`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca09518406089c86c645aa571b37a75799b274b772b04a8fef6703ffbf76ef3b`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 338.9 KB (338919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd845c75155a3609f78ca6b64788a35f72e73fb0c060ee22b4dd7b4be922372f`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8`

```console
$ docker pull caddy@sha256:09b415c1f8fa012f849386e343a9e7d1dad579e50ee8c71456798469e91d0e37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8` - linux; amd64

```console
$ docker pull caddy@sha256:c9717cb1b2fe75ed0240fc7d9216f3d7cec0e60c2960551180c6bfc7baa709d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18413116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c8872edfb8cdc1dfe40c6c7ae1d10a66eb0c65538891fd9998dbb8b801c669`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ddf8e9a461fea8308735abbe3fc8bfdf2b5fe09e2a02f8b9a12443b764d0c2`  
		Last Modified: Tue, 21 May 2024 23:51:43 GMT  
		Size: 357.7 KB (357733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536a2c9704465341ef03d8dc85d9d64353529c65d2137187d8a584584c587a0d`  
		Last Modified: Tue, 21 May 2024 23:51:42 GMT  
		Size: 7.5 KB (7454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9e53d68db658eb9c96eb4a04fceb2f155399e893ec593d5ffd054a6faf932`  
		Last Modified: Tue, 21 May 2024 23:51:44 GMT  
		Size: 14.6 MB (14639168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:3f3ee7a959d11d42882ddc5c323438139eba158283bf60e72db9bd84bd6e95ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 KB (284142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0de793337e57f17cb4e0a95c01d879420c683828a604cb258448371c109dec2`

```dockerfile
```

-	Layers:
	-	`sha256:446a08044d8851284c48a7df77ea7bdda80a353089775d276e165e0540600a54`  
		Last Modified: Tue, 21 May 2024 23:51:43 GMT  
		Size: 267.6 KB (267557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd542ebf8e38b06f6320ccb7bc45f475838e563a2c11fac0d0ceb0f5fcc01183`  
		Last Modified: Tue, 21 May 2024 23:51:43 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0164ead3b3e8f4fdc44fc1ee2514ae4cab93d89381cf74bc402597ce80f718b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17294202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875cd0a5121274fad4648b42cfdefefcd5e6d779d261d8a217fb492266c6af62`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c692e8e0d4d36792d254913f000d765d7242927ad1c089a20525c96b99173278`  
		Last Modified: Tue, 21 May 2024 23:56:05 GMT  
		Size: 358.2 KB (358173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1c19b7096fdfbde5176c6a177cdfb68acde19e4933519e4d160a68b286c748`  
		Last Modified: Tue, 21 May 2024 23:56:05 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f400bcf7f640e3cbf4a9f8e0cac07b53e4e4dd3b4117dac8b3c4aa800575c8d8`  
		Last Modified: Tue, 21 May 2024 23:56:06 GMT  
		Size: 13.8 MB (13763148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:27901300339bad76f93eb750b461f75430a84224b9f0c704b451f8e75d77fcdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 KB (16295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e814d49f6c406129a246862889ed49c55b3a5b1384f8d15e9a3d9e4d20aa0a`

```dockerfile
```

-	Layers:
	-	`sha256:813b13d988154cc05f0339e9997460e2fd71daa3e01f6a06cd1de8365dc7aa29`  
		Last Modified: Tue, 21 May 2024 23:56:04 GMT  
		Size: 16.3 KB (16295 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; arm variant v7

```console
$ docker pull caddy@sha256:87dee0fd10c53b1a02e14ea99620b7f9a9d02b92e4ec569b83a173e590ae741d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17018238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e13b41813f062ccdb1729a3440d71258385893f2de03a99d1da08188b2f33f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4dcafd23e52c5b886c8310f226c0f2451d014a5dc39a847b173b719ec52230`  
		Last Modified: Wed, 08 May 2024 17:06:12 GMT  
		Size: 354.4 KB (354422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04dc110797fb1faa37d98116f147c2af0850edde6286afd798df691bbe3d1d`  
		Last Modified: Wed, 08 May 2024 17:06:12 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e8fc0d6d1817055194a317167a311ae7b8d11be9c1ba422ec0fe7d21e5faa`  
		Last Modified: Wed, 22 May 2024 00:09:17 GMT  
		Size: 13.7 MB (13737433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:1a82490b2afa9e4944611e7e40ee01b72d03053d56451d8880c189e78c36eb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 KB (284108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39fff3b9bdfa184704133234d38b47ebd89d6ea6b3c2cb3ef577ca843d5e333`

```dockerfile
```

-	Layers:
	-	`sha256:08569b722f56b2f4231ea1ed074c582d8215e39f0008548dc34d0a66f2a8df68`  
		Last Modified: Wed, 22 May 2024 00:09:17 GMT  
		Size: 267.6 KB (267593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2947b32710e46b944657327959024d5814e2b59656c23ee5b71bd27346df24c`  
		Last Modified: Wed, 22 May 2024 00:09:17 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:0707af22bb0eba0fb7cbd0a85625779546af78424d9013f40d829aaa55bb353e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17276359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5197794b0f859cdb4df8cbc4dcfb190d39c980dc8367dce302a8a1ac7b1a5cd9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827e1cfd7ffe12f30c4740d6194b32e9ea776d3265b97435f02a7c4bfd888d4`  
		Last Modified: Wed, 08 May 2024 17:16:03 GMT  
		Size: 369.3 KB (369344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbc9353fe69483f68e9caa73d12be64cf7a07f3898b1951fcb9e7a0dec1d8c4`  
		Last Modified: Wed, 08 May 2024 17:16:03 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fae1156b8cefc3ad292d9e02bc0dd1a20c540a8adb4d88e5086512679c0f538`  
		Last Modified: Wed, 22 May 2024 02:28:29 GMT  
		Size: 13.6 MB (13551815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:7bc8cd60634ce0ca0ba300be6b2c7bce08ab6be1c73b0c5714fea1cfc38986d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.0 KB (283996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb1c7907a0c5cf5c309c702f3bd77326ab11748c1d3676ce436a5e4306f5bfc`

```dockerfile
```

-	Layers:
	-	`sha256:db16c497008323434db5e721488577bdc4cf6b17d955615e63345526f9bd90a0`  
		Last Modified: Wed, 22 May 2024 02:28:29 GMT  
		Size: 267.6 KB (267568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3af83ed12f6a47d981c84f9f245228fbad2d5d2b3b91a905b9dd03354c450ef7`  
		Last Modified: Wed, 22 May 2024 02:28:29 GMT  
		Size: 16.4 KB (16428 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; ppc64le

```console
$ docker pull caddy@sha256:de78f133035af5c4b34500e27a731dcb6eb6408872b0d58ab5466752ca546a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17029937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d866e308b5bf6a2aff7336dcc36bf7bc324b423692bbd82a3ffaee1e29a3eb6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec7ae6caf21c44ae20a3ddd76f3605eff47807b148a47620366e7e4c557414e`  
		Last Modified: Wed, 08 May 2024 17:00:52 GMT  
		Size: 370.6 KB (370590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4421597c357d304bf0fe7e6b1d285625de3608ea34ca570956b60b8e6cda446a`  
		Last Modified: Wed, 08 May 2024 17:00:52 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9263d37eb189481dda8425d400f5f8cf0086e1a71d7439cc2451423d9b1ef89`  
		Last Modified: Wed, 22 May 2024 00:01:34 GMT  
		Size: 13.3 MB (13293509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:47ebf08e52769fec8dd8518fefaeb8c16929e02ed022f4f3370bf2200940636c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 KB (282098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08adcd6789e0bebdbfcc62874256c2963ce90f0ad7495929b2f3f394c462e1d`

```dockerfile
```

-	Layers:
	-	`sha256:b7da235b39e3f6f10ecb1d60b01aeecb54d22f507236e70d2e77a102e056babe`  
		Last Modified: Wed, 22 May 2024 00:01:33 GMT  
		Size: 265.6 KB (265637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d3fbfea2086180c0cf2b41f2107d6670c5f5d3c9d218b9e1f06a161b3c1088`  
		Last Modified: Wed, 22 May 2024 00:01:33 GMT  
		Size: 16.5 KB (16461 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; s390x

```console
$ docker pull caddy@sha256:ba4bed19bac0e470fc7cafe7add75fb7dc98a05b8e30f9793c8841264cae1132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17769443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ea377f355c7c6c723629da7e0a129af102e60a4f2de53cb1c7b56fa457221a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86b611a08b9dd15c4ee238b25fe7746e020a1ca60f00b173228940e98c0a17`  
		Last Modified: Wed, 22 May 2024 00:06:56 GMT  
		Size: 365.1 KB (365141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1ac6b5c5eb6830d57722102c9b49858327bbafd903c4734dfc8f22e45c71e2`  
		Last Modified: Wed, 22 May 2024 00:06:56 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7e07fe54972dc82d342a383af853c3671d1a9eef827dbe16223ad45a01f70a`  
		Last Modified: Wed, 22 May 2024 00:06:56 GMT  
		Size: 14.2 MB (14154183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:15beabf5208ff38b319bb6d99adefa808e8dc80303316f407e06dbff99fac6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.0 KB (282018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6be4a610a6a1c5b5b762567a42d527177256a8a996e6e74ea2ab655058cc62`

```dockerfile
```

-	Layers:
	-	`sha256:e1bdabe32cfd185b4684db8b8f00bf35298cd2befd03a15746c189b84d0b8efb`  
		Last Modified: Wed, 22 May 2024 00:06:56 GMT  
		Size: 265.6 KB (265599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf944c95dfb049b2a7593a5b2cfbe3dd53aec28c3aa7ae5fb5322d84b8a1be89`  
		Last Modified: Wed, 22 May 2024 00:06:53 GMT  
		Size: 16.4 KB (16419 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:1e928a53a1d22675e8ac7610a67aa61c8d75b0e33b803276f73ca0dadd94113a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128692328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652a396f96cd4e13bb9f70cd679605874d65c68a34b4dc91b3eceeb615586986`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Tue, 21 May 2024 23:51:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 May 2024 23:52:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 21 May 2024 23:52:33 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 23:52:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8be1502ab1872108833d1c8e3ce342df72b6f81acd3539e11b5333181419744a8342d52af2bd1b8033fde9105bb6b61a19479f969cae6f0964d12e08520019e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 21 May 2024 23:52:46 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 21 May 2024 23:52:46 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 21 May 2024 23:52:47 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 23:52:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 23:52:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 23:52:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 23:52:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 23:52:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 23:52:52 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 23:52:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 23:52:53 GMT
EXPOSE 80
# Tue, 21 May 2024 23:52:54 GMT
EXPOSE 443
# Tue, 21 May 2024 23:52:54 GMT
EXPOSE 443/udp
# Tue, 21 May 2024 23:52:55 GMT
EXPOSE 2019
# Tue, 21 May 2024 23:53:00 GMT
RUN caddy version
# Tue, 21 May 2024 23:53:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d53d01a42c0a6bb5a60af6315fc38ae466d0a7c27704dde3380c8bfd1972d4e`  
		Last Modified: Tue, 21 May 2024 23:53:12 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332a37e7263a68d1bebe71ff1eaf5e5419cd520081e4eca9c08d3766fef28183`  
		Last Modified: Tue, 21 May 2024 23:53:12 GMT  
		Size: 372.9 KB (372948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b0657715ead6f3d895b8500a2637d87ea862173f71b72d994f9617d1495904`  
		Last Modified: Tue, 21 May 2024 23:53:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4e1b56318ded1e2763959559ab09662928eb8f15a5173588c59f200a8dc386`  
		Last Modified: Tue, 21 May 2024 23:53:14 GMT  
		Size: 15.3 MB (15263586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed38526b5d20a13b399ef9860e0f5c36f6f9a7004795c55f664bd23d53cf679`  
		Last Modified: Tue, 21 May 2024 23:53:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8225895d3d9d361492fdd1a32c45e1a64458152651fcc69252267499d14a640`  
		Last Modified: Tue, 21 May 2024 23:53:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07176325acf1abec1d9d8f46ace70ce29032028d909c095fa563fc198f896a73`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff10d3353b9d4807209b066537ebce0ecbb7873ee190c1b7bd83193b8d5656d`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074fd7bc1f3ee4868f989a5f6e5a19572fcd662a1be0c6e6912f421b1ef98dd2`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85e3a2b2919cf9ed0019791a43da3a0c9cc49cc81066862767e0594ac51c2e2`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e777328a70a10c2ac1381d3f06d42248cb7c874475cf169eadad57f81af948`  
		Last Modified: Tue, 21 May 2024 23:53:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304dd6f436c6a91290e32c1a5e70ecd3bb6e0e28c5e43ffafa9a63222553086f`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad69644f88f1b28f81728db89b7c8c2c9e034fb38e698b135086a58ab45a5b2d`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecc9ee6821c8a5e217e075076d0d69e51e4716385b4bf66d08270f41d1bbc75`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d0c16f56f86b652826d6940dd16735cdfc8a951141f308bdb391f771ac452`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cd8292bca9fdd5394dadb9bf57bf6c3f8b3b778f127d674008eb00989e2648`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b1d35936f1fbec2577e4ba733a5ec36114ab54c68a34d7a299a1343ee8890`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50e3fc7e2df5b834fa610172c0163405d68d716e98899e706e630dae5762bfb`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335979296be25675a4854ceffe266cdfe466ddab40aa9e4253515cbe5c677a51`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 362.4 KB (362442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed6984f20560778287d4f12326f3117b9aec06fe2b8583d05719146f22a125`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:14c7399378de06746dae0dfc7b9eaaf024ac63f71745a9a082eca86cb2c2affe
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195931716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290196a6465d2451a39ec501062a1451a2086b137801e78772ed1c9160ad5599`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Tue, 21 May 2024 23:51:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 May 2024 23:52:37 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 21 May 2024 23:52:38 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 23:53:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8be1502ab1872108833d1c8e3ce342df72b6f81acd3539e11b5333181419744a8342d52af2bd1b8033fde9105bb6b61a19479f969cae6f0964d12e08520019e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 21 May 2024 23:53:07 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 21 May 2024 23:53:07 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 21 May 2024 23:53:08 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 23:53:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 23:53:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 23:53:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 23:53:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 23:53:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 23:53:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 23:53:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 23:53:12 GMT
EXPOSE 80
# Tue, 21 May 2024 23:53:13 GMT
EXPOSE 443
# Tue, 21 May 2024 23:53:13 GMT
EXPOSE 443/udp
# Tue, 21 May 2024 23:53:14 GMT
EXPOSE 2019
# Tue, 21 May 2024 23:53:19 GMT
RUN caddy version
# Tue, 21 May 2024 23:53:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1a072620eac005d85140631084040f090145b97856d39b4a3857f3883e1222`  
		Last Modified: Tue, 21 May 2024 23:53:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fe991d4d067d7cff69c70e75a1c849954f9564c5a39a63c4498d7d9923d653`  
		Last Modified: Tue, 21 May 2024 23:53:30 GMT  
		Size: 523.5 KB (523490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b875ce4f90053b0a9a3bf3455e32b742b97d8c17a2d71e0d6b6492e693d17f27`  
		Last Modified: Tue, 21 May 2024 23:53:29 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356659c3951686b02ad5198d3e2d7df7483764d9cc6e517c24a4583dbec88da3`  
		Last Modified: Tue, 21 May 2024 23:53:31 GMT  
		Size: 15.3 MB (15296256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2f0c9f3474fbab8f3a66eae9f7f84294ab34253aa7afed69383b9f609bef15`  
		Last Modified: Tue, 21 May 2024 23:53:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792652ad3ec00b1130a297274d739ac5a53042f507faceaedd584d490d364a45`  
		Last Modified: Tue, 21 May 2024 23:53:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183414d6935f7b5648933ca337c70b53aaa87c77636df30b20c73f51fa02a780`  
		Last Modified: Tue, 21 May 2024 23:53:28 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50c3bc4760ee42116a8382f5ddfc5c39db73d58db0bef6636d553d4f3d9cffc`  
		Last Modified: Tue, 21 May 2024 23:53:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f0c42983c0d6c326f29d6c92e8d17c1761d57f10b5a99292748b7054d54dad`  
		Last Modified: Tue, 21 May 2024 23:53:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef848fd2b41ad33300c96d0eb45d0221803603cb4f25d52d4c00a115f2822516`  
		Last Modified: Tue, 21 May 2024 23:53:27 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfb035898874b9fcc5587305135c07d86d6b538935c5cf6e727f37cc924d1c6`  
		Last Modified: Tue, 21 May 2024 23:53:26 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa1caef8f291d9735bb82e3adc30833ccd1a558b9b076698e10e7b59d104ccd`  
		Last Modified: Tue, 21 May 2024 23:53:26 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5515aa07f7d355f18c8a13ceee178d29c014647f3cdd8d1ba20dece8c91de14`  
		Last Modified: Tue, 21 May 2024 23:53:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be68d5ae1605829032856fbe8b34bdd5e05cbf6b341cc2631167acaccc346a14`  
		Last Modified: Tue, 21 May 2024 23:53:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067d493076bc7939fddbdf96feaaed7eca3d687a8e48a53e48d5437bbf49228a`  
		Last Modified: Tue, 21 May 2024 23:53:25 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb98a0364e924c2877291b5b27b3f2d6b074b17ab854a53bb0fb091827dd9202`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976272be25cbe9492fe5de336e275cd6b01e5c8d8b8462afe8d2b899700f9501`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1c874aabf9b7e3b95cf27a90ee7fd24d02cd4a3a53f62e5121dba9b6faa970`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c7615674f4476c40f0cd35a2a95d758f192dca7b61e6e4aea5de9bbc72984d`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 378.4 KB (378436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0c5cc63dc69fa4bc18cac5916c9d7f097e4a16fe891263ff59c897ee821013`  
		Last Modified: Tue, 21 May 2024 23:53:23 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-alpine`

```console
$ docker pull caddy@sha256:f8660fb5414bac933e55401955e14133539f48ecff9df4741ea45505eb005bb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2.8-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:c9717cb1b2fe75ed0240fc7d9216f3d7cec0e60c2960551180c6bfc7baa709d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18413116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c8872edfb8cdc1dfe40c6c7ae1d10a66eb0c65538891fd9998dbb8b801c669`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ddf8e9a461fea8308735abbe3fc8bfdf2b5fe09e2a02f8b9a12443b764d0c2`  
		Last Modified: Tue, 21 May 2024 23:51:43 GMT  
		Size: 357.7 KB (357733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536a2c9704465341ef03d8dc85d9d64353529c65d2137187d8a584584c587a0d`  
		Last Modified: Tue, 21 May 2024 23:51:42 GMT  
		Size: 7.5 KB (7454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9e53d68db658eb9c96eb4a04fceb2f155399e893ec593d5ffd054a6faf932`  
		Last Modified: Tue, 21 May 2024 23:51:44 GMT  
		Size: 14.6 MB (14639168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3f3ee7a959d11d42882ddc5c323438139eba158283bf60e72db9bd84bd6e95ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 KB (284142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0de793337e57f17cb4e0a95c01d879420c683828a604cb258448371c109dec2`

```dockerfile
```

-	Layers:
	-	`sha256:446a08044d8851284c48a7df77ea7bdda80a353089775d276e165e0540600a54`  
		Last Modified: Tue, 21 May 2024 23:51:43 GMT  
		Size: 267.6 KB (267557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd542ebf8e38b06f6320ccb7bc45f475838e563a2c11fac0d0ceb0f5fcc01183`  
		Last Modified: Tue, 21 May 2024 23:51:43 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0164ead3b3e8f4fdc44fc1ee2514ae4cab93d89381cf74bc402597ce80f718b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17294202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875cd0a5121274fad4648b42cfdefefcd5e6d779d261d8a217fb492266c6af62`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c692e8e0d4d36792d254913f000d765d7242927ad1c089a20525c96b99173278`  
		Last Modified: Tue, 21 May 2024 23:56:05 GMT  
		Size: 358.2 KB (358173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1c19b7096fdfbde5176c6a177cdfb68acde19e4933519e4d160a68b286c748`  
		Last Modified: Tue, 21 May 2024 23:56:05 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f400bcf7f640e3cbf4a9f8e0cac07b53e4e4dd3b4117dac8b3c4aa800575c8d8`  
		Last Modified: Tue, 21 May 2024 23:56:06 GMT  
		Size: 13.8 MB (13763148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:27901300339bad76f93eb750b461f75430a84224b9f0c704b451f8e75d77fcdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 KB (16295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e814d49f6c406129a246862889ed49c55b3a5b1384f8d15e9a3d9e4d20aa0a`

```dockerfile
```

-	Layers:
	-	`sha256:813b13d988154cc05f0339e9997460e2fd71daa3e01f6a06cd1de8365dc7aa29`  
		Last Modified: Tue, 21 May 2024 23:56:04 GMT  
		Size: 16.3 KB (16295 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:87dee0fd10c53b1a02e14ea99620b7f9a9d02b92e4ec569b83a173e590ae741d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17018238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e13b41813f062ccdb1729a3440d71258385893f2de03a99d1da08188b2f33f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4dcafd23e52c5b886c8310f226c0f2451d014a5dc39a847b173b719ec52230`  
		Last Modified: Wed, 08 May 2024 17:06:12 GMT  
		Size: 354.4 KB (354422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04dc110797fb1faa37d98116f147c2af0850edde6286afd798df691bbe3d1d`  
		Last Modified: Wed, 08 May 2024 17:06:12 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e8fc0d6d1817055194a317167a311ae7b8d11be9c1ba422ec0fe7d21e5faa`  
		Last Modified: Wed, 22 May 2024 00:09:17 GMT  
		Size: 13.7 MB (13737433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1a82490b2afa9e4944611e7e40ee01b72d03053d56451d8880c189e78c36eb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 KB (284108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39fff3b9bdfa184704133234d38b47ebd89d6ea6b3c2cb3ef577ca843d5e333`

```dockerfile
```

-	Layers:
	-	`sha256:08569b722f56b2f4231ea1ed074c582d8215e39f0008548dc34d0a66f2a8df68`  
		Last Modified: Wed, 22 May 2024 00:09:17 GMT  
		Size: 267.6 KB (267593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2947b32710e46b944657327959024d5814e2b59656c23ee5b71bd27346df24c`  
		Last Modified: Wed, 22 May 2024 00:09:17 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:0707af22bb0eba0fb7cbd0a85625779546af78424d9013f40d829aaa55bb353e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17276359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5197794b0f859cdb4df8cbc4dcfb190d39c980dc8367dce302a8a1ac7b1a5cd9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827e1cfd7ffe12f30c4740d6194b32e9ea776d3265b97435f02a7c4bfd888d4`  
		Last Modified: Wed, 08 May 2024 17:16:03 GMT  
		Size: 369.3 KB (369344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbc9353fe69483f68e9caa73d12be64cf7a07f3898b1951fcb9e7a0dec1d8c4`  
		Last Modified: Wed, 08 May 2024 17:16:03 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fae1156b8cefc3ad292d9e02bc0dd1a20c540a8adb4d88e5086512679c0f538`  
		Last Modified: Wed, 22 May 2024 02:28:29 GMT  
		Size: 13.6 MB (13551815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7bc8cd60634ce0ca0ba300be6b2c7bce08ab6be1c73b0c5714fea1cfc38986d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.0 KB (283996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb1c7907a0c5cf5c309c702f3bd77326ab11748c1d3676ce436a5e4306f5bfc`

```dockerfile
```

-	Layers:
	-	`sha256:db16c497008323434db5e721488577bdc4cf6b17d955615e63345526f9bd90a0`  
		Last Modified: Wed, 22 May 2024 02:28:29 GMT  
		Size: 267.6 KB (267568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3af83ed12f6a47d981c84f9f245228fbad2d5d2b3b91a905b9dd03354c450ef7`  
		Last Modified: Wed, 22 May 2024 02:28:29 GMT  
		Size: 16.4 KB (16428 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:de78f133035af5c4b34500e27a731dcb6eb6408872b0d58ab5466752ca546a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17029937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d866e308b5bf6a2aff7336dcc36bf7bc324b423692bbd82a3ffaee1e29a3eb6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec7ae6caf21c44ae20a3ddd76f3605eff47807b148a47620366e7e4c557414e`  
		Last Modified: Wed, 08 May 2024 17:00:52 GMT  
		Size: 370.6 KB (370590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4421597c357d304bf0fe7e6b1d285625de3608ea34ca570956b60b8e6cda446a`  
		Last Modified: Wed, 08 May 2024 17:00:52 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9263d37eb189481dda8425d400f5f8cf0086e1a71d7439cc2451423d9b1ef89`  
		Last Modified: Wed, 22 May 2024 00:01:34 GMT  
		Size: 13.3 MB (13293509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:47ebf08e52769fec8dd8518fefaeb8c16929e02ed022f4f3370bf2200940636c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 KB (282098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08adcd6789e0bebdbfcc62874256c2963ce90f0ad7495929b2f3f394c462e1d`

```dockerfile
```

-	Layers:
	-	`sha256:b7da235b39e3f6f10ecb1d60b01aeecb54d22f507236e70d2e77a102e056babe`  
		Last Modified: Wed, 22 May 2024 00:01:33 GMT  
		Size: 265.6 KB (265637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d3fbfea2086180c0cf2b41f2107d6670c5f5d3c9d218b9e1f06a161b3c1088`  
		Last Modified: Wed, 22 May 2024 00:01:33 GMT  
		Size: 16.5 KB (16461 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:ba4bed19bac0e470fc7cafe7add75fb7dc98a05b8e30f9793c8841264cae1132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17769443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ea377f355c7c6c723629da7e0a129af102e60a4f2de53cb1c7b56fa457221a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7d5d17be995506566d1441bf5e35dc546992616be32d82eeddc88d8f28e1f76321da5775063e64293ba367b83d7698f4698f68c940e8bd3c4fbe9978a9eeee70' ;; 		armhf)   binArch='armv6'; checksum='ca4bc32c88c0019ee7b8fa593e19c4f33ff245db1364dcda38e71a14c17167119f26f18f65aa2afc064aa2f80c2e1dfe9feb4da08ecd6b212290a59d40bf4760' ;; 		armv7)   binArch='armv7'; checksum='c3efc0fe4875dbf91b31657022c20c5fd4fae888edddbdcda85e69289ab795f47287a01d0680d4b13085b23ea0eca8511745922f1323c5875555e13d7bf4417a' ;; 		aarch64) binArch='arm64'; checksum='b682faa859efb7959d44e721bde3684d4ed5701f9880afd40b40feda3f525e6ebaf5c5900e9c33f8ffc202d6e79ff30735333678cd62cb5a6d27e894ec25d108' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6680923022e1c4d081733fc39e5193072d7093c2b1726663c12f2f323b5bd4cc94b2af844a69228c9228019f88faa7c52aa29dfc758346b7e0020e267dac6db6' ;; 		s390x)   binArch='s390x'; checksum='9b7ffd94ef5fef8f5892097d5ca82dcb9757ce28ffa2407ce310e9a72d8ecb746ca08da5f9a5d4fba5a11b3d81eeaab4f9cd199fc503ec78ae6c9fa4adb1b8cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 21 May 2024 13:04:29 GMT
ENV XDG_DATA_HOME=/data
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 13:04:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[443/udp:{}]
# Tue, 21 May 2024 13:04:29 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /srv
# Tue, 21 May 2024 13:04:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86b611a08b9dd15c4ee238b25fe7746e020a1ca60f00b173228940e98c0a17`  
		Last Modified: Wed, 22 May 2024 00:06:56 GMT  
		Size: 365.1 KB (365141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1ac6b5c5eb6830d57722102c9b49858327bbafd903c4734dfc8f22e45c71e2`  
		Last Modified: Wed, 22 May 2024 00:06:56 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7e07fe54972dc82d342a383af853c3671d1a9eef827dbe16223ad45a01f70a`  
		Last Modified: Wed, 22 May 2024 00:06:56 GMT  
		Size: 14.2 MB (14154183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:15beabf5208ff38b319bb6d99adefa808e8dc80303316f407e06dbff99fac6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.0 KB (282018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6be4a610a6a1c5b5b762567a42d527177256a8a996e6e74ea2ab655058cc62`

```dockerfile
```

-	Layers:
	-	`sha256:e1bdabe32cfd185b4684db8b8f00bf35298cd2befd03a15746c189b84d0b8efb`  
		Last Modified: Wed, 22 May 2024 00:06:56 GMT  
		Size: 265.6 KB (265599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf944c95dfb049b2a7593a5b2cfbe3dd53aec28c3aa7ae5fb5322d84b8a1be89`  
		Last Modified: Wed, 22 May 2024 00:06:53 GMT  
		Size: 16.4 KB (16419 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8-builder`

```console
$ docker pull caddy@sha256:5d4aac8d814437adaddf8b112af61d01b82721f882fc583d3543af93612153e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-builder` - linux; amd64

```console
$ docker pull caddy@sha256:596190bd017dabf37748cbeabd00ecc150d427868f38aa23bf52d7533b066dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79611000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4105f8d88fad09569d7da4805fd37b16f5696af6da2c842441a8ce2f02255b1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667a4259027594465efe0982aec566a89095e879511d0716b4ae322f291e393d`  
		Last Modified: Tue, 14 May 2024 22:59:10 GMT  
		Size: 292.9 KB (292900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e347f261431f4a9affbd78ee6f59a7486c17be94c7c8274be137aab626f0555`  
		Last Modified: Tue, 14 May 2024 22:59:11 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db27d6512129ba324acd616fd920202156dfadb8ccae8ffd1ec862bd46277c98`  
		Last Modified: Tue, 14 May 2024 22:59:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e846fe0d3f960a8b6916b00720d7c0bacdfe605a62a18fc26a467f0b9a7c4af`  
		Last Modified: Tue, 21 May 2024 23:51:51 GMT  
		Size: 5.2 MB (5166601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a328e8efcd609b96dfb7eda6676a46eaf5c38f520d8ef9880712aa9df6da50a4`  
		Last Modified: Tue, 21 May 2024 23:51:51 GMT  
		Size: 1.4 MB (1399486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5be1aa865786d139df361183ccf79f9c45e06bfd0efc788d91d8b17497fed3`  
		Last Modified: Tue, 21 May 2024 23:51:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:2ad7981bddefd3d8da6390e1a6ccf10eec63602aa58388ba03c1f37d8bfef4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.6 KB (290556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506af7f074999b41ede1555fea7d25c464500ea0617bfed281431b76eb8f7310`

```dockerfile
```

-	Layers:
	-	`sha256:8c8eefd499b97b303c189f45f5a48571b2fff7f2078761e8c44f90bd988eed76`  
		Last Modified: Tue, 21 May 2024 23:51:50 GMT  
		Size: 271.4 KB (271400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd1b654a941b5d738e94798ec45f2eb08103b6487e5e4381952f3691f01fe8e0`  
		Last Modified: Tue, 21 May 2024 23:51:50 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d2b6326f1cfc548fb7258ce8244669795b45c6ce38cb9999cebebaba98c26fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77642680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd04efa61a228d040e731989eb9182e83fd3e5cf15533dfc725d243d7cbcb0c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad27ef8f58290014492c74a7b2f956cb2cb25394a5098ce6da1e33844d12639`  
		Last Modified: Tue, 14 May 2024 23:01:50 GMT  
		Size: 294.3 KB (294336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f87622d8ade59df0daad35a20a0a1b816a8c25ed474cf6048473d6bbd0d46f2`  
		Last Modified: Tue, 14 May 2024 23:01:52 GMT  
		Size: 67.7 MB (67715217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310eb826c90e6f890ea6ae063ba343178643fcf5b69c5543af729af28cef52af`  
		Last Modified: Tue, 14 May 2024 23:01:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7249a95bc2ba2fd7fde9ea077c9523ebc6df8b440f4c8caaf4ccae86d60f8994`  
		Last Modified: Tue, 21 May 2024 23:56:32 GMT  
		Size: 5.1 MB (5145522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e4677242fea4285ece241f06558cc2156ba4c008955b0a067f3cb034664fc4`  
		Last Modified: Tue, 21 May 2024 23:56:32 GMT  
		Size: 1.3 MB (1321618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4b7c11b2248f1b2ce0b48bc7fe35ae2d72ca623e58e6cc2c786e5c7f0abbb`  
		Last Modified: Tue, 21 May 2024 23:56:32 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:cbcf13d2848c2a93909c92c610bba77970e487b5f2b3839b1e3523674caadd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d072fb540d4553e3eaf1daab2a4d485be5f2605868eb86e02519d432b5938e`

```dockerfile
```

-	Layers:
	-	`sha256:2a5b6a920f550f8c2fcdc7ab9f22d7fffde734c8e8fedb430597b84b4b83ee14`  
		Last Modified: Tue, 21 May 2024 23:56:32 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9c72da46b73222529b2bd95df2f1ca1bf7666599026ffafe3a314b8e30e9e785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76930698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd0fbe44c6159bcf51dee01a3330571d1400fd88b8892453e1f6bf877366994`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5bc8c8a85a004d09793602cc73eb5cdd7e51489747e55adbda95159c328a70`  
		Last Modified: Wed, 15 May 2024 08:38:49 GMT  
		Size: 293.2 KB (293185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd578652b0fd72238bc2565adcc2bf2716995c086d72609492506b36ddec660`  
		Last Modified: Wed, 15 May 2024 08:36:50 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2149779e1ffef1096a27b02d94b473a272e256d5c015ce287a5ca9a26bc0171`  
		Last Modified: Wed, 15 May 2024 08:38:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aa6672f56df7e76a85a9a64f48430ef61f913d3be36ed4e8523717fe568a1c`  
		Last Modified: Wed, 15 May 2024 09:19:42 GMT  
		Size: 4.7 MB (4684536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f402c7b16f1b2e216ba1850ecfdb848f83f1f49cd56d367ede18a12064dd73b3`  
		Last Modified: Wed, 22 May 2024 00:09:57 GMT  
		Size: 1.3 MB (1318269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a374a343875002f597129ab4f702a35d79d6dba166879419e868c5c316aadb6b`  
		Last Modified: Wed, 22 May 2024 00:09:56 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:8ca6b65d9b3b8e6199a025fbebf1ec5bf6ada3ef2ececab3c5343ae14e2bec2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 KB (292472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ab52ae25c38862bc2819c0b5c0be15390b867e7bc23362ac812b7ab0bac9f0`

```dockerfile
```

-	Layers:
	-	`sha256:bafc740015ef00faa7697062a7cead89d32d8cad91cd560b029a539808bd120a`  
		Last Modified: Wed, 22 May 2024 00:09:56 GMT  
		Size: 274.0 KB (273980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587194aa0208c1226acda34675fb670bddab06a5af478805bc682ca3e6ae2517`  
		Last Modified: Wed, 22 May 2024 00:09:56 GMT  
		Size: 18.5 KB (18492 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:4576ec5e950b6be23880ab8809181e35919a70c4c4acdf6f01568819fd26c212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76489494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c3b3962781b95aebd6a06ee29b378997a0a9ec309926fba14615cdb1576d15`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e3f50b898a3ae6cfe23ad1a18c4fb0bf0e08bb7feb5503a4b7d6a65e6f31bd`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 296.1 KB (296070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df936e3f0526d99820dadd5ba236ab92b125bf8f10cf6f450093350d9d53af4`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14fcb85665c756ff07c1198b28a771bebe20fdc0b96c64bcf187e9fe23c3c48`  
		Last Modified: Wed, 15 May 2024 17:32:19 GMT  
		Size: 5.3 MB (5274784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ca0a737ad88e012175e498b9112e4fe8ec773d6ee6bbf9509edf20f8cb8c5f`  
		Last Modified: Wed, 22 May 2024 02:29:03 GMT  
		Size: 1.3 MB (1298292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c1b3a0b6fdac5587d0503eda16abbf0e021c12af2c8e290b7fb7f03aa320ce`  
		Last Modified: Wed, 22 May 2024 02:29:02 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ccd17c4442c0b7f6093a89ca1c140a9bbab7094d1372582e7af35f1b966cd5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 KB (289831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10effe1975beaff2c253e729d7eaa91290d9fafa7b9247979c9aca5d905c95f5`

```dockerfile
```

-	Layers:
	-	`sha256:1f539194852eed874d24d00a7dcb84a5cb3c418a3c6f5d2d8e1dd7c50e531b1f`  
		Last Modified: Wed, 22 May 2024 02:29:02 GMT  
		Size: 271.4 KB (271411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac94fcaa3e725efb4d6a8b21d973f39b24af657defca4b77e241e32a7c910b81`  
		Last Modified: Wed, 22 May 2024 02:29:02 GMT  
		Size: 18.4 KB (18420 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:a5a29d4364c165fed71872d75f2514bb31b63e5160e321e19904058c8a667a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76799333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65df3ad83f87680f72e70f3ea90f14921e7c384f16a1641a0df56f5b2fe7ea9d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d82ce8dbc35c2b54369f84f5d1cdca1f43f171bafaa35b9ece60118143b6960`  
		Last Modified: Wed, 15 May 2024 04:46:37 GMT  
		Size: 296.5 KB (296495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a09e6cada02540e54f2e6e8c59f80c9960dc5c4559a3d96a1cc4bcca469ff9e`  
		Last Modified: Wed, 15 May 2024 04:44:01 GMT  
		Size: 66.4 MB (66430056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f690359b53e53fdcdeaa9654150463f063113662b6108d3988eef4548dec7c`  
		Last Modified: Wed, 15 May 2024 04:46:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb36c33c03f7cc2d694530adf36ed24e233be119ad4dfd184cbf05168d05d84`  
		Last Modified: Wed, 15 May 2024 06:07:15 GMT  
		Size: 5.4 MB (5420038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2675d0999329c45238233da18ad07be0cf93573f360f5a7abefe8b1d0c6e5b39`  
		Last Modified: Wed, 22 May 2024 00:03:20 GMT  
		Size: 1.3 MB (1293796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d24a146d40ef1ad183ac0e8680b2049b51f6d886057a5202b3773072ecff271`  
		Last Modified: Wed, 22 May 2024 00:03:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:613206276bde54b3b1b57bf2eaaed1fa80ba718a9f8de5849c2c757180368b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 KB (287964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edd7a4a916137ccf7b7fb65ab247e6bf1aad1e50a9ffafd138c53af65e898b`

```dockerfile
```

-	Layers:
	-	`sha256:e828ee4c14c8ffc8e27ed5d09a8507a70853664e57658c18ca1345ad86662573`  
		Last Modified: Wed, 22 May 2024 00:03:20 GMT  
		Size: 269.5 KB (269514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22764545d76dd25a8f43bbc174a70e5e3f8f40fef2ea98ffb417d043776ba117`  
		Last Modified: Wed, 22 May 2024 00:03:20 GMT  
		Size: 18.4 KB (18450 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; s390x

```console
$ docker pull caddy@sha256:7ae6ea84ab5ae0d2c71c89bdb006c284d1d5464b444b273c04f1c722ef1ade5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78691729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63091cff37f5dc54a7ec1aff1dcbf7bab699ee6e30027d1dfe69e7a00d60dd20`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc57cebd6cab112aa720ede5bce8aa42592bcc9ea99aa91ade3eb03d2ecbbce8`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 294.1 KB (294116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b913ee17a483cc427f632db9240a13b45ee66ca5d56d622dcfedef41eaa6cd`  
		Last Modified: Wed, 15 May 2024 02:44:08 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382b267d7cbedb48e683f15d12454c6aa505137bf49f9e3258cbdb09690fc056`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2b72215992e543ae7d6e1a0d527f65a7e976d5e60b89267b0f8333a7c0fd88`  
		Last Modified: Wed, 22 May 2024 00:07:48 GMT  
		Size: 5.4 MB (5403041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77ca3f1b656fe389bdf0c9eecf55a7cc998f7dade81763873e657a1c79741f9`  
		Last Modified: Wed, 22 May 2024 00:07:47 GMT  
		Size: 1.4 MB (1352267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817a0959b14dfd66b6e3f0ea32a7fda73f5696423a89f95c73c4f10bf8f1977b`  
		Last Modified: Wed, 22 May 2024 00:07:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:cd1e04407c8e881a402fe854e7213206d6cb93bea4ad19b038630e23e83e7155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 KB (288636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94343a9784542d38f03fdc79a6856ca5630ee1dfd8d9bb10a22723a55141cc4`

```dockerfile
```

-	Layers:
	-	`sha256:27647396c770e840d607670101abfd4f4046c0d0cc1edd3cfa1f2bef1023aa59`  
		Last Modified: Wed, 22 May 2024 00:07:47 GMT  
		Size: 269.4 KB (269444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0f310547ee4bbea47b6c7552704103107c3cbea9cc551c39ffa53ebe559eb9`  
		Last Modified: Wed, 22 May 2024 00:07:47 GMT  
		Size: 19.2 KB (19192 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:b49b8aa917750ec8c9be3c2447b7f650998d3b00adc3c99d8ee547d9855046a0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212107937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cb25fe3e8328efa0e2f4a0dd54caed6b13cc2e88e73ea43e046db3dfdfeccc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:58:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:58:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:58:45 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:58:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:58:58 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:59:04 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:59:05 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:00:17 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:18 GMT
WORKDIR C:\go
# Tue, 21 May 2024 23:53:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 May 2024 23:53:34 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 23:53:35 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 23:53:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 23:53:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 21 May 2024 23:53:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90a3c07c43efebd99803cdb9bad2d8149315d6fe71ed67ca3c907554d9e0d9`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d2da37d6aadb3a05b1b91cab3d0735e673ee46930e50eff76541ca6cd703c4`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998290d6ae9e03557ab29c99bdecd95a1646d0b2b6e01375977bc9ca92e7679f`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febc0e57a30d4aaef8d997796e999f07cd8d02fefada73c1d9a8d3b2efb2d0a5`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9634b04a70d192ce4d61fc9cacd9dfe77dc2ce74925adb17ec44604eae27767e`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d148249d3a6d5d5e8a6682e3d3c7577ec3e6c4db642ff5a298431e2aa6015a`  
		Last Modified: Wed, 15 May 2024 22:00:24 GMT  
		Size: 25.4 MB (25444377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abaff09d8cdfae3edceb6c5711ad840eb5f47c5bc4b76b2e6b4da440009de54`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302450cd0c74f7f8c4e0ef1ddc17b877078794558e3bc9ea20be56798e14f0b1`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 345.6 KB (345575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5856fa608f5aaadb2aa345cb0e4e8b4727bc567c776a2ca50b9b9b2ae049ca71`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b86ddf0d69a3769b0f5587cfee9e1dee2b6c0de79f2c6b192fc06caac1639`  
		Last Modified: Wed, 15 May 2024 22:00:32 GMT  
		Size: 71.8 MB (71755992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f91b25b9e6cb7c3077ad2c0725b9b9f62ce4feb0a96fd7c1a075d356fe1b1`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686101cf48520f82ced8adf0f6eceae9c246d5f1421074009442b9a151f5023f`  
		Last Modified: Tue, 21 May 2024 23:54:00 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c642232fefc15a4f6c05c0aac894072adc92a026a83a73f02369b2779ee4360`  
		Last Modified: Tue, 21 May 2024 23:53:58 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa4b17af157f6f7719a39959f9c5d77f8bd02558ce19833f7fc94eb54a7954f`  
		Last Modified: Tue, 21 May 2024 23:53:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ac60e43b9343f1a8e1b70b5a02b5c579d6633b69539b15801863e30d1527c9`  
		Last Modified: Tue, 21 May 2024 23:53:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b5f6cd16177785679ce420617519905d774c5656e4352b37d26f7f9ef45f38`  
		Last Modified: Tue, 21 May 2024 23:53:58 GMT  
		Size: 1.9 MB (1873557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdc48da53e14468fbfdfd820c3689569be8ce15c482b195d8892c924171a43c`  
		Last Modified: Tue, 21 May 2024 23:53:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8-builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:c0fc0ee3c04847a1ab88272310a6e570b9d37ad0511c8612a78598a8efedb320
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279248203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9eed81b09376f9ca5fe679ba32e9a2a9d9fb7bafe13308ccf164618bd9e2fbe`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 22:51:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:51:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:51:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:54:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:54:20 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:54:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:54:45 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:58:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:58:59 GMT
WORKDIR C:\go
# Tue, 21 May 2024 23:52:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 May 2024 23:52:42 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 23:52:43 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 23:52:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 23:53:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 21 May 2024 23:53:17 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b721870b6ca4ac86a4dd17a9efa72d3bbbc3e2f4db24604ab3e5529ac9483`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231059aab43e3c4c95c41ffa0eaaf0a505c5a3e17b120dfc894682b1930a3968`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83508e294490f2fa915d9cd65227cc8e8661207b15aa2cfdaf074ff8ae7bb4d4`  
		Last Modified: Wed, 15 May 2024 22:59:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d676bfa2282c568dda9fa4af2f2e6d235ebca82a6c367717bf083bad7dd8b3a`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3161f170f396d7c78bb77ee80c5b634beca05d901f05396abeab4e06be7f5`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c76d7a1b3a9e63480abdc848b1fd30a006301a1e471568b571a209702755daa`  
		Last Modified: Wed, 15 May 2024 22:59:07 GMT  
		Size: 25.6 MB (25574881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dcf82dafd8633a79265dca42870493640409651674a91b43f2adf04c165a`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dac5092add95bf42e98f932737023e0c6ef6ca428f58802291c2cc4c9559b7`  
		Last Modified: Wed, 15 May 2024 22:59:03 GMT  
		Size: 345.9 KB (345903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7992418d5500de5ceeac2fa4f57b54353f18a13b476f19add206e269ef1e6fc`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad77f522384c92c66907f62599064a34ebdd67556de4d2570970de37d46d8`  
		Last Modified: Wed, 15 May 2024 22:59:13 GMT  
		Size: 71.7 MB (71743817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716ef2ea189a02632506ad12bdad7990790c5792d611ac5831fdfa2896ac298`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fffbe1628af4c0bc793aa5b6ff95a3a1fc8e1f25e355ac003a11211429d1fb2`  
		Last Modified: Tue, 21 May 2024 23:53:23 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4440ed1c4da6be361d0c988de1466d70b56eed8d6cd3a94d0ca49b0c6f12f40c`  
		Last Modified: Tue, 21 May 2024 23:53:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff3d56dc06835962b4be066c0600a4c7f6a6b14c2506fd565b152569f3b2032`  
		Last Modified: Tue, 21 May 2024 23:53:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09de3a4987028c72632ba559177c9cae577f2240ef6d8d1dcabe3c8b7016fabb`  
		Last Modified: Tue, 21 May 2024 23:53:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8203f7d63bc2b93e632dcce663161a94930eb0772804a11ff497265811df06c8`  
		Last Modified: Tue, 21 May 2024 23:53:22 GMT  
		Size: 1.9 MB (1855218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23520a05e2ecf62ec3ef9a56226fb97205dfd5d3215e8e9269908967438cb868`  
		Last Modified: Tue, 21 May 2024 23:53:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-builder-alpine`

```console
$ docker pull caddy@sha256:b02e1a687e6ac4dc1cd339635214043fde33c0106d3f34e0fad169e67f5564be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2.8-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:596190bd017dabf37748cbeabd00ecc150d427868f38aa23bf52d7533b066dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79611000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4105f8d88fad09569d7da4805fd37b16f5696af6da2c842441a8ce2f02255b1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667a4259027594465efe0982aec566a89095e879511d0716b4ae322f291e393d`  
		Last Modified: Tue, 14 May 2024 22:59:10 GMT  
		Size: 292.9 KB (292900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e347f261431f4a9affbd78ee6f59a7486c17be94c7c8274be137aab626f0555`  
		Last Modified: Tue, 14 May 2024 22:59:11 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db27d6512129ba324acd616fd920202156dfadb8ccae8ffd1ec862bd46277c98`  
		Last Modified: Tue, 14 May 2024 22:59:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e846fe0d3f960a8b6916b00720d7c0bacdfe605a62a18fc26a467f0b9a7c4af`  
		Last Modified: Tue, 21 May 2024 23:51:51 GMT  
		Size: 5.2 MB (5166601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a328e8efcd609b96dfb7eda6676a46eaf5c38f520d8ef9880712aa9df6da50a4`  
		Last Modified: Tue, 21 May 2024 23:51:51 GMT  
		Size: 1.4 MB (1399486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5be1aa865786d139df361183ccf79f9c45e06bfd0efc788d91d8b17497fed3`  
		Last Modified: Tue, 21 May 2024 23:51:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2ad7981bddefd3d8da6390e1a6ccf10eec63602aa58388ba03c1f37d8bfef4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.6 KB (290556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506af7f074999b41ede1555fea7d25c464500ea0617bfed281431b76eb8f7310`

```dockerfile
```

-	Layers:
	-	`sha256:8c8eefd499b97b303c189f45f5a48571b2fff7f2078761e8c44f90bd988eed76`  
		Last Modified: Tue, 21 May 2024 23:51:50 GMT  
		Size: 271.4 KB (271400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd1b654a941b5d738e94798ec45f2eb08103b6487e5e4381952f3691f01fe8e0`  
		Last Modified: Tue, 21 May 2024 23:51:50 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d2b6326f1cfc548fb7258ce8244669795b45c6ce38cb9999cebebaba98c26fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77642680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd04efa61a228d040e731989eb9182e83fd3e5cf15533dfc725d243d7cbcb0c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad27ef8f58290014492c74a7b2f956cb2cb25394a5098ce6da1e33844d12639`  
		Last Modified: Tue, 14 May 2024 23:01:50 GMT  
		Size: 294.3 KB (294336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f87622d8ade59df0daad35a20a0a1b816a8c25ed474cf6048473d6bbd0d46f2`  
		Last Modified: Tue, 14 May 2024 23:01:52 GMT  
		Size: 67.7 MB (67715217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310eb826c90e6f890ea6ae063ba343178643fcf5b69c5543af729af28cef52af`  
		Last Modified: Tue, 14 May 2024 23:01:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7249a95bc2ba2fd7fde9ea077c9523ebc6df8b440f4c8caaf4ccae86d60f8994`  
		Last Modified: Tue, 21 May 2024 23:56:32 GMT  
		Size: 5.1 MB (5145522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e4677242fea4285ece241f06558cc2156ba4c008955b0a067f3cb034664fc4`  
		Last Modified: Tue, 21 May 2024 23:56:32 GMT  
		Size: 1.3 MB (1321618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4b7c11b2248f1b2ce0b48bc7fe35ae2d72ca623e58e6cc2c786e5c7f0abbb`  
		Last Modified: Tue, 21 May 2024 23:56:32 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:cbcf13d2848c2a93909c92c610bba77970e487b5f2b3839b1e3523674caadd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d072fb540d4553e3eaf1daab2a4d485be5f2605868eb86e02519d432b5938e`

```dockerfile
```

-	Layers:
	-	`sha256:2a5b6a920f550f8c2fcdc7ab9f22d7fffde734c8e8fedb430597b84b4b83ee14`  
		Last Modified: Tue, 21 May 2024 23:56:32 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9c72da46b73222529b2bd95df2f1ca1bf7666599026ffafe3a314b8e30e9e785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76930698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd0fbe44c6159bcf51dee01a3330571d1400fd88b8892453e1f6bf877366994`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5bc8c8a85a004d09793602cc73eb5cdd7e51489747e55adbda95159c328a70`  
		Last Modified: Wed, 15 May 2024 08:38:49 GMT  
		Size: 293.2 KB (293185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd578652b0fd72238bc2565adcc2bf2716995c086d72609492506b36ddec660`  
		Last Modified: Wed, 15 May 2024 08:36:50 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2149779e1ffef1096a27b02d94b473a272e256d5c015ce287a5ca9a26bc0171`  
		Last Modified: Wed, 15 May 2024 08:38:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aa6672f56df7e76a85a9a64f48430ef61f913d3be36ed4e8523717fe568a1c`  
		Last Modified: Wed, 15 May 2024 09:19:42 GMT  
		Size: 4.7 MB (4684536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f402c7b16f1b2e216ba1850ecfdb848f83f1f49cd56d367ede18a12064dd73b3`  
		Last Modified: Wed, 22 May 2024 00:09:57 GMT  
		Size: 1.3 MB (1318269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a374a343875002f597129ab4f702a35d79d6dba166879419e868c5c316aadb6b`  
		Last Modified: Wed, 22 May 2024 00:09:56 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:8ca6b65d9b3b8e6199a025fbebf1ec5bf6ada3ef2ececab3c5343ae14e2bec2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 KB (292472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ab52ae25c38862bc2819c0b5c0be15390b867e7bc23362ac812b7ab0bac9f0`

```dockerfile
```

-	Layers:
	-	`sha256:bafc740015ef00faa7697062a7cead89d32d8cad91cd560b029a539808bd120a`  
		Last Modified: Wed, 22 May 2024 00:09:56 GMT  
		Size: 274.0 KB (273980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587194aa0208c1226acda34675fb670bddab06a5af478805bc682ca3e6ae2517`  
		Last Modified: Wed, 22 May 2024 00:09:56 GMT  
		Size: 18.5 KB (18492 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:4576ec5e950b6be23880ab8809181e35919a70c4c4acdf6f01568819fd26c212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76489494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c3b3962781b95aebd6a06ee29b378997a0a9ec309926fba14615cdb1576d15`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e3f50b898a3ae6cfe23ad1a18c4fb0bf0e08bb7feb5503a4b7d6a65e6f31bd`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 296.1 KB (296070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df936e3f0526d99820dadd5ba236ab92b125bf8f10cf6f450093350d9d53af4`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14fcb85665c756ff07c1198b28a771bebe20fdc0b96c64bcf187e9fe23c3c48`  
		Last Modified: Wed, 15 May 2024 17:32:19 GMT  
		Size: 5.3 MB (5274784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ca0a737ad88e012175e498b9112e4fe8ec773d6ee6bbf9509edf20f8cb8c5f`  
		Last Modified: Wed, 22 May 2024 02:29:03 GMT  
		Size: 1.3 MB (1298292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c1b3a0b6fdac5587d0503eda16abbf0e021c12af2c8e290b7fb7f03aa320ce`  
		Last Modified: Wed, 22 May 2024 02:29:02 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ccd17c4442c0b7f6093a89ca1c140a9bbab7094d1372582e7af35f1b966cd5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 KB (289831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10effe1975beaff2c253e729d7eaa91290d9fafa7b9247979c9aca5d905c95f5`

```dockerfile
```

-	Layers:
	-	`sha256:1f539194852eed874d24d00a7dcb84a5cb3c418a3c6f5d2d8e1dd7c50e531b1f`  
		Last Modified: Wed, 22 May 2024 02:29:02 GMT  
		Size: 271.4 KB (271411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac94fcaa3e725efb4d6a8b21d973f39b24af657defca4b77e241e32a7c910b81`  
		Last Modified: Wed, 22 May 2024 02:29:02 GMT  
		Size: 18.4 KB (18420 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:a5a29d4364c165fed71872d75f2514bb31b63e5160e321e19904058c8a667a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76799333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65df3ad83f87680f72e70f3ea90f14921e7c384f16a1641a0df56f5b2fe7ea9d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d82ce8dbc35c2b54369f84f5d1cdca1f43f171bafaa35b9ece60118143b6960`  
		Last Modified: Wed, 15 May 2024 04:46:37 GMT  
		Size: 296.5 KB (296495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a09e6cada02540e54f2e6e8c59f80c9960dc5c4559a3d96a1cc4bcca469ff9e`  
		Last Modified: Wed, 15 May 2024 04:44:01 GMT  
		Size: 66.4 MB (66430056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f690359b53e53fdcdeaa9654150463f063113662b6108d3988eef4548dec7c`  
		Last Modified: Wed, 15 May 2024 04:46:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb36c33c03f7cc2d694530adf36ed24e233be119ad4dfd184cbf05168d05d84`  
		Last Modified: Wed, 15 May 2024 06:07:15 GMT  
		Size: 5.4 MB (5420038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2675d0999329c45238233da18ad07be0cf93573f360f5a7abefe8b1d0c6e5b39`  
		Last Modified: Wed, 22 May 2024 00:03:20 GMT  
		Size: 1.3 MB (1293796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d24a146d40ef1ad183ac0e8680b2049b51f6d886057a5202b3773072ecff271`  
		Last Modified: Wed, 22 May 2024 00:03:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:613206276bde54b3b1b57bf2eaaed1fa80ba718a9f8de5849c2c757180368b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 KB (287964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edd7a4a916137ccf7b7fb65ab247e6bf1aad1e50a9ffafd138c53af65e898b`

```dockerfile
```

-	Layers:
	-	`sha256:e828ee4c14c8ffc8e27ed5d09a8507a70853664e57658c18ca1345ad86662573`  
		Last Modified: Wed, 22 May 2024 00:03:20 GMT  
		Size: 269.5 KB (269514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22764545d76dd25a8f43bbc174a70e5e3f8f40fef2ea98ffb417d043776ba117`  
		Last Modified: Wed, 22 May 2024 00:03:20 GMT  
		Size: 18.4 KB (18450 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:7ae6ea84ab5ae0d2c71c89bdb006c284d1d5464b444b273c04f1c722ef1ade5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78691729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63091cff37f5dc54a7ec1aff1dcbf7bab699ee6e30027d1dfe69e7a00d60dd20`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
# Tue, 21 May 2024 13:04:29 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 13:04:29 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 13:04:29 GMT
ENV XCADDY_SETCAP=1
# Tue, 21 May 2024 13:04:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 21 May 2024 13:04:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 21 May 2024 13:04:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc57cebd6cab112aa720ede5bce8aa42592bcc9ea99aa91ade3eb03d2ecbbce8`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 294.1 KB (294116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b913ee17a483cc427f632db9240a13b45ee66ca5d56d622dcfedef41eaa6cd`  
		Last Modified: Wed, 15 May 2024 02:44:08 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382b267d7cbedb48e683f15d12454c6aa505137bf49f9e3258cbdb09690fc056`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2b72215992e543ae7d6e1a0d527f65a7e976d5e60b89267b0f8333a7c0fd88`  
		Last Modified: Wed, 22 May 2024 00:07:48 GMT  
		Size: 5.4 MB (5403041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77ca3f1b656fe389bdf0c9eecf55a7cc998f7dade81763873e657a1c79741f9`  
		Last Modified: Wed, 22 May 2024 00:07:47 GMT  
		Size: 1.4 MB (1352267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817a0959b14dfd66b6e3f0ea32a7fda73f5696423a89f95c73c4f10bf8f1977b`  
		Last Modified: Wed, 22 May 2024 00:07:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:cd1e04407c8e881a402fe854e7213206d6cb93bea4ad19b038630e23e83e7155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 KB (288636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94343a9784542d38f03fdc79a6856ca5630ee1dfd8d9bb10a22723a55141cc4`

```dockerfile
```

-	Layers:
	-	`sha256:27647396c770e840d607670101abfd4f4046c0d0cc1edd3cfa1f2bef1023aa59`  
		Last Modified: Wed, 22 May 2024 00:07:47 GMT  
		Size: 269.4 KB (269444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0f310547ee4bbea47b6c7552704103107c3cbea9cc551c39ffa53ebe559eb9`  
		Last Modified: Wed, 22 May 2024 00:07:47 GMT  
		Size: 19.2 KB (19192 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:b418e77b0c76bf66eaf0a249a4ede0ba380acd76ed5b4babc0ca2c755da9697d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:c0fc0ee3c04847a1ab88272310a6e570b9d37ad0511c8612a78598a8efedb320
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279248203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9eed81b09376f9ca5fe679ba32e9a2a9d9fb7bafe13308ccf164618bd9e2fbe`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 22:51:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:51:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:51:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:54:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:54:20 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:54:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:54:45 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:58:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:58:59 GMT
WORKDIR C:\go
# Tue, 21 May 2024 23:52:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 May 2024 23:52:42 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 23:52:43 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 23:52:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 23:53:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 21 May 2024 23:53:17 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b721870b6ca4ac86a4dd17a9efa72d3bbbc3e2f4db24604ab3e5529ac9483`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231059aab43e3c4c95c41ffa0eaaf0a505c5a3e17b120dfc894682b1930a3968`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83508e294490f2fa915d9cd65227cc8e8661207b15aa2cfdaf074ff8ae7bb4d4`  
		Last Modified: Wed, 15 May 2024 22:59:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d676bfa2282c568dda9fa4af2f2e6d235ebca82a6c367717bf083bad7dd8b3a`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3161f170f396d7c78bb77ee80c5b634beca05d901f05396abeab4e06be7f5`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c76d7a1b3a9e63480abdc848b1fd30a006301a1e471568b571a209702755daa`  
		Last Modified: Wed, 15 May 2024 22:59:07 GMT  
		Size: 25.6 MB (25574881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dcf82dafd8633a79265dca42870493640409651674a91b43f2adf04c165a`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dac5092add95bf42e98f932737023e0c6ef6ca428f58802291c2cc4c9559b7`  
		Last Modified: Wed, 15 May 2024 22:59:03 GMT  
		Size: 345.9 KB (345903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7992418d5500de5ceeac2fa4f57b54353f18a13b476f19add206e269ef1e6fc`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad77f522384c92c66907f62599064a34ebdd67556de4d2570970de37d46d8`  
		Last Modified: Wed, 15 May 2024 22:59:13 GMT  
		Size: 71.7 MB (71743817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716ef2ea189a02632506ad12bdad7990790c5792d611ac5831fdfa2896ac298`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fffbe1628af4c0bc793aa5b6ff95a3a1fc8e1f25e355ac003a11211429d1fb2`  
		Last Modified: Tue, 21 May 2024 23:53:23 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4440ed1c4da6be361d0c988de1466d70b56eed8d6cd3a94d0ca49b0c6f12f40c`  
		Last Modified: Tue, 21 May 2024 23:53:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff3d56dc06835962b4be066c0600a4c7f6a6b14c2506fd565b152569f3b2032`  
		Last Modified: Tue, 21 May 2024 23:53:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09de3a4987028c72632ba559177c9cae577f2240ef6d8d1dcabe3c8b7016fabb`  
		Last Modified: Tue, 21 May 2024 23:53:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8203f7d63bc2b93e632dcce663161a94930eb0772804a11ff497265811df06c8`  
		Last Modified: Tue, 21 May 2024 23:53:22 GMT  
		Size: 1.9 MB (1855218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23520a05e2ecf62ec3ef9a56226fb97205dfd5d3215e8e9269908967438cb868`  
		Last Modified: Tue, 21 May 2024 23:53:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:a954c5051d6980eec89e33bda3af9b835f67df80febf13d62794b6a1aa7e8cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:b49b8aa917750ec8c9be3c2447b7f650998d3b00adc3c99d8ee547d9855046a0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212107937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cb25fe3e8328efa0e2f4a0dd54caed6b13cc2e88e73ea43e046db3dfdfeccc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:58:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:58:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:58:45 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:58:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:58:58 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:59:04 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:59:05 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:00:17 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:18 GMT
WORKDIR C:\go
# Tue, 21 May 2024 23:53:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 May 2024 23:53:34 GMT
ENV XCADDY_VERSION=v0.4.1
# Tue, 21 May 2024 23:53:35 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 23:53:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 21 May 2024 23:53:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 21 May 2024 23:53:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90a3c07c43efebd99803cdb9bad2d8149315d6fe71ed67ca3c907554d9e0d9`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d2da37d6aadb3a05b1b91cab3d0735e673ee46930e50eff76541ca6cd703c4`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998290d6ae9e03557ab29c99bdecd95a1646d0b2b6e01375977bc9ca92e7679f`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febc0e57a30d4aaef8d997796e999f07cd8d02fefada73c1d9a8d3b2efb2d0a5`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9634b04a70d192ce4d61fc9cacd9dfe77dc2ce74925adb17ec44604eae27767e`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d148249d3a6d5d5e8a6682e3d3c7577ec3e6c4db642ff5a298431e2aa6015a`  
		Last Modified: Wed, 15 May 2024 22:00:24 GMT  
		Size: 25.4 MB (25444377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abaff09d8cdfae3edceb6c5711ad840eb5f47c5bc4b76b2e6b4da440009de54`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302450cd0c74f7f8c4e0ef1ddc17b877078794558e3bc9ea20be56798e14f0b1`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 345.6 KB (345575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5856fa608f5aaadb2aa345cb0e4e8b4727bc567c776a2ca50b9b9b2ae049ca71`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b86ddf0d69a3769b0f5587cfee9e1dee2b6c0de79f2c6b192fc06caac1639`  
		Last Modified: Wed, 15 May 2024 22:00:32 GMT  
		Size: 71.8 MB (71755992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f91b25b9e6cb7c3077ad2c0725b9b9f62ce4feb0a96fd7c1a075d356fe1b1`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686101cf48520f82ced8adf0f6eceae9c246d5f1421074009442b9a151f5023f`  
		Last Modified: Tue, 21 May 2024 23:54:00 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c642232fefc15a4f6c05c0aac894072adc92a026a83a73f02369b2779ee4360`  
		Last Modified: Tue, 21 May 2024 23:53:58 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa4b17af157f6f7719a39959f9c5d77f8bd02558ce19833f7fc94eb54a7954f`  
		Last Modified: Tue, 21 May 2024 23:53:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ac60e43b9343f1a8e1b70b5a02b5c579d6633b69539b15801863e30d1527c9`  
		Last Modified: Tue, 21 May 2024 23:53:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b5f6cd16177785679ce420617519905d774c5656e4352b37d26f7f9ef45f38`  
		Last Modified: Tue, 21 May 2024 23:53:58 GMT  
		Size: 1.9 MB (1873557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdc48da53e14468fbfdfd820c3689569be8ce15c482b195d8892c924171a43c`  
		Last Modified: Tue, 21 May 2024 23:53:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore`

```console
$ docker pull caddy@sha256:0e880d46a3af9c1471bde55600b6c4767032976ab486060024f02990504dee04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:1e928a53a1d22675e8ac7610a67aa61c8d75b0e33b803276f73ca0dadd94113a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128692328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652a396f96cd4e13bb9f70cd679605874d65c68a34b4dc91b3eceeb615586986`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Tue, 21 May 2024 23:51:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 May 2024 23:52:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 21 May 2024 23:52:33 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 23:52:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8be1502ab1872108833d1c8e3ce342df72b6f81acd3539e11b5333181419744a8342d52af2bd1b8033fde9105bb6b61a19479f969cae6f0964d12e08520019e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 21 May 2024 23:52:46 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 21 May 2024 23:52:46 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 21 May 2024 23:52:47 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 23:52:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 23:52:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 23:52:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 23:52:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 23:52:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 23:52:52 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 23:52:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 23:52:53 GMT
EXPOSE 80
# Tue, 21 May 2024 23:52:54 GMT
EXPOSE 443
# Tue, 21 May 2024 23:52:54 GMT
EXPOSE 443/udp
# Tue, 21 May 2024 23:52:55 GMT
EXPOSE 2019
# Tue, 21 May 2024 23:53:00 GMT
RUN caddy version
# Tue, 21 May 2024 23:53:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d53d01a42c0a6bb5a60af6315fc38ae466d0a7c27704dde3380c8bfd1972d4e`  
		Last Modified: Tue, 21 May 2024 23:53:12 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332a37e7263a68d1bebe71ff1eaf5e5419cd520081e4eca9c08d3766fef28183`  
		Last Modified: Tue, 21 May 2024 23:53:12 GMT  
		Size: 372.9 KB (372948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b0657715ead6f3d895b8500a2637d87ea862173f71b72d994f9617d1495904`  
		Last Modified: Tue, 21 May 2024 23:53:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4e1b56318ded1e2763959559ab09662928eb8f15a5173588c59f200a8dc386`  
		Last Modified: Tue, 21 May 2024 23:53:14 GMT  
		Size: 15.3 MB (15263586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed38526b5d20a13b399ef9860e0f5c36f6f9a7004795c55f664bd23d53cf679`  
		Last Modified: Tue, 21 May 2024 23:53:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8225895d3d9d361492fdd1a32c45e1a64458152651fcc69252267499d14a640`  
		Last Modified: Tue, 21 May 2024 23:53:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07176325acf1abec1d9d8f46ace70ce29032028d909c095fa563fc198f896a73`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff10d3353b9d4807209b066537ebce0ecbb7873ee190c1b7bd83193b8d5656d`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074fd7bc1f3ee4868f989a5f6e5a19572fcd662a1be0c6e6912f421b1ef98dd2`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85e3a2b2919cf9ed0019791a43da3a0c9cc49cc81066862767e0594ac51c2e2`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e777328a70a10c2ac1381d3f06d42248cb7c874475cf169eadad57f81af948`  
		Last Modified: Tue, 21 May 2024 23:53:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304dd6f436c6a91290e32c1a5e70ecd3bb6e0e28c5e43ffafa9a63222553086f`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad69644f88f1b28f81728db89b7c8c2c9e034fb38e698b135086a58ab45a5b2d`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecc9ee6821c8a5e217e075076d0d69e51e4716385b4bf66d08270f41d1bbc75`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d0c16f56f86b652826d6940dd16735cdfc8a951141f308bdb391f771ac452`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cd8292bca9fdd5394dadb9bf57bf6c3f8b3b778f127d674008eb00989e2648`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b1d35936f1fbec2577e4ba733a5ec36114ab54c68a34d7a299a1343ee8890`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50e3fc7e2df5b834fa610172c0163405d68d716e98899e706e630dae5762bfb`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335979296be25675a4854ceffe266cdfe466ddab40aa9e4253515cbe5c677a51`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 362.4 KB (362442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed6984f20560778287d4f12326f3117b9aec06fe2b8583d05719146f22a125`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:14c7399378de06746dae0dfc7b9eaaf024ac63f71745a9a082eca86cb2c2affe
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195931716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290196a6465d2451a39ec501062a1451a2086b137801e78772ed1c9160ad5599`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Tue, 21 May 2024 23:51:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 May 2024 23:52:37 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 21 May 2024 23:52:38 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 23:53:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8be1502ab1872108833d1c8e3ce342df72b6f81acd3539e11b5333181419744a8342d52af2bd1b8033fde9105bb6b61a19479f969cae6f0964d12e08520019e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 21 May 2024 23:53:07 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 21 May 2024 23:53:07 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 21 May 2024 23:53:08 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 23:53:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 23:53:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 23:53:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 23:53:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 23:53:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 23:53:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 23:53:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 23:53:12 GMT
EXPOSE 80
# Tue, 21 May 2024 23:53:13 GMT
EXPOSE 443
# Tue, 21 May 2024 23:53:13 GMT
EXPOSE 443/udp
# Tue, 21 May 2024 23:53:14 GMT
EXPOSE 2019
# Tue, 21 May 2024 23:53:19 GMT
RUN caddy version
# Tue, 21 May 2024 23:53:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1a072620eac005d85140631084040f090145b97856d39b4a3857f3883e1222`  
		Last Modified: Tue, 21 May 2024 23:53:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fe991d4d067d7cff69c70e75a1c849954f9564c5a39a63c4498d7d9923d653`  
		Last Modified: Tue, 21 May 2024 23:53:30 GMT  
		Size: 523.5 KB (523490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b875ce4f90053b0a9a3bf3455e32b742b97d8c17a2d71e0d6b6492e693d17f27`  
		Last Modified: Tue, 21 May 2024 23:53:29 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356659c3951686b02ad5198d3e2d7df7483764d9cc6e517c24a4583dbec88da3`  
		Last Modified: Tue, 21 May 2024 23:53:31 GMT  
		Size: 15.3 MB (15296256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2f0c9f3474fbab8f3a66eae9f7f84294ab34253aa7afed69383b9f609bef15`  
		Last Modified: Tue, 21 May 2024 23:53:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792652ad3ec00b1130a297274d739ac5a53042f507faceaedd584d490d364a45`  
		Last Modified: Tue, 21 May 2024 23:53:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183414d6935f7b5648933ca337c70b53aaa87c77636df30b20c73f51fa02a780`  
		Last Modified: Tue, 21 May 2024 23:53:28 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50c3bc4760ee42116a8382f5ddfc5c39db73d58db0bef6636d553d4f3d9cffc`  
		Last Modified: Tue, 21 May 2024 23:53:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f0c42983c0d6c326f29d6c92e8d17c1761d57f10b5a99292748b7054d54dad`  
		Last Modified: Tue, 21 May 2024 23:53:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef848fd2b41ad33300c96d0eb45d0221803603cb4f25d52d4c00a115f2822516`  
		Last Modified: Tue, 21 May 2024 23:53:27 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfb035898874b9fcc5587305135c07d86d6b538935c5cf6e727f37cc924d1c6`  
		Last Modified: Tue, 21 May 2024 23:53:26 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa1caef8f291d9735bb82e3adc30833ccd1a558b9b076698e10e7b59d104ccd`  
		Last Modified: Tue, 21 May 2024 23:53:26 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5515aa07f7d355f18c8a13ceee178d29c014647f3cdd8d1ba20dece8c91de14`  
		Last Modified: Tue, 21 May 2024 23:53:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be68d5ae1605829032856fbe8b34bdd5e05cbf6b341cc2631167acaccc346a14`  
		Last Modified: Tue, 21 May 2024 23:53:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067d493076bc7939fddbdf96feaaed7eca3d687a8e48a53e48d5437bbf49228a`  
		Last Modified: Tue, 21 May 2024 23:53:25 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb98a0364e924c2877291b5b27b3f2d6b074b17ab854a53bb0fb091827dd9202`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976272be25cbe9492fe5de336e275cd6b01e5c8d8b8462afe8d2b899700f9501`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1c874aabf9b7e3b95cf27a90ee7fd24d02cd4a3a53f62e5121dba9b6faa970`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c7615674f4476c40f0cd35a2a95d758f192dca7b61e6e4aea5de9bbc72984d`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 378.4 KB (378436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0c5cc63dc69fa4bc18cac5916c9d7f097e4a16fe891263ff59c897ee821013`  
		Last Modified: Tue, 21 May 2024 23:53:23 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e620fbc4abfe7981be63367155a37ad0fb045ec0d9cebdce95b6be3b08006550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:14c7399378de06746dae0dfc7b9eaaf024ac63f71745a9a082eca86cb2c2affe
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195931716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290196a6465d2451a39ec501062a1451a2086b137801e78772ed1c9160ad5599`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Tue, 21 May 2024 23:51:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 May 2024 23:52:37 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 21 May 2024 23:52:38 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 23:53:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8be1502ab1872108833d1c8e3ce342df72b6f81acd3539e11b5333181419744a8342d52af2bd1b8033fde9105bb6b61a19479f969cae6f0964d12e08520019e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 21 May 2024 23:53:07 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 21 May 2024 23:53:07 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 21 May 2024 23:53:08 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 23:53:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 23:53:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 23:53:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 23:53:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 23:53:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 23:53:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 23:53:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 23:53:12 GMT
EXPOSE 80
# Tue, 21 May 2024 23:53:13 GMT
EXPOSE 443
# Tue, 21 May 2024 23:53:13 GMT
EXPOSE 443/udp
# Tue, 21 May 2024 23:53:14 GMT
EXPOSE 2019
# Tue, 21 May 2024 23:53:19 GMT
RUN caddy version
# Tue, 21 May 2024 23:53:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1a072620eac005d85140631084040f090145b97856d39b4a3857f3883e1222`  
		Last Modified: Tue, 21 May 2024 23:53:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fe991d4d067d7cff69c70e75a1c849954f9564c5a39a63c4498d7d9923d653`  
		Last Modified: Tue, 21 May 2024 23:53:30 GMT  
		Size: 523.5 KB (523490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b875ce4f90053b0a9a3bf3455e32b742b97d8c17a2d71e0d6b6492e693d17f27`  
		Last Modified: Tue, 21 May 2024 23:53:29 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356659c3951686b02ad5198d3e2d7df7483764d9cc6e517c24a4583dbec88da3`  
		Last Modified: Tue, 21 May 2024 23:53:31 GMT  
		Size: 15.3 MB (15296256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2f0c9f3474fbab8f3a66eae9f7f84294ab34253aa7afed69383b9f609bef15`  
		Last Modified: Tue, 21 May 2024 23:53:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792652ad3ec00b1130a297274d739ac5a53042f507faceaedd584d490d364a45`  
		Last Modified: Tue, 21 May 2024 23:53:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183414d6935f7b5648933ca337c70b53aaa87c77636df30b20c73f51fa02a780`  
		Last Modified: Tue, 21 May 2024 23:53:28 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50c3bc4760ee42116a8382f5ddfc5c39db73d58db0bef6636d553d4f3d9cffc`  
		Last Modified: Tue, 21 May 2024 23:53:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f0c42983c0d6c326f29d6c92e8d17c1761d57f10b5a99292748b7054d54dad`  
		Last Modified: Tue, 21 May 2024 23:53:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef848fd2b41ad33300c96d0eb45d0221803603cb4f25d52d4c00a115f2822516`  
		Last Modified: Tue, 21 May 2024 23:53:27 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfb035898874b9fcc5587305135c07d86d6b538935c5cf6e727f37cc924d1c6`  
		Last Modified: Tue, 21 May 2024 23:53:26 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa1caef8f291d9735bb82e3adc30833ccd1a558b9b076698e10e7b59d104ccd`  
		Last Modified: Tue, 21 May 2024 23:53:26 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5515aa07f7d355f18c8a13ceee178d29c014647f3cdd8d1ba20dece8c91de14`  
		Last Modified: Tue, 21 May 2024 23:53:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be68d5ae1605829032856fbe8b34bdd5e05cbf6b341cc2631167acaccc346a14`  
		Last Modified: Tue, 21 May 2024 23:53:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067d493076bc7939fddbdf96feaaed7eca3d687a8e48a53e48d5437bbf49228a`  
		Last Modified: Tue, 21 May 2024 23:53:25 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb98a0364e924c2877291b5b27b3f2d6b074b17ab854a53bb0fb091827dd9202`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976272be25cbe9492fe5de336e275cd6b01e5c8d8b8462afe8d2b899700f9501`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1c874aabf9b7e3b95cf27a90ee7fd24d02cd4a3a53f62e5121dba9b6faa970`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c7615674f4476c40f0cd35a2a95d758f192dca7b61e6e4aea5de9bbc72984d`  
		Last Modified: Tue, 21 May 2024 23:53:24 GMT  
		Size: 378.4 KB (378436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0c5cc63dc69fa4bc18cac5916c9d7f097e4a16fe891263ff59c897ee821013`  
		Last Modified: Tue, 21 May 2024 23:53:23 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:ad476043b71201fec109c8544e1f097451531ec8f27f21e4449fb9a6a65e98c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:1e928a53a1d22675e8ac7610a67aa61c8d75b0e33b803276f73ca0dadd94113a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128692328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652a396f96cd4e13bb9f70cd679605874d65c68a34b4dc91b3eceeb615586986`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Tue, 21 May 2024 23:51:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 May 2024 23:52:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 21 May 2024 23:52:33 GMT
ENV CADDY_VERSION=v2.8.0-rc.1
# Tue, 21 May 2024 23:52:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0-rc.1/caddy_2.8.0-rc.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8be1502ab1872108833d1c8e3ce342df72b6f81acd3539e11b5333181419744a8342d52af2bd1b8033fde9105bb6b61a19479f969cae6f0964d12e08520019e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 21 May 2024 23:52:46 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 21 May 2024 23:52:46 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 21 May 2024 23:52:47 GMT
LABEL org.opencontainers.image.version=v2.8.0-rc.1
# Tue, 21 May 2024 23:52:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 21 May 2024 23:52:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 21 May 2024 23:52:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 21 May 2024 23:52:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 21 May 2024 23:52:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 21 May 2024 23:52:52 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 May 2024 23:52:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 21 May 2024 23:52:53 GMT
EXPOSE 80
# Tue, 21 May 2024 23:52:54 GMT
EXPOSE 443
# Tue, 21 May 2024 23:52:54 GMT
EXPOSE 443/udp
# Tue, 21 May 2024 23:52:55 GMT
EXPOSE 2019
# Tue, 21 May 2024 23:53:00 GMT
RUN caddy version
# Tue, 21 May 2024 23:53:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d53d01a42c0a6bb5a60af6315fc38ae466d0a7c27704dde3380c8bfd1972d4e`  
		Last Modified: Tue, 21 May 2024 23:53:12 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332a37e7263a68d1bebe71ff1eaf5e5419cd520081e4eca9c08d3766fef28183`  
		Last Modified: Tue, 21 May 2024 23:53:12 GMT  
		Size: 372.9 KB (372948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b0657715ead6f3d895b8500a2637d87ea862173f71b72d994f9617d1495904`  
		Last Modified: Tue, 21 May 2024 23:53:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4e1b56318ded1e2763959559ab09662928eb8f15a5173588c59f200a8dc386`  
		Last Modified: Tue, 21 May 2024 23:53:14 GMT  
		Size: 15.3 MB (15263586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed38526b5d20a13b399ef9860e0f5c36f6f9a7004795c55f664bd23d53cf679`  
		Last Modified: Tue, 21 May 2024 23:53:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8225895d3d9d361492fdd1a32c45e1a64458152651fcc69252267499d14a640`  
		Last Modified: Tue, 21 May 2024 23:53:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07176325acf1abec1d9d8f46ace70ce29032028d909c095fa563fc198f896a73`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff10d3353b9d4807209b066537ebce0ecbb7873ee190c1b7bd83193b8d5656d`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074fd7bc1f3ee4868f989a5f6e5a19572fcd662a1be0c6e6912f421b1ef98dd2`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85e3a2b2919cf9ed0019791a43da3a0c9cc49cc81066862767e0594ac51c2e2`  
		Last Modified: Tue, 21 May 2024 23:53:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e777328a70a10c2ac1381d3f06d42248cb7c874475cf169eadad57f81af948`  
		Last Modified: Tue, 21 May 2024 23:53:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304dd6f436c6a91290e32c1a5e70ecd3bb6e0e28c5e43ffafa9a63222553086f`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad69644f88f1b28f81728db89b7c8c2c9e034fb38e698b135086a58ab45a5b2d`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecc9ee6821c8a5e217e075076d0d69e51e4716385b4bf66d08270f41d1bbc75`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77d0c16f56f86b652826d6940dd16735cdfc8a951141f308bdb391f771ac452`  
		Last Modified: Tue, 21 May 2024 23:53:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cd8292bca9fdd5394dadb9bf57bf6c3f8b3b778f127d674008eb00989e2648`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b1d35936f1fbec2577e4ba733a5ec36114ab54c68a34d7a299a1343ee8890`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50e3fc7e2df5b834fa610172c0163405d68d716e98899e706e630dae5762bfb`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335979296be25675a4854ceffe266cdfe466ddab40aa9e4253515cbe5c677a51`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 362.4 KB (362442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed6984f20560778287d4f12326f3117b9aec06fe2b8583d05719146f22a125`  
		Last Modified: Tue, 21 May 2024 23:53:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.0`

**does not exist** (yet?)

## `caddy:2.8.0-alpine`

**does not exist** (yet?)

## `caddy:2.8.0-builder`

**does not exist** (yet?)

## `caddy:2.8.0-builder-alpine`

**does not exist** (yet?)

## `caddy:2.8.0-builder-windowsservercore-1809`

**does not exist** (yet?)

## `caddy:2.8.0-builder-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `caddy:2.8.0-windowsservercore`

**does not exist** (yet?)

## `caddy:2.8.0-windowsservercore-1809`

**does not exist** (yet?)

## `caddy:2.8.0-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `caddy:alpine`

```console
$ docker pull caddy@sha256:2e1d4592f1718bb47645da5a83a846fe19094f18e6c921fdf56d174f05c63213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:7b51768d110708c44179dc299884e9ee73d243a37abccce2dc796abc36371a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18476986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e21ce508b7f91169630895a0fe9a9f58288e5eb6e899c3462f168229c84193`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88463a31d6d2c104349aaaaae3b5a60c2a63ba0ac2712ba190211e9cd15d4cc`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 360.6 KB (360570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de93e10dd6701c976a78596c69babad750fc3957060c758b8859daab7fd2dd27`  
		Last Modified: Thu, 02 May 2024 00:51:57 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae96b49a2d955ff25ddc1858d84596c16d525d531d2342bd372945ccf5e410`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 14.7 MB (14706390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:666c65a5f3beaff567eaca64d4f307c64b81695485a64ad5d33ac192c1b299e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfba4fe57beaf0920d15623535056bcc81e42e1ac5eacec9827a7932a15bc94b`

```dockerfile
```

-	Layers:
	-	`sha256:0f942a2c6c2e9440173dadc3211a6cecf73e846edcdcb423bffad328d9c8727e`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 268.9 KB (268899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f88d335506cc1ae671b94135d1dff65cbb966f39e5145fe171d82377ea601c1`  
		Last Modified: Thu, 02 May 2024 00:51:57 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a37e44b94565539d082d85ceab947792effbecc9d7db223ea6abca196ee05a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17432782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b5570c733ff428231e40e91550787c9f5ddc4bb728f09cb7effb937964fa7d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320944b9d89ce73b5dbd09f5e7a6041004d85f4bef04eb1417a27e8a24f13f5b`  
		Last Modified: Wed, 01 May 2024 21:56:04 GMT  
		Size: 357.3 KB (357340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe068432b49975aecbf4e69d7736019056ee4d62a52931a724ff06f70e86c25`  
		Last Modified: Thu, 02 May 2024 00:56:31 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb925eb8f3d094c61b238fe90aca158009b859c95c7e87ff0cad1f810e65aa9`  
		Last Modified: Thu, 02 May 2024 00:56:32 GMT  
		Size: 13.9 MB (13920901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:29db70769c20c963daa30568350c31fc72970c036d8e8a0d7a7a8a47d275300e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58dc3b1df0157f859652c398af09ae3a777bb2fb92015e0f62436f9e993a7e54`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb7c30b377cc96f8036dbe70e0f8d249776fdbc6cac9bf32c4ba0e42eaa843`  
		Last Modified: Thu, 02 May 2024 00:56:31 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:3d1e889eda417007d88637f9adca7509e5bb547492e555d4a758ce2df850a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17156262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3523597ee5af2fd110570a00e504f5e22dd8704d65c7c8778bc0c9ef96ae269`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b527911aa0f8852117f57452d522fb961c184d105b0818cb4a87109b08272643`  
		Last Modified: Wed, 01 May 2024 22:05:53 GMT  
		Size: 353.7 KB (353705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ab12f0e1a27e1224e11b4fc25b25dc760337a04bb0883175300b1a8842aff2`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fa49870fc1f8bcbe7983ca022544c47da797299179b3287255e96b1254a28d`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 13.9 MB (13893683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1f74bd28526188e78a3ee7ac25ba3de34683b3251d1e0b495cc33270910d6d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060e4e44fb56999c235e64a72bcb39cc3db4a016d5e7307bb82c1a31106afb75`

```dockerfile
```

-	Layers:
	-	`sha256:eeda73bc8fa144234fa52e9915e531709e0b3d01b8aa6ed8dabfbeaa03d8ec52`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 269.0 KB (268967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039dd7674e2f60b9d2f360db16a7759fb38a2b8153fda85eff01c915c1da050e`  
		Last Modified: Thu, 02 May 2024 01:08:17 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:578dcc962eb6776e3e6ed964d11a13d40983f294e590f0040fc9febce144fa3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17278610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220a025aa536c6d9e845318ec54c7969a55f365311b36886f0eed8b3a218012`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f50788699932589070b139144f3b1440a2948fa84be4ca81ecdc1d1a54e4e69`  
		Last Modified: Wed, 01 May 2024 22:12:04 GMT  
		Size: 368.8 KB (368765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b07f03c61a8e689485aedd78191737c91a5f2f23e95122ca9de2af436c14c`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef67f47d4ab395e9c3fa86967774f6a1f31b10e560ad19c1a48b64db88bb6ee0`  
		Last Modified: Thu, 02 May 2024 04:53:38 GMT  
		Size: 13.6 MB (13569000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:38001a08c78526af0f51525a1f82a25923b94559287782c232932bff2c9a6682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b174326e15ad188a5fc078e50318dbccac12850ef07b98ac27e0ccdf2b05e9`

```dockerfile
```

-	Layers:
	-	`sha256:93cfedcf72234e144ba3ae74894f78ff082dc5b8330cbd00229c9377c80c9d93`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 268.9 KB (268918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a58d69a87e8d3b310715fe89231c5f8d7a4d5d6ee5add7d9a97ea9273937afa`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 17.6 KB (17552 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:2c0050449fe45c8df3fa0b90fa1621dd8fb2de864d8154aa379c73b71d1ee769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17060083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913f3ac3d369a2d5a24e332dec6da8cbca6f9d6c570768127927ee62e7aa7770`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0550c488b324bf74512534b8af77dc0690e94dd12f1286c76669cb03c733692`  
		Last Modified: Wed, 01 May 2024 22:06:02 GMT  
		Size: 370.3 KB (370278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f53ff24ab7a11bdbef2dbc4774bd8c9241c60f282247607ac7401ec586a681`  
		Last Modified: Thu, 02 May 2024 01:07:51 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30849c5c1ec8a58215a8ad6e5f79db3be0b1d9c9f843dcd81c42748732a39917`  
		Last Modified: Thu, 02 May 2024 01:07:52 GMT  
		Size: 13.3 MB (13333836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:09f14bafcec41acaf23fa3fbfcb3542d754279ff9bcd6994883dd551a91d9118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 KB (284603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e3abe481d46e34ec2db9e2960600548a2a65472765919c636e793baecc365e`

```dockerfile
```

-	Layers:
	-	`sha256:d8a5956a258ed188944c638c13de5928c93ec3795de1dbc3881214c0ddb98063`  
		Last Modified: Thu, 02 May 2024 01:07:52 GMT  
		Size: 267.0 KB (267003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24c13f8f699644b031a10dbed52d9ed326c7dde29529b70a82bb603d2677989`  
		Last Modified: Thu, 02 May 2024 01:07:51 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:faab60dc3a1acc475e2d0f12c86d9f31290b49896611d5cd61feb631ea7b0b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17828011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6446726caf9ff49671c1b47b04ff608cc10c783fd3dbf2a2d79d816140cb2ea`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7649425a6a944a0c8c4f452b8bc1e2874e0e99c7e097d2aec191fb8ac784fd6d`  
		Last Modified: Wed, 01 May 2024 22:05:37 GMT  
		Size: 364.7 KB (364696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df358d50a949fe6c09ee403e747cafa7b4bcdac928dbb75cee120ea25330f4`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc640f077739a0d0aa11a1722064f9f3d5dfc31ffc720787fe16c78e49d827`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 14.2 MB (14238300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a941d2a34e67bad02c9ee6d9cb55c09fccf5ae73670d0c5cf653ba2457ae8cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 KB (284475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76679ae3672baef460ec34615d3960669d3d95e73990aeddf0e2d5bd8573af8`

```dockerfile
```

-	Layers:
	-	`sha256:144c0dfb68c151b0a1b0c92da22a910fb7b8e8cc63389ab9b7e180d746bbf9c2`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 266.9 KB (266941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958b331e0cf47b7621d5c63aafb1753bf1abd52d632a23dd19e986657b53c310`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder`

```console
$ docker pull caddy@sha256:c4ca919a359a82291778345c9886a9cf948d4e4613aee402066f0be8819179ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:2d0f98ee37151fac228829512d71cd60683bcca714b42a2accfd5b2ed0eef309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77076844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da2caebf0c82328df2582d2154aea90549512f5f8075a1d211888861edc36d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ea3408117e6ad5da2610d98c7aaaa6ab17d9280a7f00e54b78f4a8af1a13e6`  
		Last Modified: Tue, 14 May 2024 22:57:18 GMT  
		Size: 293.4 KB (293394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91320369b822ebdafa53385de29218150ed2e0c9432c803ae9ab0917b1c13e05`  
		Last Modified: Tue, 14 May 2024 22:57:19 GMT  
		Size: 67.0 MB (67007431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0406650e82959e8bef670a6825ebc6caab141ed9ad0670923af9d5998de85b1b`  
		Last Modified: Tue, 14 May 2024 22:57:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54b29b355af23f51f47454c3e17573db8b78d7b52ce85f0455a2e39d7fa074`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 5.0 MB (4973399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbee18c299cb69dbccc6437fb935315abe5ea1a53244f52a8ef81bf71b3ec7c`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 1.4 MB (1399486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3962e3b1e39ca0549762f19fbf5ce97673a3c8e25e572443e99130f629becf`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:6f76e9858ca4547fe58ff97bd2ffc98029feb869b1dfc98633fd6f628b314292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 KB (288373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d01d8efed7000405f724e82795e9cc915343e431cc02e71f7cb5c25dc349bc`

```dockerfile
```

-	Layers:
	-	`sha256:746b0306cd3cb1912a3fc855ffc1003e09c16f75c165c8632bfe6eb00f877847`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 268.0 KB (268019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8416aff5ff51dc4e8fe28c6decdd0e3d91752160f7da7909a202850f8bd690`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ac7c2575373554f84061a11c48e068678edf889b364d17fc18cae4e80ce71e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75488808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48147857ead25ab7ee7a77aa74a59e293fa9eca878fe8afdd536d5f143675028`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c253e1ccd740370512ac16dc1198d4cc7e5f79502d830e914be781d2a53ef`  
		Last Modified: Tue, 14 May 2024 23:02:34 GMT  
		Size: 294.1 KB (294052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d6f1f07c341f159f464047d7dfc24c2fe15b8492e49ca6864e4bb242a3ec8`  
		Last Modified: Tue, 14 May 2024 23:03:32 GMT  
		Size: 65.8 MB (65766197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ab3f344a28c5c3a77d5b42ed139c704c1a62bb86a51a6d424570cbeddca4f3`  
		Last Modified: Tue, 14 May 2024 23:04:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b167340b71c005d807677fbbfbac662cedcb4fec7ccda3d644fa2d7cd2160000`  
		Last Modified: Tue, 14 May 2024 23:59:49 GMT  
		Size: 5.0 MB (4959292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db00701b53c1d5eee7ae5f0370ad0e2bf8c7624155e1ccd2197c482e47a9b928`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 1.3 MB (1321618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3610115cc7dedfcb5e2e244108591d41fbe0430d9c192503193a6f2a0e0c62`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:65e3693b278d4ef7c1c71f462d35e072feb067d47d882a6357051558d5f46278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 KB (20292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883db6588355f9fff45c61143a3c184d6b5360f70087363d292d63c4ffd73363`

```dockerfile
```

-	Layers:
	-	`sha256:f9d8b3568f220dfd1bdb1ddf4e41df2a13ced2a403b7245c9a18e0b60d52fd7b`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 20.3 KB (20292 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:09a6c1b0e1bd5044d5c064715c0aa03b90e6940ba650cf16faef929b3f79fa04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74794769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a0acea946d5a81787cb9fe18c7071c5aa68a591344d13571c0ce51a5e470d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1e32b4becad7a3ff9750dab0a6195a4136fe3417839cd5d6ced26f77c37d79`  
		Last Modified: Wed, 15 May 2024 08:39:33 GMT  
		Size: 293.0 KB (292954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab304151744566becd5140e866f02946274de2d4d2a228bdba72a0e4dddfa248`  
		Last Modified: Wed, 15 May 2024 08:40:52 GMT  
		Size: 65.8 MB (65766163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ceb4452378bf5d66c4470fe48fe8427a79ec5fdc8ddb8ea1c7fc02a13ce65b`  
		Last Modified: Wed, 15 May 2024 08:43:33 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270f12d361d5c63e9937439d8ff8f1080a9e9af98e31682da7f8d67a613c759`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 4.5 MB (4515403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058f91ac0045b9c67e0b445141195571ad95b6f59a25eb681889ad831b1498dd`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 1.3 MB (1318268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4d6b7782ec5dfb52798f8e6b9b9ab819fa68f6eb20afac4a297ba01be2efae`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:7642ba203742b9113008f284cfdf3548460cbae2ee69ecb2454eb8c735b96da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 KB (291146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94a8f15a57f45b959c2c2fc76cdd718d5ad776676b941690a80ec419f5487c6`

```dockerfile
```

-	Layers:
	-	`sha256:d711709c34958acee3c07ef7e1919d12e4928a2ca18487dd1819cbe2b91d6ae5`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 270.6 KB (270635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bcb88e50c5a338a29305fce33e34c339529ad379da7ba7d1cd2088bf08e935`  
		Last Modified: Wed, 15 May 2024 09:20:10 GMT  
		Size: 20.5 KB (20511 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:022c416ba80bd913b0d16582f1065f5c4b8ad34f219855b8a021c94d106524c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74098271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d00e35d265158288ca2a81ad2fdfbedc5b7035f13ab9cd1b998d4991d8fa37`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84613e011ca8867fd82ad1a4602a9c5ca1629a8c52b91548ba0a8ce39bc63bd6`  
		Last Modified: Wed, 15 May 2024 10:25:13 GMT  
		Size: 295.8 KB (295843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a7eb7dd16a3cb705d643f2c1b3ccb0cce9120eef39b1b1844864195af6c32`  
		Last Modified: Wed, 15 May 2024 10:28:17 GMT  
		Size: 64.1 MB (64106287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788e89ea89d463b8bcafc4d5b552bddaa08b72930505c3e5b6917da512bca47c`  
		Last Modified: Wed, 15 May 2024 10:29:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119b2251effb8f032617ef72426ede6300a48b24df3322f8180c5112fcb1488`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 5.1 MB (5063898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab86c9ac1c04673c91199de9df55b222aeb76d630df93b84c38cabab987ca9b`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 1.3 MB (1298290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e12372ead2b5522c0b9d32638dcec3d9780a4b4495fe0327787759f670419`  
		Last Modified: Wed, 15 May 2024 17:32:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e620ba0bef62789334c010b7cacf7a13de0927228fc5d74634b118f93d8a5ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 KB (288452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988be65311a6efef34a6bdac2f8dcba490cc5ae7a90c13a7b4b72cd68956fd79`

```dockerfile
```

-	Layers:
	-	`sha256:b860d1f348c1e8c34388faf32ca1f31601f367503a56b8482f22e27d112f725c`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 268.0 KB (268038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0144585ac3a8859d627186fb46c2dc5e2e025006a8801d6718aca937f207427`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 20.4 KB (20414 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ed5114faaef7109c9b6d09463fe6cd92b3012e1b89d7d4881ba567e2215f37c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa437d1d5649dee8d678ada0475d1bf336545ad8ffa4a692c19bba4fe496c25f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b2216e014970a83beea11c197a24ccf7f0027acc0d35a08b3a3b2c976b5eff`  
		Last Modified: Wed, 15 May 2024 04:47:32 GMT  
		Size: 296.3 KB (296270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b672324861585f05676c004287c9eeb3ec624b063c08e6689139af3a2f1ed3df`  
		Last Modified: Wed, 15 May 2024 05:01:36 GMT  
		Size: 64.1 MB (64129414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4969b1c1838dc52cc8a18a048524a037b980febaecd9563210c4df1a96604b42`  
		Last Modified: Wed, 15 May 2024 05:23:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abcaf0a32c421ab0105f8a6eb25fa2862e92a57fe5c68c0de96702a1496789d`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 5.3 MB (5270859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14972492f5cb274941b32172d5bccee08aba0eb45858ff97fe6fb9f45719fed`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 1.3 MB (1293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad16cdba266ead2ca15865cafeddfa415df7136a8ea60d18e820ce12c1407b61`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:2b40a03abefdfce61a9c05a652fbccf303ce8b02a57d74d4a4e0b3faebc448e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7793b7cdf8a3c9fe0b5515824960473b044a9be5b121a8763e7f63d45e27617e`

```dockerfile
```

-	Layers:
	-	`sha256:a992b851d066d8fb1da7d613d1d07540e1edd799d4b99a7da6d8c73629f8982c`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 266.2 KB (266157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b35b875bfd977ef42a74ac4b84ec1b6d05e4daea22d2a52db56fab59e5a6663`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 20.5 KB (20460 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:a47a2a03f9a9b7816a7a1113d57cd13a6291da16c23508710b0ca70debbb86d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76203648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e88c1f13b847682609243dade2de8bb68fc2643f3ef6c50cf558e301e6f05f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1a1d4bba7fb363f0ef2f025a4c6c441c7026445c4b9c955c509893576ea917`  
		Last Modified: Wed, 15 May 2024 02:47:56 GMT  
		Size: 293.9 KB (293929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109cf0320d2fb40b9f56e4b0b8249d43214d262e3aaa145e939c8d7354258d89`  
		Last Modified: Wed, 15 May 2024 02:49:19 GMT  
		Size: 66.2 MB (66221838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f36caa761931318dec5fb4c6712ab1ab66f9992473dd4c5bd890ad223c3ddd`  
		Last Modified: Wed, 15 May 2024 03:08:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c238da3c7fff1913d7b837e4c0413d72ec94e770a03bf0abcdd03ee7f233c6`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 5.1 MB (5117490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4576d2e047b1a8655a7d7395721fa5506df982c1b78ffc068954ec28445a9b7`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 1.4 MB (1352270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56b016932ac8f843faffdd88108c80fcd9b38b5ac893706dc6780d4777eb88d`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:51196241f4bb937ea188f006f7ce0120d183680a55447da6b30b27c68f3d44d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03069f12e51484e13fcfe4b6c7d03806f5efafe115a28c761003f672133cde4e`

```dockerfile
```

-	Layers:
	-	`sha256:074231774abc16fdbd7854582de2bfed128864d0fdabc7f75ee0b1cb2c153ebb`  
		Last Modified: Wed, 15 May 2024 04:14:19 GMT  
		Size: 266.1 KB (266063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77307ab5bd56ac3f136ed6992239aa495abc11b377b0e06d0fc98228b8c830bb`  
		Last Modified: Wed, 15 May 2024 04:14:19 GMT  
		Size: 20.4 KB (20390 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:ad54c78bb3d28e3aed3b194e44c2cef16277742c48cbdd5b62f57cff882294c7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2209668109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95a5f06a80f188aa7801df8ddf2e4cd69fd4686d0a68e51b8c04895fb4bd333`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:00:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:00:07 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:00:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:00:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:00:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:00:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:44 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:00:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:00:52 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 15 May 2024 22:02:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:02:03 GMT
WORKDIR C:\go
# Wed, 15 May 2024 22:54:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:54:20 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 15 May 2024 22:54:21 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:54:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 May 2024 22:55:43 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 May 2024 22:55:43 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff17c3a20dffac1d58c01594126216783c6f2f9b6c28a3a59f03a8ee906e2b`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a094f0476df4af0d71317b871f0fff1466fcb871824ba980d7746c7c7e19b4a`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e701d4f2f41ad4fc9ba76dec4fe56953399cd0f2f75d73d787daac52f5d01d42`  
		Last Modified: Wed, 15 May 2024 22:02:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf8bc44f874f9876c9d4e2d6081d14f0f7cae294108bd970a95a338c78e0267`  
		Last Modified: Wed, 15 May 2024 22:02:11 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0977a400b67989adcaa14e29549e6b7cf2016f2d293c6e0ad8c7e5131d6df`  
		Last Modified: Wed, 15 May 2024 22:02:10 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7ce095d7b4c8673e3da44be3d164160077fe5ceb1277aa402a7967f956ba12`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 25.4 MB (25431934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f74875c2cc73da758ccf48534c4447970abf1ca82506c5faac57fd7387bd95`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459ecbda0c5ac4cbd3edf97e00cc0f627e4a814ef2f3ce681bc4fe3a7240782f`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 329.6 KB (329556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1542fa949c26e34cf1b1b0142a0e23a25d2081c6735416c29aab51eb11a35e92`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac01d339a495506ea26c9903ee836493dd37f673f7861ff487d34fbad8dbe3a`  
		Last Modified: Wed, 15 May 2024 22:02:18 GMT  
		Size: 69.4 MB (69376703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018e748194263b3beeeee7e77a560e00f492435701dab2bccf109bed0f9b1fa5`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72448ba01254027acfd81714f262f5a929dfcae70bdce747d1b5d32febcadc3f`  
		Last Modified: Wed, 15 May 2024 22:55:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677ff24892a40528aaf057d88da31eaeae8979c187d0ec9d3a700b10eb9c0139`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b11f0b0a347b93aa95dcd56d43ffd423093f9baf73e3160778dbaf72f5b6ba`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f42c29fd8b1472cd668f410cae0b1e058865e8cfba4dc4afbba72139a3c73d`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5db520771c4c59ce4e205c4cb1527364a5242234c8c7ccd3aa8de0921b40fc`  
		Last Modified: Wed, 15 May 2024 22:55:48 GMT  
		Size: 1.8 MB (1841438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b63369b487f355d1be166f1cb0c1daaa037fbe80ce6e867e1f5f66a42dc8f4c`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:5a908c8e961d324c5675ab4c2ab96d32fa02aa4f5989320b06753099bd224455
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2276876401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c05c04fbdab0842c80fc8d1fc925f4ffca4f1ca02e89371883ffc6d7ce887b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:51:55 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:51:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:51:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:51:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:52:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:52:47 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:53:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:53:20 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 15 May 2024 21:56:21 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:56:23 GMT
WORKDIR C:\go
# Wed, 15 May 2024 22:53:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:53:36 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 15 May 2024 22:53:37 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:53:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 May 2024 22:55:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 May 2024 22:55:09 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896e983a0a4309b805accb8ae63327cc1f3b8f992e0d75b555a5c61d02fed986`  
		Last Modified: Wed, 15 May 2024 21:56:31 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c7744622a8e10412cfb393caef5a301667c3db556da9fd3857c72be60fcdc`  
		Last Modified: Wed, 15 May 2024 21:56:31 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b652aa3eb2aa15638a8e9f572497cfd1fb6884ebeeb6ecdc9074aad63f79a69`  
		Last Modified: Wed, 15 May 2024 21:56:30 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148c74e800af547d1d14d91f5b9c167f17c75e65d02f875b5ae130c570d83299`  
		Last Modified: Wed, 15 May 2024 21:56:29 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bccf2db4b47631e2d74d6e6ad17ebb28e6387c6e6c884011fdde2bf29fac7e`  
		Last Modified: Wed, 15 May 2024 21:56:29 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d4419852279e679aaa47097723ddfa68affbce518a5f31fe47caabc8b251d`  
		Last Modified: Wed, 15 May 2024 21:56:32 GMT  
		Size: 25.6 MB (25575407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8509005ef5150522ee2b4ded57557935baf2a14c34cc5d25b2241d935a81284a`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1477c6f08b1aaca7cf172e0b0e9b08c945114f3cfca719b6d9479d28377627da`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 346.4 KB (346387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd971ba008fee57e5da9f3e4bc2084142f53a330c099ed32492c660baebc4af`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3866e6ca6d2695e04b9a5fdb00612bf63b2a25f82548a42a0e9ea44defcc619`  
		Last Modified: Wed, 15 May 2024 21:56:38 GMT  
		Size: 69.4 MB (69400042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063360e32b8a7b88e36a87b59c4cdb689ee9bce85fff56da69f8a0953db6a9c3`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517e5d69bc86420b8e423d4fd9afd5e4138c87c06149927fb1ada38053147657`  
		Last Modified: Wed, 15 May 2024 22:55:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c1d817dc7c4f2d1ed65b8ebe3020056e330b2880f3ad70d0802de6684feb54`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf22c592153e6d7c1e0037379a2ec28694088ec9e283ef66024397d93249165c`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46c8b9479856498dc80f87da766924b2bbb9fcd9f7ecaf9e84245241ac743a5`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e3a07a3c56d5582fc71b9183eadde4dc83368be6d164ae5c95c4a9f4522234`  
		Last Modified: Wed, 15 May 2024 22:55:14 GMT  
		Size: 1.8 MB (1826095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677fb13fe6786ac8f8b9f709a8cfe6db6074ad603b3a45efe55fa8c478e22766`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:1bd8cac07af2bd33d70ca237e3fa5324af77ff08d2868e890ef971eb2c9222b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:2d0f98ee37151fac228829512d71cd60683bcca714b42a2accfd5b2ed0eef309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77076844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da2caebf0c82328df2582d2154aea90549512f5f8075a1d211888861edc36d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ea3408117e6ad5da2610d98c7aaaa6ab17d9280a7f00e54b78f4a8af1a13e6`  
		Last Modified: Tue, 14 May 2024 22:57:18 GMT  
		Size: 293.4 KB (293394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91320369b822ebdafa53385de29218150ed2e0c9432c803ae9ab0917b1c13e05`  
		Last Modified: Tue, 14 May 2024 22:57:19 GMT  
		Size: 67.0 MB (67007431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0406650e82959e8bef670a6825ebc6caab141ed9ad0670923af9d5998de85b1b`  
		Last Modified: Tue, 14 May 2024 22:57:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54b29b355af23f51f47454c3e17573db8b78d7b52ce85f0455a2e39d7fa074`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 5.0 MB (4973399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbee18c299cb69dbccc6437fb935315abe5ea1a53244f52a8ef81bf71b3ec7c`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 1.4 MB (1399486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3962e3b1e39ca0549762f19fbf5ce97673a3c8e25e572443e99130f629becf`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:6f76e9858ca4547fe58ff97bd2ffc98029feb869b1dfc98633fd6f628b314292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 KB (288373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d01d8efed7000405f724e82795e9cc915343e431cc02e71f7cb5c25dc349bc`

```dockerfile
```

-	Layers:
	-	`sha256:746b0306cd3cb1912a3fc855ffc1003e09c16f75c165c8632bfe6eb00f877847`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 268.0 KB (268019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8416aff5ff51dc4e8fe28c6decdd0e3d91752160f7da7909a202850f8bd690`  
		Last Modified: Tue, 14 May 2024 23:54:33 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ac7c2575373554f84061a11c48e068678edf889b364d17fc18cae4e80ce71e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75488808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48147857ead25ab7ee7a77aa74a59e293fa9eca878fe8afdd536d5f143675028`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c253e1ccd740370512ac16dc1198d4cc7e5f79502d830e914be781d2a53ef`  
		Last Modified: Tue, 14 May 2024 23:02:34 GMT  
		Size: 294.1 KB (294052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d6f1f07c341f159f464047d7dfc24c2fe15b8492e49ca6864e4bb242a3ec8`  
		Last Modified: Tue, 14 May 2024 23:03:32 GMT  
		Size: 65.8 MB (65766197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ab3f344a28c5c3a77d5b42ed139c704c1a62bb86a51a6d424570cbeddca4f3`  
		Last Modified: Tue, 14 May 2024 23:04:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b167340b71c005d807677fbbfbac662cedcb4fec7ccda3d644fa2d7cd2160000`  
		Last Modified: Tue, 14 May 2024 23:59:49 GMT  
		Size: 5.0 MB (4959292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db00701b53c1d5eee7ae5f0370ad0e2bf8c7624155e1ccd2197c482e47a9b928`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 1.3 MB (1321618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3610115cc7dedfcb5e2e244108591d41fbe0430d9c192503193a6f2a0e0c62`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:65e3693b278d4ef7c1c71f462d35e072feb067d47d882a6357051558d5f46278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 KB (20292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883db6588355f9fff45c61143a3c184d6b5360f70087363d292d63c4ffd73363`

```dockerfile
```

-	Layers:
	-	`sha256:f9d8b3568f220dfd1bdb1ddf4e41df2a13ced2a403b7245c9a18e0b60d52fd7b`  
		Last Modified: Tue, 14 May 2024 23:59:48 GMT  
		Size: 20.3 KB (20292 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:09a6c1b0e1bd5044d5c064715c0aa03b90e6940ba650cf16faef929b3f79fa04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74794769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a0acea946d5a81787cb9fe18c7071c5aa68a591344d13571c0ce51a5e470d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1e32b4becad7a3ff9750dab0a6195a4136fe3417839cd5d6ced26f77c37d79`  
		Last Modified: Wed, 15 May 2024 08:39:33 GMT  
		Size: 293.0 KB (292954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab304151744566becd5140e866f02946274de2d4d2a228bdba72a0e4dddfa248`  
		Last Modified: Wed, 15 May 2024 08:40:52 GMT  
		Size: 65.8 MB (65766163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ceb4452378bf5d66c4470fe48fe8427a79ec5fdc8ddb8ea1c7fc02a13ce65b`  
		Last Modified: Wed, 15 May 2024 08:43:33 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270f12d361d5c63e9937439d8ff8f1080a9e9af98e31682da7f8d67a613c759`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 4.5 MB (4515403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058f91ac0045b9c67e0b445141195571ad95b6f59a25eb681889ad831b1498dd`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 1.3 MB (1318268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4d6b7782ec5dfb52798f8e6b9b9ab819fa68f6eb20afac4a297ba01be2efae`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7642ba203742b9113008f284cfdf3548460cbae2ee69ecb2454eb8c735b96da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 KB (291146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94a8f15a57f45b959c2c2fc76cdd718d5ad776676b941690a80ec419f5487c6`

```dockerfile
```

-	Layers:
	-	`sha256:d711709c34958acee3c07ef7e1919d12e4928a2ca18487dd1819cbe2b91d6ae5`  
		Last Modified: Wed, 15 May 2024 09:20:11 GMT  
		Size: 270.6 KB (270635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bcb88e50c5a338a29305fce33e34c339529ad379da7ba7d1cd2088bf08e935`  
		Last Modified: Wed, 15 May 2024 09:20:10 GMT  
		Size: 20.5 KB (20511 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:022c416ba80bd913b0d16582f1065f5c4b8ad34f219855b8a021c94d106524c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74098271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d00e35d265158288ca2a81ad2fdfbedc5b7035f13ab9cd1b998d4991d8fa37`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84613e011ca8867fd82ad1a4602a9c5ca1629a8c52b91548ba0a8ce39bc63bd6`  
		Last Modified: Wed, 15 May 2024 10:25:13 GMT  
		Size: 295.8 KB (295843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a7eb7dd16a3cb705d643f2c1b3ccb0cce9120eef39b1b1844864195af6c32`  
		Last Modified: Wed, 15 May 2024 10:28:17 GMT  
		Size: 64.1 MB (64106287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788e89ea89d463b8bcafc4d5b552bddaa08b72930505c3e5b6917da512bca47c`  
		Last Modified: Wed, 15 May 2024 10:29:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119b2251effb8f032617ef72426ede6300a48b24df3322f8180c5112fcb1488`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 5.1 MB (5063898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab86c9ac1c04673c91199de9df55b222aeb76d630df93b84c38cabab987ca9b`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 1.3 MB (1298290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e12372ead2b5522c0b9d32638dcec3d9780a4b4495fe0327787759f670419`  
		Last Modified: Wed, 15 May 2024 17:32:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e620ba0bef62789334c010b7cacf7a13de0927228fc5d74634b118f93d8a5ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 KB (288452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988be65311a6efef34a6bdac2f8dcba490cc5ae7a90c13a7b4b72cd68956fd79`

```dockerfile
```

-	Layers:
	-	`sha256:b860d1f348c1e8c34388faf32ca1f31601f367503a56b8482f22e27d112f725c`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 268.0 KB (268038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0144585ac3a8859d627186fb46c2dc5e2e025006a8801d6718aca937f207427`  
		Last Modified: Wed, 15 May 2024 17:32:46 GMT  
		Size: 20.4 KB (20414 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ed5114faaef7109c9b6d09463fe6cd92b3012e1b89d7d4881ba567e2215f37c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa437d1d5649dee8d678ada0475d1bf336545ad8ffa4a692c19bba4fe496c25f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b2216e014970a83beea11c197a24ccf7f0027acc0d35a08b3a3b2c976b5eff`  
		Last Modified: Wed, 15 May 2024 04:47:32 GMT  
		Size: 296.3 KB (296270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b672324861585f05676c004287c9eeb3ec624b063c08e6689139af3a2f1ed3df`  
		Last Modified: Wed, 15 May 2024 05:01:36 GMT  
		Size: 64.1 MB (64129414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4969b1c1838dc52cc8a18a048524a037b980febaecd9563210c4df1a96604b42`  
		Last Modified: Wed, 15 May 2024 05:23:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abcaf0a32c421ab0105f8a6eb25fa2862e92a57fe5c68c0de96702a1496789d`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 5.3 MB (5270859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14972492f5cb274941b32172d5bccee08aba0eb45858ff97fe6fb9f45719fed`  
		Last Modified: Wed, 15 May 2024 06:09:04 GMT  
		Size: 1.3 MB (1293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad16cdba266ead2ca15865cafeddfa415df7136a8ea60d18e820ce12c1407b61`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2b40a03abefdfce61a9c05a652fbccf303ce8b02a57d74d4a4e0b3faebc448e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7793b7cdf8a3c9fe0b5515824960473b044a9be5b121a8763e7f63d45e27617e`

```dockerfile
```

-	Layers:
	-	`sha256:a992b851d066d8fb1da7d613d1d07540e1edd799d4b99a7da6d8c73629f8982c`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 266.2 KB (266157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b35b875bfd977ef42a74ac4b84ec1b6d05e4daea22d2a52db56fab59e5a6663`  
		Last Modified: Wed, 15 May 2024 06:09:03 GMT  
		Size: 20.5 KB (20460 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:a47a2a03f9a9b7816a7a1113d57cd13a6291da16c23508710b0ca70debbb86d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76203648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e88c1f13b847682609243dade2de8bb68fc2643f3ef6c50cf558e301e6f05f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:28:41 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 16:28:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:28:41 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:28:41 GMT
WORKDIR /go
# Wed, 08 May 2024 13:06:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 08 May 2024 13:06:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 May 2024 13:06:02 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 May 2024 13:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='d4866142b2c816dce25685b68af6aa4b65aab01090eb58ffbe963b854f83d3d9ea8c46381d888d5435b8ff971c65878236c23aa9891586a2a69b495fc910b342' ;; 		armhf)   binArch='armv6'; checksum='f3aa9db51a9130ba78da70ef026986ca51df3365449e5b0df6fa8c7bc3f88ad03b6a4072e61a0065fffe115511645c3b31f1deff0aa7590e2f7bab853bda9b3b' ;; 		armv7)   binArch='armv7'; checksum='1c007bd092b2422432e2db7d5c3ecc422c54af669e57bc16df316baadd9857ad4be960852ffd08af9b5530ff31218c458bde3961554fb1218f8519349b6949e7' ;; 		aarch64) binArch='arm64'; checksum='8d2462a174f2caf092b0d3ced612d0cd352a0afba736b0b81ca100c5ffbdb09b6d1978f49db7b1953e559eae42956912f20f59995112813b120217a624a21893' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e99b53e5dd805dc4e06ada2af7fc417a3073e24cba25d400395aa28f385be80db4f4b95ce8548be91c7d668f3a331dcf2293d295f903bf0703e1ca8a95ba47cb' ;; 		s390x)   binArch='s390x'; checksum='edadaa2aa6ff491517697ab887fbe3909026d7085dff772d754fb93d02a5008b344aeed995088bb79afb8b1cc01ed1c96af7b832c0b6888f1c5bedd3d567c4f6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 May 2024 13:06:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 May 2024 13:06:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1a1d4bba7fb363f0ef2f025a4c6c441c7026445c4b9c955c509893576ea917`  
		Last Modified: Wed, 15 May 2024 02:47:56 GMT  
		Size: 293.9 KB (293929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109cf0320d2fb40b9f56e4b0b8249d43214d262e3aaa145e939c8d7354258d89`  
		Last Modified: Wed, 15 May 2024 02:49:19 GMT  
		Size: 66.2 MB (66221838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f36caa761931318dec5fb4c6712ab1ab66f9992473dd4c5bd890ad223c3ddd`  
		Last Modified: Wed, 15 May 2024 03:08:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c238da3c7fff1913d7b837e4c0413d72ec94e770a03bf0abcdd03ee7f233c6`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 5.1 MB (5117490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4576d2e047b1a8655a7d7395721fa5506df982c1b78ffc068954ec28445a9b7`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 1.4 MB (1352270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56b016932ac8f843faffdd88108c80fcd9b38b5ac893706dc6780d4777eb88d`  
		Last Modified: Wed, 15 May 2024 04:14:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:51196241f4bb937ea188f006f7ce0120d183680a55447da6b30b27c68f3d44d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03069f12e51484e13fcfe4b6c7d03806f5efafe115a28c761003f672133cde4e`

```dockerfile
```

-	Layers:
	-	`sha256:074231774abc16fdbd7854582de2bfed128864d0fdabc7f75ee0b1cb2c153ebb`  
		Last Modified: Wed, 15 May 2024 04:14:19 GMT  
		Size: 266.1 KB (266063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77307ab5bd56ac3f136ed6992239aa495abc11b377b0e06d0fc98228b8c830bb`  
		Last Modified: Wed, 15 May 2024 04:14:19 GMT  
		Size: 20.4 KB (20390 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:d9056f7c8ccc04e12cf3daf31698cdcf5f083170891372f94d61c8da6db21187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:5a908c8e961d324c5675ab4c2ab96d32fa02aa4f5989320b06753099bd224455
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2276876401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c05c04fbdab0842c80fc8d1fc925f4ffca4f1ca02e89371883ffc6d7ce887b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:51:55 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:51:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:51:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:51:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:52:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:52:47 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:53:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:53:20 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 15 May 2024 21:56:21 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:56:23 GMT
WORKDIR C:\go
# Wed, 15 May 2024 22:53:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:53:36 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 15 May 2024 22:53:37 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:53:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 May 2024 22:55:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 May 2024 22:55:09 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896e983a0a4309b805accb8ae63327cc1f3b8f992e0d75b555a5c61d02fed986`  
		Last Modified: Wed, 15 May 2024 21:56:31 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c7744622a8e10412cfb393caef5a301667c3db556da9fd3857c72be60fcdc`  
		Last Modified: Wed, 15 May 2024 21:56:31 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b652aa3eb2aa15638a8e9f572497cfd1fb6884ebeeb6ecdc9074aad63f79a69`  
		Last Modified: Wed, 15 May 2024 21:56:30 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148c74e800af547d1d14d91f5b9c167f17c75e65d02f875b5ae130c570d83299`  
		Last Modified: Wed, 15 May 2024 21:56:29 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bccf2db4b47631e2d74d6e6ad17ebb28e6387c6e6c884011fdde2bf29fac7e`  
		Last Modified: Wed, 15 May 2024 21:56:29 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d4419852279e679aaa47097723ddfa68affbce518a5f31fe47caabc8b251d`  
		Last Modified: Wed, 15 May 2024 21:56:32 GMT  
		Size: 25.6 MB (25575407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8509005ef5150522ee2b4ded57557935baf2a14c34cc5d25b2241d935a81284a`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1477c6f08b1aaca7cf172e0b0e9b08c945114f3cfca719b6d9479d28377627da`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 346.4 KB (346387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd971ba008fee57e5da9f3e4bc2084142f53a330c099ed32492c660baebc4af`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3866e6ca6d2695e04b9a5fdb00612bf63b2a25f82548a42a0e9ea44defcc619`  
		Last Modified: Wed, 15 May 2024 21:56:38 GMT  
		Size: 69.4 MB (69400042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063360e32b8a7b88e36a87b59c4cdb689ee9bce85fff56da69f8a0953db6a9c3`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517e5d69bc86420b8e423d4fd9afd5e4138c87c06149927fb1ada38053147657`  
		Last Modified: Wed, 15 May 2024 22:55:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c1d817dc7c4f2d1ed65b8ebe3020056e330b2880f3ad70d0802de6684feb54`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf22c592153e6d7c1e0037379a2ec28694088ec9e283ef66024397d93249165c`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46c8b9479856498dc80f87da766924b2bbb9fcd9f7ecaf9e84245241ac743a5`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e3a07a3c56d5582fc71b9183eadde4dc83368be6d164ae5c95c4a9f4522234`  
		Last Modified: Wed, 15 May 2024 22:55:14 GMT  
		Size: 1.8 MB (1826095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677fb13fe6786ac8f8b9f709a8cfe6db6074ad603b3a45efe55fa8c478e22766`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:556e1cdffb3884bd3e44b4b252bd2886642eb4470ca6a9612f027f00f3f6a366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:ad54c78bb3d28e3aed3b194e44c2cef16277742c48cbdd5b62f57cff882294c7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2209668109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95a5f06a80f188aa7801df8ddf2e4cd69fd4686d0a68e51b8c04895fb4bd333`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:00:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:00:07 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:00:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:00:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:00:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:00:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:44 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:00:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:00:52 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 15 May 2024 22:02:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:02:03 GMT
WORKDIR C:\go
# Wed, 15 May 2024 22:54:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:54:20 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 15 May 2024 22:54:21 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:54:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 May 2024 22:55:43 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 May 2024 22:55:43 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff17c3a20dffac1d58c01594126216783c6f2f9b6c28a3a59f03a8ee906e2b`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a094f0476df4af0d71317b871f0fff1466fcb871824ba980d7746c7c7e19b4a`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e701d4f2f41ad4fc9ba76dec4fe56953399cd0f2f75d73d787daac52f5d01d42`  
		Last Modified: Wed, 15 May 2024 22:02:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf8bc44f874f9876c9d4e2d6081d14f0f7cae294108bd970a95a338c78e0267`  
		Last Modified: Wed, 15 May 2024 22:02:11 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0977a400b67989adcaa14e29549e6b7cf2016f2d293c6e0ad8c7e5131d6df`  
		Last Modified: Wed, 15 May 2024 22:02:10 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7ce095d7b4c8673e3da44be3d164160077fe5ceb1277aa402a7967f956ba12`  
		Last Modified: Wed, 15 May 2024 22:02:12 GMT  
		Size: 25.4 MB (25431934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f74875c2cc73da758ccf48534c4447970abf1ca82506c5faac57fd7387bd95`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459ecbda0c5ac4cbd3edf97e00cc0f627e4a814ef2f3ce681bc4fe3a7240782f`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 329.6 KB (329556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1542fa949c26e34cf1b1b0142a0e23a25d2081c6735416c29aab51eb11a35e92`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac01d339a495506ea26c9903ee836493dd37f673f7861ff487d34fbad8dbe3a`  
		Last Modified: Wed, 15 May 2024 22:02:18 GMT  
		Size: 69.4 MB (69376703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018e748194263b3beeeee7e77a560e00f492435701dab2bccf109bed0f9b1fa5`  
		Last Modified: Wed, 15 May 2024 22:02:08 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72448ba01254027acfd81714f262f5a929dfcae70bdce747d1b5d32febcadc3f`  
		Last Modified: Wed, 15 May 2024 22:55:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677ff24892a40528aaf057d88da31eaeae8979c187d0ec9d3a700b10eb9c0139`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b11f0b0a347b93aa95dcd56d43ffd423093f9baf73e3160778dbaf72f5b6ba`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f42c29fd8b1472cd668f410cae0b1e058865e8cfba4dc4afbba72139a3c73d`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5db520771c4c59ce4e205c4cb1527364a5242234c8c7ccd3aa8de0921b40fc`  
		Last Modified: Wed, 15 May 2024 22:55:48 GMT  
		Size: 1.8 MB (1841438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b63369b487f355d1be166f1cb0c1daaa037fbe80ce6e867e1f5f66a42dc8f4c`  
		Last Modified: Wed, 15 May 2024 22:55:47 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:236c6a30ccb84fa412a5360ca8b586d804faba0621ea182fb45902608cd8a563
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:7b51768d110708c44179dc299884e9ee73d243a37abccce2dc796abc36371a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18476986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e21ce508b7f91169630895a0fe9a9f58288e5eb6e899c3462f168229c84193`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88463a31d6d2c104349aaaaae3b5a60c2a63ba0ac2712ba190211e9cd15d4cc`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 360.6 KB (360570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de93e10dd6701c976a78596c69babad750fc3957060c758b8859daab7fd2dd27`  
		Last Modified: Thu, 02 May 2024 00:51:57 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae96b49a2d955ff25ddc1858d84596c16d525d531d2342bd372945ccf5e410`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 14.7 MB (14706390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:666c65a5f3beaff567eaca64d4f307c64b81695485a64ad5d33ac192c1b299e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfba4fe57beaf0920d15623535056bcc81e42e1ac5eacec9827a7932a15bc94b`

```dockerfile
```

-	Layers:
	-	`sha256:0f942a2c6c2e9440173dadc3211a6cecf73e846edcdcb423bffad328d9c8727e`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 268.9 KB (268899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f88d335506cc1ae671b94135d1dff65cbb966f39e5145fe171d82377ea601c1`  
		Last Modified: Thu, 02 May 2024 00:51:57 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a37e44b94565539d082d85ceab947792effbecc9d7db223ea6abca196ee05a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17432782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b5570c733ff428231e40e91550787c9f5ddc4bb728f09cb7effb937964fa7d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320944b9d89ce73b5dbd09f5e7a6041004d85f4bef04eb1417a27e8a24f13f5b`  
		Last Modified: Wed, 01 May 2024 21:56:04 GMT  
		Size: 357.3 KB (357340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe068432b49975aecbf4e69d7736019056ee4d62a52931a724ff06f70e86c25`  
		Last Modified: Thu, 02 May 2024 00:56:31 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb925eb8f3d094c61b238fe90aca158009b859c95c7e87ff0cad1f810e65aa9`  
		Last Modified: Thu, 02 May 2024 00:56:32 GMT  
		Size: 13.9 MB (13920901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:29db70769c20c963daa30568350c31fc72970c036d8e8a0d7a7a8a47d275300e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58dc3b1df0157f859652c398af09ae3a777bb2fb92015e0f62436f9e993a7e54`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb7c30b377cc96f8036dbe70e0f8d249776fdbc6cac9bf32c4ba0e42eaa843`  
		Last Modified: Thu, 02 May 2024 00:56:31 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:3d1e889eda417007d88637f9adca7509e5bb547492e555d4a758ce2df850a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17156262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3523597ee5af2fd110570a00e504f5e22dd8704d65c7c8778bc0c9ef96ae269`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b527911aa0f8852117f57452d522fb961c184d105b0818cb4a87109b08272643`  
		Last Modified: Wed, 01 May 2024 22:05:53 GMT  
		Size: 353.7 KB (353705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ab12f0e1a27e1224e11b4fc25b25dc760337a04bb0883175300b1a8842aff2`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fa49870fc1f8bcbe7983ca022544c47da797299179b3287255e96b1254a28d`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 13.9 MB (13893683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:1f74bd28526188e78a3ee7ac25ba3de34683b3251d1e0b495cc33270910d6d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060e4e44fb56999c235e64a72bcb39cc3db4a016d5e7307bb82c1a31106afb75`

```dockerfile
```

-	Layers:
	-	`sha256:eeda73bc8fa144234fa52e9915e531709e0b3d01b8aa6ed8dabfbeaa03d8ec52`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 269.0 KB (268967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039dd7674e2f60b9d2f360db16a7759fb38a2b8153fda85eff01c915c1da050e`  
		Last Modified: Thu, 02 May 2024 01:08:17 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:578dcc962eb6776e3e6ed964d11a13d40983f294e590f0040fc9febce144fa3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17278610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220a025aa536c6d9e845318ec54c7969a55f365311b36886f0eed8b3a218012`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f50788699932589070b139144f3b1440a2948fa84be4ca81ecdc1d1a54e4e69`  
		Last Modified: Wed, 01 May 2024 22:12:04 GMT  
		Size: 368.8 KB (368765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b07f03c61a8e689485aedd78191737c91a5f2f23e95122ca9de2af436c14c`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef67f47d4ab395e9c3fa86967774f6a1f31b10e560ad19c1a48b64db88bb6ee0`  
		Last Modified: Thu, 02 May 2024 04:53:38 GMT  
		Size: 13.6 MB (13569000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:38001a08c78526af0f51525a1f82a25923b94559287782c232932bff2c9a6682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b174326e15ad188a5fc078e50318dbccac12850ef07b98ac27e0ccdf2b05e9`

```dockerfile
```

-	Layers:
	-	`sha256:93cfedcf72234e144ba3ae74894f78ff082dc5b8330cbd00229c9377c80c9d93`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 268.9 KB (268918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a58d69a87e8d3b310715fe89231c5f8d7a4d5d6ee5add7d9a97ea9273937afa`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 17.6 KB (17552 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:2c0050449fe45c8df3fa0b90fa1621dd8fb2de864d8154aa379c73b71d1ee769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17060083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913f3ac3d369a2d5a24e332dec6da8cbca6f9d6c570768127927ee62e7aa7770`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0550c488b324bf74512534b8af77dc0690e94dd12f1286c76669cb03c733692`  
		Last Modified: Wed, 01 May 2024 22:06:02 GMT  
		Size: 370.3 KB (370278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f53ff24ab7a11bdbef2dbc4774bd8c9241c60f282247607ac7401ec586a681`  
		Last Modified: Thu, 02 May 2024 01:07:51 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30849c5c1ec8a58215a8ad6e5f79db3be0b1d9c9f843dcd81c42748732a39917`  
		Last Modified: Thu, 02 May 2024 01:07:52 GMT  
		Size: 13.3 MB (13333836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:09f14bafcec41acaf23fa3fbfcb3542d754279ff9bcd6994883dd551a91d9118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 KB (284603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e3abe481d46e34ec2db9e2960600548a2a65472765919c636e793baecc365e`

```dockerfile
```

-	Layers:
	-	`sha256:d8a5956a258ed188944c638c13de5928c93ec3795de1dbc3881214c0ddb98063`  
		Last Modified: Thu, 02 May 2024 01:07:52 GMT  
		Size: 267.0 KB (267003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24c13f8f699644b031a10dbed52d9ed326c7dde29529b70a82bb603d2677989`  
		Last Modified: Thu, 02 May 2024 01:07:51 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:faab60dc3a1acc475e2d0f12c86d9f31290b49896611d5cd61feb631ea7b0b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17828011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6446726caf9ff49671c1b47b04ff608cc10c783fd3dbf2a2d79d816140cb2ea`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7649425a6a944a0c8c4f452b8bc1e2874e0e99c7e097d2aec191fb8ac784fd6d`  
		Last Modified: Wed, 01 May 2024 22:05:37 GMT  
		Size: 364.7 KB (364696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df358d50a949fe6c09ee403e747cafa7b4bcdac928dbb75cee120ea25330f4`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc640f077739a0d0aa11a1722064f9f3d5dfc31ffc720787fe16c78e49d827`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 14.2 MB (14238300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:a941d2a34e67bad02c9ee6d9cb55c09fccf5ae73670d0c5cf653ba2457ae8cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 KB (284475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76679ae3672baef460ec34615d3960669d3d95e73990aeddf0e2d5bd8573af8`

```dockerfile
```

-	Layers:
	-	`sha256:144c0dfb68c151b0a1b0c92da22a910fb7b8e8cc63389ab9b7e180d746bbf9c2`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 266.9 KB (266941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958b331e0cf47b7621d5c63aafb1753bf1abd52d632a23dd19e986657b53c310`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e2f8b997d964717694810a581f3548bb7c88de368a40ad9de4f8ed414fa2c8bc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128741780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48489f36ce94641f6ce5703ea4babbd5e2e2ec4dbffc55809b7eb8c1c1508cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:03:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:03:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 22:04:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:04:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 22:04:09 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 22:04:10 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 22:04:10 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 22:04:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 22:04:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 22:04:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 80
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 443
# Wed, 15 May 2024 22:04:17 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 22:04:18 GMT
EXPOSE 2019
# Wed, 15 May 2024 22:04:22 GMT
RUN caddy version
# Wed, 15 May 2024 22:04:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cabe3592a5a508b32120c2f3f50485ce2af3e5b977d817fa71bff28061336aa`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7474cb4a8c303c68700f525e09e3bd29bb30d75dc33c01ea4a44732e7e7423f7`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 364.6 KB (364646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6d09183adf4d940c7dac96cc9d75af33bcb47d7d1811a7a296ad60e0d1b1c`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ce5e1d365ba13fb9103a5020b6644b3ae71e76d5e4d159b2f58914673cf2bf`  
		Last Modified: Wed, 15 May 2024 22:04:31 GMT  
		Size: 15.3 MB (15344884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aded66dd078b571ebb532e084c4af4f6beb685bd8a5b7524468e97c168f1a5`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37260cc3f9937e208886001176fd42c7113d3d49bdfd01a29d269126dc8538b4`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c851cec2c829abe440fde3ba79f95ec4728dfa01da5cb2b09e817e7581dc6b`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358cdf5957564add30758b73811ebe0f230cea2692cbb624fb5e8c369dcacc32`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b6a2684656992e4dbd6e42d4dd8ee988d00626cd55d362075a3a9243af3b54`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccb203e5de222a30a89c733e9964e55090c4ff8911cd1ccd005de5e27d7523`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097f79242227f6445dd34eaf655c51b48ce991b72a1ff5589b72787ee42f0fee`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e44fe3122406544397fc58d026c1cbeea8aec0444aaa6d12a759f86d4714c4`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401e6d173f17fd472a9adf0f3ce231ed4fa53e327b3fbd222c6900a64dc1573`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571e94ebd3fc2965298bc42c3810c16d0f6f6c9743a4b5aea94dc66e91aad8e2`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484373c77dd756bb7eb292a32b21c4039a936fdd0871ca3bc6c7467fcf29c77f`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9921976cbc4a4e3222ce034a2dbd34e498f4bc4fc93f52173e5339e8fb9571`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca02ad3a0dd4ff383e5fe8cef81201aa747f513bd724391e69d4272e441fb1c3`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0fb2e91e46705b26409f246c0bf3647718c5187bb6ffa4c5dafddfc2a2edd`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca09518406089c86c645aa571b37a75799b274b772b04a8fef6703ffbf76ef3b`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 338.9 KB (338919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd845c75155a3609f78ca6b64788a35f72e73fb0c060ee22b4dd7b4be922372f`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:39ca8d38bb88e8ba8d04cd6eeeff4530e4db12daa30aa37e9a0c216a3e2bcfcd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195917858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d1ee2064b2ba3276dc02e0d45d90e35c36d900905b3034b07989d7ed715418`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:53:10 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 21:53:11 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 21:53:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 21:53:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 21:53:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 21:53:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 21:53:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 21:53:47 GMT
EXPOSE 80
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 21:53:49 GMT
EXPOSE 2019
# Wed, 15 May 2024 21:54:15 GMT
RUN caddy version
# Wed, 15 May 2024 21:54:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf806c2d672572084312cc8aa494c8cec9af9daeed5057140149ccdd78dfb80`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b711793313f153495eabe6635f5e8f65dc570d25985f5f6f5ef8c5c0a553b3`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 490.6 KB (490620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d512e0e145af2eec1bd2d32a9b70d48703e256b6d9f9d9199a3a7f36a6c9ff`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4f52645186abe39ac028b27c3e9ffdd710c940ddd12cbbf6d0d29065a18491`  
		Last Modified: Wed, 15 May 2024 21:54:23 GMT  
		Size: 15.3 MB (15345743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa23f4c47c349e446197c7316ed9a453a261ab1fdd2c0e3f6d97d0992d65bdef`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97aa1e7097461ea94ece8afce1dd51ee1513ef285e26743e89614b29a473ed`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576b04f13aae77f986a510a286ba44a00cca8d03b5fffdd0cd881ff59ace8a29`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e02a14a1675118d3895f8691bae0b4c39b9fb31f41a7cee00b3ee9d5d4c6c88`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029ead0bd0493b4a27aca7d5c7dca9fd26f0cc230fe67e95131782faf30b3c7`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be7a0a749e1ab96c5b49167c6b4740f6dc3bd739e58052f848e479c157bbf16`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dc01200272cf83484b850657355cb0afd45801fd642b0e293ddd0a66f5bc6e`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff9d61cc398e1efd41ad219b45a7b7954fdca6b77c3641a047a7d3bba2d24ca`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdefed17ab78afabf07e8a0de1c83420d9eb0a05a6a13b1bd7c6e4f42b785ff`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a28a34a28f7595618aa6579263ace412ec6492a68f265fb56920fb0f52e98e`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e3072da47a79873523ce57465acf158d0f749d150dc2c354873ef27355441a`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709eb7f911c45eec7a80d9be6b73eb9c5b76c363f768c6b678b5e5ec589fb7e0`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118c06d85763da95dd5181f248564978ab3507b219ffb98f85c7473509bec42`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec0cdeef31f251bce3d39ed741232e9eb28b233af8a7373cf3c706afbfbbab4`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb36f279201594c9a4f90cc70e1669eb98c980e9582e2bb7b53fd70ec5071dda`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 348.0 KB (348008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a72e74ca019379f2a07ba0eaa7e4164da0d80823fab977d9182936d89dcf225`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:a5b412c8ac820da3d8ce408bc4bcb2fbc19a99c67fd16ff5c2c4ecce76276fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e2f8b997d964717694810a581f3548bb7c88de368a40ad9de4f8ed414fa2c8bc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128741780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48489f36ce94641f6ce5703ea4babbd5e2e2ec4dbffc55809b7eb8c1c1508cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:03:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:03:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 22:04:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:04:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 22:04:09 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 22:04:10 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 22:04:10 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 22:04:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 22:04:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 22:04:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 80
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 443
# Wed, 15 May 2024 22:04:17 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 22:04:18 GMT
EXPOSE 2019
# Wed, 15 May 2024 22:04:22 GMT
RUN caddy version
# Wed, 15 May 2024 22:04:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cabe3592a5a508b32120c2f3f50485ce2af3e5b977d817fa71bff28061336aa`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7474cb4a8c303c68700f525e09e3bd29bb30d75dc33c01ea4a44732e7e7423f7`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 364.6 KB (364646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6d09183adf4d940c7dac96cc9d75af33bcb47d7d1811a7a296ad60e0d1b1c`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ce5e1d365ba13fb9103a5020b6644b3ae71e76d5e4d159b2f58914673cf2bf`  
		Last Modified: Wed, 15 May 2024 22:04:31 GMT  
		Size: 15.3 MB (15344884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aded66dd078b571ebb532e084c4af4f6beb685bd8a5b7524468e97c168f1a5`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37260cc3f9937e208886001176fd42c7113d3d49bdfd01a29d269126dc8538b4`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c851cec2c829abe440fde3ba79f95ec4728dfa01da5cb2b09e817e7581dc6b`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358cdf5957564add30758b73811ebe0f230cea2692cbb624fb5e8c369dcacc32`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b6a2684656992e4dbd6e42d4dd8ee988d00626cd55d362075a3a9243af3b54`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccb203e5de222a30a89c733e9964e55090c4ff8911cd1ccd005de5e27d7523`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097f79242227f6445dd34eaf655c51b48ce991b72a1ff5589b72787ee42f0fee`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e44fe3122406544397fc58d026c1cbeea8aec0444aaa6d12a759f86d4714c4`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401e6d173f17fd472a9adf0f3ce231ed4fa53e327b3fbd222c6900a64dc1573`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571e94ebd3fc2965298bc42c3810c16d0f6f6c9743a4b5aea94dc66e91aad8e2`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484373c77dd756bb7eb292a32b21c4039a936fdd0871ca3bc6c7467fcf29c77f`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9921976cbc4a4e3222ce034a2dbd34e498f4bc4fc93f52173e5339e8fb9571`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca02ad3a0dd4ff383e5fe8cef81201aa747f513bd724391e69d4272e441fb1c3`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0fb2e91e46705b26409f246c0bf3647718c5187bb6ffa4c5dafddfc2a2edd`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca09518406089c86c645aa571b37a75799b274b772b04a8fef6703ffbf76ef3b`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 338.9 KB (338919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd845c75155a3609f78ca6b64788a35f72e73fb0c060ee22b4dd7b4be922372f`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:39ca8d38bb88e8ba8d04cd6eeeff4530e4db12daa30aa37e9a0c216a3e2bcfcd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195917858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d1ee2064b2ba3276dc02e0d45d90e35c36d900905b3034b07989d7ed715418`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:53:10 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 21:53:11 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 21:53:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 21:53:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 21:53:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 21:53:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 21:53:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 21:53:47 GMT
EXPOSE 80
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 21:53:49 GMT
EXPOSE 2019
# Wed, 15 May 2024 21:54:15 GMT
RUN caddy version
# Wed, 15 May 2024 21:54:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf806c2d672572084312cc8aa494c8cec9af9daeed5057140149ccdd78dfb80`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b711793313f153495eabe6635f5e8f65dc570d25985f5f6f5ef8c5c0a553b3`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 490.6 KB (490620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d512e0e145af2eec1bd2d32a9b70d48703e256b6d9f9d9199a3a7f36a6c9ff`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4f52645186abe39ac028b27c3e9ffdd710c940ddd12cbbf6d0d29065a18491`  
		Last Modified: Wed, 15 May 2024 21:54:23 GMT  
		Size: 15.3 MB (15345743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa23f4c47c349e446197c7316ed9a453a261ab1fdd2c0e3f6d97d0992d65bdef`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97aa1e7097461ea94ece8afce1dd51ee1513ef285e26743e89614b29a473ed`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576b04f13aae77f986a510a286ba44a00cca8d03b5fffdd0cd881ff59ace8a29`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e02a14a1675118d3895f8691bae0b4c39b9fb31f41a7cee00b3ee9d5d4c6c88`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029ead0bd0493b4a27aca7d5c7dca9fd26f0cc230fe67e95131782faf30b3c7`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be7a0a749e1ab96c5b49167c6b4740f6dc3bd739e58052f848e479c157bbf16`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dc01200272cf83484b850657355cb0afd45801fd642b0e293ddd0a66f5bc6e`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff9d61cc398e1efd41ad219b45a7b7954fdca6b77c3641a047a7d3bba2d24ca`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdefed17ab78afabf07e8a0de1c83420d9eb0a05a6a13b1bd7c6e4f42b785ff`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a28a34a28f7595618aa6579263ace412ec6492a68f265fb56920fb0f52e98e`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e3072da47a79873523ce57465acf158d0f749d150dc2c354873ef27355441a`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709eb7f911c45eec7a80d9be6b73eb9c5b76c363f768c6b678b5e5ec589fb7e0`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118c06d85763da95dd5181f248564978ab3507b219ffb98f85c7473509bec42`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec0cdeef31f251bce3d39ed741232e9eb28b233af8a7373cf3c706afbfbbab4`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb36f279201594c9a4f90cc70e1669eb98c980e9582e2bb7b53fd70ec5071dda`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 348.0 KB (348008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a72e74ca019379f2a07ba0eaa7e4164da0d80823fab977d9182936d89dcf225`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:719e7a5b787e20985b0cdeec13fd4a3fba6b6c86a9b79341a5aaa6c2a3bab316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:39ca8d38bb88e8ba8d04cd6eeeff4530e4db12daa30aa37e9a0c216a3e2bcfcd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195917858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d1ee2064b2ba3276dc02e0d45d90e35c36d900905b3034b07989d7ed715418`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:53:10 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 21:53:11 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 21:53:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 21:53:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 21:53:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 21:53:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 21:53:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 21:53:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 21:53:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 21:53:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 21:53:47 GMT
EXPOSE 80
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443
# Wed, 15 May 2024 21:53:48 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 21:53:49 GMT
EXPOSE 2019
# Wed, 15 May 2024 21:54:15 GMT
RUN caddy version
# Wed, 15 May 2024 21:54:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf806c2d672572084312cc8aa494c8cec9af9daeed5057140149ccdd78dfb80`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b711793313f153495eabe6635f5e8f65dc570d25985f5f6f5ef8c5c0a553b3`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 490.6 KB (490620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d512e0e145af2eec1bd2d32a9b70d48703e256b6d9f9d9199a3a7f36a6c9ff`  
		Last Modified: Wed, 15 May 2024 21:54:22 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4f52645186abe39ac028b27c3e9ffdd710c940ddd12cbbf6d0d29065a18491`  
		Last Modified: Wed, 15 May 2024 21:54:23 GMT  
		Size: 15.3 MB (15345743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa23f4c47c349e446197c7316ed9a453a261ab1fdd2c0e3f6d97d0992d65bdef`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc97aa1e7097461ea94ece8afce1dd51ee1513ef285e26743e89614b29a473ed`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576b04f13aae77f986a510a286ba44a00cca8d03b5fffdd0cd881ff59ace8a29`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e02a14a1675118d3895f8691bae0b4c39b9fb31f41a7cee00b3ee9d5d4c6c88`  
		Last Modified: Wed, 15 May 2024 21:54:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5029ead0bd0493b4a27aca7d5c7dca9fd26f0cc230fe67e95131782faf30b3c7`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be7a0a749e1ab96c5b49167c6b4740f6dc3bd739e58052f848e479c157bbf16`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dc01200272cf83484b850657355cb0afd45801fd642b0e293ddd0a66f5bc6e`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff9d61cc398e1efd41ad219b45a7b7954fdca6b77c3641a047a7d3bba2d24ca`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdefed17ab78afabf07e8a0de1c83420d9eb0a05a6a13b1bd7c6e4f42b785ff`  
		Last Modified: Wed, 15 May 2024 21:54:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a28a34a28f7595618aa6579263ace412ec6492a68f265fb56920fb0f52e98e`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e3072da47a79873523ce57465acf158d0f749d150dc2c354873ef27355441a`  
		Last Modified: Wed, 15 May 2024 21:54:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709eb7f911c45eec7a80d9be6b73eb9c5b76c363f768c6b678b5e5ec589fb7e0`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118c06d85763da95dd5181f248564978ab3507b219ffb98f85c7473509bec42`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec0cdeef31f251bce3d39ed741232e9eb28b233af8a7373cf3c706afbfbbab4`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb36f279201594c9a4f90cc70e1669eb98c980e9582e2bb7b53fd70ec5071dda`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 348.0 KB (348008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a72e74ca019379f2a07ba0eaa7e4164da0d80823fab977d9182936d89dcf225`  
		Last Modified: Wed, 15 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:d5b364dd26bbab8a208d93d622f59091ff21942823dea37c1fcf16137353d746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e2f8b997d964717694810a581f3548bb7c88de368a40ad9de4f8ed414fa2c8bc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128741780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48489f36ce94641f6ce5703ea4babbd5e2e2ec4dbffc55809b7eb8c1c1508cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 22:03:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:03:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 May 2024 22:04:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:04:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 May 2024 22:04:09 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 May 2024 22:04:10 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 May 2024 22:04:10 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 15 May 2024 22:04:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 May 2024 22:04:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 May 2024 22:04:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 May 2024 22:04:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 May 2024 22:04:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 80
# Wed, 15 May 2024 22:04:16 GMT
EXPOSE 443
# Wed, 15 May 2024 22:04:17 GMT
EXPOSE 443/udp
# Wed, 15 May 2024 22:04:18 GMT
EXPOSE 2019
# Wed, 15 May 2024 22:04:22 GMT
RUN caddy version
# Wed, 15 May 2024 22:04:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cabe3592a5a508b32120c2f3f50485ce2af3e5b977d817fa71bff28061336aa`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7474cb4a8c303c68700f525e09e3bd29bb30d75dc33c01ea4a44732e7e7423f7`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 364.6 KB (364646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6d09183adf4d940c7dac96cc9d75af33bcb47d7d1811a7a296ad60e0d1b1c`  
		Last Modified: Wed, 15 May 2024 22:04:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ce5e1d365ba13fb9103a5020b6644b3ae71e76d5e4d159b2f58914673cf2bf`  
		Last Modified: Wed, 15 May 2024 22:04:31 GMT  
		Size: 15.3 MB (15344884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aded66dd078b571ebb532e084c4af4f6beb685bd8a5b7524468e97c168f1a5`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37260cc3f9937e208886001176fd42c7113d3d49bdfd01a29d269126dc8538b4`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c851cec2c829abe440fde3ba79f95ec4728dfa01da5cb2b09e817e7581dc6b`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358cdf5957564add30758b73811ebe0f230cea2692cbb624fb5e8c369dcacc32`  
		Last Modified: Wed, 15 May 2024 22:04:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b6a2684656992e4dbd6e42d4dd8ee988d00626cd55d362075a3a9243af3b54`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccb203e5de222a30a89c733e9964e55090c4ff8911cd1ccd005de5e27d7523`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097f79242227f6445dd34eaf655c51b48ce991b72a1ff5589b72787ee42f0fee`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e44fe3122406544397fc58d026c1cbeea8aec0444aaa6d12a759f86d4714c4`  
		Last Modified: Wed, 15 May 2024 22:04:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9401e6d173f17fd472a9adf0f3ce231ed4fa53e327b3fbd222c6900a64dc1573`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571e94ebd3fc2965298bc42c3810c16d0f6f6c9743a4b5aea94dc66e91aad8e2`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484373c77dd756bb7eb292a32b21c4039a936fdd0871ca3bc6c7467fcf29c77f`  
		Last Modified: Wed, 15 May 2024 22:04:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9921976cbc4a4e3222ce034a2dbd34e498f4bc4fc93f52173e5339e8fb9571`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca02ad3a0dd4ff383e5fe8cef81201aa747f513bd724391e69d4272e441fb1c3`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0fb2e91e46705b26409f246c0bf3647718c5187bb6ffa4c5dafddfc2a2edd`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca09518406089c86c645aa571b37a75799b274b772b04a8fef6703ffbf76ef3b`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 338.9 KB (338919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd845c75155a3609f78ca6b64788a35f72e73fb0c060ee22b4dd7b4be922372f`  
		Last Modified: Wed, 15 May 2024 22:04:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
