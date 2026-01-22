## `caddy:latest`

```console
$ docker pull caddy@sha256:2adb640cdc0ce1d8870887c30af1e21edfb3cdfd8433431b2a15f40119a7d654
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:cad41ae98f1b85859198d0091efa5e3bb713dbec041d3e8ac08976c543048ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22499810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e428fb4d0c7a2b0610f5a90dd2797e1b7790de0de9e46e9c2b90fdd745dd201e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:47:40 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Fri, 16 Jan 2026 21:47:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Fri, 16 Jan 2026 21:47:42 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 16 Jan 2026 21:47:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 16 Jan 2026 21:47:42 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 16 Jan 2026 21:47:42 GMT
ENV XDG_DATA_HOME=/data
# Fri, 16 Jan 2026 21:47:42 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 21:47:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 21:47:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 21:47:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 21:47:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 21:47:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 21:47:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 21:47:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 21:47:42 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 Jan 2026 21:47:42 GMT
EXPOSE map[443/tcp:{}]
# Fri, 16 Jan 2026 21:47:42 GMT
EXPOSE map[443/udp:{}]
# Fri, 16 Jan 2026 21:47:42 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 16 Jan 2026 21:47:42 GMT
WORKDIR /srv
# Fri, 16 Jan 2026 21:47:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0865e082b52872f664c068cf059d50fc8136cdaa0a2c35eef05dfdf1947285e`  
		Last Modified: Fri, 16 Jan 2026 21:47:48 GMT  
		Size: 2.8 MB (2765854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0c27ccfb2b19119185f84cdffe65c21d32ddc0eda89df9c48a859d220f50f4`  
		Last Modified: Fri, 16 Jan 2026 21:47:49 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311754a576e94d3eecda1d2fc473b839a5e65aeb37c80f2b4054cde1a99bd986`  
		Last Modified: Fri, 16 Jan 2026 21:47:49 GMT  
		Size: 15.9 MB (15923975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:2a47c5692b061e16c60a3078267fa5275cf1a967f741d317c6cd1354b581fb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.1 KB (338111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53465fcca372d42d13b63c1ccf207810501a09c1f409a50679bf71d793e46c2b`

```dockerfile
```

-	Layers:
	-	`sha256:f2cc31be8a7c09b325db3832af4e5124229d1dcbe95621e8fbdc249807018cb9`  
		Last Modified: Fri, 16 Jan 2026 21:47:49 GMT  
		Size: 319.8 KB (319817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24be2089bf558af1ad11a9071382a3a216f4e9bf5833ce2ac3d3ce8704b3aeab`  
		Last Modified: Fri, 16 Jan 2026 21:47:49 GMT  
		Size: 18.3 KB (18294 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d2a9bdd57bed99bcbe6ee6ef814ef9b2fc9ffc2c76354bde8f4b160efe901f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21261124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f4fb99e52fc5d4dcdeabb146e094dc2614aac5748cb1dec8aa647f0e3f307f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:44:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Fri, 16 Jan 2026 21:44:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Fri, 16 Jan 2026 21:44:51 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 16 Jan 2026 21:44:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 16 Jan 2026 21:44:51 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 16 Jan 2026 21:44:51 GMT
ENV XDG_DATA_HOME=/data
# Fri, 16 Jan 2026 21:44:51 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 21:44:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 21:44:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 21:44:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 21:44:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 21:44:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 21:44:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 21:44:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 21:44:51 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 Jan 2026 21:44:51 GMT
EXPOSE map[443/tcp:{}]
# Fri, 16 Jan 2026 21:44:51 GMT
EXPOSE map[443/udp:{}]
# Fri, 16 Jan 2026 21:44:51 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 16 Jan 2026 21:44:51 GMT
WORKDIR /srv
# Fri, 16 Jan 2026 21:44:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:10 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51237077cff6b8b3e1e078c0f398b39c313b27b5a8d49158a593f3f1c44d7e`  
		Last Modified: Fri, 16 Jan 2026 21:44:56 GMT  
		Size: 2.7 MB (2701011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4190e8018b7413dc7360d5c8129c7e736603d12a658d33d90e17892e9796630`  
		Last Modified: Fri, 16 Jan 2026 21:44:56 GMT  
		Size: 7.5 KB (7492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfec25e70d0beecae4ef337f4532862b6be21dac57f213a80c5831435f9fd0`  
		Last Modified: Fri, 16 Jan 2026 21:44:57 GMT  
		Size: 15.0 MB (15048509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:dd3a62ba5ff9e9d5242acf94effc1bc3a358bd5f3c9f51b36932480d034c5cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7646e70755e4b7e7a42094346e6b203f2acb82aa9d00810187f9319cee0ed0d5`

```dockerfile
```

-	Layers:
	-	`sha256:b3449ea94aa67661c631ca75b277286bdd990a6c8718f60cd97e42756d9df010`  
		Last Modified: Fri, 16 Jan 2026 21:44:56 GMT  
		Size: 18.2 KB (18216 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7d1af3b9b99ac7ce05c0eab8849b89e604149bcb875773a1b98b84bae4b24761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20843997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cc9da5fb3a64ded12818f6e431cccb01e9701100757792fd63cc3444bb7ce8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:44:55 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Fri, 16 Jan 2026 21:44:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Fri, 16 Jan 2026 21:44:56 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 16 Jan 2026 21:44:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 16 Jan 2026 21:44:56 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 16 Jan 2026 21:44:56 GMT
ENV XDG_DATA_HOME=/data
# Fri, 16 Jan 2026 21:44:56 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 21:44:56 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 21:44:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 21:44:56 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 21:44:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 21:44:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 21:44:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 21:44:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 21:44:56 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 Jan 2026 21:44:56 GMT
EXPOSE map[443/tcp:{}]
# Fri, 16 Jan 2026 21:44:56 GMT
EXPOSE map[443/udp:{}]
# Fri, 16 Jan 2026 21:44:56 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 16 Jan 2026 21:44:56 GMT
WORKDIR /srv
# Fri, 16 Jan 2026 21:44:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d8e26f9b8e305761a939412bd153467ec00ec6695ddfde4b0f304451506531`  
		Last Modified: Fri, 16 Jan 2026 21:45:03 GMT  
		Size: 2.6 MB (2582951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c31ca1b0d0956169bb723fb9c79a9a43de4f8107913ec79543f57b8b696192f`  
		Last Modified: Fri, 16 Jan 2026 21:45:03 GMT  
		Size: 7.5 KB (7492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ed6f01bcc66b6b4221197cfd6815bdd52ce5ca6a1b2685fb9e384dff797f71`  
		Last Modified: Fri, 16 Jan 2026 21:45:03 GMT  
		Size: 15.0 MB (15031967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:45d6a31266ee645a6db87232048ac2194a8d025f73c54e930172900c30857a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 KB (338317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27899684322ae8d4e60e21e69967640b1c99c50afbd993f6b308f69af36349c7`

```dockerfile
```

-	Layers:
	-	`sha256:f8e60dfd0b1a58360f9cbe1d09cfcdb4bda0b41b0721902a745dbd3dbc693978`  
		Last Modified: Fri, 16 Jan 2026 21:45:03 GMT  
		Size: 319.9 KB (319885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5cd0725a23f5597cf2cab3f4f0ed5e75e4963c222ccc7683488131a2e3af619`  
		Last Modified: Fri, 16 Jan 2026 21:45:03 GMT  
		Size: 18.4 KB (18432 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:faa97df376502e01ec1e1897e93151e1651d7462959486876b7d2fce478df0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21436160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454c485fdb0d01db1dd2cd54ef208e75ea3be9e5972b7f8774a75cad5bf19e08`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:47:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Fri, 16 Jan 2026 21:47:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Fri, 16 Jan 2026 21:47:51 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 16 Jan 2026 21:47:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 16 Jan 2026 21:47:51 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 16 Jan 2026 21:47:51 GMT
ENV XDG_DATA_HOME=/data
# Fri, 16 Jan 2026 21:47:51 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 21:47:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 21:47:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 21:47:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 21:47:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 21:47:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 21:47:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 21:47:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 21:47:51 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 Jan 2026 21:47:51 GMT
EXPOSE map[443/tcp:{}]
# Fri, 16 Jan 2026 21:47:51 GMT
EXPOSE map[443/udp:{}]
# Fri, 16 Jan 2026 21:47:51 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 16 Jan 2026 21:47:51 GMT
WORKDIR /srv
# Fri, 16 Jan 2026 21:47:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec2c2f67368119144d3b41f74de6113b281487660b61b041e23b840c4a8d505`  
		Last Modified: Fri, 16 Jan 2026 21:47:57 GMT  
		Size: 2.8 MB (2773027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0effe29daeb09ada4f4dad9f5b5b5b474fcdbfc0db4b83fc2a7f4815d32622e`  
		Last Modified: Fri, 16 Jan 2026 21:47:57 GMT  
		Size: 7.5 KB (7493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fee99a1274e5cbbece891688d5815038c5915c00553e7b7da4dc7850d66d93`  
		Last Modified: Fri, 16 Jan 2026 21:47:57 GMT  
		Size: 14.5 MB (14517539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:d090e65c7822ac2b58cde2162128a2c1bb0c16ece15ce2833b215ded1eeb0286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 KB (338397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f332a46d7a291af0c36d4d19499711746e66ce49bfb79fd7c55424a0d2b0366`

```dockerfile
```

-	Layers:
	-	`sha256:5979767b5cca3960b2a9999973133e3e5545195f046298173234f4078122c69c`  
		Last Modified: Fri, 16 Jan 2026 21:47:57 GMT  
		Size: 319.9 KB (319921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b5a2b7aef2436933b8f1f844b59c2197be4231f930ae86670d0d0b40042850`  
		Last Modified: Fri, 16 Jan 2026 21:47:57 GMT  
		Size: 18.5 KB (18476 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:27d1db88091470194bd0cd9873092f693b980371f0c017b73422fc63d4423478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21116687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daaa69c3de0b849304bf294b24c33546c7a52c18e1b49f81576e8a67ef4ee91`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:56:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Fri, 16 Jan 2026 21:56:50 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Fri, 16 Jan 2026 21:56:53 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 16 Jan 2026 21:56:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 16 Jan 2026 21:56:53 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 16 Jan 2026 21:56:53 GMT
ENV XDG_DATA_HOME=/data
# Fri, 16 Jan 2026 21:56:53 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 21:56:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 21:56:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 21:56:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 21:56:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 21:56:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 21:56:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 21:56:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 21:56:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 Jan 2026 21:56:53 GMT
EXPOSE map[443/tcp:{}]
# Fri, 16 Jan 2026 21:56:53 GMT
EXPOSE map[443/udp:{}]
# Fri, 16 Jan 2026 21:56:53 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 16 Jan 2026 21:56:54 GMT
WORKDIR /srv
# Fri, 16 Jan 2026 21:56:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:06 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813ea2decd5834e9e5006afe5caeed0b4fe010dc31cbfb18716a2e2b6b5ec626`  
		Last Modified: Fri, 16 Jan 2026 21:57:26 GMT  
		Size: 2.9 MB (2880997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46303c932b05c47de9a82d4c6739c7a8abe90a94830cc2933a5caccbd1d3b32`  
		Last Modified: Fri, 16 Jan 2026 21:57:25 GMT  
		Size: 7.5 KB (7498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8d26dfc242c73d5bfb2fac54b2701e4979494594ae475c0f23750713309ec4`  
		Last Modified: Fri, 16 Jan 2026 21:57:26 GMT  
		Size: 14.5 MB (14495919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:5fddc2781b48f77c7eb9ca2376f561b3aa68d58343c181001cb5fb0007a68be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 KB (336290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc8602fee1505768e8c76669c6eea7a6f75f27ad0df0b5679e05d549d21ec5a`

```dockerfile
```

-	Layers:
	-	`sha256:4c3b6dece03b52ffc216c0a35db3f9bf22e2c581b936181a9600e6da10b0a6a1`  
		Last Modified: Fri, 16 Jan 2026 21:57:25 GMT  
		Size: 317.9 KB (317924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108b242dcd00bcee391c9c67992576085763179906c45ca275137979f0fbc763`  
		Last Modified: Fri, 16 Jan 2026 21:57:25 GMT  
		Size: 18.4 KB (18366 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; riscv64

```console
$ docker pull caddy@sha256:61a13dbf8a6d683cfa819b4516039ae89b1bcb0c21ec5d2012d55a40b6ba6a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21542216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f408c5005cfe36e39780b2a38220f53133009f7b159b1df1df23036c412781c1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 19 Jan 2026 09:09:44 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Mon, 19 Jan 2026 09:09:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Mon, 19 Jan 2026 09:09:51 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 19 Jan 2026 09:09:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 19 Jan 2026 09:09:51 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 19 Jan 2026 09:09:51 GMT
ENV XDG_DATA_HOME=/data
# Mon, 19 Jan 2026 09:09:51 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 19 Jan 2026 09:09:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 19 Jan 2026 09:09:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 19 Jan 2026 09:09:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 19 Jan 2026 09:09:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 19 Jan 2026 09:09:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 19 Jan 2026 09:09:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 19 Jan 2026 09:09:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 19 Jan 2026 09:09:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 19 Jan 2026 09:09:51 GMT
EXPOSE map[443/tcp:{}]
# Mon, 19 Jan 2026 09:09:51 GMT
EXPOSE map[443/udp:{}]
# Mon, 19 Jan 2026 09:09:51 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 19 Jan 2026 09:09:51 GMT
WORKDIR /srv
# Mon, 19 Jan 2026 09:09:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:17:39 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5debc3271876b99d5dadf72da4db52dac0408e9493a795a644461b97928220f`  
		Last Modified: Mon, 19 Jan 2026 09:10:38 GMT  
		Size: 2.9 MB (2889147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac80ebf11e4e11632868cb13ec6dd4ef8039b00060870dd0f55dfff2d5694f`  
		Last Modified: Mon, 19 Jan 2026 09:10:38 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa36ecfd6706692f3124d0ffc1f3344a9de7cca30aeff15ded2ecf4222cb11b`  
		Last Modified: Mon, 19 Jan 2026 09:10:40 GMT  
		Size: 15.1 MB (15130300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:f13a2a863ba350a59a85acd447caec21a6f56e1af5b307156e33ae3f7b65e1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 KB (336286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7d33b280fa8fb5c7ed62ab8460e9c12be92170988b2f54620a7764376f0f08`

```dockerfile
```

-	Layers:
	-	`sha256:40c38455d6df0a0859d3fda7e7bb2557e3bee8eb4ac4b3d20e4de2d59a6d463e`  
		Last Modified: Mon, 19 Jan 2026 09:10:38 GMT  
		Size: 317.9 KB (317920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c32128d41289326e69dc819ca3e4195dd4d8d259845b4752a114e8bb656fcf3`  
		Last Modified: Mon, 19 Jan 2026 09:10:38 GMT  
		Size: 18.4 KB (18366 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:717d460445d6ca4b3b8521e3cfab0f5b5691a4b41f98c1a8b0cb591ac1470070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21925131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ff86652ca6b96834f7517630c825f2eb26f3ba4288ba5d18c29c9b84cecb09`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 21:47:32 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Fri, 16 Jan 2026 21:47:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Fri, 16 Jan 2026 21:47:34 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 16 Jan 2026 21:47:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 16 Jan 2026 21:47:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 16 Jan 2026 21:47:34 GMT
ENV XDG_DATA_HOME=/data
# Fri, 16 Jan 2026 21:47:34 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 21:47:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 21:47:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 21:47:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 21:47:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 21:47:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 21:47:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 21:47:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 21:47:34 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 Jan 2026 21:47:34 GMT
EXPOSE map[443/tcp:{}]
# Fri, 16 Jan 2026 21:47:34 GMT
EXPOSE map[443/udp:{}]
# Fri, 16 Jan 2026 21:47:34 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 16 Jan 2026 21:47:34 GMT
WORKDIR /srv
# Fri, 16 Jan 2026 21:47:34 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a266cc60179d7e641a609ff09ad484b2c74d2f113b654a87e68c11539f8135`  
		Last Modified: Fri, 16 Jan 2026 21:47:44 GMT  
		Size: 2.9 MB (2911702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7cb2f303df067105fd27b141ece673ac7879d3d54d1d9bdd3a062de981018f`  
		Last Modified: Fri, 16 Jan 2026 21:47:44 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511cd461f97701e72fb7309c63e447106bfbba33b14213320c6ed2b615270654`  
		Last Modified: Fri, 16 Jan 2026 21:47:44 GMT  
		Size: 15.4 MB (15356656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:3ccd6b9a909c7237830c5966fd92efd72cfff7225949fcef9597922752868321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.2 KB (336160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e85cf637ef7b0d5c1e79e6fe9bb1dd4a34ef9d07a9ae225a7290e231b1ee3c`

```dockerfile
```

-	Layers:
	-	`sha256:e9d0e90441c7e7db720e59cd77b5165cafc5f4f7b6287996a93d432c2684c85c`  
		Last Modified: Fri, 16 Jan 2026 21:47:44 GMT  
		Size: 317.9 KB (317866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de55bc7f020cbe679fc3416e5ec9e41b2aeea6cc12583999bdc1a86ac3e22f66`  
		Last Modified: Fri, 16 Jan 2026 21:47:44 GMT  
		Size: 18.3 KB (18294 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - windows version 10.0.26100.32230; amd64

```console
$ docker pull caddy@sha256:de3d1803d449ab02b73296f3ed11e210b30b0e3f7b83665bd85cae0ec1049175
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1513252253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24887a74e96798d4529e46beae49f382b1a10d043a14d7bca49b4cecbdca5dbd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Fri, 16 Jan 2026 21:47:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Jan 2026 21:47:44 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 16 Jan 2026 21:47:45 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 16 Jan 2026 21:48:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 16 Jan 2026 21:48:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 16 Jan 2026 21:48:11 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 16 Jan 2026 21:48:11 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 21:48:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 21:48:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 21:48:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 21:48:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 21:48:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 21:48:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 21:48:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 21:48:16 GMT
EXPOSE 80
# Fri, 16 Jan 2026 21:48:17 GMT
EXPOSE 443
# Fri, 16 Jan 2026 21:48:18 GMT
EXPOSE 443/udp
# Fri, 16 Jan 2026 21:48:19 GMT
EXPOSE 2019
# Fri, 16 Jan 2026 21:48:26 GMT
RUN caddy version
# Fri, 16 Jan 2026 21:48:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b7436bdde4954ab997653ca362b6410146a18fcf3b8b83a54c551cf59c9c73`  
		Last Modified: Fri, 16 Jan 2026 21:48:36 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8984e104b3c0ff05fa60406f16ff2c4a2f58af5476a4da8460d993e5b15c54`  
		Last Modified: Fri, 16 Jan 2026 21:48:36 GMT  
		Size: 400.1 KB (400124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d50d69015e54959d508b06414479a76601f3f1c0c143302fa9815426f0ecdb`  
		Last Modified: Fri, 16 Jan 2026 21:48:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dd758177c1c66b62710c9ed34334f9a3b5978222bc6019718dfae6fd235898`  
		Last Modified: Fri, 16 Jan 2026 21:48:38 GMT  
		Size: 16.7 MB (16685267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6469db906ffeec163dc378daa88374a7395d787fbd64478d4a423691f7aa1c6`  
		Last Modified: Fri, 16 Jan 2026 21:48:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9460c8b42281a2a84615f002cbb6533907bb7414d370ba83f99b09259c4b8577`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6125a52e3a7563428016564d117f80bd877e38a7a37181bab82f031fc024b8`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4f6273de3485d3093bea4161194792b0a4895d56b17d19ea0ae955de131723`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bb815f2b06c4f07495bb86c150cb225f1e14a30832c182218467729a2c22cd`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3bb0e23239e46f5ac1baf3505b72062c5c1b0a2b56accf494255279b81dc6c`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a0214cac497353d4d26a9e5729390a85a2cb4422324ad1a8dc9b7cbc10c883`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a97fe8c2c247a6fcaf584e485cc9b3d5bc584d4f0b7e97ca098fd712ffcc10e`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe22cb691633447fd4bb8f450aa6f4382ed47bc70c2f393e6eec96f267f6872`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3985fbe8b539cb8a152f3c35d7e7df4d60e2640770f2aa39f00fe07553a32e4`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e323161037befd8a9185eb6af7db6e238ccb4451b0f64284a255f3062f58ac`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5852fd37e891f32ad639c4d4d7f6645b31ca2efe1e9bc6b7b588d6046bce65ab`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1abadcb16f8b7383029dbb8f7528efb9cddedd7ff75d0847ef53f11e744b75c`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051e8ff0c84b5e9acf20fae62134d7bb0807d09f14fe921287c0ca135f987422`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa1ae318ebbfdc86e2311719b9629cade532ac567939ea85a8dd9fd1f236062`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 384.3 KB (384316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3e746bfff6a737ce01c0ec0226a66bf3b12acfd3f6c44c2fd4fc4809d15811`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.4648; amd64

```console
$ docker pull caddy@sha256:c10a12076add43fa2fcacfce590ac2f6a9e0d01cd2e1354b67e470bf0d06bd56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1853115354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f606fbff6b8d9ec8bbb5c43b8421f44d197c4f55842e54a82c05797112718a32`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Fri, 16 Jan 2026 21:47:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Jan 2026 21:47:39 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 16 Jan 2026 21:47:40 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 16 Jan 2026 21:47:50 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 16 Jan 2026 21:47:50 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 16 Jan 2026 21:47:51 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 16 Jan 2026 21:47:52 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 21:47:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 21:47:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 21:47:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 21:47:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 21:47:57 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 21:47:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 21:47:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 21:48:00 GMT
EXPOSE 80
# Fri, 16 Jan 2026 21:48:00 GMT
EXPOSE 443
# Fri, 16 Jan 2026 21:48:01 GMT
EXPOSE 443/udp
# Fri, 16 Jan 2026 21:48:02 GMT
EXPOSE 2019
# Fri, 16 Jan 2026 21:48:11 GMT
RUN caddy version
# Fri, 16 Jan 2026 21:48:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da84340b07e1cad15dbe51c11c05f559aa95ab7eed9c6e68dc4a812c0906345b`  
		Last Modified: Fri, 16 Jan 2026 21:48:21 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f4160a6438b1a19d88835ec1728c72ae59f039f5784b9526691a7eeb82534b`  
		Last Modified: Fri, 16 Jan 2026 21:48:21 GMT  
		Size: 501.7 KB (501660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79009ba30b634a5be800711a4826a3472717eebab51a739db447021acd08cf23`  
		Last Modified: Fri, 16 Jan 2026 21:48:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9b614b74a27be3bfbabfae99d05eee3a8c9519f9f22b63874fd166b1478dd5`  
		Last Modified: Fri, 16 Jan 2026 21:48:23 GMT  
		Size: 16.6 MB (16574503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7410e33005a69fb0873209de68263e1b4f2915be399c4f43aa318a5fcb9fd1`  
		Last Modified: Fri, 16 Jan 2026 21:48:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4929bb4e999d90782a313f7c9b9b7c0435cb0745857211642bb657132e716240`  
		Last Modified: Fri, 16 Jan 2026 21:48:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538a350f92fb6ac1f4078601f7b59d9fd2f687f613930258988a571d227ddf45`  
		Last Modified: Fri, 16 Jan 2026 21:48:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2770b5e6afd5fc8d518455cb07fe2fa7bbfc026746e7d85fa24b9c3e0eaa24b8`  
		Last Modified: Fri, 16 Jan 2026 21:48:19 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4940ace21147a2455987b5d6fb5173346a78c22c1f7b6a67aa49a65e3d6b217f`  
		Last Modified: Fri, 16 Jan 2026 21:48:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa00dab456cb8086de15acacb6e660122a0aaf402479cdb95e473c6721052456`  
		Last Modified: Fri, 16 Jan 2026 21:48:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc014ece1282be27edce301ee3c6569096f34dbea5174b32918638fd985d9d2`  
		Last Modified: Fri, 16 Jan 2026 21:48:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9925c02e110fb56805cb659030ffd87a3a4035f403366d9489efdd0fff509fe6`  
		Last Modified: Fri, 16 Jan 2026 21:48:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc38634bbbc8d62ac19edafe1c5c534965984ef837f6921a41227105f80c98c`  
		Last Modified: Fri, 16 Jan 2026 21:48:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa2f1c08e7e6bffba7e2aafe2cae668cdbae2d991f19beda42da8df5df3b57a`  
		Last Modified: Fri, 16 Jan 2026 21:48:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a925076807ae691e68aab5bdcd04ad643544b23148d12a721bf71f657fc9c0`  
		Last Modified: Fri, 16 Jan 2026 21:48:18 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7733bea24770f80b76f2796916cd7abe848203317f7a263a87e0d9738944fec1`  
		Last Modified: Fri, 16 Jan 2026 21:48:16 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ac31721ac6a9a67ce9b5f1586d31f549412d51993ac1cb6432bd891cd5d263`  
		Last Modified: Fri, 16 Jan 2026 21:48:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e09078b5a083a4a9e63b2fcc5bac2ca609b27d3aad7d7680f8f3855a00e74ce`  
		Last Modified: Fri, 16 Jan 2026 21:48:16 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc66546b510325c0a603db853cfaae858d0aea3e3f9b244947cd5d1b91934c6a`  
		Last Modified: Fri, 16 Jan 2026 21:48:16 GMT  
		Size: 357.8 KB (357768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12efdcf8eadcbf183e0c9807135be6f68bb4557242cdf88beea64f37bf7cc32`  
		Last Modified: Fri, 16 Jan 2026 21:48:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
