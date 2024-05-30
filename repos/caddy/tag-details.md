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
$ docker pull caddy@sha256:62bfd9c832a180abdfe1eb02a1b442c1c0f2d3543d15df25620c6f67105a9663
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
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
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
$ docker pull caddy@sha256:93b7c47f8ad5db9e6662e6018efcf3b3aede09c400b3978dee435972c3f55e2a
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
$ docker pull caddy@sha256:c09429949e5c834379efa9c8492fcad5c6413387c93a3c6a00375b5f11672fdf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212216243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12185eff8c33d102395152a3742f93209b1362f0d193f74263230680c4550403`
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
# Wed, 29 May 2024 23:05:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:05:06 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:05:07 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:05:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:06:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:06:56 GMT
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
	-	`sha256:158cbccfebe80cafe7188c003a4c87b6743f8d6682dc0fcb6a7d3d28e05d23ed`  
		Last Modified: Wed, 29 May 2024 23:07:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7a7c7950a5406ed0ff722fd82562ae6f9af0ee4307dbc78688f04bd76d7ed2`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53421374c589a80a5004b0c4fe8d85122534126b9bbdc79345b3136f7a6074bc`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3762c686b3728133d7059475a7274d86e7fe75c3130e9ea0118436b1e3b70e6`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8cac3de0392d16a83051080f23fa784c9896b204fbb3758326a007ecd576ca`  
		Last Modified: Wed, 29 May 2024 23:07:04 GMT  
		Size: 2.0 MB (1981768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6035122c179504a9cba3672ee9b8a1bcbc5d84798210712d1f9eaf26406100`  
		Last Modified: Wed, 29 May 2024 23:07:08 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:a7debc4af5c3b80134a1f3390eaa748914c21377a647a36f3ed1be9f594d4816
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e544e6afc9d0184b969e3f6f29e79c32c22c5c5177846684707130fd5216a9`
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
# Wed, 29 May 2024 23:06:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:06:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:06:42 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:06:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:08:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:08:11 GMT
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
	-	`sha256:7d706d6a19cc7686be564f5426ce4c5c8a038d84e4a59b24886fb5f8e4e389c1`  
		Last Modified: Wed, 29 May 2024 23:08:18 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f838fd148ce21638cb82eaab415cf4210b896eca8ef01e534c840ade4c50cb`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc9d58b58ee6593b6062f725a8be2aa094f78e2e8809f9f700eb590549a0d3`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a61fc28a12470711ef45e0a503222bdf44062910fff80c75d7425271817d26`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ded10626674dd72fc8b5a825b416215e687ef27d585df495fe6ae90159f3ae`  
		Last Modified: Wed, 29 May 2024 23:08:16 GMT  
		Size: 2.0 MB (1951467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6dae68cf59ca5244ea9116fe7147326b59ed215b7ac72e94a0c1ebccc7999`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1297 bytes)  
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
$ docker pull caddy@sha256:2162c8d91596cf33c164cfaaa6300dd54512a3ea2a2c0f3132262c9965aac27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:a7debc4af5c3b80134a1f3390eaa748914c21377a647a36f3ed1be9f594d4816
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e544e6afc9d0184b969e3f6f29e79c32c22c5c5177846684707130fd5216a9`
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
# Wed, 29 May 2024 23:06:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:06:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:06:42 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:06:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:08:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:08:11 GMT
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
	-	`sha256:7d706d6a19cc7686be564f5426ce4c5c8a038d84e4a59b24886fb5f8e4e389c1`  
		Last Modified: Wed, 29 May 2024 23:08:18 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f838fd148ce21638cb82eaab415cf4210b896eca8ef01e534c840ade4c50cb`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc9d58b58ee6593b6062f725a8be2aa094f78e2e8809f9f700eb590549a0d3`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a61fc28a12470711ef45e0a503222bdf44062910fff80c75d7425271817d26`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ded10626674dd72fc8b5a825b416215e687ef27d585df495fe6ae90159f3ae`  
		Last Modified: Wed, 29 May 2024 23:08:16 GMT  
		Size: 2.0 MB (1951467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6dae68cf59ca5244ea9116fe7147326b59ed215b7ac72e94a0c1ebccc7999`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:fa7eeb932cf580da883cf104d8fd4aa2e973a049f3cdefdbdb42403431630eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:c09429949e5c834379efa9c8492fcad5c6413387c93a3c6a00375b5f11672fdf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212216243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12185eff8c33d102395152a3742f93209b1362f0d193f74263230680c4550403`
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
# Wed, 29 May 2024 23:05:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:05:06 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:05:07 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:05:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:06:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:06:56 GMT
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
	-	`sha256:158cbccfebe80cafe7188c003a4c87b6743f8d6682dc0fcb6a7d3d28e05d23ed`  
		Last Modified: Wed, 29 May 2024 23:07:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7a7c7950a5406ed0ff722fd82562ae6f9af0ee4307dbc78688f04bd76d7ed2`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53421374c589a80a5004b0c4fe8d85122534126b9bbdc79345b3136f7a6074bc`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3762c686b3728133d7059475a7274d86e7fe75c3130e9ea0118436b1e3b70e6`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8cac3de0392d16a83051080f23fa784c9896b204fbb3758326a007ecd576ca`  
		Last Modified: Wed, 29 May 2024 23:07:04 GMT  
		Size: 2.0 MB (1981768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6035122c179504a9cba3672ee9b8a1bcbc5d84798210712d1f9eaf26406100`  
		Last Modified: Wed, 29 May 2024 23:07:08 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:0d476cf9b9b3d8875d77f6addbc80f6f2dcb5e470500911c1f32847f8fac929c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ac43dca678ccee7b5359683d08a67241c8cd7365ce008c89b5d0c5e045b65122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:c2ac2c98081daa80cbfa807745e176733338271d2c8391ece0320bf580ee177f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8`

```console
$ docker pull caddy@sha256:db840fd1cc7952ace823fda730188a3ea9d2613c54394250303de7867736f817
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
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
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
$ docker pull caddy@sha256:82efe7d2697870d1f8ab6bd67989dcc95804ed8fc7637bbd810cb49c80079d07
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
$ docker pull caddy@sha256:c09429949e5c834379efa9c8492fcad5c6413387c93a3c6a00375b5f11672fdf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212216243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12185eff8c33d102395152a3742f93209b1362f0d193f74263230680c4550403`
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
# Wed, 29 May 2024 23:05:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:05:06 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:05:07 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:05:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:06:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:06:56 GMT
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
	-	`sha256:158cbccfebe80cafe7188c003a4c87b6743f8d6682dc0fcb6a7d3d28e05d23ed`  
		Last Modified: Wed, 29 May 2024 23:07:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7a7c7950a5406ed0ff722fd82562ae6f9af0ee4307dbc78688f04bd76d7ed2`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53421374c589a80a5004b0c4fe8d85122534126b9bbdc79345b3136f7a6074bc`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3762c686b3728133d7059475a7274d86e7fe75c3130e9ea0118436b1e3b70e6`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8cac3de0392d16a83051080f23fa784c9896b204fbb3758326a007ecd576ca`  
		Last Modified: Wed, 29 May 2024 23:07:04 GMT  
		Size: 2.0 MB (1981768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6035122c179504a9cba3672ee9b8a1bcbc5d84798210712d1f9eaf26406100`  
		Last Modified: Wed, 29 May 2024 23:07:08 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8-builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:a7debc4af5c3b80134a1f3390eaa748914c21377a647a36f3ed1be9f594d4816
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e544e6afc9d0184b969e3f6f29e79c32c22c5c5177846684707130fd5216a9`
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
# Wed, 29 May 2024 23:06:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:06:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:06:42 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:06:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:08:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:08:11 GMT
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
	-	`sha256:7d706d6a19cc7686be564f5426ce4c5c8a038d84e4a59b24886fb5f8e4e389c1`  
		Last Modified: Wed, 29 May 2024 23:08:18 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f838fd148ce21638cb82eaab415cf4210b896eca8ef01e534c840ade4c50cb`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc9d58b58ee6593b6062f725a8be2aa094f78e2e8809f9f700eb590549a0d3`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a61fc28a12470711ef45e0a503222bdf44062910fff80c75d7425271817d26`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ded10626674dd72fc8b5a825b416215e687ef27d585df495fe6ae90159f3ae`  
		Last Modified: Wed, 29 May 2024 23:08:16 GMT  
		Size: 2.0 MB (1951467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6dae68cf59ca5244ea9116fe7147326b59ed215b7ac72e94a0c1ebccc7999`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1297 bytes)  
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
$ docker pull caddy@sha256:2162c8d91596cf33c164cfaaa6300dd54512a3ea2a2c0f3132262c9965aac27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:a7debc4af5c3b80134a1f3390eaa748914c21377a647a36f3ed1be9f594d4816
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e544e6afc9d0184b969e3f6f29e79c32c22c5c5177846684707130fd5216a9`
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
# Wed, 29 May 2024 23:06:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:06:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:06:42 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:06:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:08:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:08:11 GMT
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
	-	`sha256:7d706d6a19cc7686be564f5426ce4c5c8a038d84e4a59b24886fb5f8e4e389c1`  
		Last Modified: Wed, 29 May 2024 23:08:18 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f838fd148ce21638cb82eaab415cf4210b896eca8ef01e534c840ade4c50cb`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc9d58b58ee6593b6062f725a8be2aa094f78e2e8809f9f700eb590549a0d3`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a61fc28a12470711ef45e0a503222bdf44062910fff80c75d7425271817d26`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ded10626674dd72fc8b5a825b416215e687ef27d585df495fe6ae90159f3ae`  
		Last Modified: Wed, 29 May 2024 23:08:16 GMT  
		Size: 2.0 MB (1951467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6dae68cf59ca5244ea9116fe7147326b59ed215b7ac72e94a0c1ebccc7999`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:fa7eeb932cf580da883cf104d8fd4aa2e973a049f3cdefdbdb42403431630eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:c09429949e5c834379efa9c8492fcad5c6413387c93a3c6a00375b5f11672fdf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212216243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12185eff8c33d102395152a3742f93209b1362f0d193f74263230680c4550403`
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
# Wed, 29 May 2024 23:05:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:05:06 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:05:07 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:05:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:06:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:06:56 GMT
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
	-	`sha256:158cbccfebe80cafe7188c003a4c87b6743f8d6682dc0fcb6a7d3d28e05d23ed`  
		Last Modified: Wed, 29 May 2024 23:07:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7a7c7950a5406ed0ff722fd82562ae6f9af0ee4307dbc78688f04bd76d7ed2`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53421374c589a80a5004b0c4fe8d85122534126b9bbdc79345b3136f7a6074bc`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3762c686b3728133d7059475a7274d86e7fe75c3130e9ea0118436b1e3b70e6`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8cac3de0392d16a83051080f23fa784c9896b204fbb3758326a007ecd576ca`  
		Last Modified: Wed, 29 May 2024 23:07:04 GMT  
		Size: 2.0 MB (1981768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6035122c179504a9cba3672ee9b8a1bcbc5d84798210712d1f9eaf26406100`  
		Last Modified: Wed, 29 May 2024 23:07:08 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore`

```console
$ docker pull caddy@sha256:0d476cf9b9b3d8875d77f6addbc80f6f2dcb5e470500911c1f32847f8fac929c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ac43dca678ccee7b5359683d08a67241c8cd7365ce008c89b5d0c5e045b65122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:c2ac2c98081daa80cbfa807745e176733338271d2c8391ece0320bf580ee177f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.0`

```console
$ docker pull caddy@sha256:0d476cf9b9b3d8875d77f6addbc80f6f2dcb5e470500911c1f32847f8fac929c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.0` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8.0` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.0-alpine`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.8.0-builder`

