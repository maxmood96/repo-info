## `caddy:alpine`

```console
$ docker pull caddy@sha256:953131cfea8e12bfe1c631a36308e9660e4389f0c3dfb3be957044d3ac92d446
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:5c18f4b845cd8f2cbb344ffa6fe0391d8c975ed921848c9968298f1eb8940a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20089474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4bd530ab75a01a5c22fbb097938267e4cde118eab50ae68078df59ce83bceb2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_DATA_HOME=/data
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[80/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/udp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /srv
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094994dd0a888230052dc694e55fba90dcfb325d8fa94440c3ed81c87c95ae06`  
		Last Modified: Sun, 07 Dec 2025 23:56:00 GMT  
		Size: 355.5 KB (355523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bad5cd4577dae30587abbb0a8108d45d58e384305b5d123d2fbd738042ef0a`  
		Last Modified: Sun, 07 Dec 2025 23:56:00 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e3c8bc26d8f0e5df4ea5405a1c979aa5493679cef2e1eb255aa07bffeb7e28`  
		Last Modified: Sun, 07 Dec 2025 23:56:02 GMT  
		Size: 15.9 MB (15923971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c49b5bb9fafca5664bab24f64ba8ed9dbf93ef119619a617a6452dbf94aaec01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 KB (316904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194872cafbada5fb4b567a53b5af6d05580e5abe137958b1e592a22e47e59dfe`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa8f91e4e6d082719891371a594a00815377c6afc3b17e781e134a69d944ca`  
		Last Modified: Thu, 09 Oct 2025 00:52:26 GMT  
		Size: 298.6 KB (298626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d0898f0570e1e6c5fb9ac17d060df7d1755cc23e0ff533c5f93f46ef6bd6e89`  
		Last Modified: Thu, 09 Oct 2025 00:52:26 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:119e4266b8542835dfdd2e1235c73880429d8901fbbbbefa59739a889250d324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18916344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848a24afa8857404c1db30cb3234be39b847d9c524e7e573eeb26de9d6883b7c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_DATA_HOME=/data
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[80/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/udp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /srv
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4068a1404a3bfc3a9d39e4e6ed58c4bd0bf13a7ff30669d35fbb4a2a1fcb1a9e`  
		Last Modified: Wed, 08 Oct 2025 22:37:01 GMT  
		Size: 356.2 KB (356225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c2b98bd8058d99e4e9d2603a3b3d495f94a487ef4e2fb3827e0023ccec3b8d`  
		Last Modified: Wed, 08 Oct 2025 22:37:01 GMT  
		Size: 7.5 KB (7490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355ca295561e63362f38ae44b4f8a4a61f418a3835168e0abe66cd9f6405b2ee`  
		Last Modified: Wed, 08 Oct 2025 22:37:02 GMT  
		Size: 15.0 MB (15048517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7a488aae60ec4ba389c2472f39291944dfa9934d1d185b24a1455c2d62728b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e2aa1a57598620fc663719e9c572d5a655d51a84be73e2f3085a302f03c63d`

```dockerfile
```

-	Layers:
	-	`sha256:220487e07a536398b13c979c0c2923b286d14f8ebefe18b58c3a15f95dec5899`  
		Last Modified: Thu, 09 Oct 2025 00:52:30 GMT  
		Size: 18.2 KB (18199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:55cc489b0b057671f28154c12e6efd8dc866439d973c017a384b80e6966859ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18613363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f5b018e558891ec02aacf9023eb56f6bc43f8d9d4afc2e6d04142741ae3fd3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_DATA_HOME=/data
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[80/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/udp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /srv
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed7b3aea9da2e9093fac5eab39359b1b1ed7f459049adc7f163635dc3fde275`  
		Last Modified: Wed, 08 Oct 2025 22:41:51 GMT  
		Size: 352.3 KB (352304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbdbf7405c9b11eb2fdfd10042e53ef02555f95133524de57691739d23486c7`  
		Last Modified: Wed, 08 Oct 2025 22:41:51 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e890a196f1f388e7a8c914c50df4b9c6d78413035af5bc67f47f3857df152538`  
		Last Modified: Wed, 08 Oct 2025 22:41:52 GMT  
		Size: 15.0 MB (15031977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b25d1c67e49ab8e556cacaa0e92752c7235de8b79521b0871774dde15ac33afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 KB (317110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e05b4a365bd9f15bfe41a15c1c33a9ea079066d21ae6a36519127e90c21cfa`

```dockerfile
```

-	Layers:
	-	`sha256:a3d13a3b269943cd2177d415f6e0851cf9a1d8e52a58f485cae286ac3d4bd822`  
		Last Modified: Thu, 09 Oct 2025 00:52:33 GMT  
		Size: 298.7 KB (298694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4c8144aefab9edb5c2dc9d3e131d9a901d6d5b09867afaeb889693622f26e6`  
		Last Modified: Thu, 09 Oct 2025 00:52:33 GMT  
		Size: 18.4 KB (18416 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:3ec909d297a11a136cd78a90765e157967466bc0c19b99cd884d0479c563a1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19029206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab23159d0dc076a83c3b43bccd0cbace50741387dd06ce1293b64e1d177db69d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_DATA_HOME=/data
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[80/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/udp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /srv
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737ecdde2e2ecef51a250ce1ae99f4b40bd6977e422b973993c377e3548f3120`  
		Last Modified: Mon, 08 Dec 2025 00:00:12 GMT  
		Size: 366.1 KB (366071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87847351977cacbef726e63b52c02bde04850613395b130b5fc259498472b45`  
		Last Modified: Mon, 08 Dec 2025 00:00:11 GMT  
		Size: 7.5 KB (7491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166c5fb722cb3f17cdf3d805d0bbec06601f118525a417434ea03108e4ae9303`  
		Last Modified: Mon, 08 Dec 2025 00:00:13 GMT  
		Size: 14.5 MB (14517543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ffd8c624ab9b845fdd098717dfc3d51149894f6feb30a016597c6a91d110a8e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 KB (317190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbba4df62057f013eff99f1e1aabf21a863470a34fb4403210c4fcaf05daa5f5`

```dockerfile
```

-	Layers:
	-	`sha256:11061761934d5f4870704f8c2a38ff3c5712ae1199f6f958fe792ccb03ec549b`  
		Last Modified: Mon, 08 Dec 2025 00:07:24 GMT  
		Size: 298.7 KB (298730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039e7e391f2c23076faaef089a9b6e63074143d3da4d8f33f2cfd8d78301af62`  
		Last Modified: Mon, 08 Dec 2025 00:07:24 GMT  
		Size: 18.5 KB (18460 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:c412ccb85bc54ed540b5a37862b752217c20f5fa15424502784a56fe6fded2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18604500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825677b7a0f25f5d25b1b5926cb5553fde21617b52abbcf6e13266a05ef47c9f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_DATA_HOME=/data
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[80/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/udp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /srv
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823cf6229661310faccbee1d81ef556247257e7da24430c526114dbc8fd565dd`  
		Last Modified: Thu, 09 Oct 2025 05:14:19 GMT  
		Size: 368.8 KB (368814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1164d333279d1866242da65da41a739090482761127f8428f3188ada453b5b`  
		Last Modified: Thu, 09 Oct 2025 05:14:19 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4151e8f114cfa8dbc24530e7e3a0617344547b919e0dd4a79683e88baa2db42`  
		Last Modified: Thu, 09 Oct 2025 05:14:20 GMT  
		Size: 14.5 MB (14495918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e5d4055c821a73fec1ede6b5518bbe658c79ea08c1db00fa74d7d9442e5fbb53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 KB (315083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b3548a25c24af7e613c93da9f56a691c9377c9406febdc3627b04da4067bac`

```dockerfile
```

-	Layers:
	-	`sha256:ddb9817790624763af2957f7a6550a1113adfc93bca0f5fc83c9d5bda44cf9ef`  
		Last Modified: Thu, 09 Oct 2025 06:52:27 GMT  
		Size: 296.7 KB (296733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:894e4f2ec1c4231bcec21b4c775a309dda0fdc472fe917a94e07274429aaa4e3`  
		Last Modified: Thu, 09 Oct 2025 06:52:28 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:bd48c4c0645a0decebeedd8def18dd1bff76cb1f5b4d0f137f1bd1820a6b98b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19010573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cd22ec803f9ed446075d808813065397ccc018efa2915a49250fcb2c22df6c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_DATA_HOME=/data
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[80/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/udp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /srv
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a79220ebb0a3e08ea34645a8fc471f021e631eb17a4723f52eb790f9134555`  
		Last Modified: Sat, 11 Oct 2025 20:41:37 GMT  
		Size: 357.5 KB (357524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c02683713ca00f90319fb1a7459899cd6e8e0bdeefa520ecae6dfa0a6579b0`  
		Last Modified: Sat, 11 Oct 2025 20:41:37 GMT  
		Size: 7.5 KB (7499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b6471262dc4736f73060a2425e36fb287a6ceed81bc70abb377457a46e5994`  
		Last Modified: Sat, 11 Oct 2025 20:41:39 GMT  
		Size: 15.1 MB (15130278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:74e38a3ffadc9cb09f34e2c6475fc7803aaded49c472e238af9dc7726fe2fa13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 KB (315079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf1af4e79b4cb12c79161b403d81d1d3f07829a01aeec45d394b5aaea585e35`

```dockerfile
```

-	Layers:
	-	`sha256:e994c824db677103dd1c5e88ea1381a424575158eade63614edaf7a5a84b2251`  
		Last Modified: Sat, 11 Oct 2025 21:52:36 GMT  
		Size: 296.7 KB (296729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b68e426924114a18ac7806b153757cd235876fa326ffca96dc314d03a50fe4`  
		Last Modified: Sat, 11 Oct 2025 21:52:36 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:dae181e2f6395ea9498cd26625526593784d448e820401a3cc194f1a6534be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19376672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353725c9febf90a18472b414f23e22351302e9055c08c7b536f64ee30d6b9985`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XDG_DATA_HOME=/data
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 23 Aug 2025 03:19:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[80/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[443/udp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /srv
# Sat, 23 Aug 2025 03:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd28ddaea64762437c8dee6ad76815bd5f7fb8175436a4b0e4a0002f1941ad38`  
		Last Modified: Thu, 09 Oct 2025 06:16:29 GMT  
		Size: 363.2 KB (363249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e391259e509e3414f28ef229fdcd3edf6273e5f42568464a824ffad2e39c772`  
		Last Modified: Thu, 09 Oct 2025 06:16:29 GMT  
		Size: 7.5 KB (7494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990c9c9e981b91fb34daa330777c96dda3beff4e682a6603dd1224eb64bd7063`  
		Last Modified: Thu, 09 Oct 2025 06:16:30 GMT  
		Size: 15.4 MB (15356653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:352e1ae47755173298c8de06e1dc46e0deceaf7d7fa6352de09cd8ef9ea80b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 KB (314953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc116143972450499216c79e29560c9d33d52ff5fc32fb71a9d7d37ef89a355`

```dockerfile
```

-	Layers:
	-	`sha256:2897d683303bb3918107982c7b4cecb28f3389696a76b7516df25952b6ce5dd3`  
		Last Modified: Thu, 09 Oct 2025 09:52:32 GMT  
		Size: 296.7 KB (296675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21179f92b65d1c78268208373774025f0ea774983d58f47e6a0af0b4992f0c5d`  
		Last Modified: Thu, 09 Oct 2025 09:52:33 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json
