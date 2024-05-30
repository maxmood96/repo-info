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
$ docker pull caddy@sha256:1a68e74443e509a8a4f8ca08d3a509507f6f49f10f36da178d57d47d0b634cab
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
$ docker pull caddy@sha256:f6bdaeaa2da17edf5a8c33cd6f3cde4e96b37152c2791d4308c1b6695e2a79f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2528051e99d3f23b9fddb25e751078881b1a4237ff2e4bdd77c4c503b66563bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb615d7326964b43a9e5dd3dd14734c53a02dc2cef9fa9ffc00314a64e79a3fe`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 357.4 KB (357368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb87b8526d1948b1e9d896525df20cef23bed00873f22a774db258b070e92a`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333cc5c2a4bdfc22594bac44d124a78fd574d27c4da57ec41e156269d656a58`  
		Last Modified: Wed, 29 May 2024 23:01:06 GMT  
		Size: 14.6 MB (14639245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:9cdbbc45a19237aea8ac5d7ebb37954541082503b26be511135699351c58b4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574268ca9e9da984347d108b60adfdee7bb5792198f3904485d2570a0d3c5e06`

```dockerfile
```

-	Layers:
	-	`sha256:5a044e0dbe68da74ba6be9d21c1fd4ffcc1d42e0061d9f810df5a7b5bf3804ab`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa7cd9091a42e6e0007de5a9ef9c7b132d08ecd23fcb96aadf925cbef4ccef6`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:690174bca4a22f78fd061b913fb9af04c35053cf591739e4274f1e5758136779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a1618df6b54bfa5f963ddc58cc727860e3264267ceba5a03a89dd90f4a5cd6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6242b091285cd3a94637051278e15e4e5fac103eba7cc862f4c049dbd89e5d8`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 357.7 KB (357710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8165fbffda6934ae4fa48e7fb8912c4a52fffdf33dddb24e1fa2823af18b77`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b840d124a7e1135a2bccb8f1921209ee443c13f74e6b5270dbf3d9b5905d87`  
		Last Modified: Thu, 30 May 2024 00:33:31 GMT  
		Size: 13.8 MB (13763171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:18ca096172a9af5d32f39e949ca51c2f3a04b0c3fdd3d3c19c61dc3edacddf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db94e6c76f858c4cb979b37ea5de4a12782484dd46cfca89e9dd213837ad5b74`

```dockerfile
```

-	Layers:
	-	`sha256:a26aa7bb711b04c54e7691a704b1edf426a27937b3bda1721d70aaeddb786cc5`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
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
$ docker pull caddy@sha256:a901a1a96c982a13a5b375f9854ac2881ada2dad6e0b51a280e4e0409b3be7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaa0aacb2cad6d7dedd2ae0e0a01b4240ab829d2054697264b7f35a3c8c727`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dffc4dc5008bcfd45facfcd56c34ac3e08dcd41d6dcf4dbf7b1304998e48f7`  
		Last Modified: Thu, 30 May 2024 01:51:03 GMT  
		Size: 14.2 MB (14154597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:f8f994f364719dfc87e3eec9d3d9370870f7dd53fc55a85894cd74b295a064e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279088462e9f352f79f89f32ee4c95eb980369084a4efdd389b4d8de75cdaba`

```dockerfile
```

-	Layers:
	-	`sha256:ad7f9ab13108a2a745e3bc6420a3bc827b9c09669eede8eaabf3013581262027`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79640b0ba457ce4da05d0515c66bb0761b3ba7246808b89cff28c88c7d94f23`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 17.5 KB (17533 bytes)  
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
$ docker pull caddy@sha256:7750cb6f08350f2c39207ea87232f7b278f586410232e912542f1d128995636c
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
$ docker pull caddy@sha256:f6bdaeaa2da17edf5a8c33cd6f3cde4e96b37152c2791d4308c1b6695e2a79f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2528051e99d3f23b9fddb25e751078881b1a4237ff2e4bdd77c4c503b66563bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb615d7326964b43a9e5dd3dd14734c53a02dc2cef9fa9ffc00314a64e79a3fe`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 357.4 KB (357368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb87b8526d1948b1e9d896525df20cef23bed00873f22a774db258b070e92a`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333cc5c2a4bdfc22594bac44d124a78fd574d27c4da57ec41e156269d656a58`  
		Last Modified: Wed, 29 May 2024 23:01:06 GMT  
		Size: 14.6 MB (14639245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9cdbbc45a19237aea8ac5d7ebb37954541082503b26be511135699351c58b4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574268ca9e9da984347d108b60adfdee7bb5792198f3904485d2570a0d3c5e06`

```dockerfile
```

-	Layers:
	-	`sha256:5a044e0dbe68da74ba6be9d21c1fd4ffcc1d42e0061d9f810df5a7b5bf3804ab`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa7cd9091a42e6e0007de5a9ef9c7b132d08ecd23fcb96aadf925cbef4ccef6`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:690174bca4a22f78fd061b913fb9af04c35053cf591739e4274f1e5758136779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a1618df6b54bfa5f963ddc58cc727860e3264267ceba5a03a89dd90f4a5cd6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6242b091285cd3a94637051278e15e4e5fac103eba7cc862f4c049dbd89e5d8`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 357.7 KB (357710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8165fbffda6934ae4fa48e7fb8912c4a52fffdf33dddb24e1fa2823af18b77`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b840d124a7e1135a2bccb8f1921209ee443c13f74e6b5270dbf3d9b5905d87`  
		Last Modified: Thu, 30 May 2024 00:33:31 GMT  
		Size: 13.8 MB (13763171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:18ca096172a9af5d32f39e949ca51c2f3a04b0c3fdd3d3c19c61dc3edacddf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db94e6c76f858c4cb979b37ea5de4a12782484dd46cfca89e9dd213837ad5b74`

```dockerfile
```

-	Layers:
	-	`sha256:a26aa7bb711b04c54e7691a704b1edf426a27937b3bda1721d70aaeddb786cc5`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
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
$ docker pull caddy@sha256:a901a1a96c982a13a5b375f9854ac2881ada2dad6e0b51a280e4e0409b3be7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaa0aacb2cad6d7dedd2ae0e0a01b4240ab829d2054697264b7f35a3c8c727`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dffc4dc5008bcfd45facfcd56c34ac3e08dcd41d6dcf4dbf7b1304998e48f7`  
		Last Modified: Thu, 30 May 2024 01:51:03 GMT  
		Size: 14.2 MB (14154597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f8f994f364719dfc87e3eec9d3d9370870f7dd53fc55a85894cd74b295a064e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279088462e9f352f79f89f32ee4c95eb980369084a4efdd389b4d8de75cdaba`

```dockerfile
```

-	Layers:
	-	`sha256:ad7f9ab13108a2a745e3bc6420a3bc827b9c09669eede8eaabf3013581262027`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79640b0ba457ce4da05d0515c66bb0761b3ba7246808b89cff28c88c7d94f23`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 17.5 KB (17533 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:95b26402e9c139e0c6303ef9eb0b052ec5e432315407ba0d95747dede41234d1
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
$ docker pull caddy@sha256:1d97a1bfc689534068bc99b432822dc9842c649e729cc0c154f8c154d63f45b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb6b1b4823de1adba6bebfdf129c46e2b64995736eb6673f1ab8feb5553ee9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402b0dc7c1ee13bd10aeed32ca6f6730dfbbd53b36df1c2c43ba6c1ac0ca1a8`  
		Last Modified: Wed, 29 May 2024 23:01:15 GMT  
		Size: 5.9 MB (5914555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4feb0354e90f2c326e6b7d6e8aa8f0c14cb5cafeedd520bbe661cbcdc54876`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 1.5 MB (1500672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6a145aba22dc1cdd83e6e4bc89d3dcd83fed07b9df5447bb29107c926a4222`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a53a011c1a5f9f4482d50088c1170f9d734d111fd6e53b13901390301dbc987a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502eef3ba542c157731565e6b10b6f605c5bbaa4cb2f1a8aa0fcea2fe89d7105`

```dockerfile
```

-	Layers:
	-	`sha256:b40a1d307eafd54bf402058964d29328638bc46540b1ff0e89cfafd693be59c2`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008d2100174b1ae9d0f0f9e9dac7a9d327aa68c96b29fb0f6f7eb63a109c8d9e`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:76b024f4bfc423eed7169d9548312432f113ec180d6fe4abf9dea3056f08e013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f41be2f19d58f1bc9f7f405236e380a2cb5591a9f3861c7f8f42818200283`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b97bf58febbeb200aa9d2afef8fe6cd7c0ec7c32c2924df16f50e5b908515`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 5.9 MB (5863420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60932c3d4c230ff0adc1536a623aef6a7587fbec36b8add10672330287c9ad0`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e115e84021acc84d0da9a8c93309a09a344ee4fb560abec304c2c599386f62`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3461e07084978dfa05c463d289dc6dbd055b41fd9e6b22f8f58c976d1d3cb9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a214bf5aa952a1965e3eb6e089d2e3d6c4e0cf8cf288c820163d16eb47481c41`

```dockerfile
```

-	Layers:
	-	`sha256:8c82281543d077f647436232fe98bb809e9db5bbe6cda5cae4f0916f0b000d43`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 19.5 KB (19501 bytes)  
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
$ docker pull caddy@sha256:e53c2ec5bc7bb3e46c3b08cbe2793d45479d1264c40b5503bef29eac2c91bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3723281c06eda99cbaeea6f288865cad6be253c3b7ed970ae0073b1cff680a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea9d4fd6b7817ea21385211ac68cd734b6e36168539fdfc45a17147cdfbeb5`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 1.5 MB (1451783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd654ccf1647a25716cd5ade72e99d159e39c702b954bd5e1e628ad8095cbc7`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:208946b4132505ebe3d024e76404801b3efceaa335e267fc1147680e4d0a72dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba39e663c5c23602c18674f4c908a2b81d5f5fce9def8350942c92d2c701d6`

```dockerfile
```

-	Layers:
	-	`sha256:726f8c49f1c023380c093fbb8f09dfe9021e323fbdbef3ad8057b76e18e391dd`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97dd399ce6968f36de5122b2b40bebfdca47410eb2e2264e7dd75c76b02ca0e`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 19.6 KB (19599 bytes)  
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
$ docker pull caddy@sha256:bdfd9eda328f615f3948329761abc99013772fafb97c6c41bb882815a11d322f
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
$ docker pull caddy@sha256:1d97a1bfc689534068bc99b432822dc9842c649e729cc0c154f8c154d63f45b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb6b1b4823de1adba6bebfdf129c46e2b64995736eb6673f1ab8feb5553ee9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402b0dc7c1ee13bd10aeed32ca6f6730dfbbd53b36df1c2c43ba6c1ac0ca1a8`  
		Last Modified: Wed, 29 May 2024 23:01:15 GMT  
		Size: 5.9 MB (5914555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4feb0354e90f2c326e6b7d6e8aa8f0c14cb5cafeedd520bbe661cbcdc54876`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 1.5 MB (1500672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6a145aba22dc1cdd83e6e4bc89d3dcd83fed07b9df5447bb29107c926a4222`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a53a011c1a5f9f4482d50088c1170f9d734d111fd6e53b13901390301dbc987a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502eef3ba542c157731565e6b10b6f605c5bbaa4cb2f1a8aa0fcea2fe89d7105`

```dockerfile
```

-	Layers:
	-	`sha256:b40a1d307eafd54bf402058964d29328638bc46540b1ff0e89cfafd693be59c2`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008d2100174b1ae9d0f0f9e9dac7a9d327aa68c96b29fb0f6f7eb63a109c8d9e`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:76b024f4bfc423eed7169d9548312432f113ec180d6fe4abf9dea3056f08e013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f41be2f19d58f1bc9f7f405236e380a2cb5591a9f3861c7f8f42818200283`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b97bf58febbeb200aa9d2afef8fe6cd7c0ec7c32c2924df16f50e5b908515`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 5.9 MB (5863420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60932c3d4c230ff0adc1536a623aef6a7587fbec36b8add10672330287c9ad0`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e115e84021acc84d0da9a8c93309a09a344ee4fb560abec304c2c599386f62`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3461e07084978dfa05c463d289dc6dbd055b41fd9e6b22f8f58c976d1d3cb9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a214bf5aa952a1965e3eb6e089d2e3d6c4e0cf8cf288c820163d16eb47481c41`

```dockerfile
```

-	Layers:
	-	`sha256:8c82281543d077f647436232fe98bb809e9db5bbe6cda5cae4f0916f0b000d43`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 19.5 KB (19501 bytes)  
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
$ docker pull caddy@sha256:e53c2ec5bc7bb3e46c3b08cbe2793d45479d1264c40b5503bef29eac2c91bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3723281c06eda99cbaeea6f288865cad6be253c3b7ed970ae0073b1cff680a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea9d4fd6b7817ea21385211ac68cd734b6e36168539fdfc45a17147cdfbeb5`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 1.5 MB (1451783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd654ccf1647a25716cd5ade72e99d159e39c702b954bd5e1e628ad8095cbc7`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:208946b4132505ebe3d024e76404801b3efceaa335e267fc1147680e4d0a72dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba39e663c5c23602c18674f4c908a2b81d5f5fce9def8350942c92d2c701d6`

```dockerfile
```

-	Layers:
	-	`sha256:726f8c49f1c023380c093fbb8f09dfe9021e323fbdbef3ad8057b76e18e391dd`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97dd399ce6968f36de5122b2b40bebfdca47410eb2e2264e7dd75c76b02ca0e`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 19.6 KB (19599 bytes)  
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
$ docker pull caddy@sha256:37e0a5c284cc3f7306b2156e7227369783e0c776585844a5c9d435d47620b69b
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
$ docker pull caddy@sha256:f6bdaeaa2da17edf5a8c33cd6f3cde4e96b37152c2791d4308c1b6695e2a79f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2528051e99d3f23b9fddb25e751078881b1a4237ff2e4bdd77c4c503b66563bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb615d7326964b43a9e5dd3dd14734c53a02dc2cef9fa9ffc00314a64e79a3fe`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 357.4 KB (357368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb87b8526d1948b1e9d896525df20cef23bed00873f22a774db258b070e92a`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333cc5c2a4bdfc22594bac44d124a78fd574d27c4da57ec41e156269d656a58`  
		Last Modified: Wed, 29 May 2024 23:01:06 GMT  
		Size: 14.6 MB (14639245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:9cdbbc45a19237aea8ac5d7ebb37954541082503b26be511135699351c58b4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574268ca9e9da984347d108b60adfdee7bb5792198f3904485d2570a0d3c5e06`

```dockerfile
```

-	Layers:
	-	`sha256:5a044e0dbe68da74ba6be9d21c1fd4ffcc1d42e0061d9f810df5a7b5bf3804ab`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa7cd9091a42e6e0007de5a9ef9c7b132d08ecd23fcb96aadf925cbef4ccef6`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; arm variant v6

```console
$ docker pull caddy@sha256:690174bca4a22f78fd061b913fb9af04c35053cf591739e4274f1e5758136779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a1618df6b54bfa5f963ddc58cc727860e3264267ceba5a03a89dd90f4a5cd6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6242b091285cd3a94637051278e15e4e5fac103eba7cc862f4c049dbd89e5d8`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 357.7 KB (357710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8165fbffda6934ae4fa48e7fb8912c4a52fffdf33dddb24e1fa2823af18b77`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b840d124a7e1135a2bccb8f1921209ee443c13f74e6b5270dbf3d9b5905d87`  
		Last Modified: Thu, 30 May 2024 00:33:31 GMT  
		Size: 13.8 MB (13763171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:18ca096172a9af5d32f39e949ca51c2f3a04b0c3fdd3d3c19c61dc3edacddf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db94e6c76f858c4cb979b37ea5de4a12782484dd46cfca89e9dd213837ad5b74`

```dockerfile
```

-	Layers:
	-	`sha256:a26aa7bb711b04c54e7691a704b1edf426a27937b3bda1721d70aaeddb786cc5`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 17.4 KB (17443 bytes)  
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
$ docker pull caddy@sha256:a901a1a96c982a13a5b375f9854ac2881ada2dad6e0b51a280e4e0409b3be7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaa0aacb2cad6d7dedd2ae0e0a01b4240ab829d2054697264b7f35a3c8c727`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dffc4dc5008bcfd45facfcd56c34ac3e08dcd41d6dcf4dbf7b1304998e48f7`  
		Last Modified: Thu, 30 May 2024 01:51:03 GMT  
		Size: 14.2 MB (14154597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:f8f994f364719dfc87e3eec9d3d9370870f7dd53fc55a85894cd74b295a064e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279088462e9f352f79f89f32ee4c95eb980369084a4efdd389b4d8de75cdaba`

```dockerfile
```

-	Layers:
	-	`sha256:ad7f9ab13108a2a745e3bc6420a3bc827b9c09669eede8eaabf3013581262027`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79640b0ba457ce4da05d0515c66bb0761b3ba7246808b89cff28c88c7d94f23`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 17.5 KB (17533 bytes)  
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
$ docker pull caddy@sha256:8fbafcd2af8b9e008e8e248d6ba2bc8b00a339f74662cb68387347aff7b9799c
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
$ docker pull caddy@sha256:f6bdaeaa2da17edf5a8c33cd6f3cde4e96b37152c2791d4308c1b6695e2a79f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2528051e99d3f23b9fddb25e751078881b1a4237ff2e4bdd77c4c503b66563bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb615d7326964b43a9e5dd3dd14734c53a02dc2cef9fa9ffc00314a64e79a3fe`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 357.4 KB (357368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb87b8526d1948b1e9d896525df20cef23bed00873f22a774db258b070e92a`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333cc5c2a4bdfc22594bac44d124a78fd574d27c4da57ec41e156269d656a58`  
		Last Modified: Wed, 29 May 2024 23:01:06 GMT  
		Size: 14.6 MB (14639245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9cdbbc45a19237aea8ac5d7ebb37954541082503b26be511135699351c58b4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574268ca9e9da984347d108b60adfdee7bb5792198f3904485d2570a0d3c5e06`

```dockerfile
```

-	Layers:
	-	`sha256:5a044e0dbe68da74ba6be9d21c1fd4ffcc1d42e0061d9f810df5a7b5bf3804ab`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa7cd9091a42e6e0007de5a9ef9c7b132d08ecd23fcb96aadf925cbef4ccef6`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:690174bca4a22f78fd061b913fb9af04c35053cf591739e4274f1e5758136779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a1618df6b54bfa5f963ddc58cc727860e3264267ceba5a03a89dd90f4a5cd6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6242b091285cd3a94637051278e15e4e5fac103eba7cc862f4c049dbd89e5d8`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 357.7 KB (357710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8165fbffda6934ae4fa48e7fb8912c4a52fffdf33dddb24e1fa2823af18b77`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b840d124a7e1135a2bccb8f1921209ee443c13f74e6b5270dbf3d9b5905d87`  
		Last Modified: Thu, 30 May 2024 00:33:31 GMT  
		Size: 13.8 MB (13763171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:18ca096172a9af5d32f39e949ca51c2f3a04b0c3fdd3d3c19c61dc3edacddf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db94e6c76f858c4cb979b37ea5de4a12782484dd46cfca89e9dd213837ad5b74`

```dockerfile
```

-	Layers:
	-	`sha256:a26aa7bb711b04c54e7691a704b1edf426a27937b3bda1721d70aaeddb786cc5`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 17.4 KB (17443 bytes)  
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
$ docker pull caddy@sha256:a901a1a96c982a13a5b375f9854ac2881ada2dad6e0b51a280e4e0409b3be7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaa0aacb2cad6d7dedd2ae0e0a01b4240ab829d2054697264b7f35a3c8c727`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dffc4dc5008bcfd45facfcd56c34ac3e08dcd41d6dcf4dbf7b1304998e48f7`  
		Last Modified: Thu, 30 May 2024 01:51:03 GMT  
		Size: 14.2 MB (14154597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f8f994f364719dfc87e3eec9d3d9370870f7dd53fc55a85894cd74b295a064e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279088462e9f352f79f89f32ee4c95eb980369084a4efdd389b4d8de75cdaba`

```dockerfile
```

-	Layers:
	-	`sha256:ad7f9ab13108a2a745e3bc6420a3bc827b9c09669eede8eaabf3013581262027`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79640b0ba457ce4da05d0515c66bb0761b3ba7246808b89cff28c88c7d94f23`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 17.5 KB (17533 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8-builder`

```console
$ docker pull caddy@sha256:0f7fdb2b5d9576ff07b7a386e324f9f2b92055f75eb9d9a86cfcb5ea4f067122
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
$ docker pull caddy@sha256:1d97a1bfc689534068bc99b432822dc9842c649e729cc0c154f8c154d63f45b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb6b1b4823de1adba6bebfdf129c46e2b64995736eb6673f1ab8feb5553ee9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402b0dc7c1ee13bd10aeed32ca6f6730dfbbd53b36df1c2c43ba6c1ac0ca1a8`  
		Last Modified: Wed, 29 May 2024 23:01:15 GMT  
		Size: 5.9 MB (5914555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4feb0354e90f2c326e6b7d6e8aa8f0c14cb5cafeedd520bbe661cbcdc54876`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 1.5 MB (1500672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6a145aba22dc1cdd83e6e4bc89d3dcd83fed07b9df5447bb29107c926a4222`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a53a011c1a5f9f4482d50088c1170f9d734d111fd6e53b13901390301dbc987a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502eef3ba542c157731565e6b10b6f605c5bbaa4cb2f1a8aa0fcea2fe89d7105`

```dockerfile
```

-	Layers:
	-	`sha256:b40a1d307eafd54bf402058964d29328638bc46540b1ff0e89cfafd693be59c2`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008d2100174b1ae9d0f0f9e9dac7a9d327aa68c96b29fb0f6f7eb63a109c8d9e`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:76b024f4bfc423eed7169d9548312432f113ec180d6fe4abf9dea3056f08e013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f41be2f19d58f1bc9f7f405236e380a2cb5591a9f3861c7f8f42818200283`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b97bf58febbeb200aa9d2afef8fe6cd7c0ec7c32c2924df16f50e5b908515`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 5.9 MB (5863420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60932c3d4c230ff0adc1536a623aef6a7587fbec36b8add10672330287c9ad0`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e115e84021acc84d0da9a8c93309a09a344ee4fb560abec304c2c599386f62`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3461e07084978dfa05c463d289dc6dbd055b41fd9e6b22f8f58c976d1d3cb9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a214bf5aa952a1965e3eb6e089d2e3d6c4e0cf8cf288c820163d16eb47481c41`

```dockerfile
```

-	Layers:
	-	`sha256:8c82281543d077f647436232fe98bb809e9db5bbe6cda5cae4f0916f0b000d43`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 19.5 KB (19501 bytes)  
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
$ docker pull caddy@sha256:e53c2ec5bc7bb3e46c3b08cbe2793d45479d1264c40b5503bef29eac2c91bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3723281c06eda99cbaeea6f288865cad6be253c3b7ed970ae0073b1cff680a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea9d4fd6b7817ea21385211ac68cd734b6e36168539fdfc45a17147cdfbeb5`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 1.5 MB (1451783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd654ccf1647a25716cd5ade72e99d159e39c702b954bd5e1e628ad8095cbc7`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:208946b4132505ebe3d024e76404801b3efceaa335e267fc1147680e4d0a72dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba39e663c5c23602c18674f4c908a2b81d5f5fce9def8350942c92d2c701d6`

```dockerfile
```

-	Layers:
	-	`sha256:726f8c49f1c023380c093fbb8f09dfe9021e323fbdbef3ad8057b76e18e391dd`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97dd399ce6968f36de5122b2b40bebfdca47410eb2e2264e7dd75c76b02ca0e`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 19.6 KB (19599 bytes)  
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
$ docker pull caddy@sha256:815830b747d83f216942fc1f840a5fa007f71e5a9b774e8923b274b743685386
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
$ docker pull caddy@sha256:1d97a1bfc689534068bc99b432822dc9842c649e729cc0c154f8c154d63f45b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb6b1b4823de1adba6bebfdf129c46e2b64995736eb6673f1ab8feb5553ee9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402b0dc7c1ee13bd10aeed32ca6f6730dfbbd53b36df1c2c43ba6c1ac0ca1a8`  
		Last Modified: Wed, 29 May 2024 23:01:15 GMT  
		Size: 5.9 MB (5914555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4feb0354e90f2c326e6b7d6e8aa8f0c14cb5cafeedd520bbe661cbcdc54876`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 1.5 MB (1500672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6a145aba22dc1cdd83e6e4bc89d3dcd83fed07b9df5447bb29107c926a4222`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a53a011c1a5f9f4482d50088c1170f9d734d111fd6e53b13901390301dbc987a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502eef3ba542c157731565e6b10b6f605c5bbaa4cb2f1a8aa0fcea2fe89d7105`

```dockerfile
```

-	Layers:
	-	`sha256:b40a1d307eafd54bf402058964d29328638bc46540b1ff0e89cfafd693be59c2`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008d2100174b1ae9d0f0f9e9dac7a9d327aa68c96b29fb0f6f7eb63a109c8d9e`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:76b024f4bfc423eed7169d9548312432f113ec180d6fe4abf9dea3056f08e013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f41be2f19d58f1bc9f7f405236e380a2cb5591a9f3861c7f8f42818200283`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b97bf58febbeb200aa9d2afef8fe6cd7c0ec7c32c2924df16f50e5b908515`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 5.9 MB (5863420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60932c3d4c230ff0adc1536a623aef6a7587fbec36b8add10672330287c9ad0`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e115e84021acc84d0da9a8c93309a09a344ee4fb560abec304c2c599386f62`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3461e07084978dfa05c463d289dc6dbd055b41fd9e6b22f8f58c976d1d3cb9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a214bf5aa952a1965e3eb6e089d2e3d6c4e0cf8cf288c820163d16eb47481c41`

```dockerfile
```

-	Layers:
	-	`sha256:8c82281543d077f647436232fe98bb809e9db5bbe6cda5cae4f0916f0b000d43`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 19.5 KB (19501 bytes)  
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
$ docker pull caddy@sha256:e53c2ec5bc7bb3e46c3b08cbe2793d45479d1264c40b5503bef29eac2c91bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3723281c06eda99cbaeea6f288865cad6be253c3b7ed970ae0073b1cff680a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea9d4fd6b7817ea21385211ac68cd734b6e36168539fdfc45a17147cdfbeb5`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 1.5 MB (1451783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd654ccf1647a25716cd5ade72e99d159e39c702b954bd5e1e628ad8095cbc7`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:208946b4132505ebe3d024e76404801b3efceaa335e267fc1147680e4d0a72dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba39e663c5c23602c18674f4c908a2b81d5f5fce9def8350942c92d2c701d6`

```dockerfile
```

-	Layers:
	-	`sha256:726f8c49f1c023380c093fbb8f09dfe9021e323fbdbef3ad8057b76e18e391dd`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97dd399ce6968f36de5122b2b40bebfdca47410eb2e2264e7dd75c76b02ca0e`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 19.6 KB (19599 bytes)  
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
$ docker pull caddy@sha256:5c4cc451b96450e711e40e65789d6e59ee7a0d7a81557fd9ff138828d7cd7047
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.0` - linux; amd64

```console
$ docker pull caddy@sha256:f6bdaeaa2da17edf5a8c33cd6f3cde4e96b37152c2791d4308c1b6695e2a79f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2528051e99d3f23b9fddb25e751078881b1a4237ff2e4bdd77c4c503b66563bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb615d7326964b43a9e5dd3dd14734c53a02dc2cef9fa9ffc00314a64e79a3fe`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 357.4 KB (357368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb87b8526d1948b1e9d896525df20cef23bed00873f22a774db258b070e92a`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333cc5c2a4bdfc22594bac44d124a78fd574d27c4da57ec41e156269d656a58`  
		Last Modified: Wed, 29 May 2024 23:01:06 GMT  
		Size: 14.6 MB (14639245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0` - unknown; unknown

```console
$ docker pull caddy@sha256:9cdbbc45a19237aea8ac5d7ebb37954541082503b26be511135699351c58b4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574268ca9e9da984347d108b60adfdee7bb5792198f3904485d2570a0d3c5e06`

```dockerfile
```

-	Layers:
	-	`sha256:5a044e0dbe68da74ba6be9d21c1fd4ffcc1d42e0061d9f810df5a7b5bf3804ab`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa7cd9091a42e6e0007de5a9ef9c7b132d08ecd23fcb96aadf925cbef4ccef6`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.0` - linux; arm variant v6

```console
$ docker pull caddy@sha256:690174bca4a22f78fd061b913fb9af04c35053cf591739e4274f1e5758136779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a1618df6b54bfa5f963ddc58cc727860e3264267ceba5a03a89dd90f4a5cd6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6242b091285cd3a94637051278e15e4e5fac103eba7cc862f4c049dbd89e5d8`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 357.7 KB (357710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8165fbffda6934ae4fa48e7fb8912c4a52fffdf33dddb24e1fa2823af18b77`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b840d124a7e1135a2bccb8f1921209ee443c13f74e6b5270dbf3d9b5905d87`  
		Last Modified: Thu, 30 May 2024 00:33:31 GMT  
		Size: 13.8 MB (13763171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0` - unknown; unknown

```console
$ docker pull caddy@sha256:18ca096172a9af5d32f39e949ca51c2f3a04b0c3fdd3d3c19c61dc3edacddf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db94e6c76f858c4cb979b37ea5de4a12782484dd46cfca89e9dd213837ad5b74`

```dockerfile
```

-	Layers:
	-	`sha256:a26aa7bb711b04c54e7691a704b1edf426a27937b3bda1721d70aaeddb786cc5`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.0` - linux; s390x

```console
$ docker pull caddy@sha256:a901a1a96c982a13a5b375f9854ac2881ada2dad6e0b51a280e4e0409b3be7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaa0aacb2cad6d7dedd2ae0e0a01b4240ab829d2054697264b7f35a3c8c727`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dffc4dc5008bcfd45facfcd56c34ac3e08dcd41d6dcf4dbf7b1304998e48f7`  
		Last Modified: Thu, 30 May 2024 01:51:03 GMT  
		Size: 14.2 MB (14154597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0` - unknown; unknown

```console
$ docker pull caddy@sha256:f8f994f364719dfc87e3eec9d3d9370870f7dd53fc55a85894cd74b295a064e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279088462e9f352f79f89f32ee4c95eb980369084a4efdd389b4d8de75cdaba`

```dockerfile
```

-	Layers:
	-	`sha256:ad7f9ab13108a2a745e3bc6420a3bc827b9c09669eede8eaabf3013581262027`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79640b0ba457ce4da05d0515c66bb0761b3ba7246808b89cff28c88c7d94f23`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 17.5 KB (17533 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull caddy@sha256:7ed0c647dce908e2b339e897aceacb3a02c4f1fbdd912e60ac55ce8cfd9bcc31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2.8.0-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:f6bdaeaa2da17edf5a8c33cd6f3cde4e96b37152c2791d4308c1b6695e2a79f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2528051e99d3f23b9fddb25e751078881b1a4237ff2e4bdd77c4c503b66563bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb615d7326964b43a9e5dd3dd14734c53a02dc2cef9fa9ffc00314a64e79a3fe`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 357.4 KB (357368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb87b8526d1948b1e9d896525df20cef23bed00873f22a774db258b070e92a`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333cc5c2a4bdfc22594bac44d124a78fd574d27c4da57ec41e156269d656a58`  
		Last Modified: Wed, 29 May 2024 23:01:06 GMT  
		Size: 14.6 MB (14639245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9cdbbc45a19237aea8ac5d7ebb37954541082503b26be511135699351c58b4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574268ca9e9da984347d108b60adfdee7bb5792198f3904485d2570a0d3c5e06`

```dockerfile
```

-	Layers:
	-	`sha256:5a044e0dbe68da74ba6be9d21c1fd4ffcc1d42e0061d9f810df5a7b5bf3804ab`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa7cd9091a42e6e0007de5a9ef9c7b132d08ecd23fcb96aadf925cbef4ccef6`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.0-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:690174bca4a22f78fd061b913fb9af04c35053cf591739e4274f1e5758136779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a1618df6b54bfa5f963ddc58cc727860e3264267ceba5a03a89dd90f4a5cd6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6242b091285cd3a94637051278e15e4e5fac103eba7cc862f4c049dbd89e5d8`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 357.7 KB (357710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8165fbffda6934ae4fa48e7fb8912c4a52fffdf33dddb24e1fa2823af18b77`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b840d124a7e1135a2bccb8f1921209ee443c13f74e6b5270dbf3d9b5905d87`  
		Last Modified: Thu, 30 May 2024 00:33:31 GMT  
		Size: 13.8 MB (13763171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:18ca096172a9af5d32f39e949ca51c2f3a04b0c3fdd3d3c19c61dc3edacddf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db94e6c76f858c4cb979b37ea5de4a12782484dd46cfca89e9dd213837ad5b74`

```dockerfile
```

-	Layers:
	-	`sha256:a26aa7bb711b04c54e7691a704b1edf426a27937b3bda1721d70aaeddb786cc5`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.0-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:a901a1a96c982a13a5b375f9854ac2881ada2dad6e0b51a280e4e0409b3be7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaa0aacb2cad6d7dedd2ae0e0a01b4240ab829d2054697264b7f35a3c8c727`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dffc4dc5008bcfd45facfcd56c34ac3e08dcd41d6dcf4dbf7b1304998e48f7`  
		Last Modified: Thu, 30 May 2024 01:51:03 GMT  
		Size: 14.2 MB (14154597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f8f994f364719dfc87e3eec9d3d9370870f7dd53fc55a85894cd74b295a064e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279088462e9f352f79f89f32ee4c95eb980369084a4efdd389b4d8de75cdaba`

```dockerfile
```

-	Layers:
	-	`sha256:ad7f9ab13108a2a745e3bc6420a3bc827b9c09669eede8eaabf3013581262027`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79640b0ba457ce4da05d0515c66bb0761b3ba7246808b89cff28c88c7d94f23`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 17.5 KB (17533 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8.0-builder`

```console
$ docker pull caddy@sha256:d047eba8ecebe4f5071b6d6d94b31915d6907c6df7c36b2e706cddf9cac9d3c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.0-builder` - linux; amd64

```console
$ docker pull caddy@sha256:1d97a1bfc689534068bc99b432822dc9842c649e729cc0c154f8c154d63f45b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb6b1b4823de1adba6bebfdf129c46e2b64995736eb6673f1ab8feb5553ee9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402b0dc7c1ee13bd10aeed32ca6f6730dfbbd53b36df1c2c43ba6c1ac0ca1a8`  
		Last Modified: Wed, 29 May 2024 23:01:15 GMT  
		Size: 5.9 MB (5914555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4feb0354e90f2c326e6b7d6e8aa8f0c14cb5cafeedd520bbe661cbcdc54876`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 1.5 MB (1500672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6a145aba22dc1cdd83e6e4bc89d3dcd83fed07b9df5447bb29107c926a4222`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a53a011c1a5f9f4482d50088c1170f9d734d111fd6e53b13901390301dbc987a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502eef3ba542c157731565e6b10b6f605c5bbaa4cb2f1a8aa0fcea2fe89d7105`

```dockerfile
```

-	Layers:
	-	`sha256:b40a1d307eafd54bf402058964d29328638bc46540b1ff0e89cfafd693be59c2`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008d2100174b1ae9d0f0f9e9dac7a9d327aa68c96b29fb0f6f7eb63a109c8d9e`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.0-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:76b024f4bfc423eed7169d9548312432f113ec180d6fe4abf9dea3056f08e013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f41be2f19d58f1bc9f7f405236e380a2cb5591a9f3861c7f8f42818200283`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b97bf58febbeb200aa9d2afef8fe6cd7c0ec7c32c2924df16f50e5b908515`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 5.9 MB (5863420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60932c3d4c230ff0adc1536a623aef6a7587fbec36b8add10672330287c9ad0`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e115e84021acc84d0da9a8c93309a09a344ee4fb560abec304c2c599386f62`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3461e07084978dfa05c463d289dc6dbd055b41fd9e6b22f8f58c976d1d3cb9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a214bf5aa952a1965e3eb6e089d2e3d6c4e0cf8cf288c820163d16eb47481c41`

```dockerfile
```

-	Layers:
	-	`sha256:8c82281543d077f647436232fe98bb809e9db5bbe6cda5cae4f0916f0b000d43`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.0-builder` - linux; s390x

```console
$ docker pull caddy@sha256:e53c2ec5bc7bb3e46c3b08cbe2793d45479d1264c40b5503bef29eac2c91bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3723281c06eda99cbaeea6f288865cad6be253c3b7ed970ae0073b1cff680a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea9d4fd6b7817ea21385211ac68cd734b6e36168539fdfc45a17147cdfbeb5`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 1.5 MB (1451783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd654ccf1647a25716cd5ade72e99d159e39c702b954bd5e1e628ad8095cbc7`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:208946b4132505ebe3d024e76404801b3efceaa335e267fc1147680e4d0a72dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba39e663c5c23602c18674f4c908a2b81d5f5fce9def8350942c92d2c701d6`

```dockerfile
```

-	Layers:
	-	`sha256:726f8c49f1c023380c093fbb8f09dfe9021e323fbdbef3ad8057b76e18e391dd`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97dd399ce6968f36de5122b2b40bebfdca47410eb2e2264e7dd75c76b02ca0e`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull caddy@sha256:b45b202739078898e1b9783fc50a6b65cdc73e5966e47593d19289f0720d3db8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2.8.0-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:1d97a1bfc689534068bc99b432822dc9842c649e729cc0c154f8c154d63f45b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb6b1b4823de1adba6bebfdf129c46e2b64995736eb6673f1ab8feb5553ee9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402b0dc7c1ee13bd10aeed32ca6f6730dfbbd53b36df1c2c43ba6c1ac0ca1a8`  
		Last Modified: Wed, 29 May 2024 23:01:15 GMT  
		Size: 5.9 MB (5914555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4feb0354e90f2c326e6b7d6e8aa8f0c14cb5cafeedd520bbe661cbcdc54876`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 1.5 MB (1500672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6a145aba22dc1cdd83e6e4bc89d3dcd83fed07b9df5447bb29107c926a4222`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a53a011c1a5f9f4482d50088c1170f9d734d111fd6e53b13901390301dbc987a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502eef3ba542c157731565e6b10b6f605c5bbaa4cb2f1a8aa0fcea2fe89d7105`

```dockerfile
```

-	Layers:
	-	`sha256:b40a1d307eafd54bf402058964d29328638bc46540b1ff0e89cfafd693be59c2`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008d2100174b1ae9d0f0f9e9dac7a9d327aa68c96b29fb0f6f7eb63a109c8d9e`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.0-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:76b024f4bfc423eed7169d9548312432f113ec180d6fe4abf9dea3056f08e013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f41be2f19d58f1bc9f7f405236e380a2cb5591a9f3861c7f8f42818200283`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b97bf58febbeb200aa9d2afef8fe6cd7c0ec7c32c2924df16f50e5b908515`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 5.9 MB (5863420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60932c3d4c230ff0adc1536a623aef6a7587fbec36b8add10672330287c9ad0`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e115e84021acc84d0da9a8c93309a09a344ee4fb560abec304c2c599386f62`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3461e07084978dfa05c463d289dc6dbd055b41fd9e6b22f8f58c976d1d3cb9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a214bf5aa952a1965e3eb6e089d2e3d6c4e0cf8cf288c820163d16eb47481c41`

```dockerfile
```

-	Layers:
	-	`sha256:8c82281543d077f647436232fe98bb809e9db5bbe6cda5cae4f0916f0b000d43`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.0-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:e53c2ec5bc7bb3e46c3b08cbe2793d45479d1264c40b5503bef29eac2c91bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3723281c06eda99cbaeea6f288865cad6be253c3b7ed970ae0073b1cff680a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea9d4fd6b7817ea21385211ac68cd734b6e36168539fdfc45a17147cdfbeb5`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 1.5 MB (1451783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd654ccf1647a25716cd5ade72e99d159e39c702b954bd5e1e628ad8095cbc7`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.0-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:208946b4132505ebe3d024e76404801b3efceaa335e267fc1147680e4d0a72dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba39e663c5c23602c18674f4c908a2b81d5f5fce9def8350942c92d2c701d6`

```dockerfile
```

-	Layers:
	-	`sha256:726f8c49f1c023380c093fbb8f09dfe9021e323fbdbef3ad8057b76e18e391dd`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97dd399ce6968f36de5122b2b40bebfdca47410eb2e2264e7dd75c76b02ca0e`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull caddy@sha256:7750cb6f08350f2c39207ea87232f7b278f586410232e912542f1d128995636c
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
$ docker pull caddy@sha256:f6bdaeaa2da17edf5a8c33cd6f3cde4e96b37152c2791d4308c1b6695e2a79f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2528051e99d3f23b9fddb25e751078881b1a4237ff2e4bdd77c4c503b66563bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb615d7326964b43a9e5dd3dd14734c53a02dc2cef9fa9ffc00314a64e79a3fe`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 357.4 KB (357368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb87b8526d1948b1e9d896525df20cef23bed00873f22a774db258b070e92a`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333cc5c2a4bdfc22594bac44d124a78fd574d27c4da57ec41e156269d656a58`  
		Last Modified: Wed, 29 May 2024 23:01:06 GMT  
		Size: 14.6 MB (14639245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9cdbbc45a19237aea8ac5d7ebb37954541082503b26be511135699351c58b4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574268ca9e9da984347d108b60adfdee7bb5792198f3904485d2570a0d3c5e06`

```dockerfile
```

-	Layers:
	-	`sha256:5a044e0dbe68da74ba6be9d21c1fd4ffcc1d42e0061d9f810df5a7b5bf3804ab`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa7cd9091a42e6e0007de5a9ef9c7b132d08ecd23fcb96aadf925cbef4ccef6`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:690174bca4a22f78fd061b913fb9af04c35053cf591739e4274f1e5758136779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a1618df6b54bfa5f963ddc58cc727860e3264267ceba5a03a89dd90f4a5cd6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6242b091285cd3a94637051278e15e4e5fac103eba7cc862f4c049dbd89e5d8`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 357.7 KB (357710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8165fbffda6934ae4fa48e7fb8912c4a52fffdf33dddb24e1fa2823af18b77`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b840d124a7e1135a2bccb8f1921209ee443c13f74e6b5270dbf3d9b5905d87`  
		Last Modified: Thu, 30 May 2024 00:33:31 GMT  
		Size: 13.8 MB (13763171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:18ca096172a9af5d32f39e949ca51c2f3a04b0c3fdd3d3c19c61dc3edacddf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db94e6c76f858c4cb979b37ea5de4a12782484dd46cfca89e9dd213837ad5b74`

```dockerfile
```

-	Layers:
	-	`sha256:a26aa7bb711b04c54e7691a704b1edf426a27937b3bda1721d70aaeddb786cc5`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
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
$ docker pull caddy@sha256:a901a1a96c982a13a5b375f9854ac2881ada2dad6e0b51a280e4e0409b3be7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaa0aacb2cad6d7dedd2ae0e0a01b4240ab829d2054697264b7f35a3c8c727`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dffc4dc5008bcfd45facfcd56c34ac3e08dcd41d6dcf4dbf7b1304998e48f7`  
		Last Modified: Thu, 30 May 2024 01:51:03 GMT  
		Size: 14.2 MB (14154597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f8f994f364719dfc87e3eec9d3d9370870f7dd53fc55a85894cd74b295a064e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279088462e9f352f79f89f32ee4c95eb980369084a4efdd389b4d8de75cdaba`

```dockerfile
```

-	Layers:
	-	`sha256:ad7f9ab13108a2a745e3bc6420a3bc827b9c09669eede8eaabf3013581262027`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79640b0ba457ce4da05d0515c66bb0761b3ba7246808b89cff28c88c7d94f23`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 17.5 KB (17533 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder`

```console
$ docker pull caddy@sha256:95b26402e9c139e0c6303ef9eb0b052ec5e432315407ba0d95747dede41234d1
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
$ docker pull caddy@sha256:1d97a1bfc689534068bc99b432822dc9842c649e729cc0c154f8c154d63f45b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb6b1b4823de1adba6bebfdf129c46e2b64995736eb6673f1ab8feb5553ee9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402b0dc7c1ee13bd10aeed32ca6f6730dfbbd53b36df1c2c43ba6c1ac0ca1a8`  
		Last Modified: Wed, 29 May 2024 23:01:15 GMT  
		Size: 5.9 MB (5914555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4feb0354e90f2c326e6b7d6e8aa8f0c14cb5cafeedd520bbe661cbcdc54876`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 1.5 MB (1500672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6a145aba22dc1cdd83e6e4bc89d3dcd83fed07b9df5447bb29107c926a4222`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a53a011c1a5f9f4482d50088c1170f9d734d111fd6e53b13901390301dbc987a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502eef3ba542c157731565e6b10b6f605c5bbaa4cb2f1a8aa0fcea2fe89d7105`

```dockerfile
```

-	Layers:
	-	`sha256:b40a1d307eafd54bf402058964d29328638bc46540b1ff0e89cfafd693be59c2`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008d2100174b1ae9d0f0f9e9dac7a9d327aa68c96b29fb0f6f7eb63a109c8d9e`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:76b024f4bfc423eed7169d9548312432f113ec180d6fe4abf9dea3056f08e013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f41be2f19d58f1bc9f7f405236e380a2cb5591a9f3861c7f8f42818200283`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b97bf58febbeb200aa9d2afef8fe6cd7c0ec7c32c2924df16f50e5b908515`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 5.9 MB (5863420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60932c3d4c230ff0adc1536a623aef6a7587fbec36b8add10672330287c9ad0`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e115e84021acc84d0da9a8c93309a09a344ee4fb560abec304c2c599386f62`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3461e07084978dfa05c463d289dc6dbd055b41fd9e6b22f8f58c976d1d3cb9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a214bf5aa952a1965e3eb6e089d2e3d6c4e0cf8cf288c820163d16eb47481c41`

```dockerfile
```

-	Layers:
	-	`sha256:8c82281543d077f647436232fe98bb809e9db5bbe6cda5cae4f0916f0b000d43`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 19.5 KB (19501 bytes)  
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
$ docker pull caddy@sha256:e53c2ec5bc7bb3e46c3b08cbe2793d45479d1264c40b5503bef29eac2c91bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3723281c06eda99cbaeea6f288865cad6be253c3b7ed970ae0073b1cff680a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea9d4fd6b7817ea21385211ac68cd734b6e36168539fdfc45a17147cdfbeb5`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 1.5 MB (1451783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd654ccf1647a25716cd5ade72e99d159e39c702b954bd5e1e628ad8095cbc7`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:208946b4132505ebe3d024e76404801b3efceaa335e267fc1147680e4d0a72dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba39e663c5c23602c18674f4c908a2b81d5f5fce9def8350942c92d2c701d6`

```dockerfile
```

-	Layers:
	-	`sha256:726f8c49f1c023380c093fbb8f09dfe9021e323fbdbef3ad8057b76e18e391dd`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97dd399ce6968f36de5122b2b40bebfdca47410eb2e2264e7dd75c76b02ca0e`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 19.6 KB (19599 bytes)  
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
$ docker pull caddy@sha256:bdfd9eda328f615f3948329761abc99013772fafb97c6c41bb882815a11d322f
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
$ docker pull caddy@sha256:1d97a1bfc689534068bc99b432822dc9842c649e729cc0c154f8c154d63f45b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb6b1b4823de1adba6bebfdf129c46e2b64995736eb6673f1ab8feb5553ee9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402b0dc7c1ee13bd10aeed32ca6f6730dfbbd53b36df1c2c43ba6c1ac0ca1a8`  
		Last Modified: Wed, 29 May 2024 23:01:15 GMT  
		Size: 5.9 MB (5914555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4feb0354e90f2c326e6b7d6e8aa8f0c14cb5cafeedd520bbe661cbcdc54876`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 1.5 MB (1500672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6a145aba22dc1cdd83e6e4bc89d3dcd83fed07b9df5447bb29107c926a4222`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a53a011c1a5f9f4482d50088c1170f9d734d111fd6e53b13901390301dbc987a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502eef3ba542c157731565e6b10b6f605c5bbaa4cb2f1a8aa0fcea2fe89d7105`

```dockerfile
```

-	Layers:
	-	`sha256:b40a1d307eafd54bf402058964d29328638bc46540b1ff0e89cfafd693be59c2`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008d2100174b1ae9d0f0f9e9dac7a9d327aa68c96b29fb0f6f7eb63a109c8d9e`  
		Last Modified: Wed, 29 May 2024 23:01:14 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:76b024f4bfc423eed7169d9548312432f113ec180d6fe4abf9dea3056f08e013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f41be2f19d58f1bc9f7f405236e380a2cb5591a9f3861c7f8f42818200283`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b97bf58febbeb200aa9d2afef8fe6cd7c0ec7c32c2924df16f50e5b908515`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 5.9 MB (5863420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60932c3d4c230ff0adc1536a623aef6a7587fbec36b8add10672330287c9ad0`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e115e84021acc84d0da9a8c93309a09a344ee4fb560abec304c2c599386f62`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3461e07084978dfa05c463d289dc6dbd055b41fd9e6b22f8f58c976d1d3cb9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a214bf5aa952a1965e3eb6e089d2e3d6c4e0cf8cf288c820163d16eb47481c41`

```dockerfile
```

-	Layers:
	-	`sha256:8c82281543d077f647436232fe98bb809e9db5bbe6cda5cae4f0916f0b000d43`  
		Last Modified: Thu, 30 May 2024 00:34:00 GMT  
		Size: 19.5 KB (19501 bytes)  
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
$ docker pull caddy@sha256:e53c2ec5bc7bb3e46c3b08cbe2793d45479d1264c40b5503bef29eac2c91bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3723281c06eda99cbaeea6f288865cad6be253c3b7ed970ae0073b1cff680a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 29 May 2024 21:22:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 29 May 2024 21:22:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea9d4fd6b7817ea21385211ac68cd734b6e36168539fdfc45a17147cdfbeb5`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 1.5 MB (1451783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd654ccf1647a25716cd5ade72e99d159e39c702b954bd5e1e628ad8095cbc7`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:208946b4132505ebe3d024e76404801b3efceaa335e267fc1147680e4d0a72dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba39e663c5c23602c18674f4c908a2b81d5f5fce9def8350942c92d2c701d6`

```dockerfile
```

-	Layers:
	-	`sha256:726f8c49f1c023380c093fbb8f09dfe9021e323fbdbef3ad8057b76e18e391dd`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97dd399ce6968f36de5122b2b40bebfdca47410eb2e2264e7dd75c76b02ca0e`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 19.6 KB (19599 bytes)  
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
$ docker pull caddy@sha256:1a68e74443e509a8a4f8ca08d3a509507f6f49f10f36da178d57d47d0b634cab
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
$ docker pull caddy@sha256:f6bdaeaa2da17edf5a8c33cd6f3cde4e96b37152c2791d4308c1b6695e2a79f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2528051e99d3f23b9fddb25e751078881b1a4237ff2e4bdd77c4c503b66563bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb615d7326964b43a9e5dd3dd14734c53a02dc2cef9fa9ffc00314a64e79a3fe`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 357.4 KB (357368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb87b8526d1948b1e9d896525df20cef23bed00873f22a774db258b070e92a`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333cc5c2a4bdfc22594bac44d124a78fd574d27c4da57ec41e156269d656a58`  
		Last Modified: Wed, 29 May 2024 23:01:06 GMT  
		Size: 14.6 MB (14639245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:9cdbbc45a19237aea8ac5d7ebb37954541082503b26be511135699351c58b4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574268ca9e9da984347d108b60adfdee7bb5792198f3904485d2570a0d3c5e06`

```dockerfile
```

-	Layers:
	-	`sha256:5a044e0dbe68da74ba6be9d21c1fd4ffcc1d42e0061d9f810df5a7b5bf3804ab`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa7cd9091a42e6e0007de5a9ef9c7b132d08ecd23fcb96aadf925cbef4ccef6`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:690174bca4a22f78fd061b913fb9af04c35053cf591739e4274f1e5758136779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a1618df6b54bfa5f963ddc58cc727860e3264267ceba5a03a89dd90f4a5cd6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6242b091285cd3a94637051278e15e4e5fac103eba7cc862f4c049dbd89e5d8`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 357.7 KB (357710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8165fbffda6934ae4fa48e7fb8912c4a52fffdf33dddb24e1fa2823af18b77`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b840d124a7e1135a2bccb8f1921209ee443c13f74e6b5270dbf3d9b5905d87`  
		Last Modified: Thu, 30 May 2024 00:33:31 GMT  
		Size: 13.8 MB (13763171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:18ca096172a9af5d32f39e949ca51c2f3a04b0c3fdd3d3c19c61dc3edacddf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db94e6c76f858c4cb979b37ea5de4a12782484dd46cfca89e9dd213837ad5b74`

```dockerfile
```

-	Layers:
	-	`sha256:a26aa7bb711b04c54e7691a704b1edf426a27937b3bda1721d70aaeddb786cc5`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
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
$ docker pull caddy@sha256:a901a1a96c982a13a5b375f9854ac2881ada2dad6e0b51a280e4e0409b3be7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaa0aacb2cad6d7dedd2ae0e0a01b4240ab829d2054697264b7f35a3c8c727`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dffc4dc5008bcfd45facfcd56c34ac3e08dcd41d6dcf4dbf7b1304998e48f7`  
		Last Modified: Thu, 30 May 2024 01:51:03 GMT  
		Size: 14.2 MB (14154597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:f8f994f364719dfc87e3eec9d3d9370870f7dd53fc55a85894cd74b295a064e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279088462e9f352f79f89f32ee4c95eb980369084a4efdd389b4d8de75cdaba`

```dockerfile
```

-	Layers:
	-	`sha256:ad7f9ab13108a2a745e3bc6420a3bc827b9c09669eede8eaabf3013581262027`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79640b0ba457ce4da05d0515c66bb0761b3ba7246808b89cff28c88c7d94f23`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 17.5 KB (17533 bytes)  
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