```console
$ docker pull caddy@sha256:3447ae016402924b97442e3b6eee7579767d0e84c94ef696d60b51f84d811e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.0-builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:c09429949e5c834379efa9c8492fcad5c6413387c93a3c6a00375b5f11672fdf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212216243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12185eff8c33d102395152a3742f93209b1362f0d193f74263230680c4550403`
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
# Wed, 29 May 2024 23:05:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:05:06 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:05:07 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:05:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:06:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:06:56 GMT
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
	-	`sha256:158cbccfebe80cafe7188c003a4c87b6743f8d6682dc0fcb6a7d3d28e05d23ed`  
		Last Modified: Wed, 29 May 2024 23:07:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7a7c7950a5406ed0ff722fd82562ae6f9af0ee4307dbc78688f04bd76d7ed2`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53421374c589a80a5004b0c4fe8d85122534126b9bbdc79345b3136f7a6074bc`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3762c686b3728133d7059475a7274d86e7fe75c3130e9ea0118436b1e3b70e6`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8cac3de0392d16a83051080f23fa784c9896b204fbb3758326a007ecd576ca`  
		Last Modified: Wed, 29 May 2024 23:07:04 GMT  
		Size: 2.0 MB (1981768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6035122c179504a9cba3672ee9b8a1bcbc5d84798210712d1f9eaf26406100`  
		Last Modified: Wed, 29 May 2024 23:07:08 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8.0-builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:a7debc4af5c3b80134a1f3390eaa748914c21377a647a36f3ed1be9f594d4816
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e544e6afc9d0184b969e3f6f29e79c32c22c5c5177846684707130fd5216a9`
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
# Wed, 29 May 2024 23:06:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:06:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:06:42 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:06:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:08:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:08:11 GMT
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
	-	`sha256:7d706d6a19cc7686be564f5426ce4c5c8a038d84e4a59b24886fb5f8e4e389c1`  
		Last Modified: Wed, 29 May 2024 23:08:18 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f838fd148ce21638cb82eaab415cf4210b896eca8ef01e534c840ade4c50cb`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc9d58b58ee6593b6062f725a8be2aa094f78e2e8809f9f700eb590549a0d3`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a61fc28a12470711ef45e0a503222bdf44062910fff80c75d7425271817d26`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ded10626674dd72fc8b5a825b416215e687ef27d585df495fe6ae90159f3ae`  
		Last Modified: Wed, 29 May 2024 23:08:16 GMT  
		Size: 2.0 MB (1951467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6dae68cf59ca5244ea9116fe7147326b59ed215b7ac72e94a0c1ebccc7999`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.0-builder-alpine`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.8.0-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:2162c8d91596cf33c164cfaaa6300dd54512a3ea2a2c0f3132262c9965aac27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.0-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:a7debc4af5c3b80134a1f3390eaa748914c21377a647a36f3ed1be9f594d4816
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e544e6afc9d0184b969e3f6f29e79c32c22c5c5177846684707130fd5216a9`
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
# Wed, 29 May 2024 23:06:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:06:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:06:42 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:06:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:08:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:08:11 GMT
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
	-	`sha256:7d706d6a19cc7686be564f5426ce4c5c8a038d84e4a59b24886fb5f8e4e389c1`  
		Last Modified: Wed, 29 May 2024 23:08:18 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f838fd148ce21638cb82eaab415cf4210b896eca8ef01e534c840ade4c50cb`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc9d58b58ee6593b6062f725a8be2aa094f78e2e8809f9f700eb590549a0d3`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a61fc28a12470711ef45e0a503222bdf44062910fff80c75d7425271817d26`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ded10626674dd72fc8b5a825b416215e687ef27d585df495fe6ae90159f3ae`  
		Last Modified: Wed, 29 May 2024 23:08:16 GMT  
		Size: 2.0 MB (1951467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6dae68cf59ca5244ea9116fe7147326b59ed215b7ac72e94a0c1ebccc7999`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.0-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:fa7eeb932cf580da883cf104d8fd4aa2e973a049f3cdefdbdb42403431630eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8.0-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:c09429949e5c834379efa9c8492fcad5c6413387c93a3c6a00375b5f11672fdf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212216243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12185eff8c33d102395152a3742f93209b1362f0d193f74263230680c4550403`
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
# Wed, 29 May 2024 23:05:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:05:06 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:05:07 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:05:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:06:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:06:56 GMT
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
	-	`sha256:158cbccfebe80cafe7188c003a4c87b6743f8d6682dc0fcb6a7d3d28e05d23ed`  
		Last Modified: Wed, 29 May 2024 23:07:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7a7c7950a5406ed0ff722fd82562ae6f9af0ee4307dbc78688f04bd76d7ed2`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53421374c589a80a5004b0c4fe8d85122534126b9bbdc79345b3136f7a6074bc`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3762c686b3728133d7059475a7274d86e7fe75c3130e9ea0118436b1e3b70e6`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8cac3de0392d16a83051080f23fa784c9896b204fbb3758326a007ecd576ca`  
		Last Modified: Wed, 29 May 2024 23:07:04 GMT  
		Size: 2.0 MB (1981768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6035122c179504a9cba3672ee9b8a1bcbc5d84798210712d1f9eaf26406100`  
		Last Modified: Wed, 29 May 2024 23:07:08 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.0-windowsservercore`

```console
$ docker pull caddy@sha256:0d476cf9b9b3d8875d77f6addbc80f6f2dcb5e470500911c1f32847f8fac929c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.0-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8.0-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.0-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ac43dca678ccee7b5359683d08a67241c8cd7365ce008c89b5d0c5e045b65122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.0-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.0-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:c2ac2c98081daa80cbfa807745e176733338271d2c8391ece0320bf580ee177f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull caddy@sha256:93b7c47f8ad5db9e6662e6018efcf3b3aede09c400b3978dee435972c3f55e2a
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
$ docker pull caddy@sha256:c09429949e5c834379efa9c8492fcad5c6413387c93a3c6a00375b5f11672fdf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212216243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12185eff8c33d102395152a3742f93209b1362f0d193f74263230680c4550403`
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
# Wed, 29 May 2024 23:05:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:05:06 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:05:07 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:05:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:06:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:06:56 GMT
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
	-	`sha256:158cbccfebe80cafe7188c003a4c87b6743f8d6682dc0fcb6a7d3d28e05d23ed`  
		Last Modified: Wed, 29 May 2024 23:07:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7a7c7950a5406ed0ff722fd82562ae6f9af0ee4307dbc78688f04bd76d7ed2`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53421374c589a80a5004b0c4fe8d85122534126b9bbdc79345b3136f7a6074bc`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3762c686b3728133d7059475a7274d86e7fe75c3130e9ea0118436b1e3b70e6`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8cac3de0392d16a83051080f23fa784c9896b204fbb3758326a007ecd576ca`  
		Last Modified: Wed, 29 May 2024 23:07:04 GMT  
		Size: 2.0 MB (1981768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6035122c179504a9cba3672ee9b8a1bcbc5d84798210712d1f9eaf26406100`  
		Last Modified: Wed, 29 May 2024 23:07:08 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:a7debc4af5c3b80134a1f3390eaa748914c21377a647a36f3ed1be9f594d4816
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e544e6afc9d0184b969e3f6f29e79c32c22c5c5177846684707130fd5216a9`
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
# Wed, 29 May 2024 23:06:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:06:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:06:42 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:06:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:08:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:08:11 GMT
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
	-	`sha256:7d706d6a19cc7686be564f5426ce4c5c8a038d84e4a59b24886fb5f8e4e389c1`  
		Last Modified: Wed, 29 May 2024 23:08:18 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f838fd148ce21638cb82eaab415cf4210b896eca8ef01e534c840ade4c50cb`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc9d58b58ee6593b6062f725a8be2aa094f78e2e8809f9f700eb590549a0d3`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a61fc28a12470711ef45e0a503222bdf44062910fff80c75d7425271817d26`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ded10626674dd72fc8b5a825b416215e687ef27d585df495fe6ae90159f3ae`  
		Last Modified: Wed, 29 May 2024 23:08:16 GMT  
		Size: 2.0 MB (1951467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6dae68cf59ca5244ea9116fe7147326b59ed215b7ac72e94a0c1ebccc7999`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1297 bytes)  
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
$ docker pull caddy@sha256:2162c8d91596cf33c164cfaaa6300dd54512a3ea2a2c0f3132262c9965aac27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:a7debc4af5c3b80134a1f3390eaa748914c21377a647a36f3ed1be9f594d4816
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e544e6afc9d0184b969e3f6f29e79c32c22c5c5177846684707130fd5216a9`
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
# Wed, 29 May 2024 23:06:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:06:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:06:42 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:06:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:08:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:08:11 GMT
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
	-	`sha256:7d706d6a19cc7686be564f5426ce4c5c8a038d84e4a59b24886fb5f8e4e389c1`  
		Last Modified: Wed, 29 May 2024 23:08:18 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f838fd148ce21638cb82eaab415cf4210b896eca8ef01e534c840ade4c50cb`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc9d58b58ee6593b6062f725a8be2aa094f78e2e8809f9f700eb590549a0d3`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a61fc28a12470711ef45e0a503222bdf44062910fff80c75d7425271817d26`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ded10626674dd72fc8b5a825b416215e687ef27d585df495fe6ae90159f3ae`  
		Last Modified: Wed, 29 May 2024 23:08:16 GMT  
		Size: 2.0 MB (1951467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6dae68cf59ca5244ea9116fe7147326b59ed215b7ac72e94a0c1ebccc7999`  
		Last Modified: Wed, 29 May 2024 23:08:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:fa7eeb932cf580da883cf104d8fd4aa2e973a049f3cdefdbdb42403431630eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:c09429949e5c834379efa9c8492fcad5c6413387c93a3c6a00375b5f11672fdf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212216243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12185eff8c33d102395152a3742f93209b1362f0d193f74263230680c4550403`
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
# Wed, 29 May 2024 23:05:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:05:06 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 23:05:07 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:05:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 23:06:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 29 May 2024 23:06:56 GMT
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
	-	`sha256:158cbccfebe80cafe7188c003a4c87b6743f8d6682dc0fcb6a7d3d28e05d23ed`  
		Last Modified: Wed, 29 May 2024 23:07:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7a7c7950a5406ed0ff722fd82562ae6f9af0ee4307dbc78688f04bd76d7ed2`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53421374c589a80a5004b0c4fe8d85122534126b9bbdc79345b3136f7a6074bc`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3762c686b3728133d7059475a7274d86e7fe75c3130e9ea0118436b1e3b70e6`  
		Last Modified: Wed, 29 May 2024 23:07:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8cac3de0392d16a83051080f23fa784c9896b204fbb3758326a007ecd576ca`  
		Last Modified: Wed, 29 May 2024 23:07:04 GMT  
		Size: 2.0 MB (1981768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6035122c179504a9cba3672ee9b8a1bcbc5d84798210712d1f9eaf26406100`  
		Last Modified: Wed, 29 May 2024 23:07:08 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:62bfd9c832a180abdfe1eb02a1b442c1c0f2d3543d15df25620c6f67105a9663
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
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:0d476cf9b9b3d8875d77f6addbc80f6f2dcb5e470500911c1f32847f8fac929c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:ac43dca678ccee7b5359683d08a67241c8cd7365ce008c89b5d0c5e045b65122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:9fb9a9e70d001e2bbf209fd0a9b7a3167816aeefebc222dcf31e82e5ff0308d6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195919685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c9f3f928fcb39956b52f9dd94d2c7d262846a14cc87342ab685490b6137dc6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:02:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:14 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:44 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:49 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:05:15 GMT
RUN caddy version
# Wed, 29 May 2024 23:05:16 GMT
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
	-	`sha256:99e0fb5e7e3ce5d56d35ea6e1a2d10eb01b31497fa60763b93f7267a763e3a3b`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac62d141d38539827ad98a883989be09b021957dfce89f07a00533c91ed049`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 525.0 KB (524974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4185f6e481e083253090445484ce9d549cf69be98e927781971fd297cab9bb86`  
		Last Modified: Wed, 29 May 2024 23:05:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdca1720373fc6cd3f6a530b515cd3dcad6caae8d30aa1f0f70d957edc994a4`  
		Last Modified: Wed, 29 May 2024 23:05:27 GMT  
		Size: 15.3 MB (15289391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72eaa7ecc5d7a340001fe6435adc0cd3a9dd982ede226b3846db358433fb54`  
		Last Modified: Wed, 29 May 2024 23:05:22 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e30011895f01d598f111a4385b101c1041d9c9877d083fecb47b94ec60dd1bb`  
		Last Modified: Wed, 29 May 2024 23:05:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8e38b1181c0218192ecb1b77c8f6610d5962d9f80a98954f2fdc00785e46`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c551d007155335c62bbf1c17f4b567d721b5640525af7f071f66cb8b8f86c3`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2151a81296d906deb5d36013c066f3cdede76e3e82fa2e34c82dbc98fc3935`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ee6d34e21af671759b2572fa0f5ddc27a9498682ac52d85321458cb8f729c`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60342916957f74d993721686fbe5ade279c46f362364b57a41eebc3c773143de`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931c8d3a4da1039c08b21ad94166c161caffed27987619f84540ff09d495c8e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14406065e72ea375f56f95f8faf27f6b1d16152c7d5e9073103993b7b21525`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1517dfc03ed6b24944f94351e12516250872382c2907f8fe851fd37f7077b3e`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a625c3f70a8c3a25d69ed36bfc9675c3dcc7b189b900741dcefd0bd63e73e9`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343e385458280437a0df5d18b3b889c60ff9c490cf3f5047d25373ecc2a28204`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd1c3158baee60e987f6801b1a421fcc4eefb8cfa8a5bee61ea5972c1620c0`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b801cffe6dfa6ce88a9ba49688bfd5ea05a6db6d8eb259b002c9831a18705`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822cde4338f5a6f19c7e5558af8bd0e77615dc43e229285306f77b122dcaeb94`  
		Last Modified: Wed, 29 May 2024 23:05:19 GMT  
		Size: 371.9 KB (371877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518339094b8afcf48ae43460d41469d10f546e107f5b55ef2de0eb3a78921d5d`  
		Last Modified: Wed, 29 May 2024 23:05:18 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:c2ac2c98081daa80cbfa807745e176733338271d2c8391ece0320bf580ee177f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:6a18978ffbc393583ec9e82d2f28c38093fb2c46658d422820d3aacff72a5adf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d0e06f90a0832497aa1f26ffa4bcdcdfa9dfc2266ed0b0dda40414664accd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:02:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:04:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 29 May 2024 23:04:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 23:04:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('403789c4e18a53e5f6d0d170de4d8784b84821a4b3c739b9799863019d10ebd5e90af82588d0ea036611f6e0907e2b144b76a33c7dbf23d05d51ab63d990a0d0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 29 May 2024 23:04:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 29 May 2024 23:04:43 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 29 May 2024 23:04:44 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 23:04:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 23:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 23:04:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 23:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 23:04:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 80
# Wed, 29 May 2024 23:04:50 GMT
EXPOSE 443
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 443/udp
# Wed, 29 May 2024 23:04:51 GMT
EXPOSE 2019
# Wed, 29 May 2024 23:04:57 GMT
RUN caddy version
# Wed, 29 May 2024 23:04:57 GMT
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
	-	`sha256:dffe20958b72548de73d2e91d2a038ee3291259fa18a8ab56bd19a2814adbb34`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d67ba9da0f386f62c69c34b92f526ec882fc0f6077990820516ae0a83f966`  
		Last Modified: Wed, 29 May 2024 23:05:08 GMT  
		Size: 362.8 KB (362765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dadb17334855f531328c9f050ecfc28c2c02ac3e4eac6d51a7f42c6e72696`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86bb3bd6467ecbfc6f9fe75ff873f17d80c85a850b0858d7163defce9b65e6c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 15.2 MB (15220458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6bc83565b198b6a275a4213d058c86d06203d5c6fdc953e60daf54f2a5b7ae`  
		Last Modified: Wed, 29 May 2024 23:05:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0c7e36271afc841753c9b2cd4b43fe7a8a8c0a2bd6cf786bb6e15406f5c010`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231223afb2b494150472d15d93576cf24c5b60201ff0464a2a5569132b8c9e9f`  
		Last Modified: Wed, 29 May 2024 23:05:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155bc36233cfd38049c34678d8941361438f257758fd862b1b773954c553c93`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28cdc40021b08cfe18268fa3c96a8b8b9a6b039398cc237d31e5765862169b3`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f086e6518536ea0d024fc0a500a4adbc628720a51b10937b92c94a4f56ac55`  
		Last Modified: Wed, 29 May 2024 23:05:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fdb5d71629385e2ff4abad1b668db6b49acf348d1db94c3c7029f955b428b5`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9500b94c744611615ef96f05a6bbcaa5f5cae79da1b2623484cdc311c915e6`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dfc7ce699794f06660d94ffb64afbebb3ccb21e7f7dae3137bddfc9039010`  
		Last Modified: Wed, 29 May 2024 23:05:04 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194438f949367fcd78c1f63d8c6c8fb456831be2480e496b4900893f05a313db`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969674f6c83757343cd34e24aaaeee6637008597a0d6750bff7b2316267720e4`  
		Last Modified: Wed, 29 May 2024 23:05:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2383c4faaa8d33593eee6e6056dd78855b79638bb17e51738a8d647b955716f`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8560a68c3e36b65d6d38792064abbabe3f36e9d1d3bed3ee764cd8412e1a2d`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1175073624cda6c642d3ae4f407f89695788a94c5e3beac8e942c2a87f1fa`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b50183854a011c9b2265db2d37bd80c3d292add425838b5afaeb14169b9a1fe`  
		Last Modified: Wed, 29 May 2024 23:05:02 GMT  
		Size: 316.6 KB (316591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5990ce164a3773ee451372551985c1d3bb3d6f514ba8e6521883b350815b`  
		Last Modified: Wed, 29 May 2024 23:05:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
