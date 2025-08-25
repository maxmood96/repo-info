<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-ltsc2022`](#caddy2-builder-windowsservercore-ltsc2022)
-	[`caddy:2-builder-windowsservercore-ltsc2025`](#caddy2-builder-windowsservercore-ltsc2025)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-ltsc2022`](#caddy2-windowsservercore-ltsc2022)
-	[`caddy:2-windowsservercore-ltsc2025`](#caddy2-windowsservercore-ltsc2025)
-	[`caddy:2.10`](#caddy210)
-	[`caddy:2.10-alpine`](#caddy210-alpine)
-	[`caddy:2.10-builder`](#caddy210-builder)
-	[`caddy:2.10-builder-alpine`](#caddy210-builder-alpine)
-	[`caddy:2.10-builder-windowsservercore-ltsc2022`](#caddy210-builder-windowsservercore-ltsc2022)
-	[`caddy:2.10-builder-windowsservercore-ltsc2025`](#caddy210-builder-windowsservercore-ltsc2025)
-	[`caddy:2.10-windowsservercore`](#caddy210-windowsservercore)
-	[`caddy:2.10-windowsservercore-ltsc2022`](#caddy210-windowsservercore-ltsc2022)
-	[`caddy:2.10-windowsservercore-ltsc2025`](#caddy210-windowsservercore-ltsc2025)
-	[`caddy:2.10.2`](#caddy2102)
-	[`caddy:2.10.2-alpine`](#caddy2102-alpine)
-	[`caddy:2.10.2-builder`](#caddy2102-builder)
-	[`caddy:2.10.2-builder-alpine`](#caddy2102-builder-alpine)
-	[`caddy:2.10.2-builder-windowsservercore-ltsc2022`](#caddy2102-builder-windowsservercore-ltsc2022)
-	[`caddy:2.10.2-builder-windowsservercore-ltsc2025`](#caddy2102-builder-windowsservercore-ltsc2025)
-	[`caddy:2.10.2-windowsservercore`](#caddy2102-windowsservercore)
-	[`caddy:2.10.2-windowsservercore-ltsc2022`](#caddy2102-windowsservercore-ltsc2022)
-	[`caddy:2.10.2-windowsservercore-ltsc2025`](#caddy2102-windowsservercore-ltsc2025)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:builder-alpine`](#caddybuilder-alpine)
-	[`caddy:builder-windowsservercore-ltsc2022`](#caddybuilder-windowsservercore-ltsc2022)
-	[`caddy:builder-windowsservercore-ltsc2025`](#caddybuilder-windowsservercore-ltsc2025)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-ltsc2022`](#caddywindowsservercore-ltsc2022)
-	[`caddy:windowsservercore-ltsc2025`](#caddywindowsservercore-ltsc2025)

## `caddy:2`

```console
$ docker pull caddy@sha256:73ba793f1b2355cfefe2a7ec53ac2f2db0531bf52679deaf16df087fd35ce4ea
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
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:e9fd95fd7cea0c3403c622c5c2457cddcaf355a5eba11048b17cb3d99a828f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20077764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a72cdc384a6f6b8c1d99f569290cee6606bec3cca68812feba43bfda45028`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634211206164759ba5e5df423465aed056f9cc799700d15b89ca49626779515f`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 346.6 KB (346592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edccfae94f0e103409f8c3283a9e19bb7585db1ed9bd9e3a0311de9e0149c1de`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e53616944a4fa3ff99b33d90d938827b7d63bdb00324b94dab3ad40ab166831`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 15.9 MB (15923955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:30f634f6f0e9e39136903c3b81be8f780a4b805b66163bfc0e683fafb62a3f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 KB (314291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d132bcee2e485d83458421325b31111463d1718ccf62b18456e97d495bc57`

```dockerfile
```

-	Layers:
	-	`sha256:91d8c07f79d660b96ebece0d8847c92fd5160edb83b97e31865c2af067eeb8f0`  
		Last Modified: Mon, 25 Aug 2025 21:52:42 GMT  
		Size: 296.0 KB (296013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d27f4d928535909dc6d7b276be2d1e63901b6b627c43a4bfd594a0b899c110`  
		Last Modified: Mon, 25 Aug 2025 21:52:43 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bf497dbd5122b8bce808c55b47aa082eb84d06f77831adf2d8cc0b5f11e66438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18903449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ba67aa2169d0dbd6426eb009d3bd28de88cb829cb8453b2e628f0443f6e9f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8aa6aa6b1802d86bbc73e75216bbb426a1a8ebad8fab1ccf37a1adfdd1b779`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 346.5 KB (346493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3bd303b867cb629d2b99f58967b240f288c9b1dbf712003b3e56200692140c`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e6b087db3bea6b06b1a48ee30c1fc4db8efebe5b0e6670b418e3db437e8c38`  
		Last Modified: Mon, 25 Aug 2025 19:48:46 GMT  
		Size: 15.0 MB (15048518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:286477e027ad1c6350295044f9c520fa196eb08183d4939ae7ed071fc7320c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16e2d2b0cb8b273b15b42a3b1d12c77c076d757e265061f5e61b31763a6a52`

```dockerfile
```

-	Layers:
	-	`sha256:29f2ff0c73ef6349295d38ad6646decc7e0677799f04a1a1ce633e18c85a4327`  
		Last Modified: Mon, 25 Aug 2025 21:52:47 GMT  
		Size: 18.2 KB (18197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d5af7163676df0baffb41f5bce9c4f0775a69609bc2384b101ff4ba749f0050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18601748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e276120a8a2d3df3a422b6d9a2b02c16b9f92c6b28ac595c34fcc06410127c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979c078f866daa2820e22fa7f8a9cc664e49f7d538de1341a2c2c9a60489560`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 343.2 KB (343205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeca689d2f3de3a319b91d9ddb84048521f017d394555aa2ab895ef9cdb98e2`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711aca2485d7f9dfbfccd9cf2a11a6db8015c154383632363d1ac44b755cb55`  
		Last Modified: Mon, 25 Aug 2025 19:48:47 GMT  
		Size: 15.0 MB (15031978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:8049ae7cb8cf21da392232342dd2c386e8e79bb9a7093ef47dec2cd1e4d8d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 KB (314493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b289ec4bc1157ad5848221ba42af4a065fd5af769065351ada6548da41f5c1`

```dockerfile
```

-	Layers:
	-	`sha256:7653918e29fb0de220bc0644efa15394bed69ae8f40081cd705aa96205888b4c`  
		Last Modified: Mon, 25 Aug 2025 21:52:51 GMT  
		Size: 296.1 KB (296081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fb47d806abc1bee7ac987c99961bb2c58274d6cbc04b58ea4c3c026b94f2ce`  
		Last Modified: Mon, 25 Aug 2025 21:52:52 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:4c3be81b7ee70190ce5291230e5a5d4dd8ea998c44cfb5fcc4680a60ea6c5621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19013546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b37c5f2910ca9daf3b5cd9f63bb06d782d2062d4daceced81673d49fe4a1c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ebf372d05e77b4bdc3cea55c048537aaac7759aa0079ed9944004ac30c980c`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 357.7 KB (357727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f163ee242da1ec76c0ab875c407ba39c49aa3eab955a46b9ea14d94a86c4d48e`  
		Last Modified: Mon, 25 Aug 2025 19:48:51 GMT  
		Size: 7.5 KB (7492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225b3b694c911c2a8b8814871c8353f7b7686cc9ea3fc2b02dba2f45803dd75`  
		Last Modified: Mon, 25 Aug 2025 19:48:55 GMT  
		Size: 14.5 MB (14517545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:a657dd5aa41ae2796a14d32f91e630f0efcefa03e3261ac63d39793887cea22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 KB (314576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469b3383a6f868625bafb61aa5dd86ccd26899761e2bdb5fafafbc7e250ef24b`

```dockerfile
```

-	Layers:
	-	`sha256:4f49301002ed8e6230d3ea527498b3328f01453f1b0e12e3bbcb7ce771cca15b`  
		Last Modified: Mon, 25 Aug 2025 21:52:55 GMT  
		Size: 296.1 KB (296117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fbb94c8995329e1c4b3235561ee976502480bebaab9183f926bf2529444c9d`  
		Last Modified: Mon, 25 Aug 2025 21:52:56 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:67112be943616a31dfbf0c815ed5325bf71a9d8c6cfe49a1935b244bd3b109e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18591170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f3d87694b9256e003a6824820cec8dfc82ad339b7d3bc41671c4996663a0a3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe739855dbbb9a1403a242cd984b1b9b4439925fb4fcedc9d3d6ade9baf3dd5`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 360.6 KB (360616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab33549ec0ff70ed9ba5ea43079d739e8d6fe698b0578958a9e2675602d1f6`  
		Last Modified: Mon, 25 Aug 2025 19:49:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6276663ba0f6c95bde9cd5440dc7ec15f6e100f8283c704efd10d02181f066dc`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 14.5 MB (14495915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:54c1de5978b47c2325c8f34e5589b9e4befd54792776c52701944ded623d9922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 KB (312470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d525e05914ec596f61ab5f038622c17b75382bd36e15638e19d2ef0b54ab4`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2fa5edceb1da7dbf0f53e0b3b6e55ebdebce9112144575d69508ba7ea1f29`  
		Last Modified: Mon, 25 Aug 2025 21:53:01 GMT  
		Size: 294.1 KB (294120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2488d35b692ff2f9eeccf6177b581e0b4012821bcd0e7079a6755296fdc31433`  
		Last Modified: Mon, 25 Aug 2025 21:53:02 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; riscv64

```console
$ docker pull caddy@sha256:fab4c562bd13d4fe11cc47963461b4b2f197e38afa3be8a61b698b6319238f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17956644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c209b028cc287828f645bdd0dc227ee3dbc69f503f5bf1a4ad3a944252b78b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29116abe2cb7489bfe0d514003d7c4822eaf03d2b44e5f1c10c878a603eceb13`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 348.3 KB (348289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ceaafe79989c43b373a7e7780390f12740f15ad106a2c987605998f180cea`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 7.5 KB (7498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9baf51ef7381285244300ec8288209b2b0dc82267a2c3547eb0644ce4c7948`  
		Last Modified: Fri, 18 Jul 2025 07:36:44 GMT  
		Size: 14.3 MB (14251735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:608fabfae5954b1485e44928f39c3844fbdc7de236202d87c4380838c748a018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 KB (303605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff983ccc8020f39b317500f82d9596ad6b4299338ecb828eaa0685950b57aa46`

```dockerfile
```

-	Layers:
	-	`sha256:090b4908e38667b8110e66242c7d88a6c27ba9f8dc2ebc126e04430fcaff531c`  
		Last Modified: Fri, 18 Jul 2025 09:52:30 GMT  
		Size: 285.3 KB (285255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e87f231dbdaabee2c8a7c7375c70ff7387e5d2387ed1a26033f1a9b77c0e427`  
		Last Modified: Fri, 18 Jul 2025 09:52:31 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:df924d28949f8a3be699c88ab40eb6b5ca37234e6af5431cb6a1cca63e58a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19362618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85040edfc178cf9c5de8611792e65c67f07629a5c76b7089bf0828d075163a0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff98415fc23c99d5ff9b731b3ed1f5f263fca7f05ddbb51c47d7d8b6df1f89e8`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 353.5 KB (353456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e6340a3b7a63c6c76d521ec65f90ba0718a26fb02520f02216f158300c89e`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd56c657dc325cdf0a5d0c300a1380b0fe6abd98dcee92bcf38b02d14d579062`  
		Last Modified: Mon, 25 Aug 2025 19:51:46 GMT  
		Size: 15.4 MB (15356663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:ce406a252aedd52a38cc6938d993637d83f2aedbe10e9eb385f4b60a12418812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 KB (312340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190d69bf6d55a424c64ecfe71fedbf83d368d2191338ab24083d5426fa60e861`

```dockerfile
```

-	Layers:
	-	`sha256:ea8886b3a4622ffdcc38a8a441716fbb95afc7feb55738ebaae75b137a193925`  
		Last Modified: Mon, 25 Aug 2025 21:53:08 GMT  
		Size: 294.1 KB (294062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5011fab561f7f812f810ba45504c8489c7a5e0383d88863c43b47478a136a21a`  
		Last Modified: Mon, 25 Aug 2025 21:53:09 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:64642fe1e2319c999d20aa489a73e261b5b4ae4fab29385b61e5221287af5c42
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

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:e9fd95fd7cea0c3403c622c5c2457cddcaf355a5eba11048b17cb3d99a828f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20077764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a72cdc384a6f6b8c1d99f569290cee6606bec3cca68812feba43bfda45028`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634211206164759ba5e5df423465aed056f9cc799700d15b89ca49626779515f`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 346.6 KB (346592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edccfae94f0e103409f8c3283a9e19bb7585db1ed9bd9e3a0311de9e0149c1de`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e53616944a4fa3ff99b33d90d938827b7d63bdb00324b94dab3ad40ab166831`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 15.9 MB (15923955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:30f634f6f0e9e39136903c3b81be8f780a4b805b66163bfc0e683fafb62a3f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 KB (314291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d132bcee2e485d83458421325b31111463d1718ccf62b18456e97d495bc57`

```dockerfile
```

-	Layers:
	-	`sha256:91d8c07f79d660b96ebece0d8847c92fd5160edb83b97e31865c2af067eeb8f0`  
		Last Modified: Mon, 25 Aug 2025 21:52:42 GMT  
		Size: 296.0 KB (296013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d27f4d928535909dc6d7b276be2d1e63901b6b627c43a4bfd594a0b899c110`  
		Last Modified: Mon, 25 Aug 2025 21:52:43 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bf497dbd5122b8bce808c55b47aa082eb84d06f77831adf2d8cc0b5f11e66438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18903449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ba67aa2169d0dbd6426eb009d3bd28de88cb829cb8453b2e628f0443f6e9f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8aa6aa6b1802d86bbc73e75216bbb426a1a8ebad8fab1ccf37a1adfdd1b779`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 346.5 KB (346493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3bd303b867cb629d2b99f58967b240f288c9b1dbf712003b3e56200692140c`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e6b087db3bea6b06b1a48ee30c1fc4db8efebe5b0e6670b418e3db437e8c38`  
		Last Modified: Mon, 25 Aug 2025 19:48:46 GMT  
		Size: 15.0 MB (15048518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:286477e027ad1c6350295044f9c520fa196eb08183d4939ae7ed071fc7320c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16e2d2b0cb8b273b15b42a3b1d12c77c076d757e265061f5e61b31763a6a52`

```dockerfile
```

-	Layers:
	-	`sha256:29f2ff0c73ef6349295d38ad6646decc7e0677799f04a1a1ce633e18c85a4327`  
		Last Modified: Mon, 25 Aug 2025 21:52:47 GMT  
		Size: 18.2 KB (18197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d5af7163676df0baffb41f5bce9c4f0775a69609bc2384b101ff4ba749f0050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18601748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e276120a8a2d3df3a422b6d9a2b02c16b9f92c6b28ac595c34fcc06410127c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979c078f866daa2820e22fa7f8a9cc664e49f7d538de1341a2c2c9a60489560`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 343.2 KB (343205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeca689d2f3de3a319b91d9ddb84048521f017d394555aa2ab895ef9cdb98e2`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711aca2485d7f9dfbfccd9cf2a11a6db8015c154383632363d1ac44b755cb55`  
		Last Modified: Mon, 25 Aug 2025 19:48:47 GMT  
		Size: 15.0 MB (15031978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:8049ae7cb8cf21da392232342dd2c386e8e79bb9a7093ef47dec2cd1e4d8d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 KB (314493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b289ec4bc1157ad5848221ba42af4a065fd5af769065351ada6548da41f5c1`

```dockerfile
```

-	Layers:
	-	`sha256:7653918e29fb0de220bc0644efa15394bed69ae8f40081cd705aa96205888b4c`  
		Last Modified: Mon, 25 Aug 2025 21:52:51 GMT  
		Size: 296.1 KB (296081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fb47d806abc1bee7ac987c99961bb2c58274d6cbc04b58ea4c3c026b94f2ce`  
		Last Modified: Mon, 25 Aug 2025 21:52:52 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:4c3be81b7ee70190ce5291230e5a5d4dd8ea998c44cfb5fcc4680a60ea6c5621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19013546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b37c5f2910ca9daf3b5cd9f63bb06d782d2062d4daceced81673d49fe4a1c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ebf372d05e77b4bdc3cea55c048537aaac7759aa0079ed9944004ac30c980c`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 357.7 KB (357727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f163ee242da1ec76c0ab875c407ba39c49aa3eab955a46b9ea14d94a86c4d48e`  
		Last Modified: Mon, 25 Aug 2025 19:48:51 GMT  
		Size: 7.5 KB (7492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225b3b694c911c2a8b8814871c8353f7b7686cc9ea3fc2b02dba2f45803dd75`  
		Last Modified: Mon, 25 Aug 2025 19:48:55 GMT  
		Size: 14.5 MB (14517545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a657dd5aa41ae2796a14d32f91e630f0efcefa03e3261ac63d39793887cea22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 KB (314576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469b3383a6f868625bafb61aa5dd86ccd26899761e2bdb5fafafbc7e250ef24b`

```dockerfile
```

-	Layers:
	-	`sha256:4f49301002ed8e6230d3ea527498b3328f01453f1b0e12e3bbcb7ce771cca15b`  
		Last Modified: Mon, 25 Aug 2025 21:52:55 GMT  
		Size: 296.1 KB (296117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fbb94c8995329e1c4b3235561ee976502480bebaab9183f926bf2529444c9d`  
		Last Modified: Mon, 25 Aug 2025 21:52:56 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:67112be943616a31dfbf0c815ed5325bf71a9d8c6cfe49a1935b244bd3b109e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18591170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f3d87694b9256e003a6824820cec8dfc82ad339b7d3bc41671c4996663a0a3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe739855dbbb9a1403a242cd984b1b9b4439925fb4fcedc9d3d6ade9baf3dd5`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 360.6 KB (360616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab33549ec0ff70ed9ba5ea43079d739e8d6fe698b0578958a9e2675602d1f6`  
		Last Modified: Mon, 25 Aug 2025 19:49:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6276663ba0f6c95bde9cd5440dc7ec15f6e100f8283c704efd10d02181f066dc`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 14.5 MB (14495915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:54c1de5978b47c2325c8f34e5589b9e4befd54792776c52701944ded623d9922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 KB (312470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d525e05914ec596f61ab5f038622c17b75382bd36e15638e19d2ef0b54ab4`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2fa5edceb1da7dbf0f53e0b3b6e55ebdebce9112144575d69508ba7ea1f29`  
		Last Modified: Mon, 25 Aug 2025 21:53:01 GMT  
		Size: 294.1 KB (294120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2488d35b692ff2f9eeccf6177b581e0b4012821bcd0e7079a6755296fdc31433`  
		Last Modified: Mon, 25 Aug 2025 21:53:02 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:fab4c562bd13d4fe11cc47963461b4b2f197e38afa3be8a61b698b6319238f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17956644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c209b028cc287828f645bdd0dc227ee3dbc69f503f5bf1a4ad3a944252b78b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29116abe2cb7489bfe0d514003d7c4822eaf03d2b44e5f1c10c878a603eceb13`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 348.3 KB (348289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ceaafe79989c43b373a7e7780390f12740f15ad106a2c987605998f180cea`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 7.5 KB (7498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9baf51ef7381285244300ec8288209b2b0dc82267a2c3547eb0644ce4c7948`  
		Last Modified: Fri, 18 Jul 2025 07:36:44 GMT  
		Size: 14.3 MB (14251735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:608fabfae5954b1485e44928f39c3844fbdc7de236202d87c4380838c748a018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 KB (303605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff983ccc8020f39b317500f82d9596ad6b4299338ecb828eaa0685950b57aa46`

```dockerfile
```

-	Layers:
	-	`sha256:090b4908e38667b8110e66242c7d88a6c27ba9f8dc2ebc126e04430fcaff531c`  
		Last Modified: Fri, 18 Jul 2025 09:52:30 GMT  
		Size: 285.3 KB (285255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e87f231dbdaabee2c8a7c7375c70ff7387e5d2387ed1a26033f1a9b77c0e427`  
		Last Modified: Fri, 18 Jul 2025 09:52:31 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:df924d28949f8a3be699c88ab40eb6b5ca37234e6af5431cb6a1cca63e58a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19362618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85040edfc178cf9c5de8611792e65c67f07629a5c76b7089bf0828d075163a0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff98415fc23c99d5ff9b731b3ed1f5f263fca7f05ddbb51c47d7d8b6df1f89e8`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 353.5 KB (353456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e6340a3b7a63c6c76d521ec65f90ba0718a26fb02520f02216f158300c89e`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd56c657dc325cdf0a5d0c300a1380b0fe6abd98dcee92bcf38b02d14d579062`  
		Last Modified: Mon, 25 Aug 2025 19:51:46 GMT  
		Size: 15.4 MB (15356663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ce406a252aedd52a38cc6938d993637d83f2aedbe10e9eb385f4b60a12418812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 KB (312340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190d69bf6d55a424c64ecfe71fedbf83d368d2191338ab24083d5426fa60e861`

```dockerfile
```

-	Layers:
	-	`sha256:ea8886b3a4622ffdcc38a8a441716fbb95afc7feb55738ebaae75b137a193925`  
		Last Modified: Mon, 25 Aug 2025 21:53:08 GMT  
		Size: 294.1 KB (294062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5011fab561f7f812f810ba45504c8489c7a5e0383d88863c43b47478a136a21a`  
		Last Modified: Mon, 25 Aug 2025 21:53:09 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:38708d13dba3aafb83ed97d8b1f9ed00823a6d0eb63de314945a55ada80db2d8
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
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:baa56c9394d7025fb7e344f5a1d52c7d0ae2a428a6d8e4d7acf85480477cf819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72186376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0205b23d29755cb0085885d9fa3ac1ea66ce75020051c0185f423ea947bc24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d4ca09441bdb9129d5708d2aa8802e233b2d11d1797317158c4095e9df8fc`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 282.4 KB (282437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18414ed0f6669fd1d6e137922f2a57e37aaf0a63ae6968c499fe69b17d148d14`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36dd3b7005cdf211c5d6cd7f47820b1ffa15134a87c84b500f754613863411`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.2 MB (6211320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc4a072890c37012160bb87d003d188e34244b09f60d9a7e33a521175aa4914`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.8 MB (1846494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45676fbd1b151c4eb76c6df8afe515dd1b8001736b55aba9841182177b17`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:f5d337972eff4ad3e0c109de0443e6695887aae29e94c1df6e6189ef17e777df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3035b7074d5121642859847a37b0e722a8cb9137408b7356cf5e5a79d0a6760c`

```dockerfile
```

-	Layers:
	-	`sha256:f41e395e3e21569a16f8d91a8825c71ee9146373ca8d37c13d6e6de553f55627`  
		Last Modified: Mon, 25 Aug 2025 21:53:16 GMT  
		Size: 276.8 KB (276799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a6e841ccf0c2ac296066a2cd3354ab00dcc598ae922e619237f17aebd1bb82`  
		Last Modified: Mon, 25 Aug 2025 21:53:17 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e1edbceed451136633244ae771982f55dd7d7218a4ffc50369af9eefbb5266a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70630913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8be52c140ce9073b5e99046435e6d10435d169d31239bff87fc88de3e317a56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b30dde5a6a0bd25a99ef148aafdaf794991c98c7b0798149f6d4e21ebc6ccd`  
		Last Modified: Wed, 13 Aug 2025 19:12:26 GMT  
		Size: 59.0 MB (58976836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63714916874ab7e10bdc757c1f8a9e57104a40067c294f970c9d8ff49423866`  
		Last Modified: Wed, 13 Aug 2025 18:04:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96b63bb94735bf5a233756bdc50074d4de4f13340afa4a5b52a444075d8471d`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 6.1 MB (6124248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cae36cb0796b19b218d007f943c4a58a98847586c215d0b9182edb25f4b08`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d14e3b2c944638da45ebffd7d320249acf6ca96e796a9c2aaee17c71e23a4d`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:b2b71368948bedcdbe1fe1b49cbffe11bca901b908dde0561b73953dad703bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b200e21ab8337407084c2f915782c003a30ed1b357ddf279a1faf52f479fd277`

```dockerfile
```

-	Layers:
	-	`sha256:995e27d2c9f18e3d1278c03b04caf0d92d8524cca3c1f98d0b486e78c8fdec72`  
		Last Modified: Mon, 25 Aug 2025 21:53:21 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7570894dd8642571d29a3f9a172447dc68c92466e954fbfe509dd4c1002c62d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69821208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303120483e85eaa18d5623ff884d6ba6bc5329cf64792dafc7122ec47e98f1b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0ef49cd2af3f26990fbdb01d76c5d72224144a9082720b843066d506cd46c9`  
		Last Modified: Thu, 14 Aug 2025 04:30:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee18d4be11a0ac51fa3627c2b017b3aef767f70a39ea0d73d6de35cd618a71f`  
		Last Modified: Mon, 25 Aug 2025 19:49:07 GMT  
		Size: 5.6 MB (5603426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6551895b1ab029d74729175b98ce97b83c07b3112d073fc90b8fe101237e63`  
		Last Modified: Mon, 25 Aug 2025 19:49:09 GMT  
		Size: 1.7 MB (1738756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b87d17c36733a93bfd68173426cc2ef130e2195c9c450df58a04dc2c5fab0f`  
		Last Modified: Mon, 25 Aug 2025 19:49:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:55c648a2b1f1e4d6d07485531af3a8734047d606ae8f624a5e55a14a84c3badd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 KB (300079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cdb0bd297a9f9a841359ac15ef57a33be96fe2dae32e84f34341e6fbcf5b69`

```dockerfile
```

-	Layers:
	-	`sha256:8823ee0afb3d9696b6ca5b09a159c39bf7a8fe6690d1fb9851fe5f74584f325f`  
		Last Modified: Mon, 25 Aug 2025 21:53:25 GMT  
		Size: 279.8 KB (279843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486c238d647f7578251e57dd34ce120fb465b25780a1e60cf69ec3bd36b22be4`  
		Last Modified: Mon, 25 Aug 2025 21:53:26 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:32fa6d72e61b79987dd65c0d108e5078c0e0dc93af0460612778e63182c2076c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69951490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9745840960c0e962feb8ce93ade81f3d2d7c4014b1aa7675e1ae02d0a7aff9ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1a427e917c48b164eae3ec3692b4741f5de528261925d2e5efc62a43e5bfc4`  
		Last Modified: Mon, 28 Jul 2025 20:42:19 GMT  
		Size: 284.7 KB (284709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b50d3516e3fbf4aca43b9416e7dd8914c2623a08d12eeb55d98d72b864d50c`  
		Last Modified: Wed, 13 Aug 2025 21:40:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b905d71c6a895e4f8e02255340a28c48f2a71d4744873257004c40c0d2aa00`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.3 MB (6263485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f8b26f147c3aad964c448d6607cf74ae215e3ac1c4cbba753fa3e968275e88`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3231a1494a810504f8b0f942889fffa994e046e8e88d228e3a5088783ce72`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:2afba1033f0a6e1546bfc4ba308b2a11e83940382cb23e26214953132de73502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e5578a03d1c8f2a6f8ffcbe41b2176db7f2e9fe34e3740615730082fda76c7`

```dockerfile
```

-	Layers:
	-	`sha256:748645f9a413db4552bbf182353615a0b12bcd436e3be618d281b3d593030ede`  
		Last Modified: Mon, 25 Aug 2025 21:53:30 GMT  
		Size: 276.9 KB (276903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93bc5bdadeab69d30a633aee167e91118e46d1789c6f0ffd8919e02d2abce29`  
		Last Modified: Mon, 25 Aug 2025 21:53:31 GMT  
		Size: 20.3 KB (20279 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:af183020c3351759ff8b8f4bafc2723eeff7c818144664e3694cc95a57ce5b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70304708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562175980913c7c3795d4d816c57841adf59a5bc12f44a1cd0eeb9e6e600f14a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe3e6d4a1713a75edf1789d38233b2e8d48f54cebae5e9d0789eb1af52023b`  
		Last Modified: Mon, 28 Jul 2025 20:30:54 GMT  
		Size: 285.1 KB (285114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269abe529e66aa5bca30329a5b15eb3b1dc68dbfb72494192487eabaf2c75ea7`  
		Last Modified: Wed, 13 Aug 2025 22:24:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b70f44dd4f808419f6fd44bceba6d166aca8e19f4cc6cbd8b36f33239207db`  
		Last Modified: Mon, 25 Aug 2025 19:50:03 GMT  
		Size: 6.6 MB (6550799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d7bd24bb9deffe0ca1b77e298776a06b4a558884001c7bb47966dadc97ca43`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd6fde2d426e5936d85b957d51eeee4fe29a27e410fcafc97d0874ffda5b0a7`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0aebec967107348a51c2631c5a8092b2a9ddf49e4a53aa5e56b903b7db8da90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 KB (295105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5483635ad7faac1a9e8b342df273f4ba0a4bdbe31f6c156346534eee30d30458`

```dockerfile
```

-	Layers:
	-	`sha256:41a25cf6cf15b6b37e3661b3ac34bd18681863b0b85f51cec56d1d316f0397a5`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 274.9 KB (274920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b02b106246f8f724524bb0de7288d77cf1087c013b38171b388fcaf0f37f9e0`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:fb87571ab0cfe463d5b70a18f7fc659670b5c55747db3031ea04cb59192007d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87901339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc43b273027a52c8474444595317de4089d1356a37708213bb7d600ddde35e7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03fbadbe664ad3d80e3509b96250ae628b3c572ce60e514d1ab20170b9d16f`  
		Last Modified: Wed, 06 Aug 2025 20:35:39 GMT  
		Size: 76.3 MB (76329537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3100604e2ac3ab2afb5cfbb5b614bf8a221677bd8062fec6e7c8d427bd3a227`  
		Last Modified: Wed, 06 Aug 2025 20:38:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7fcb5eb3236cdaf4c847395cb3593f761279c79096d30f3e7cf35380880458`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 6.2 MB (6227728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ffbcd6b9606b2af427eeec605dcacf7cd7d3373be452b10e2bb22f249781e`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 1.7 MB (1711639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cfb2de1c2d535f5db75d479624e79d3c03d09237fa02bfe0e3cdaca96319d6`  
		Last Modified: Wed, 06 Aug 2025 21:55:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e726fabc45a470f841e6101b22886180e210ce12d35e7294ff41bda3d5fca48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 KB (310664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b2a779549901a2e89720d3b51ed603f8cad90098f71519ddbb0679b33cb68`

```dockerfile
```

-	Layers:
	-	`sha256:ccc7ede165f095820a25ffb389a248d0b37c8e904fc5ab03cd1183fef473c6fd`  
		Last Modified: Thu, 07 Aug 2025 00:52:47 GMT  
		Size: 290.5 KB (290479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f30acaaa6bd313ee7a3e5ee0cf46680343b632c7fc49a20989d0b539919b4f`  
		Last Modified: Thu, 07 Aug 2025 00:52:48 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:28695f2cfaee062b9a0ca60163b294c9aa426d62328db2bface2b85e282b88ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71589730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3295b1278233227188e8477c2827afae51d241b108713916b5ef77d03eb41a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27212710686629ba49777b5e0cccdf04e89cbe41c95c072e1c75381906d724e9`  
		Last Modified: Wed, 13 Aug 2025 22:25:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b7f018e46a54de4eea0e2dad72f4490579e3365d43915d3250d53ae7ec1890`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 6.5 MB (6502043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c049c1b926591fbe94ed04678a617c00476cf93094e56c118b4aa7d5301293`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8d48eb228a3be3c4a90c83ceb3a374f1cbf2cd8b2704f4bfb913c41a3321d`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ffc6ef944b883b81dfd10aedf994982d8dabb9a7bb31e67921f976ef1da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 KB (294963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0eadd91f1fd0a0f91b5c7391ac0c55f701c738d3b6db0537f39f79f0269f79`

```dockerfile
```

-	Layers:
	-	`sha256:518491161b596d1ff8a9f6f9f6edaf63f977efff9396b1be87c42e36e666a14a`  
		Last Modified: Mon, 25 Aug 2025 21:53:42 GMT  
		Size: 274.8 KB (274848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba037ad301b98b30c070866ceb9f8b5b99f8482275c68bd46ba5664c7b6e5e90`  
		Last Modified: Mon, 25 Aug 2025 21:53:43 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:f0ecd5bc38691c997cfbb4eaff5bede8b9d25421e5a2fb78b50ac5fbf79f08f5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3615224351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b87c61031d564c20e4c7aadd128b369ac69af5472854d710e6709eec622c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 13 Aug 2025 18:08:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:08:27 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:08:29 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:08:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:08:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:08:50 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:10:07 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:10:07 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:56:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:56:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:56:36 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:56:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:56:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:56:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3329feb8c3f471d93f04a4afc376778f359481b9b10abd677ae7f8105b7a1982`  
		Last Modified: Wed, 13 Aug 2025 18:14:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b683ebca7e697913d8f93eeb03b85a4924fa297a5830b694441bb31e2ef2a8`  
		Last Modified: Wed, 13 Aug 2025 18:14:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a25a1b355f0af537456d6695b8cbf9c0c5582795add71831072b1f2067593`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5469c0152f4c91f8d66bd59239beec913796e4d17d8977dcf67364f6916d3aae`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9e732885c916712df386d920174e3f95dcc40377352391c6f5e8ccc9e59be5`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9ebf49453f4f127c2dffe22dcb483f4eeef5d0260fe4724472d7fc5b89ecaf`  
		Last Modified: Wed, 13 Aug 2025 18:14:25 GMT  
		Size: 51.2 MB (51223826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55bb43d7b4377e022452dadea8a547292c78952945e888b4c3a99193a0e78f`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec885b71c379ce9bdce0b6477ef6652f6b9d9f566e7e571c9863ba6adb40cede`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 351.5 KB (351496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e05cdc4ff30cbd5098771fc7b97628d410fe4d7f2afb43e7ddcd5256d51d407`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5def4f4469cc1db786df7b6975d1fc3c3bd4c534434e05e676d67edd1f0af9f`  
		Last Modified: Wed, 13 Aug 2025 18:14:22 GMT  
		Size: 62.5 MB (62477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dd29c29527d22890d7b81985987d57cceb811888344ca07659b7c0f2e94151`  
		Last Modified: Wed, 13 Aug 2025 18:14:10 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8523736186869f7a49f95f8b318bee25824ebbb010838d15db88667b969e3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb124c01828ece301417db645f6bd33502d9fa4004bbabb93d8483d9adee73fc`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc48728b561dbd7581689079fb9e459be5b1b835c2a19d3e6ad8d63472b2b7b4`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009143406fac9c3402bce23cf7487a8d83bf93fd0dacf936aa17661011450dd`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a06a632575ebdb5c471cc6aeed6865b4ed1bda3ead85aaa00ed5488712d68f3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 2.3 MB (2324141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb76a0655e886937e45d30114efbcbb8b7dcf4f622e834abea3396c37a8494`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:fae8c3555cf3840ff8637313f178c0317b41466226312ea50a9d597b377a982b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2397840105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5006347b108bafda0318a83f34338f8ef74ab52d118e9d335f14fcd1870a70a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 13 Aug 2025 18:06:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:06:54 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:06:55 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:07:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:07:11 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:07:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:07:18 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:08:48 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:49 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:53 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:49:54 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:50:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:50:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9380c184b3613450235fc0562d48b7c1aeb69072e1e188efd675b317114e13`  
		Last Modified: Wed, 13 Aug 2025 18:10:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb25f9f3a6b5b2e582eb535d357af7f125a5eb0d07250886e7275753bba63b`  
		Last Modified: Wed, 13 Aug 2025 18:10:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1b81a88b515880f2398d85c50e12604a0be218b43024e6273e174b171a33`  
		Last Modified: Wed, 13 Aug 2025 18:10:31 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe632c05e48eccbb4f65220b5c6cd3d2c38482c1aff7c8a70dedef13c2d8cde3`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2281e6abc340f61cf79bb6641d015955f72d05413007591f91ca52d8fcb2020b`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6aa352166614c00f1cc5419011f1a211ffaa26ece1203ddb8a7248c0f9dee1`  
		Last Modified: Wed, 13 Aug 2025 18:10:50 GMT  
		Size: 51.2 MB (51199537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36716abacdfd69d4d84aaeb498a02c39e5df07d380dc62c6f93a43dd18bd8b36`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992bb304a4c05d05ad6f9fce52e761eaca24471880c19303b2d27362b731cf77`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 335.3 KB (335287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363744c527b6172af2deba44c4735f38293dd27bc326cde515fa1e40d983cbed`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6c232258d56f8ebfb4d22b50309c11595a9cd50805699bb1edc2ff5cac8dc2`  
		Last Modified: Wed, 13 Aug 2025 18:11:01 GMT  
		Size: 62.3 MB (62261944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318c09560fb6a640397158d02fb52738a3d51b23a8f80d35724a4ece31d4cf72`  
		Last Modified: Wed, 13 Aug 2025 18:10:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1f3385040c90c1ee57f2d21940227c7a049f3442ac13a978b145cf185a15f`  
		Last Modified: Mon, 25 Aug 2025 19:50:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe569c48af273bca5f90b236956c3823ba707807419d4b3d31037b23731ca95`  
		Last Modified: Mon, 25 Aug 2025 19:50:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244ee2fe3346da9436f4b3f9faa2052570d594821c15b4458df33433e70d4cf0`  
		Last Modified: Mon, 25 Aug 2025 19:50:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bbd758a87764c779cea8fe9429c091634198b909b6faadc2c04c4add5049a0`  
		Last Modified: Mon, 25 Aug 2025 19:50:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0dab63cb896e209cbc5b4577e607d35a3df8d9e39d5dca15bc9208710b2ec`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 2.3 MB (2334479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769960fd4bcf873320f369a1ea9ae102548c30a01938b0886cbafefe311b4353`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:2cf9b153f9f65bc7dbaef420968aee70bc0c9e570b2c217777014e1c329de416
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

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:baa56c9394d7025fb7e344f5a1d52c7d0ae2a428a6d8e4d7acf85480477cf819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72186376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0205b23d29755cb0085885d9fa3ac1ea66ce75020051c0185f423ea947bc24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d4ca09441bdb9129d5708d2aa8802e233b2d11d1797317158c4095e9df8fc`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 282.4 KB (282437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18414ed0f6669fd1d6e137922f2a57e37aaf0a63ae6968c499fe69b17d148d14`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36dd3b7005cdf211c5d6cd7f47820b1ffa15134a87c84b500f754613863411`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.2 MB (6211320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc4a072890c37012160bb87d003d188e34244b09f60d9a7e33a521175aa4914`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.8 MB (1846494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45676fbd1b151c4eb76c6df8afe515dd1b8001736b55aba9841182177b17`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f5d337972eff4ad3e0c109de0443e6695887aae29e94c1df6e6189ef17e777df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3035b7074d5121642859847a37b0e722a8cb9137408b7356cf5e5a79d0a6760c`

```dockerfile
```

-	Layers:
	-	`sha256:f41e395e3e21569a16f8d91a8825c71ee9146373ca8d37c13d6e6de553f55627`  
		Last Modified: Mon, 25 Aug 2025 21:53:16 GMT  
		Size: 276.8 KB (276799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a6e841ccf0c2ac296066a2cd3354ab00dcc598ae922e619237f17aebd1bb82`  
		Last Modified: Mon, 25 Aug 2025 21:53:17 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e1edbceed451136633244ae771982f55dd7d7218a4ffc50369af9eefbb5266a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70630913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8be52c140ce9073b5e99046435e6d10435d169d31239bff87fc88de3e317a56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b30dde5a6a0bd25a99ef148aafdaf794991c98c7b0798149f6d4e21ebc6ccd`  
		Last Modified: Wed, 13 Aug 2025 19:12:26 GMT  
		Size: 59.0 MB (58976836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63714916874ab7e10bdc757c1f8a9e57104a40067c294f970c9d8ff49423866`  
		Last Modified: Wed, 13 Aug 2025 18:04:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96b63bb94735bf5a233756bdc50074d4de4f13340afa4a5b52a444075d8471d`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 6.1 MB (6124248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cae36cb0796b19b218d007f943c4a58a98847586c215d0b9182edb25f4b08`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d14e3b2c944638da45ebffd7d320249acf6ca96e796a9c2aaee17c71e23a4d`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b2b71368948bedcdbe1fe1b49cbffe11bca901b908dde0561b73953dad703bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b200e21ab8337407084c2f915782c003a30ed1b357ddf279a1faf52f479fd277`

```dockerfile
```

-	Layers:
	-	`sha256:995e27d2c9f18e3d1278c03b04caf0d92d8524cca3c1f98d0b486e78c8fdec72`  
		Last Modified: Mon, 25 Aug 2025 21:53:21 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7570894dd8642571d29a3f9a172447dc68c92466e954fbfe509dd4c1002c62d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69821208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303120483e85eaa18d5623ff884d6ba6bc5329cf64792dafc7122ec47e98f1b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0ef49cd2af3f26990fbdb01d76c5d72224144a9082720b843066d506cd46c9`  
		Last Modified: Thu, 14 Aug 2025 04:30:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee18d4be11a0ac51fa3627c2b017b3aef767f70a39ea0d73d6de35cd618a71f`  
		Last Modified: Mon, 25 Aug 2025 19:49:07 GMT  
		Size: 5.6 MB (5603426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6551895b1ab029d74729175b98ce97b83c07b3112d073fc90b8fe101237e63`  
		Last Modified: Mon, 25 Aug 2025 19:49:09 GMT  
		Size: 1.7 MB (1738756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b87d17c36733a93bfd68173426cc2ef130e2195c9c450df58a04dc2c5fab0f`  
		Last Modified: Mon, 25 Aug 2025 19:49:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:55c648a2b1f1e4d6d07485531af3a8734047d606ae8f624a5e55a14a84c3badd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 KB (300079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cdb0bd297a9f9a841359ac15ef57a33be96fe2dae32e84f34341e6fbcf5b69`

```dockerfile
```

-	Layers:
	-	`sha256:8823ee0afb3d9696b6ca5b09a159c39bf7a8fe6690d1fb9851fe5f74584f325f`  
		Last Modified: Mon, 25 Aug 2025 21:53:25 GMT  
		Size: 279.8 KB (279843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486c238d647f7578251e57dd34ce120fb465b25780a1e60cf69ec3bd36b22be4`  
		Last Modified: Mon, 25 Aug 2025 21:53:26 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:32fa6d72e61b79987dd65c0d108e5078c0e0dc93af0460612778e63182c2076c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69951490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9745840960c0e962feb8ce93ade81f3d2d7c4014b1aa7675e1ae02d0a7aff9ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1a427e917c48b164eae3ec3692b4741f5de528261925d2e5efc62a43e5bfc4`  
		Last Modified: Mon, 28 Jul 2025 20:42:19 GMT  
		Size: 284.7 KB (284709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b50d3516e3fbf4aca43b9416e7dd8914c2623a08d12eeb55d98d72b864d50c`  
		Last Modified: Wed, 13 Aug 2025 21:40:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b905d71c6a895e4f8e02255340a28c48f2a71d4744873257004c40c0d2aa00`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.3 MB (6263485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f8b26f147c3aad964c448d6607cf74ae215e3ac1c4cbba753fa3e968275e88`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3231a1494a810504f8b0f942889fffa994e046e8e88d228e3a5088783ce72`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2afba1033f0a6e1546bfc4ba308b2a11e83940382cb23e26214953132de73502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e5578a03d1c8f2a6f8ffcbe41b2176db7f2e9fe34e3740615730082fda76c7`

```dockerfile
```

-	Layers:
	-	`sha256:748645f9a413db4552bbf182353615a0b12bcd436e3be618d281b3d593030ede`  
		Last Modified: Mon, 25 Aug 2025 21:53:30 GMT  
		Size: 276.9 KB (276903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93bc5bdadeab69d30a633aee167e91118e46d1789c6f0ffd8919e02d2abce29`  
		Last Modified: Mon, 25 Aug 2025 21:53:31 GMT  
		Size: 20.3 KB (20279 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:af183020c3351759ff8b8f4bafc2723eeff7c818144664e3694cc95a57ce5b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70304708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562175980913c7c3795d4d816c57841adf59a5bc12f44a1cd0eeb9e6e600f14a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe3e6d4a1713a75edf1789d38233b2e8d48f54cebae5e9d0789eb1af52023b`  
		Last Modified: Mon, 28 Jul 2025 20:30:54 GMT  
		Size: 285.1 KB (285114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269abe529e66aa5bca30329a5b15eb3b1dc68dbfb72494192487eabaf2c75ea7`  
		Last Modified: Wed, 13 Aug 2025 22:24:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b70f44dd4f808419f6fd44bceba6d166aca8e19f4cc6cbd8b36f33239207db`  
		Last Modified: Mon, 25 Aug 2025 19:50:03 GMT  
		Size: 6.6 MB (6550799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d7bd24bb9deffe0ca1b77e298776a06b4a558884001c7bb47966dadc97ca43`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd6fde2d426e5936d85b957d51eeee4fe29a27e410fcafc97d0874ffda5b0a7`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0aebec967107348a51c2631c5a8092b2a9ddf49e4a53aa5e56b903b7db8da90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 KB (295105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5483635ad7faac1a9e8b342df273f4ba0a4bdbe31f6c156346534eee30d30458`

```dockerfile
```

-	Layers:
	-	`sha256:41a25cf6cf15b6b37e3661b3ac34bd18681863b0b85f51cec56d1d316f0397a5`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 274.9 KB (274920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b02b106246f8f724524bb0de7288d77cf1087c013b38171b388fcaf0f37f9e0`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:fb87571ab0cfe463d5b70a18f7fc659670b5c55747db3031ea04cb59192007d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87901339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc43b273027a52c8474444595317de4089d1356a37708213bb7d600ddde35e7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03fbadbe664ad3d80e3509b96250ae628b3c572ce60e514d1ab20170b9d16f`  
		Last Modified: Wed, 06 Aug 2025 20:35:39 GMT  
		Size: 76.3 MB (76329537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3100604e2ac3ab2afb5cfbb5b614bf8a221677bd8062fec6e7c8d427bd3a227`  
		Last Modified: Wed, 06 Aug 2025 20:38:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7fcb5eb3236cdaf4c847395cb3593f761279c79096d30f3e7cf35380880458`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 6.2 MB (6227728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ffbcd6b9606b2af427eeec605dcacf7cd7d3373be452b10e2bb22f249781e`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 1.7 MB (1711639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cfb2de1c2d535f5db75d479624e79d3c03d09237fa02bfe0e3cdaca96319d6`  
		Last Modified: Wed, 06 Aug 2025 21:55:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e726fabc45a470f841e6101b22886180e210ce12d35e7294ff41bda3d5fca48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 KB (310664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b2a779549901a2e89720d3b51ed603f8cad90098f71519ddbb0679b33cb68`

```dockerfile
```

-	Layers:
	-	`sha256:ccc7ede165f095820a25ffb389a248d0b37c8e904fc5ab03cd1183fef473c6fd`  
		Last Modified: Thu, 07 Aug 2025 00:52:47 GMT  
		Size: 290.5 KB (290479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f30acaaa6bd313ee7a3e5ee0cf46680343b632c7fc49a20989d0b539919b4f`  
		Last Modified: Thu, 07 Aug 2025 00:52:48 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:28695f2cfaee062b9a0ca60163b294c9aa426d62328db2bface2b85e282b88ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71589730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3295b1278233227188e8477c2827afae51d241b108713916b5ef77d03eb41a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27212710686629ba49777b5e0cccdf04e89cbe41c95c072e1c75381906d724e9`  
		Last Modified: Wed, 13 Aug 2025 22:25:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b7f018e46a54de4eea0e2dad72f4490579e3365d43915d3250d53ae7ec1890`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 6.5 MB (6502043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c049c1b926591fbe94ed04678a617c00476cf93094e56c118b4aa7d5301293`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8d48eb228a3be3c4a90c83ceb3a374f1cbf2cd8b2704f4bfb913c41a3321d`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ffc6ef944b883b81dfd10aedf994982d8dabb9a7bb31e67921f976ef1da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 KB (294963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0eadd91f1fd0a0f91b5c7391ac0c55f701c738d3b6db0537f39f79f0269f79`

```dockerfile
```

-	Layers:
	-	`sha256:518491161b596d1ff8a9f6f9f6edaf63f977efff9396b1be87c42e36e666a14a`  
		Last Modified: Mon, 25 Aug 2025 21:53:42 GMT  
		Size: 274.8 KB (274848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba037ad301b98b30c070866ceb9f8b5b99f8482275c68bd46ba5664c7b6e5e90`  
		Last Modified: Mon, 25 Aug 2025 21:53:43 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:f3fcc4c5efa8823e03e7be22f1a617cc774c603b0d8f168c048688337bdeb715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:fae8c3555cf3840ff8637313f178c0317b41466226312ea50a9d597b377a982b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2397840105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5006347b108bafda0318a83f34338f8ef74ab52d118e9d335f14fcd1870a70a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 13 Aug 2025 18:06:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:06:54 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:06:55 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:07:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:07:11 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:07:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:07:18 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:08:48 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:49 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:53 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:49:54 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:50:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:50:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9380c184b3613450235fc0562d48b7c1aeb69072e1e188efd675b317114e13`  
		Last Modified: Wed, 13 Aug 2025 18:10:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb25f9f3a6b5b2e582eb535d357af7f125a5eb0d07250886e7275753bba63b`  
		Last Modified: Wed, 13 Aug 2025 18:10:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1b81a88b515880f2398d85c50e12604a0be218b43024e6273e174b171a33`  
		Last Modified: Wed, 13 Aug 2025 18:10:31 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe632c05e48eccbb4f65220b5c6cd3d2c38482c1aff7c8a70dedef13c2d8cde3`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2281e6abc340f61cf79bb6641d015955f72d05413007591f91ca52d8fcb2020b`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6aa352166614c00f1cc5419011f1a211ffaa26ece1203ddb8a7248c0f9dee1`  
		Last Modified: Wed, 13 Aug 2025 18:10:50 GMT  
		Size: 51.2 MB (51199537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36716abacdfd69d4d84aaeb498a02c39e5df07d380dc62c6f93a43dd18bd8b36`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992bb304a4c05d05ad6f9fce52e761eaca24471880c19303b2d27362b731cf77`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 335.3 KB (335287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363744c527b6172af2deba44c4735f38293dd27bc326cde515fa1e40d983cbed`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6c232258d56f8ebfb4d22b50309c11595a9cd50805699bb1edc2ff5cac8dc2`  
		Last Modified: Wed, 13 Aug 2025 18:11:01 GMT  
		Size: 62.3 MB (62261944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318c09560fb6a640397158d02fb52738a3d51b23a8f80d35724a4ece31d4cf72`  
		Last Modified: Wed, 13 Aug 2025 18:10:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1f3385040c90c1ee57f2d21940227c7a049f3442ac13a978b145cf185a15f`  
		Last Modified: Mon, 25 Aug 2025 19:50:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe569c48af273bca5f90b236956c3823ba707807419d4b3d31037b23731ca95`  
		Last Modified: Mon, 25 Aug 2025 19:50:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244ee2fe3346da9436f4b3f9faa2052570d594821c15b4458df33433e70d4cf0`  
		Last Modified: Mon, 25 Aug 2025 19:50:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bbd758a87764c779cea8fe9429c091634198b909b6faadc2c04c4add5049a0`  
		Last Modified: Mon, 25 Aug 2025 19:50:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0dab63cb896e209cbc5b4577e607d35a3df8d9e39d5dca15bc9208710b2ec`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 2.3 MB (2334479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769960fd4bcf873320f369a1ea9ae102548c30a01938b0886cbafefe311b4353`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:c8f1420ef1f3b2c6beee3989c77169c5b35e505098aecbd8cdf91fa99cc1342e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `caddy:2-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:f0ecd5bc38691c997cfbb4eaff5bede8b9d25421e5a2fb78b50ac5fbf79f08f5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3615224351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b87c61031d564c20e4c7aadd128b369ac69af5472854d710e6709eec622c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 13 Aug 2025 18:08:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:08:27 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:08:29 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:08:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:08:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:08:50 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:10:07 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:10:07 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:56:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:56:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:56:36 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:56:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:56:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:56:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3329feb8c3f471d93f04a4afc376778f359481b9b10abd677ae7f8105b7a1982`  
		Last Modified: Wed, 13 Aug 2025 18:14:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b683ebca7e697913d8f93eeb03b85a4924fa297a5830b694441bb31e2ef2a8`  
		Last Modified: Wed, 13 Aug 2025 18:14:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a25a1b355f0af537456d6695b8cbf9c0c5582795add71831072b1f2067593`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5469c0152f4c91f8d66bd59239beec913796e4d17d8977dcf67364f6916d3aae`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9e732885c916712df386d920174e3f95dcc40377352391c6f5e8ccc9e59be5`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9ebf49453f4f127c2dffe22dcb483f4eeef5d0260fe4724472d7fc5b89ecaf`  
		Last Modified: Wed, 13 Aug 2025 18:14:25 GMT  
		Size: 51.2 MB (51223826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55bb43d7b4377e022452dadea8a547292c78952945e888b4c3a99193a0e78f`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec885b71c379ce9bdce0b6477ef6652f6b9d9f566e7e571c9863ba6adb40cede`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 351.5 KB (351496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e05cdc4ff30cbd5098771fc7b97628d410fe4d7f2afb43e7ddcd5256d51d407`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5def4f4469cc1db786df7b6975d1fc3c3bd4c534434e05e676d67edd1f0af9f`  
		Last Modified: Wed, 13 Aug 2025 18:14:22 GMT  
		Size: 62.5 MB (62477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dd29c29527d22890d7b81985987d57cceb811888344ca07659b7c0f2e94151`  
		Last Modified: Wed, 13 Aug 2025 18:14:10 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8523736186869f7a49f95f8b318bee25824ebbb010838d15db88667b969e3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb124c01828ece301417db645f6bd33502d9fa4004bbabb93d8483d9adee73fc`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc48728b561dbd7581689079fb9e459be5b1b835c2a19d3e6ad8d63472b2b7b4`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009143406fac9c3402bce23cf7487a8d83bf93fd0dacf936aa17661011450dd`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a06a632575ebdb5c471cc6aeed6865b4ed1bda3ead85aaa00ed5488712d68f3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 2.3 MB (2324141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb76a0655e886937e45d30114efbcbb8b7dcf4f622e834abea3396c37a8494`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:c2e9243204fd55beead5b9d893a8ca326f04ee4f2331dec60ad5a1d2a6992777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:2-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:3ebb7e7a0141c5f1434331567920cb6803bcb77417482786ce8e21cc1efad8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:eadadcb9a4804f2c2f6ace69b31243ddc25d10923eb9d7148361a38dfde75b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `caddy:2-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10`

```console
$ docker pull caddy@sha256:73ba793f1b2355cfefe2a7ec53ac2f2db0531bf52679deaf16df087fd35ce4ea
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
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:2.10` - linux; amd64

```console
$ docker pull caddy@sha256:e9fd95fd7cea0c3403c622c5c2457cddcaf355a5eba11048b17cb3d99a828f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20077764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a72cdc384a6f6b8c1d99f569290cee6606bec3cca68812feba43bfda45028`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634211206164759ba5e5df423465aed056f9cc799700d15b89ca49626779515f`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 346.6 KB (346592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edccfae94f0e103409f8c3283a9e19bb7585db1ed9bd9e3a0311de9e0149c1de`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e53616944a4fa3ff99b33d90d938827b7d63bdb00324b94dab3ad40ab166831`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 15.9 MB (15923955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10` - unknown; unknown

```console
$ docker pull caddy@sha256:30f634f6f0e9e39136903c3b81be8f780a4b805b66163bfc0e683fafb62a3f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 KB (314291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d132bcee2e485d83458421325b31111463d1718ccf62b18456e97d495bc57`

```dockerfile
```

-	Layers:
	-	`sha256:91d8c07f79d660b96ebece0d8847c92fd5160edb83b97e31865c2af067eeb8f0`  
		Last Modified: Mon, 25 Aug 2025 21:52:42 GMT  
		Size: 296.0 KB (296013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d27f4d928535909dc6d7b276be2d1e63901b6b627c43a4bfd594a0b899c110`  
		Last Modified: Mon, 25 Aug 2025 21:52:43 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bf497dbd5122b8bce808c55b47aa082eb84d06f77831adf2d8cc0b5f11e66438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18903449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ba67aa2169d0dbd6426eb009d3bd28de88cb829cb8453b2e628f0443f6e9f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8aa6aa6b1802d86bbc73e75216bbb426a1a8ebad8fab1ccf37a1adfdd1b779`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 346.5 KB (346493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3bd303b867cb629d2b99f58967b240f288c9b1dbf712003b3e56200692140c`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e6b087db3bea6b06b1a48ee30c1fc4db8efebe5b0e6670b418e3db437e8c38`  
		Last Modified: Mon, 25 Aug 2025 19:48:46 GMT  
		Size: 15.0 MB (15048518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10` - unknown; unknown

```console
$ docker pull caddy@sha256:286477e027ad1c6350295044f9c520fa196eb08183d4939ae7ed071fc7320c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16e2d2b0cb8b273b15b42a3b1d12c77c076d757e265061f5e61b31763a6a52`

```dockerfile
```

-	Layers:
	-	`sha256:29f2ff0c73ef6349295d38ad6646decc7e0677799f04a1a1ce633e18c85a4327`  
		Last Modified: Mon, 25 Aug 2025 21:52:47 GMT  
		Size: 18.2 KB (18197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d5af7163676df0baffb41f5bce9c4f0775a69609bc2384b101ff4ba749f0050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18601748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e276120a8a2d3df3a422b6d9a2b02c16b9f92c6b28ac595c34fcc06410127c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979c078f866daa2820e22fa7f8a9cc664e49f7d538de1341a2c2c9a60489560`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 343.2 KB (343205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeca689d2f3de3a319b91d9ddb84048521f017d394555aa2ab895ef9cdb98e2`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711aca2485d7f9dfbfccd9cf2a11a6db8015c154383632363d1ac44b755cb55`  
		Last Modified: Mon, 25 Aug 2025 19:48:47 GMT  
		Size: 15.0 MB (15031978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10` - unknown; unknown

```console
$ docker pull caddy@sha256:8049ae7cb8cf21da392232342dd2c386e8e79bb9a7093ef47dec2cd1e4d8d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 KB (314493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b289ec4bc1157ad5848221ba42af4a065fd5af769065351ada6548da41f5c1`

```dockerfile
```

-	Layers:
	-	`sha256:7653918e29fb0de220bc0644efa15394bed69ae8f40081cd705aa96205888b4c`  
		Last Modified: Mon, 25 Aug 2025 21:52:51 GMT  
		Size: 296.1 KB (296081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fb47d806abc1bee7ac987c99961bb2c58274d6cbc04b58ea4c3c026b94f2ce`  
		Last Modified: Mon, 25 Aug 2025 21:52:52 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:4c3be81b7ee70190ce5291230e5a5d4dd8ea998c44cfb5fcc4680a60ea6c5621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19013546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b37c5f2910ca9daf3b5cd9f63bb06d782d2062d4daceced81673d49fe4a1c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ebf372d05e77b4bdc3cea55c048537aaac7759aa0079ed9944004ac30c980c`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 357.7 KB (357727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f163ee242da1ec76c0ab875c407ba39c49aa3eab955a46b9ea14d94a86c4d48e`  
		Last Modified: Mon, 25 Aug 2025 19:48:51 GMT  
		Size: 7.5 KB (7492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225b3b694c911c2a8b8814871c8353f7b7686cc9ea3fc2b02dba2f45803dd75`  
		Last Modified: Mon, 25 Aug 2025 19:48:55 GMT  
		Size: 14.5 MB (14517545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10` - unknown; unknown

```console
$ docker pull caddy@sha256:a657dd5aa41ae2796a14d32f91e630f0efcefa03e3261ac63d39793887cea22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 KB (314576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469b3383a6f868625bafb61aa5dd86ccd26899761e2bdb5fafafbc7e250ef24b`

```dockerfile
```

-	Layers:
	-	`sha256:4f49301002ed8e6230d3ea527498b3328f01453f1b0e12e3bbcb7ce771cca15b`  
		Last Modified: Mon, 25 Aug 2025 21:52:55 GMT  
		Size: 296.1 KB (296117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fbb94c8995329e1c4b3235561ee976502480bebaab9183f926bf2529444c9d`  
		Last Modified: Mon, 25 Aug 2025 21:52:56 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10` - linux; ppc64le

```console
$ docker pull caddy@sha256:67112be943616a31dfbf0c815ed5325bf71a9d8c6cfe49a1935b244bd3b109e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18591170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f3d87694b9256e003a6824820cec8dfc82ad339b7d3bc41671c4996663a0a3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe739855dbbb9a1403a242cd984b1b9b4439925fb4fcedc9d3d6ade9baf3dd5`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 360.6 KB (360616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab33549ec0ff70ed9ba5ea43079d739e8d6fe698b0578958a9e2675602d1f6`  
		Last Modified: Mon, 25 Aug 2025 19:49:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6276663ba0f6c95bde9cd5440dc7ec15f6e100f8283c704efd10d02181f066dc`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 14.5 MB (14495915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10` - unknown; unknown

```console
$ docker pull caddy@sha256:54c1de5978b47c2325c8f34e5589b9e4befd54792776c52701944ded623d9922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 KB (312470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d525e05914ec596f61ab5f038622c17b75382bd36e15638e19d2ef0b54ab4`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2fa5edceb1da7dbf0f53e0b3b6e55ebdebce9112144575d69508ba7ea1f29`  
		Last Modified: Mon, 25 Aug 2025 21:53:01 GMT  
		Size: 294.1 KB (294120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2488d35b692ff2f9eeccf6177b581e0b4012821bcd0e7079a6755296fdc31433`  
		Last Modified: Mon, 25 Aug 2025 21:53:02 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10` - linux; riscv64

```console
$ docker pull caddy@sha256:fab4c562bd13d4fe11cc47963461b4b2f197e38afa3be8a61b698b6319238f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17956644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c209b028cc287828f645bdd0dc227ee3dbc69f503f5bf1a4ad3a944252b78b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29116abe2cb7489bfe0d514003d7c4822eaf03d2b44e5f1c10c878a603eceb13`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 348.3 KB (348289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ceaafe79989c43b373a7e7780390f12740f15ad106a2c987605998f180cea`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 7.5 KB (7498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9baf51ef7381285244300ec8288209b2b0dc82267a2c3547eb0644ce4c7948`  
		Last Modified: Fri, 18 Jul 2025 07:36:44 GMT  
		Size: 14.3 MB (14251735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10` - unknown; unknown

```console
$ docker pull caddy@sha256:608fabfae5954b1485e44928f39c3844fbdc7de236202d87c4380838c748a018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 KB (303605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff983ccc8020f39b317500f82d9596ad6b4299338ecb828eaa0685950b57aa46`

```dockerfile
```

-	Layers:
	-	`sha256:090b4908e38667b8110e66242c7d88a6c27ba9f8dc2ebc126e04430fcaff531c`  
		Last Modified: Fri, 18 Jul 2025 09:52:30 GMT  
		Size: 285.3 KB (285255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e87f231dbdaabee2c8a7c7375c70ff7387e5d2387ed1a26033f1a9b77c0e427`  
		Last Modified: Fri, 18 Jul 2025 09:52:31 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10` - linux; s390x

```console
$ docker pull caddy@sha256:df924d28949f8a3be699c88ab40eb6b5ca37234e6af5431cb6a1cca63e58a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19362618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85040edfc178cf9c5de8611792e65c67f07629a5c76b7089bf0828d075163a0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff98415fc23c99d5ff9b731b3ed1f5f263fca7f05ddbb51c47d7d8b6df1f89e8`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 353.5 KB (353456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e6340a3b7a63c6c76d521ec65f90ba0718a26fb02520f02216f158300c89e`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd56c657dc325cdf0a5d0c300a1380b0fe6abd98dcee92bcf38b02d14d579062`  
		Last Modified: Mon, 25 Aug 2025 19:51:46 GMT  
		Size: 15.4 MB (15356663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10` - unknown; unknown

```console
$ docker pull caddy@sha256:ce406a252aedd52a38cc6938d993637d83f2aedbe10e9eb385f4b60a12418812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 KB (312340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190d69bf6d55a424c64ecfe71fedbf83d368d2191338ab24083d5426fa60e861`

```dockerfile
```

-	Layers:
	-	`sha256:ea8886b3a4622ffdcc38a8a441716fbb95afc7feb55738ebaae75b137a193925`  
		Last Modified: Mon, 25 Aug 2025 21:53:08 GMT  
		Size: 294.1 KB (294062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5011fab561f7f812f810ba45504c8489c7a5e0383d88863c43b47478a136a21a`  
		Last Modified: Mon, 25 Aug 2025 21:53:09 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.10` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10-alpine`

```console
$ docker pull caddy@sha256:64642fe1e2319c999d20aa489a73e261b5b4ae4fab29385b61e5221287af5c42
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

### `caddy:2.10-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:e9fd95fd7cea0c3403c622c5c2457cddcaf355a5eba11048b17cb3d99a828f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20077764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a72cdc384a6f6b8c1d99f569290cee6606bec3cca68812feba43bfda45028`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634211206164759ba5e5df423465aed056f9cc799700d15b89ca49626779515f`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 346.6 KB (346592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edccfae94f0e103409f8c3283a9e19bb7585db1ed9bd9e3a0311de9e0149c1de`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e53616944a4fa3ff99b33d90d938827b7d63bdb00324b94dab3ad40ab166831`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 15.9 MB (15923955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:30f634f6f0e9e39136903c3b81be8f780a4b805b66163bfc0e683fafb62a3f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 KB (314291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d132bcee2e485d83458421325b31111463d1718ccf62b18456e97d495bc57`

```dockerfile
```

-	Layers:
	-	`sha256:91d8c07f79d660b96ebece0d8847c92fd5160edb83b97e31865c2af067eeb8f0`  
		Last Modified: Mon, 25 Aug 2025 21:52:42 GMT  
		Size: 296.0 KB (296013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d27f4d928535909dc6d7b276be2d1e63901b6b627c43a4bfd594a0b899c110`  
		Last Modified: Mon, 25 Aug 2025 21:52:43 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bf497dbd5122b8bce808c55b47aa082eb84d06f77831adf2d8cc0b5f11e66438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18903449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ba67aa2169d0dbd6426eb009d3bd28de88cb829cb8453b2e628f0443f6e9f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8aa6aa6b1802d86bbc73e75216bbb426a1a8ebad8fab1ccf37a1adfdd1b779`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 346.5 KB (346493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3bd303b867cb629d2b99f58967b240f288c9b1dbf712003b3e56200692140c`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e6b087db3bea6b06b1a48ee30c1fc4db8efebe5b0e6670b418e3db437e8c38`  
		Last Modified: Mon, 25 Aug 2025 19:48:46 GMT  
		Size: 15.0 MB (15048518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:286477e027ad1c6350295044f9c520fa196eb08183d4939ae7ed071fc7320c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16e2d2b0cb8b273b15b42a3b1d12c77c076d757e265061f5e61b31763a6a52`

```dockerfile
```

-	Layers:
	-	`sha256:29f2ff0c73ef6349295d38ad6646decc7e0677799f04a1a1ce633e18c85a4327`  
		Last Modified: Mon, 25 Aug 2025 21:52:47 GMT  
		Size: 18.2 KB (18197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d5af7163676df0baffb41f5bce9c4f0775a69609bc2384b101ff4ba749f0050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18601748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e276120a8a2d3df3a422b6d9a2b02c16b9f92c6b28ac595c34fcc06410127c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979c078f866daa2820e22fa7f8a9cc664e49f7d538de1341a2c2c9a60489560`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 343.2 KB (343205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeca689d2f3de3a319b91d9ddb84048521f017d394555aa2ab895ef9cdb98e2`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711aca2485d7f9dfbfccd9cf2a11a6db8015c154383632363d1ac44b755cb55`  
		Last Modified: Mon, 25 Aug 2025 19:48:47 GMT  
		Size: 15.0 MB (15031978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:8049ae7cb8cf21da392232342dd2c386e8e79bb9a7093ef47dec2cd1e4d8d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 KB (314493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b289ec4bc1157ad5848221ba42af4a065fd5af769065351ada6548da41f5c1`

```dockerfile
```

-	Layers:
	-	`sha256:7653918e29fb0de220bc0644efa15394bed69ae8f40081cd705aa96205888b4c`  
		Last Modified: Mon, 25 Aug 2025 21:52:51 GMT  
		Size: 296.1 KB (296081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fb47d806abc1bee7ac987c99961bb2c58274d6cbc04b58ea4c3c026b94f2ce`  
		Last Modified: Mon, 25 Aug 2025 21:52:52 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:4c3be81b7ee70190ce5291230e5a5d4dd8ea998c44cfb5fcc4680a60ea6c5621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19013546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b37c5f2910ca9daf3b5cd9f63bb06d782d2062d4daceced81673d49fe4a1c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ebf372d05e77b4bdc3cea55c048537aaac7759aa0079ed9944004ac30c980c`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 357.7 KB (357727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f163ee242da1ec76c0ab875c407ba39c49aa3eab955a46b9ea14d94a86c4d48e`  
		Last Modified: Mon, 25 Aug 2025 19:48:51 GMT  
		Size: 7.5 KB (7492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225b3b694c911c2a8b8814871c8353f7b7686cc9ea3fc2b02dba2f45803dd75`  
		Last Modified: Mon, 25 Aug 2025 19:48:55 GMT  
		Size: 14.5 MB (14517545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a657dd5aa41ae2796a14d32f91e630f0efcefa03e3261ac63d39793887cea22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 KB (314576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469b3383a6f868625bafb61aa5dd86ccd26899761e2bdb5fafafbc7e250ef24b`

```dockerfile
```

-	Layers:
	-	`sha256:4f49301002ed8e6230d3ea527498b3328f01453f1b0e12e3bbcb7ce771cca15b`  
		Last Modified: Mon, 25 Aug 2025 21:52:55 GMT  
		Size: 296.1 KB (296117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fbb94c8995329e1c4b3235561ee976502480bebaab9183f926bf2529444c9d`  
		Last Modified: Mon, 25 Aug 2025 21:52:56 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:67112be943616a31dfbf0c815ed5325bf71a9d8c6cfe49a1935b244bd3b109e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18591170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f3d87694b9256e003a6824820cec8dfc82ad339b7d3bc41671c4996663a0a3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe739855dbbb9a1403a242cd984b1b9b4439925fb4fcedc9d3d6ade9baf3dd5`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 360.6 KB (360616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab33549ec0ff70ed9ba5ea43079d739e8d6fe698b0578958a9e2675602d1f6`  
		Last Modified: Mon, 25 Aug 2025 19:49:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6276663ba0f6c95bde9cd5440dc7ec15f6e100f8283c704efd10d02181f066dc`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 14.5 MB (14495915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:54c1de5978b47c2325c8f34e5589b9e4befd54792776c52701944ded623d9922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 KB (312470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d525e05914ec596f61ab5f038622c17b75382bd36e15638e19d2ef0b54ab4`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2fa5edceb1da7dbf0f53e0b3b6e55ebdebce9112144575d69508ba7ea1f29`  
		Last Modified: Mon, 25 Aug 2025 21:53:01 GMT  
		Size: 294.1 KB (294120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2488d35b692ff2f9eeccf6177b581e0b4012821bcd0e7079a6755296fdc31433`  
		Last Modified: Mon, 25 Aug 2025 21:53:02 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:fab4c562bd13d4fe11cc47963461b4b2f197e38afa3be8a61b698b6319238f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17956644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c209b028cc287828f645bdd0dc227ee3dbc69f503f5bf1a4ad3a944252b78b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29116abe2cb7489bfe0d514003d7c4822eaf03d2b44e5f1c10c878a603eceb13`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 348.3 KB (348289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ceaafe79989c43b373a7e7780390f12740f15ad106a2c987605998f180cea`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 7.5 KB (7498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9baf51ef7381285244300ec8288209b2b0dc82267a2c3547eb0644ce4c7948`  
		Last Modified: Fri, 18 Jul 2025 07:36:44 GMT  
		Size: 14.3 MB (14251735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:608fabfae5954b1485e44928f39c3844fbdc7de236202d87c4380838c748a018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 KB (303605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff983ccc8020f39b317500f82d9596ad6b4299338ecb828eaa0685950b57aa46`

```dockerfile
```

-	Layers:
	-	`sha256:090b4908e38667b8110e66242c7d88a6c27ba9f8dc2ebc126e04430fcaff531c`  
		Last Modified: Fri, 18 Jul 2025 09:52:30 GMT  
		Size: 285.3 KB (285255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e87f231dbdaabee2c8a7c7375c70ff7387e5d2387ed1a26033f1a9b77c0e427`  
		Last Modified: Fri, 18 Jul 2025 09:52:31 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:df924d28949f8a3be699c88ab40eb6b5ca37234e6af5431cb6a1cca63e58a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19362618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85040edfc178cf9c5de8611792e65c67f07629a5c76b7089bf0828d075163a0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff98415fc23c99d5ff9b731b3ed1f5f263fca7f05ddbb51c47d7d8b6df1f89e8`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 353.5 KB (353456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e6340a3b7a63c6c76d521ec65f90ba0718a26fb02520f02216f158300c89e`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd56c657dc325cdf0a5d0c300a1380b0fe6abd98dcee92bcf38b02d14d579062`  
		Last Modified: Mon, 25 Aug 2025 19:51:46 GMT  
		Size: 15.4 MB (15356663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ce406a252aedd52a38cc6938d993637d83f2aedbe10e9eb385f4b60a12418812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 KB (312340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190d69bf6d55a424c64ecfe71fedbf83d368d2191338ab24083d5426fa60e861`

```dockerfile
```

-	Layers:
	-	`sha256:ea8886b3a4622ffdcc38a8a441716fbb95afc7feb55738ebaae75b137a193925`  
		Last Modified: Mon, 25 Aug 2025 21:53:08 GMT  
		Size: 294.1 KB (294062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5011fab561f7f812f810ba45504c8489c7a5e0383d88863c43b47478a136a21a`  
		Last Modified: Mon, 25 Aug 2025 21:53:09 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.10-builder`

```console
$ docker pull caddy@sha256:38708d13dba3aafb83ed97d8b1f9ed00823a6d0eb63de314945a55ada80db2d8
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
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:2.10-builder` - linux; amd64

```console
$ docker pull caddy@sha256:baa56c9394d7025fb7e344f5a1d52c7d0ae2a428a6d8e4d7acf85480477cf819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72186376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0205b23d29755cb0085885d9fa3ac1ea66ce75020051c0185f423ea947bc24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d4ca09441bdb9129d5708d2aa8802e233b2d11d1797317158c4095e9df8fc`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 282.4 KB (282437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18414ed0f6669fd1d6e137922f2a57e37aaf0a63ae6968c499fe69b17d148d14`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36dd3b7005cdf211c5d6cd7f47820b1ffa15134a87c84b500f754613863411`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.2 MB (6211320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc4a072890c37012160bb87d003d188e34244b09f60d9a7e33a521175aa4914`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.8 MB (1846494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45676fbd1b151c4eb76c6df8afe515dd1b8001736b55aba9841182177b17`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:f5d337972eff4ad3e0c109de0443e6695887aae29e94c1df6e6189ef17e777df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3035b7074d5121642859847a37b0e722a8cb9137408b7356cf5e5a79d0a6760c`

```dockerfile
```

-	Layers:
	-	`sha256:f41e395e3e21569a16f8d91a8825c71ee9146373ca8d37c13d6e6de553f55627`  
		Last Modified: Mon, 25 Aug 2025 21:53:16 GMT  
		Size: 276.8 KB (276799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a6e841ccf0c2ac296066a2cd3354ab00dcc598ae922e619237f17aebd1bb82`  
		Last Modified: Mon, 25 Aug 2025 21:53:17 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e1edbceed451136633244ae771982f55dd7d7218a4ffc50369af9eefbb5266a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70630913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8be52c140ce9073b5e99046435e6d10435d169d31239bff87fc88de3e317a56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b30dde5a6a0bd25a99ef148aafdaf794991c98c7b0798149f6d4e21ebc6ccd`  
		Last Modified: Wed, 13 Aug 2025 19:12:26 GMT  
		Size: 59.0 MB (58976836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63714916874ab7e10bdc757c1f8a9e57104a40067c294f970c9d8ff49423866`  
		Last Modified: Wed, 13 Aug 2025 18:04:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96b63bb94735bf5a233756bdc50074d4de4f13340afa4a5b52a444075d8471d`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 6.1 MB (6124248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cae36cb0796b19b218d007f943c4a58a98847586c215d0b9182edb25f4b08`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d14e3b2c944638da45ebffd7d320249acf6ca96e796a9c2aaee17c71e23a4d`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:b2b71368948bedcdbe1fe1b49cbffe11bca901b908dde0561b73953dad703bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b200e21ab8337407084c2f915782c003a30ed1b357ddf279a1faf52f479fd277`

```dockerfile
```

-	Layers:
	-	`sha256:995e27d2c9f18e3d1278c03b04caf0d92d8524cca3c1f98d0b486e78c8fdec72`  
		Last Modified: Mon, 25 Aug 2025 21:53:21 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7570894dd8642571d29a3f9a172447dc68c92466e954fbfe509dd4c1002c62d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69821208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303120483e85eaa18d5623ff884d6ba6bc5329cf64792dafc7122ec47e98f1b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0ef49cd2af3f26990fbdb01d76c5d72224144a9082720b843066d506cd46c9`  
		Last Modified: Thu, 14 Aug 2025 04:30:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee18d4be11a0ac51fa3627c2b017b3aef767f70a39ea0d73d6de35cd618a71f`  
		Last Modified: Mon, 25 Aug 2025 19:49:07 GMT  
		Size: 5.6 MB (5603426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6551895b1ab029d74729175b98ce97b83c07b3112d073fc90b8fe101237e63`  
		Last Modified: Mon, 25 Aug 2025 19:49:09 GMT  
		Size: 1.7 MB (1738756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b87d17c36733a93bfd68173426cc2ef130e2195c9c450df58a04dc2c5fab0f`  
		Last Modified: Mon, 25 Aug 2025 19:49:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:55c648a2b1f1e4d6d07485531af3a8734047d606ae8f624a5e55a14a84c3badd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 KB (300079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cdb0bd297a9f9a841359ac15ef57a33be96fe2dae32e84f34341e6fbcf5b69`

```dockerfile
```

-	Layers:
	-	`sha256:8823ee0afb3d9696b6ca5b09a159c39bf7a8fe6690d1fb9851fe5f74584f325f`  
		Last Modified: Mon, 25 Aug 2025 21:53:25 GMT  
		Size: 279.8 KB (279843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486c238d647f7578251e57dd34ce120fb465b25780a1e60cf69ec3bd36b22be4`  
		Last Modified: Mon, 25 Aug 2025 21:53:26 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:32fa6d72e61b79987dd65c0d108e5078c0e0dc93af0460612778e63182c2076c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69951490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9745840960c0e962feb8ce93ade81f3d2d7c4014b1aa7675e1ae02d0a7aff9ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1a427e917c48b164eae3ec3692b4741f5de528261925d2e5efc62a43e5bfc4`  
		Last Modified: Mon, 28 Jul 2025 20:42:19 GMT  
		Size: 284.7 KB (284709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b50d3516e3fbf4aca43b9416e7dd8914c2623a08d12eeb55d98d72b864d50c`  
		Last Modified: Wed, 13 Aug 2025 21:40:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b905d71c6a895e4f8e02255340a28c48f2a71d4744873257004c40c0d2aa00`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.3 MB (6263485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f8b26f147c3aad964c448d6607cf74ae215e3ac1c4cbba753fa3e968275e88`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3231a1494a810504f8b0f942889fffa994e046e8e88d228e3a5088783ce72`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:2afba1033f0a6e1546bfc4ba308b2a11e83940382cb23e26214953132de73502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e5578a03d1c8f2a6f8ffcbe41b2176db7f2e9fe34e3740615730082fda76c7`

```dockerfile
```

-	Layers:
	-	`sha256:748645f9a413db4552bbf182353615a0b12bcd436e3be618d281b3d593030ede`  
		Last Modified: Mon, 25 Aug 2025 21:53:30 GMT  
		Size: 276.9 KB (276903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93bc5bdadeab69d30a633aee167e91118e46d1789c6f0ffd8919e02d2abce29`  
		Last Modified: Mon, 25 Aug 2025 21:53:31 GMT  
		Size: 20.3 KB (20279 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:af183020c3351759ff8b8f4bafc2723eeff7c818144664e3694cc95a57ce5b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70304708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562175980913c7c3795d4d816c57841adf59a5bc12f44a1cd0eeb9e6e600f14a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe3e6d4a1713a75edf1789d38233b2e8d48f54cebae5e9d0789eb1af52023b`  
		Last Modified: Mon, 28 Jul 2025 20:30:54 GMT  
		Size: 285.1 KB (285114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269abe529e66aa5bca30329a5b15eb3b1dc68dbfb72494192487eabaf2c75ea7`  
		Last Modified: Wed, 13 Aug 2025 22:24:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b70f44dd4f808419f6fd44bceba6d166aca8e19f4cc6cbd8b36f33239207db`  
		Last Modified: Mon, 25 Aug 2025 19:50:03 GMT  
		Size: 6.6 MB (6550799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d7bd24bb9deffe0ca1b77e298776a06b4a558884001c7bb47966dadc97ca43`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd6fde2d426e5936d85b957d51eeee4fe29a27e410fcafc97d0874ffda5b0a7`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0aebec967107348a51c2631c5a8092b2a9ddf49e4a53aa5e56b903b7db8da90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 KB (295105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5483635ad7faac1a9e8b342df273f4ba0a4bdbe31f6c156346534eee30d30458`

```dockerfile
```

-	Layers:
	-	`sha256:41a25cf6cf15b6b37e3661b3ac34bd18681863b0b85f51cec56d1d316f0397a5`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 274.9 KB (274920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b02b106246f8f724524bb0de7288d77cf1087c013b38171b388fcaf0f37f9e0`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:fb87571ab0cfe463d5b70a18f7fc659670b5c55747db3031ea04cb59192007d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87901339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc43b273027a52c8474444595317de4089d1356a37708213bb7d600ddde35e7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03fbadbe664ad3d80e3509b96250ae628b3c572ce60e514d1ab20170b9d16f`  
		Last Modified: Wed, 06 Aug 2025 20:35:39 GMT  
		Size: 76.3 MB (76329537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3100604e2ac3ab2afb5cfbb5b614bf8a221677bd8062fec6e7c8d427bd3a227`  
		Last Modified: Wed, 06 Aug 2025 20:38:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7fcb5eb3236cdaf4c847395cb3593f761279c79096d30f3e7cf35380880458`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 6.2 MB (6227728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ffbcd6b9606b2af427eeec605dcacf7cd7d3373be452b10e2bb22f249781e`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 1.7 MB (1711639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cfb2de1c2d535f5db75d479624e79d3c03d09237fa02bfe0e3cdaca96319d6`  
		Last Modified: Wed, 06 Aug 2025 21:55:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e726fabc45a470f841e6101b22886180e210ce12d35e7294ff41bda3d5fca48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 KB (310664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b2a779549901a2e89720d3b51ed603f8cad90098f71519ddbb0679b33cb68`

```dockerfile
```

-	Layers:
	-	`sha256:ccc7ede165f095820a25ffb389a248d0b37c8e904fc5ab03cd1183fef473c6fd`  
		Last Modified: Thu, 07 Aug 2025 00:52:47 GMT  
		Size: 290.5 KB (290479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f30acaaa6bd313ee7a3e5ee0cf46680343b632c7fc49a20989d0b539919b4f`  
		Last Modified: Thu, 07 Aug 2025 00:52:48 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder` - linux; s390x

```console
$ docker pull caddy@sha256:28695f2cfaee062b9a0ca60163b294c9aa426d62328db2bface2b85e282b88ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71589730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3295b1278233227188e8477c2827afae51d241b108713916b5ef77d03eb41a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27212710686629ba49777b5e0cccdf04e89cbe41c95c072e1c75381906d724e9`  
		Last Modified: Wed, 13 Aug 2025 22:25:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b7f018e46a54de4eea0e2dad72f4490579e3365d43915d3250d53ae7ec1890`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 6.5 MB (6502043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c049c1b926591fbe94ed04678a617c00476cf93094e56c118b4aa7d5301293`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8d48eb228a3be3c4a90c83ceb3a374f1cbf2cd8b2704f4bfb913c41a3321d`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ffc6ef944b883b81dfd10aedf994982d8dabb9a7bb31e67921f976ef1da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 KB (294963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0eadd91f1fd0a0f91b5c7391ac0c55f701c738d3b6db0537f39f79f0269f79`

```dockerfile
```

-	Layers:
	-	`sha256:518491161b596d1ff8a9f6f9f6edaf63f977efff9396b1be87c42e36e666a14a`  
		Last Modified: Mon, 25 Aug 2025 21:53:42 GMT  
		Size: 274.8 KB (274848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba037ad301b98b30c070866ceb9f8b5b99f8482275c68bd46ba5664c7b6e5e90`  
		Last Modified: Mon, 25 Aug 2025 21:53:43 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:f0ecd5bc38691c997cfbb4eaff5bede8b9d25421e5a2fb78b50ac5fbf79f08f5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3615224351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b87c61031d564c20e4c7aadd128b369ac69af5472854d710e6709eec622c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 13 Aug 2025 18:08:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:08:27 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:08:29 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:08:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:08:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:08:50 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:10:07 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:10:07 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:56:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:56:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:56:36 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:56:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:56:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:56:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3329feb8c3f471d93f04a4afc376778f359481b9b10abd677ae7f8105b7a1982`  
		Last Modified: Wed, 13 Aug 2025 18:14:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b683ebca7e697913d8f93eeb03b85a4924fa297a5830b694441bb31e2ef2a8`  
		Last Modified: Wed, 13 Aug 2025 18:14:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a25a1b355f0af537456d6695b8cbf9c0c5582795add71831072b1f2067593`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5469c0152f4c91f8d66bd59239beec913796e4d17d8977dcf67364f6916d3aae`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9e732885c916712df386d920174e3f95dcc40377352391c6f5e8ccc9e59be5`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9ebf49453f4f127c2dffe22dcb483f4eeef5d0260fe4724472d7fc5b89ecaf`  
		Last Modified: Wed, 13 Aug 2025 18:14:25 GMT  
		Size: 51.2 MB (51223826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55bb43d7b4377e022452dadea8a547292c78952945e888b4c3a99193a0e78f`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec885b71c379ce9bdce0b6477ef6652f6b9d9f566e7e571c9863ba6adb40cede`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 351.5 KB (351496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e05cdc4ff30cbd5098771fc7b97628d410fe4d7f2afb43e7ddcd5256d51d407`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5def4f4469cc1db786df7b6975d1fc3c3bd4c534434e05e676d67edd1f0af9f`  
		Last Modified: Wed, 13 Aug 2025 18:14:22 GMT  
		Size: 62.5 MB (62477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dd29c29527d22890d7b81985987d57cceb811888344ca07659b7c0f2e94151`  
		Last Modified: Wed, 13 Aug 2025 18:14:10 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8523736186869f7a49f95f8b318bee25824ebbb010838d15db88667b969e3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb124c01828ece301417db645f6bd33502d9fa4004bbabb93d8483d9adee73fc`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc48728b561dbd7581689079fb9e459be5b1b835c2a19d3e6ad8d63472b2b7b4`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009143406fac9c3402bce23cf7487a8d83bf93fd0dacf936aa17661011450dd`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a06a632575ebdb5c471cc6aeed6865b4ed1bda3ead85aaa00ed5488712d68f3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 2.3 MB (2324141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb76a0655e886937e45d30114efbcbb8b7dcf4f622e834abea3396c37a8494`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.10-builder` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:fae8c3555cf3840ff8637313f178c0317b41466226312ea50a9d597b377a982b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2397840105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5006347b108bafda0318a83f34338f8ef74ab52d118e9d335f14fcd1870a70a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 13 Aug 2025 18:06:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:06:54 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:06:55 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:07:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:07:11 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:07:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:07:18 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:08:48 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:49 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:53 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:49:54 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:50:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:50:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9380c184b3613450235fc0562d48b7c1aeb69072e1e188efd675b317114e13`  
		Last Modified: Wed, 13 Aug 2025 18:10:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb25f9f3a6b5b2e582eb535d357af7f125a5eb0d07250886e7275753bba63b`  
		Last Modified: Wed, 13 Aug 2025 18:10:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1b81a88b515880f2398d85c50e12604a0be218b43024e6273e174b171a33`  
		Last Modified: Wed, 13 Aug 2025 18:10:31 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe632c05e48eccbb4f65220b5c6cd3d2c38482c1aff7c8a70dedef13c2d8cde3`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2281e6abc340f61cf79bb6641d015955f72d05413007591f91ca52d8fcb2020b`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6aa352166614c00f1cc5419011f1a211ffaa26ece1203ddb8a7248c0f9dee1`  
		Last Modified: Wed, 13 Aug 2025 18:10:50 GMT  
		Size: 51.2 MB (51199537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36716abacdfd69d4d84aaeb498a02c39e5df07d380dc62c6f93a43dd18bd8b36`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992bb304a4c05d05ad6f9fce52e761eaca24471880c19303b2d27362b731cf77`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 335.3 KB (335287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363744c527b6172af2deba44c4735f38293dd27bc326cde515fa1e40d983cbed`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6c232258d56f8ebfb4d22b50309c11595a9cd50805699bb1edc2ff5cac8dc2`  
		Last Modified: Wed, 13 Aug 2025 18:11:01 GMT  
		Size: 62.3 MB (62261944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318c09560fb6a640397158d02fb52738a3d51b23a8f80d35724a4ece31d4cf72`  
		Last Modified: Wed, 13 Aug 2025 18:10:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1f3385040c90c1ee57f2d21940227c7a049f3442ac13a978b145cf185a15f`  
		Last Modified: Mon, 25 Aug 2025 19:50:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe569c48af273bca5f90b236956c3823ba707807419d4b3d31037b23731ca95`  
		Last Modified: Mon, 25 Aug 2025 19:50:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244ee2fe3346da9436f4b3f9faa2052570d594821c15b4458df33433e70d4cf0`  
		Last Modified: Mon, 25 Aug 2025 19:50:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bbd758a87764c779cea8fe9429c091634198b909b6faadc2c04c4add5049a0`  
		Last Modified: Mon, 25 Aug 2025 19:50:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0dab63cb896e209cbc5b4577e607d35a3df8d9e39d5dca15bc9208710b2ec`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 2.3 MB (2334479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769960fd4bcf873320f369a1ea9ae102548c30a01938b0886cbafefe311b4353`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10-builder-alpine`

```console
$ docker pull caddy@sha256:2cf9b153f9f65bc7dbaef420968aee70bc0c9e570b2c217777014e1c329de416
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

### `caddy:2.10-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:baa56c9394d7025fb7e344f5a1d52c7d0ae2a428a6d8e4d7acf85480477cf819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72186376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0205b23d29755cb0085885d9fa3ac1ea66ce75020051c0185f423ea947bc24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d4ca09441bdb9129d5708d2aa8802e233b2d11d1797317158c4095e9df8fc`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 282.4 KB (282437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18414ed0f6669fd1d6e137922f2a57e37aaf0a63ae6968c499fe69b17d148d14`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36dd3b7005cdf211c5d6cd7f47820b1ffa15134a87c84b500f754613863411`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.2 MB (6211320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc4a072890c37012160bb87d003d188e34244b09f60d9a7e33a521175aa4914`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.8 MB (1846494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45676fbd1b151c4eb76c6df8afe515dd1b8001736b55aba9841182177b17`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f5d337972eff4ad3e0c109de0443e6695887aae29e94c1df6e6189ef17e777df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3035b7074d5121642859847a37b0e722a8cb9137408b7356cf5e5a79d0a6760c`

```dockerfile
```

-	Layers:
	-	`sha256:f41e395e3e21569a16f8d91a8825c71ee9146373ca8d37c13d6e6de553f55627`  
		Last Modified: Mon, 25 Aug 2025 21:53:16 GMT  
		Size: 276.8 KB (276799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a6e841ccf0c2ac296066a2cd3354ab00dcc598ae922e619237f17aebd1bb82`  
		Last Modified: Mon, 25 Aug 2025 21:53:17 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e1edbceed451136633244ae771982f55dd7d7218a4ffc50369af9eefbb5266a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70630913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8be52c140ce9073b5e99046435e6d10435d169d31239bff87fc88de3e317a56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b30dde5a6a0bd25a99ef148aafdaf794991c98c7b0798149f6d4e21ebc6ccd`  
		Last Modified: Wed, 13 Aug 2025 19:12:26 GMT  
		Size: 59.0 MB (58976836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63714916874ab7e10bdc757c1f8a9e57104a40067c294f970c9d8ff49423866`  
		Last Modified: Wed, 13 Aug 2025 18:04:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96b63bb94735bf5a233756bdc50074d4de4f13340afa4a5b52a444075d8471d`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 6.1 MB (6124248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cae36cb0796b19b218d007f943c4a58a98847586c215d0b9182edb25f4b08`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d14e3b2c944638da45ebffd7d320249acf6ca96e796a9c2aaee17c71e23a4d`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b2b71368948bedcdbe1fe1b49cbffe11bca901b908dde0561b73953dad703bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b200e21ab8337407084c2f915782c003a30ed1b357ddf279a1faf52f479fd277`

```dockerfile
```

-	Layers:
	-	`sha256:995e27d2c9f18e3d1278c03b04caf0d92d8524cca3c1f98d0b486e78c8fdec72`  
		Last Modified: Mon, 25 Aug 2025 21:53:21 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7570894dd8642571d29a3f9a172447dc68c92466e954fbfe509dd4c1002c62d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69821208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303120483e85eaa18d5623ff884d6ba6bc5329cf64792dafc7122ec47e98f1b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0ef49cd2af3f26990fbdb01d76c5d72224144a9082720b843066d506cd46c9`  
		Last Modified: Thu, 14 Aug 2025 04:30:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee18d4be11a0ac51fa3627c2b017b3aef767f70a39ea0d73d6de35cd618a71f`  
		Last Modified: Mon, 25 Aug 2025 19:49:07 GMT  
		Size: 5.6 MB (5603426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6551895b1ab029d74729175b98ce97b83c07b3112d073fc90b8fe101237e63`  
		Last Modified: Mon, 25 Aug 2025 19:49:09 GMT  
		Size: 1.7 MB (1738756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b87d17c36733a93bfd68173426cc2ef130e2195c9c450df58a04dc2c5fab0f`  
		Last Modified: Mon, 25 Aug 2025 19:49:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:55c648a2b1f1e4d6d07485531af3a8734047d606ae8f624a5e55a14a84c3badd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 KB (300079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cdb0bd297a9f9a841359ac15ef57a33be96fe2dae32e84f34341e6fbcf5b69`

```dockerfile
```

-	Layers:
	-	`sha256:8823ee0afb3d9696b6ca5b09a159c39bf7a8fe6690d1fb9851fe5f74584f325f`  
		Last Modified: Mon, 25 Aug 2025 21:53:25 GMT  
		Size: 279.8 KB (279843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486c238d647f7578251e57dd34ce120fb465b25780a1e60cf69ec3bd36b22be4`  
		Last Modified: Mon, 25 Aug 2025 21:53:26 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:32fa6d72e61b79987dd65c0d108e5078c0e0dc93af0460612778e63182c2076c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69951490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9745840960c0e962feb8ce93ade81f3d2d7c4014b1aa7675e1ae02d0a7aff9ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1a427e917c48b164eae3ec3692b4741f5de528261925d2e5efc62a43e5bfc4`  
		Last Modified: Mon, 28 Jul 2025 20:42:19 GMT  
		Size: 284.7 KB (284709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b50d3516e3fbf4aca43b9416e7dd8914c2623a08d12eeb55d98d72b864d50c`  
		Last Modified: Wed, 13 Aug 2025 21:40:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b905d71c6a895e4f8e02255340a28c48f2a71d4744873257004c40c0d2aa00`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.3 MB (6263485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f8b26f147c3aad964c448d6607cf74ae215e3ac1c4cbba753fa3e968275e88`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3231a1494a810504f8b0f942889fffa994e046e8e88d228e3a5088783ce72`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2afba1033f0a6e1546bfc4ba308b2a11e83940382cb23e26214953132de73502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e5578a03d1c8f2a6f8ffcbe41b2176db7f2e9fe34e3740615730082fda76c7`

```dockerfile
```

-	Layers:
	-	`sha256:748645f9a413db4552bbf182353615a0b12bcd436e3be618d281b3d593030ede`  
		Last Modified: Mon, 25 Aug 2025 21:53:30 GMT  
		Size: 276.9 KB (276903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93bc5bdadeab69d30a633aee167e91118e46d1789c6f0ffd8919e02d2abce29`  
		Last Modified: Mon, 25 Aug 2025 21:53:31 GMT  
		Size: 20.3 KB (20279 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:af183020c3351759ff8b8f4bafc2723eeff7c818144664e3694cc95a57ce5b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70304708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562175980913c7c3795d4d816c57841adf59a5bc12f44a1cd0eeb9e6e600f14a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe3e6d4a1713a75edf1789d38233b2e8d48f54cebae5e9d0789eb1af52023b`  
		Last Modified: Mon, 28 Jul 2025 20:30:54 GMT  
		Size: 285.1 KB (285114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269abe529e66aa5bca30329a5b15eb3b1dc68dbfb72494192487eabaf2c75ea7`  
		Last Modified: Wed, 13 Aug 2025 22:24:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b70f44dd4f808419f6fd44bceba6d166aca8e19f4cc6cbd8b36f33239207db`  
		Last Modified: Mon, 25 Aug 2025 19:50:03 GMT  
		Size: 6.6 MB (6550799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d7bd24bb9deffe0ca1b77e298776a06b4a558884001c7bb47966dadc97ca43`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd6fde2d426e5936d85b957d51eeee4fe29a27e410fcafc97d0874ffda5b0a7`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0aebec967107348a51c2631c5a8092b2a9ddf49e4a53aa5e56b903b7db8da90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 KB (295105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5483635ad7faac1a9e8b342df273f4ba0a4bdbe31f6c156346534eee30d30458`

```dockerfile
```

-	Layers:
	-	`sha256:41a25cf6cf15b6b37e3661b3ac34bd18681863b0b85f51cec56d1d316f0397a5`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 274.9 KB (274920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b02b106246f8f724524bb0de7288d77cf1087c013b38171b388fcaf0f37f9e0`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:fb87571ab0cfe463d5b70a18f7fc659670b5c55747db3031ea04cb59192007d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87901339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc43b273027a52c8474444595317de4089d1356a37708213bb7d600ddde35e7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03fbadbe664ad3d80e3509b96250ae628b3c572ce60e514d1ab20170b9d16f`  
		Last Modified: Wed, 06 Aug 2025 20:35:39 GMT  
		Size: 76.3 MB (76329537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3100604e2ac3ab2afb5cfbb5b614bf8a221677bd8062fec6e7c8d427bd3a227`  
		Last Modified: Wed, 06 Aug 2025 20:38:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7fcb5eb3236cdaf4c847395cb3593f761279c79096d30f3e7cf35380880458`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 6.2 MB (6227728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ffbcd6b9606b2af427eeec605dcacf7cd7d3373be452b10e2bb22f249781e`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 1.7 MB (1711639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cfb2de1c2d535f5db75d479624e79d3c03d09237fa02bfe0e3cdaca96319d6`  
		Last Modified: Wed, 06 Aug 2025 21:55:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e726fabc45a470f841e6101b22886180e210ce12d35e7294ff41bda3d5fca48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 KB (310664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b2a779549901a2e89720d3b51ed603f8cad90098f71519ddbb0679b33cb68`

```dockerfile
```

-	Layers:
	-	`sha256:ccc7ede165f095820a25ffb389a248d0b37c8e904fc5ab03cd1183fef473c6fd`  
		Last Modified: Thu, 07 Aug 2025 00:52:47 GMT  
		Size: 290.5 KB (290479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f30acaaa6bd313ee7a3e5ee0cf46680343b632c7fc49a20989d0b539919b4f`  
		Last Modified: Thu, 07 Aug 2025 00:52:48 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:28695f2cfaee062b9a0ca60163b294c9aa426d62328db2bface2b85e282b88ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71589730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3295b1278233227188e8477c2827afae51d241b108713916b5ef77d03eb41a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27212710686629ba49777b5e0cccdf04e89cbe41c95c072e1c75381906d724e9`  
		Last Modified: Wed, 13 Aug 2025 22:25:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b7f018e46a54de4eea0e2dad72f4490579e3365d43915d3250d53ae7ec1890`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 6.5 MB (6502043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c049c1b926591fbe94ed04678a617c00476cf93094e56c118b4aa7d5301293`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8d48eb228a3be3c4a90c83ceb3a374f1cbf2cd8b2704f4bfb913c41a3321d`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ffc6ef944b883b81dfd10aedf994982d8dabb9a7bb31e67921f976ef1da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 KB (294963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0eadd91f1fd0a0f91b5c7391ac0c55f701c738d3b6db0537f39f79f0269f79`

```dockerfile
```

-	Layers:
	-	`sha256:518491161b596d1ff8a9f6f9f6edaf63f977efff9396b1be87c42e36e666a14a`  
		Last Modified: Mon, 25 Aug 2025 21:53:42 GMT  
		Size: 274.8 KB (274848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba037ad301b98b30c070866ceb9f8b5b99f8482275c68bd46ba5664c7b6e5e90`  
		Last Modified: Mon, 25 Aug 2025 21:53:43 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.10-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:f3fcc4c5efa8823e03e7be22f1a617cc774c603b0d8f168c048688337bdeb715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:2.10-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:fae8c3555cf3840ff8637313f178c0317b41466226312ea50a9d597b377a982b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2397840105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5006347b108bafda0318a83f34338f8ef74ab52d118e9d335f14fcd1870a70a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 13 Aug 2025 18:06:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:06:54 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:06:55 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:07:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:07:11 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:07:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:07:18 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:08:48 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:49 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:53 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:49:54 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:50:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:50:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9380c184b3613450235fc0562d48b7c1aeb69072e1e188efd675b317114e13`  
		Last Modified: Wed, 13 Aug 2025 18:10:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb25f9f3a6b5b2e582eb535d357af7f125a5eb0d07250886e7275753bba63b`  
		Last Modified: Wed, 13 Aug 2025 18:10:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1b81a88b515880f2398d85c50e12604a0be218b43024e6273e174b171a33`  
		Last Modified: Wed, 13 Aug 2025 18:10:31 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe632c05e48eccbb4f65220b5c6cd3d2c38482c1aff7c8a70dedef13c2d8cde3`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2281e6abc340f61cf79bb6641d015955f72d05413007591f91ca52d8fcb2020b`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6aa352166614c00f1cc5419011f1a211ffaa26ece1203ddb8a7248c0f9dee1`  
		Last Modified: Wed, 13 Aug 2025 18:10:50 GMT  
		Size: 51.2 MB (51199537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36716abacdfd69d4d84aaeb498a02c39e5df07d380dc62c6f93a43dd18bd8b36`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992bb304a4c05d05ad6f9fce52e761eaca24471880c19303b2d27362b731cf77`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 335.3 KB (335287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363744c527b6172af2deba44c4735f38293dd27bc326cde515fa1e40d983cbed`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6c232258d56f8ebfb4d22b50309c11595a9cd50805699bb1edc2ff5cac8dc2`  
		Last Modified: Wed, 13 Aug 2025 18:11:01 GMT  
		Size: 62.3 MB (62261944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318c09560fb6a640397158d02fb52738a3d51b23a8f80d35724a4ece31d4cf72`  
		Last Modified: Wed, 13 Aug 2025 18:10:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1f3385040c90c1ee57f2d21940227c7a049f3442ac13a978b145cf185a15f`  
		Last Modified: Mon, 25 Aug 2025 19:50:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe569c48af273bca5f90b236956c3823ba707807419d4b3d31037b23731ca95`  
		Last Modified: Mon, 25 Aug 2025 19:50:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244ee2fe3346da9436f4b3f9faa2052570d594821c15b4458df33433e70d4cf0`  
		Last Modified: Mon, 25 Aug 2025 19:50:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bbd758a87764c779cea8fe9429c091634198b909b6faadc2c04c4add5049a0`  
		Last Modified: Mon, 25 Aug 2025 19:50:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0dab63cb896e209cbc5b4577e607d35a3df8d9e39d5dca15bc9208710b2ec`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 2.3 MB (2334479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769960fd4bcf873320f369a1ea9ae102548c30a01938b0886cbafefe311b4353`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:c8f1420ef1f3b2c6beee3989c77169c5b35e505098aecbd8cdf91fa99cc1342e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `caddy:2.10-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:f0ecd5bc38691c997cfbb4eaff5bede8b9d25421e5a2fb78b50ac5fbf79f08f5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3615224351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b87c61031d564c20e4c7aadd128b369ac69af5472854d710e6709eec622c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 13 Aug 2025 18:08:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:08:27 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:08:29 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:08:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:08:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:08:50 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:10:07 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:10:07 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:56:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:56:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:56:36 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:56:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:56:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:56:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3329feb8c3f471d93f04a4afc376778f359481b9b10abd677ae7f8105b7a1982`  
		Last Modified: Wed, 13 Aug 2025 18:14:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b683ebca7e697913d8f93eeb03b85a4924fa297a5830b694441bb31e2ef2a8`  
		Last Modified: Wed, 13 Aug 2025 18:14:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a25a1b355f0af537456d6695b8cbf9c0c5582795add71831072b1f2067593`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5469c0152f4c91f8d66bd59239beec913796e4d17d8977dcf67364f6916d3aae`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9e732885c916712df386d920174e3f95dcc40377352391c6f5e8ccc9e59be5`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9ebf49453f4f127c2dffe22dcb483f4eeef5d0260fe4724472d7fc5b89ecaf`  
		Last Modified: Wed, 13 Aug 2025 18:14:25 GMT  
		Size: 51.2 MB (51223826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55bb43d7b4377e022452dadea8a547292c78952945e888b4c3a99193a0e78f`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec885b71c379ce9bdce0b6477ef6652f6b9d9f566e7e571c9863ba6adb40cede`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 351.5 KB (351496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e05cdc4ff30cbd5098771fc7b97628d410fe4d7f2afb43e7ddcd5256d51d407`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5def4f4469cc1db786df7b6975d1fc3c3bd4c534434e05e676d67edd1f0af9f`  
		Last Modified: Wed, 13 Aug 2025 18:14:22 GMT  
		Size: 62.5 MB (62477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dd29c29527d22890d7b81985987d57cceb811888344ca07659b7c0f2e94151`  
		Last Modified: Wed, 13 Aug 2025 18:14:10 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8523736186869f7a49f95f8b318bee25824ebbb010838d15db88667b969e3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb124c01828ece301417db645f6bd33502d9fa4004bbabb93d8483d9adee73fc`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc48728b561dbd7581689079fb9e459be5b1b835c2a19d3e6ad8d63472b2b7b4`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009143406fac9c3402bce23cf7487a8d83bf93fd0dacf936aa17661011450dd`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a06a632575ebdb5c471cc6aeed6865b4ed1bda3ead85aaa00ed5488712d68f3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 2.3 MB (2324141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb76a0655e886937e45d30114efbcbb8b7dcf4f622e834abea3396c37a8494`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10-windowsservercore`

```console
$ docker pull caddy@sha256:c2e9243204fd55beead5b9d893a8ca326f04ee4f2331dec60ad5a1d2a6992777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:2.10-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.10-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:3ebb7e7a0141c5f1434331567920cb6803bcb77417482786ce8e21cc1efad8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:2.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:eadadcb9a4804f2c2f6ace69b31243ddc25d10923eb9d7148361a38dfde75b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `caddy:2.10-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10.2`

```console
$ docker pull caddy@sha256:7f2af82ffc1849dff5f4b9d9b0405eae77ed6cebe6740b181ae72a668e3ed525
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
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:2.10.2` - linux; amd64

```console
$ docker pull caddy@sha256:e9fd95fd7cea0c3403c622c5c2457cddcaf355a5eba11048b17cb3d99a828f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20077764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a72cdc384a6f6b8c1d99f569290cee6606bec3cca68812feba43bfda45028`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634211206164759ba5e5df423465aed056f9cc799700d15b89ca49626779515f`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 346.6 KB (346592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edccfae94f0e103409f8c3283a9e19bb7585db1ed9bd9e3a0311de9e0149c1de`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e53616944a4fa3ff99b33d90d938827b7d63bdb00324b94dab3ad40ab166831`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 15.9 MB (15923955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2` - unknown; unknown

```console
$ docker pull caddy@sha256:30f634f6f0e9e39136903c3b81be8f780a4b805b66163bfc0e683fafb62a3f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 KB (314291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d132bcee2e485d83458421325b31111463d1718ccf62b18456e97d495bc57`

```dockerfile
```

-	Layers:
	-	`sha256:91d8c07f79d660b96ebece0d8847c92fd5160edb83b97e31865c2af067eeb8f0`  
		Last Modified: Mon, 25 Aug 2025 21:52:42 GMT  
		Size: 296.0 KB (296013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d27f4d928535909dc6d7b276be2d1e63901b6b627c43a4bfd594a0b899c110`  
		Last Modified: Mon, 25 Aug 2025 21:52:43 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bf497dbd5122b8bce808c55b47aa082eb84d06f77831adf2d8cc0b5f11e66438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18903449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ba67aa2169d0dbd6426eb009d3bd28de88cb829cb8453b2e628f0443f6e9f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8aa6aa6b1802d86bbc73e75216bbb426a1a8ebad8fab1ccf37a1adfdd1b779`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 346.5 KB (346493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3bd303b867cb629d2b99f58967b240f288c9b1dbf712003b3e56200692140c`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e6b087db3bea6b06b1a48ee30c1fc4db8efebe5b0e6670b418e3db437e8c38`  
		Last Modified: Mon, 25 Aug 2025 19:48:46 GMT  
		Size: 15.0 MB (15048518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2` - unknown; unknown

```console
$ docker pull caddy@sha256:286477e027ad1c6350295044f9c520fa196eb08183d4939ae7ed071fc7320c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16e2d2b0cb8b273b15b42a3b1d12c77c076d757e265061f5e61b31763a6a52`

```dockerfile
```

-	Layers:
	-	`sha256:29f2ff0c73ef6349295d38ad6646decc7e0677799f04a1a1ce633e18c85a4327`  
		Last Modified: Mon, 25 Aug 2025 21:52:47 GMT  
		Size: 18.2 KB (18197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d5af7163676df0baffb41f5bce9c4f0775a69609bc2384b101ff4ba749f0050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18601748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e276120a8a2d3df3a422b6d9a2b02c16b9f92c6b28ac595c34fcc06410127c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979c078f866daa2820e22fa7f8a9cc664e49f7d538de1341a2c2c9a60489560`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 343.2 KB (343205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeca689d2f3de3a319b91d9ddb84048521f017d394555aa2ab895ef9cdb98e2`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711aca2485d7f9dfbfccd9cf2a11a6db8015c154383632363d1ac44b755cb55`  
		Last Modified: Mon, 25 Aug 2025 19:48:47 GMT  
		Size: 15.0 MB (15031978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2` - unknown; unknown

```console
$ docker pull caddy@sha256:8049ae7cb8cf21da392232342dd2c386e8e79bb9a7093ef47dec2cd1e4d8d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 KB (314493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b289ec4bc1157ad5848221ba42af4a065fd5af769065351ada6548da41f5c1`

```dockerfile
```

-	Layers:
	-	`sha256:7653918e29fb0de220bc0644efa15394bed69ae8f40081cd705aa96205888b4c`  
		Last Modified: Mon, 25 Aug 2025 21:52:51 GMT  
		Size: 296.1 KB (296081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fb47d806abc1bee7ac987c99961bb2c58274d6cbc04b58ea4c3c026b94f2ce`  
		Last Modified: Mon, 25 Aug 2025 21:52:52 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:4c3be81b7ee70190ce5291230e5a5d4dd8ea998c44cfb5fcc4680a60ea6c5621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19013546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b37c5f2910ca9daf3b5cd9f63bb06d782d2062d4daceced81673d49fe4a1c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ebf372d05e77b4bdc3cea55c048537aaac7759aa0079ed9944004ac30c980c`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 357.7 KB (357727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f163ee242da1ec76c0ab875c407ba39c49aa3eab955a46b9ea14d94a86c4d48e`  
		Last Modified: Mon, 25 Aug 2025 19:48:51 GMT  
		Size: 7.5 KB (7492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225b3b694c911c2a8b8814871c8353f7b7686cc9ea3fc2b02dba2f45803dd75`  
		Last Modified: Mon, 25 Aug 2025 19:48:55 GMT  
		Size: 14.5 MB (14517545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2` - unknown; unknown

```console
$ docker pull caddy@sha256:a657dd5aa41ae2796a14d32f91e630f0efcefa03e3261ac63d39793887cea22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 KB (314576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469b3383a6f868625bafb61aa5dd86ccd26899761e2bdb5fafafbc7e250ef24b`

```dockerfile
```

-	Layers:
	-	`sha256:4f49301002ed8e6230d3ea527498b3328f01453f1b0e12e3bbcb7ce771cca15b`  
		Last Modified: Mon, 25 Aug 2025 21:52:55 GMT  
		Size: 296.1 KB (296117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fbb94c8995329e1c4b3235561ee976502480bebaab9183f926bf2529444c9d`  
		Last Modified: Mon, 25 Aug 2025 21:52:56 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2` - linux; ppc64le

```console
$ docker pull caddy@sha256:67112be943616a31dfbf0c815ed5325bf71a9d8c6cfe49a1935b244bd3b109e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18591170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f3d87694b9256e003a6824820cec8dfc82ad339b7d3bc41671c4996663a0a3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe739855dbbb9a1403a242cd984b1b9b4439925fb4fcedc9d3d6ade9baf3dd5`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 360.6 KB (360616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab33549ec0ff70ed9ba5ea43079d739e8d6fe698b0578958a9e2675602d1f6`  
		Last Modified: Mon, 25 Aug 2025 19:49:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6276663ba0f6c95bde9cd5440dc7ec15f6e100f8283c704efd10d02181f066dc`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 14.5 MB (14495915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2` - unknown; unknown

```console
$ docker pull caddy@sha256:54c1de5978b47c2325c8f34e5589b9e4befd54792776c52701944ded623d9922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 KB (312470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d525e05914ec596f61ab5f038622c17b75382bd36e15638e19d2ef0b54ab4`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2fa5edceb1da7dbf0f53e0b3b6e55ebdebce9112144575d69508ba7ea1f29`  
		Last Modified: Mon, 25 Aug 2025 21:53:01 GMT  
		Size: 294.1 KB (294120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2488d35b692ff2f9eeccf6177b581e0b4012821bcd0e7079a6755296fdc31433`  
		Last Modified: Mon, 25 Aug 2025 21:53:02 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2` - linux; s390x

```console
$ docker pull caddy@sha256:df924d28949f8a3be699c88ab40eb6b5ca37234e6af5431cb6a1cca63e58a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19362618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85040edfc178cf9c5de8611792e65c67f07629a5c76b7089bf0828d075163a0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff98415fc23c99d5ff9b731b3ed1f5f263fca7f05ddbb51c47d7d8b6df1f89e8`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 353.5 KB (353456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e6340a3b7a63c6c76d521ec65f90ba0718a26fb02520f02216f158300c89e`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd56c657dc325cdf0a5d0c300a1380b0fe6abd98dcee92bcf38b02d14d579062`  
		Last Modified: Mon, 25 Aug 2025 19:51:46 GMT  
		Size: 15.4 MB (15356663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2` - unknown; unknown

```console
$ docker pull caddy@sha256:ce406a252aedd52a38cc6938d993637d83f2aedbe10e9eb385f4b60a12418812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 KB (312340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190d69bf6d55a424c64ecfe71fedbf83d368d2191338ab24083d5426fa60e861`

```dockerfile
```

-	Layers:
	-	`sha256:ea8886b3a4622ffdcc38a8a441716fbb95afc7feb55738ebaae75b137a193925`  
		Last Modified: Mon, 25 Aug 2025 21:53:08 GMT  
		Size: 294.1 KB (294062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5011fab561f7f812f810ba45504c8489c7a5e0383d88863c43b47478a136a21a`  
		Last Modified: Mon, 25 Aug 2025 21:53:09 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.10.2` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10.2-alpine`

```console
$ docker pull caddy@sha256:22ee08d42987c0fce9d9fe8922faed0d6f20cce5d464e8370dbab73b229af969
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

### `caddy:2.10.2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:e9fd95fd7cea0c3403c622c5c2457cddcaf355a5eba11048b17cb3d99a828f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20077764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a72cdc384a6f6b8c1d99f569290cee6606bec3cca68812feba43bfda45028`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634211206164759ba5e5df423465aed056f9cc799700d15b89ca49626779515f`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 346.6 KB (346592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edccfae94f0e103409f8c3283a9e19bb7585db1ed9bd9e3a0311de9e0149c1de`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e53616944a4fa3ff99b33d90d938827b7d63bdb00324b94dab3ad40ab166831`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 15.9 MB (15923955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:30f634f6f0e9e39136903c3b81be8f780a4b805b66163bfc0e683fafb62a3f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 KB (314291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d132bcee2e485d83458421325b31111463d1718ccf62b18456e97d495bc57`

```dockerfile
```

-	Layers:
	-	`sha256:91d8c07f79d660b96ebece0d8847c92fd5160edb83b97e31865c2af067eeb8f0`  
		Last Modified: Mon, 25 Aug 2025 21:52:42 GMT  
		Size: 296.0 KB (296013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d27f4d928535909dc6d7b276be2d1e63901b6b627c43a4bfd594a0b899c110`  
		Last Modified: Mon, 25 Aug 2025 21:52:43 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bf497dbd5122b8bce808c55b47aa082eb84d06f77831adf2d8cc0b5f11e66438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18903449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ba67aa2169d0dbd6426eb009d3bd28de88cb829cb8453b2e628f0443f6e9f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8aa6aa6b1802d86bbc73e75216bbb426a1a8ebad8fab1ccf37a1adfdd1b779`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 346.5 KB (346493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3bd303b867cb629d2b99f58967b240f288c9b1dbf712003b3e56200692140c`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e6b087db3bea6b06b1a48ee30c1fc4db8efebe5b0e6670b418e3db437e8c38`  
		Last Modified: Mon, 25 Aug 2025 19:48:46 GMT  
		Size: 15.0 MB (15048518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:286477e027ad1c6350295044f9c520fa196eb08183d4939ae7ed071fc7320c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16e2d2b0cb8b273b15b42a3b1d12c77c076d757e265061f5e61b31763a6a52`

```dockerfile
```

-	Layers:
	-	`sha256:29f2ff0c73ef6349295d38ad6646decc7e0677799f04a1a1ce633e18c85a4327`  
		Last Modified: Mon, 25 Aug 2025 21:52:47 GMT  
		Size: 18.2 KB (18197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d5af7163676df0baffb41f5bce9c4f0775a69609bc2384b101ff4ba749f0050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18601748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e276120a8a2d3df3a422b6d9a2b02c16b9f92c6b28ac595c34fcc06410127c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979c078f866daa2820e22fa7f8a9cc664e49f7d538de1341a2c2c9a60489560`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 343.2 KB (343205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeca689d2f3de3a319b91d9ddb84048521f017d394555aa2ab895ef9cdb98e2`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711aca2485d7f9dfbfccd9cf2a11a6db8015c154383632363d1ac44b755cb55`  
		Last Modified: Mon, 25 Aug 2025 19:48:47 GMT  
		Size: 15.0 MB (15031978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:8049ae7cb8cf21da392232342dd2c386e8e79bb9a7093ef47dec2cd1e4d8d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 KB (314493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b289ec4bc1157ad5848221ba42af4a065fd5af769065351ada6548da41f5c1`

```dockerfile
```

-	Layers:
	-	`sha256:7653918e29fb0de220bc0644efa15394bed69ae8f40081cd705aa96205888b4c`  
		Last Modified: Mon, 25 Aug 2025 21:52:51 GMT  
		Size: 296.1 KB (296081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fb47d806abc1bee7ac987c99961bb2c58274d6cbc04b58ea4c3c026b94f2ce`  
		Last Modified: Mon, 25 Aug 2025 21:52:52 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:4c3be81b7ee70190ce5291230e5a5d4dd8ea998c44cfb5fcc4680a60ea6c5621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19013546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b37c5f2910ca9daf3b5cd9f63bb06d782d2062d4daceced81673d49fe4a1c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ebf372d05e77b4bdc3cea55c048537aaac7759aa0079ed9944004ac30c980c`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 357.7 KB (357727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f163ee242da1ec76c0ab875c407ba39c49aa3eab955a46b9ea14d94a86c4d48e`  
		Last Modified: Mon, 25 Aug 2025 19:48:51 GMT  
		Size: 7.5 KB (7492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225b3b694c911c2a8b8814871c8353f7b7686cc9ea3fc2b02dba2f45803dd75`  
		Last Modified: Mon, 25 Aug 2025 19:48:55 GMT  
		Size: 14.5 MB (14517545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a657dd5aa41ae2796a14d32f91e630f0efcefa03e3261ac63d39793887cea22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 KB (314576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469b3383a6f868625bafb61aa5dd86ccd26899761e2bdb5fafafbc7e250ef24b`

```dockerfile
```

-	Layers:
	-	`sha256:4f49301002ed8e6230d3ea527498b3328f01453f1b0e12e3bbcb7ce771cca15b`  
		Last Modified: Mon, 25 Aug 2025 21:52:55 GMT  
		Size: 296.1 KB (296117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fbb94c8995329e1c4b3235561ee976502480bebaab9183f926bf2529444c9d`  
		Last Modified: Mon, 25 Aug 2025 21:52:56 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:67112be943616a31dfbf0c815ed5325bf71a9d8c6cfe49a1935b244bd3b109e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18591170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f3d87694b9256e003a6824820cec8dfc82ad339b7d3bc41671c4996663a0a3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe739855dbbb9a1403a242cd984b1b9b4439925fb4fcedc9d3d6ade9baf3dd5`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 360.6 KB (360616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab33549ec0ff70ed9ba5ea43079d739e8d6fe698b0578958a9e2675602d1f6`  
		Last Modified: Mon, 25 Aug 2025 19:49:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6276663ba0f6c95bde9cd5440dc7ec15f6e100f8283c704efd10d02181f066dc`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 14.5 MB (14495915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:54c1de5978b47c2325c8f34e5589b9e4befd54792776c52701944ded623d9922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 KB (312470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d525e05914ec596f61ab5f038622c17b75382bd36e15638e19d2ef0b54ab4`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2fa5edceb1da7dbf0f53e0b3b6e55ebdebce9112144575d69508ba7ea1f29`  
		Last Modified: Mon, 25 Aug 2025 21:53:01 GMT  
		Size: 294.1 KB (294120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2488d35b692ff2f9eeccf6177b581e0b4012821bcd0e7079a6755296fdc31433`  
		Last Modified: Mon, 25 Aug 2025 21:53:02 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:df924d28949f8a3be699c88ab40eb6b5ca37234e6af5431cb6a1cca63e58a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19362618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85040edfc178cf9c5de8611792e65c67f07629a5c76b7089bf0828d075163a0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff98415fc23c99d5ff9b731b3ed1f5f263fca7f05ddbb51c47d7d8b6df1f89e8`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 353.5 KB (353456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e6340a3b7a63c6c76d521ec65f90ba0718a26fb02520f02216f158300c89e`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd56c657dc325cdf0a5d0c300a1380b0fe6abd98dcee92bcf38b02d14d579062`  
		Last Modified: Mon, 25 Aug 2025 19:51:46 GMT  
		Size: 15.4 MB (15356663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ce406a252aedd52a38cc6938d993637d83f2aedbe10e9eb385f4b60a12418812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 KB (312340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190d69bf6d55a424c64ecfe71fedbf83d368d2191338ab24083d5426fa60e861`

```dockerfile
```

-	Layers:
	-	`sha256:ea8886b3a4622ffdcc38a8a441716fbb95afc7feb55738ebaae75b137a193925`  
		Last Modified: Mon, 25 Aug 2025 21:53:08 GMT  
		Size: 294.1 KB (294062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5011fab561f7f812f810ba45504c8489c7a5e0383d88863c43b47478a136a21a`  
		Last Modified: Mon, 25 Aug 2025 21:53:09 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.10.2-builder`

```console
$ docker pull caddy@sha256:22ff419120e17d257b9744216ecae0b2305d81ff570490fba03625f047c4195a
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
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:2.10.2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:baa56c9394d7025fb7e344f5a1d52c7d0ae2a428a6d8e4d7acf85480477cf819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72186376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0205b23d29755cb0085885d9fa3ac1ea66ce75020051c0185f423ea947bc24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d4ca09441bdb9129d5708d2aa8802e233b2d11d1797317158c4095e9df8fc`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 282.4 KB (282437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18414ed0f6669fd1d6e137922f2a57e37aaf0a63ae6968c499fe69b17d148d14`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36dd3b7005cdf211c5d6cd7f47820b1ffa15134a87c84b500f754613863411`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.2 MB (6211320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc4a072890c37012160bb87d003d188e34244b09f60d9a7e33a521175aa4914`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.8 MB (1846494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45676fbd1b151c4eb76c6df8afe515dd1b8001736b55aba9841182177b17`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:f5d337972eff4ad3e0c109de0443e6695887aae29e94c1df6e6189ef17e777df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3035b7074d5121642859847a37b0e722a8cb9137408b7356cf5e5a79d0a6760c`

```dockerfile
```

-	Layers:
	-	`sha256:f41e395e3e21569a16f8d91a8825c71ee9146373ca8d37c13d6e6de553f55627`  
		Last Modified: Mon, 25 Aug 2025 21:53:16 GMT  
		Size: 276.8 KB (276799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a6e841ccf0c2ac296066a2cd3354ab00dcc598ae922e619237f17aebd1bb82`  
		Last Modified: Mon, 25 Aug 2025 21:53:17 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e1edbceed451136633244ae771982f55dd7d7218a4ffc50369af9eefbb5266a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70630913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8be52c140ce9073b5e99046435e6d10435d169d31239bff87fc88de3e317a56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b30dde5a6a0bd25a99ef148aafdaf794991c98c7b0798149f6d4e21ebc6ccd`  
		Last Modified: Wed, 13 Aug 2025 19:12:26 GMT  
		Size: 59.0 MB (58976836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63714916874ab7e10bdc757c1f8a9e57104a40067c294f970c9d8ff49423866`  
		Last Modified: Wed, 13 Aug 2025 18:04:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96b63bb94735bf5a233756bdc50074d4de4f13340afa4a5b52a444075d8471d`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 6.1 MB (6124248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cae36cb0796b19b218d007f943c4a58a98847586c215d0b9182edb25f4b08`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d14e3b2c944638da45ebffd7d320249acf6ca96e796a9c2aaee17c71e23a4d`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:b2b71368948bedcdbe1fe1b49cbffe11bca901b908dde0561b73953dad703bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b200e21ab8337407084c2f915782c003a30ed1b357ddf279a1faf52f479fd277`

```dockerfile
```

-	Layers:
	-	`sha256:995e27d2c9f18e3d1278c03b04caf0d92d8524cca3c1f98d0b486e78c8fdec72`  
		Last Modified: Mon, 25 Aug 2025 21:53:21 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7570894dd8642571d29a3f9a172447dc68c92466e954fbfe509dd4c1002c62d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69821208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303120483e85eaa18d5623ff884d6ba6bc5329cf64792dafc7122ec47e98f1b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0ef49cd2af3f26990fbdb01d76c5d72224144a9082720b843066d506cd46c9`  
		Last Modified: Thu, 14 Aug 2025 04:30:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee18d4be11a0ac51fa3627c2b017b3aef767f70a39ea0d73d6de35cd618a71f`  
		Last Modified: Mon, 25 Aug 2025 19:49:07 GMT  
		Size: 5.6 MB (5603426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6551895b1ab029d74729175b98ce97b83c07b3112d073fc90b8fe101237e63`  
		Last Modified: Mon, 25 Aug 2025 19:49:09 GMT  
		Size: 1.7 MB (1738756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b87d17c36733a93bfd68173426cc2ef130e2195c9c450df58a04dc2c5fab0f`  
		Last Modified: Mon, 25 Aug 2025 19:49:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:55c648a2b1f1e4d6d07485531af3a8734047d606ae8f624a5e55a14a84c3badd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 KB (300079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cdb0bd297a9f9a841359ac15ef57a33be96fe2dae32e84f34341e6fbcf5b69`

```dockerfile
```

-	Layers:
	-	`sha256:8823ee0afb3d9696b6ca5b09a159c39bf7a8fe6690d1fb9851fe5f74584f325f`  
		Last Modified: Mon, 25 Aug 2025 21:53:25 GMT  
		Size: 279.8 KB (279843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486c238d647f7578251e57dd34ce120fb465b25780a1e60cf69ec3bd36b22be4`  
		Last Modified: Mon, 25 Aug 2025 21:53:26 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:32fa6d72e61b79987dd65c0d108e5078c0e0dc93af0460612778e63182c2076c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69951490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9745840960c0e962feb8ce93ade81f3d2d7c4014b1aa7675e1ae02d0a7aff9ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1a427e917c48b164eae3ec3692b4741f5de528261925d2e5efc62a43e5bfc4`  
		Last Modified: Mon, 28 Jul 2025 20:42:19 GMT  
		Size: 284.7 KB (284709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b50d3516e3fbf4aca43b9416e7dd8914c2623a08d12eeb55d98d72b864d50c`  
		Last Modified: Wed, 13 Aug 2025 21:40:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b905d71c6a895e4f8e02255340a28c48f2a71d4744873257004c40c0d2aa00`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.3 MB (6263485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f8b26f147c3aad964c448d6607cf74ae215e3ac1c4cbba753fa3e968275e88`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3231a1494a810504f8b0f942889fffa994e046e8e88d228e3a5088783ce72`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:2afba1033f0a6e1546bfc4ba308b2a11e83940382cb23e26214953132de73502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e5578a03d1c8f2a6f8ffcbe41b2176db7f2e9fe34e3740615730082fda76c7`

```dockerfile
```

-	Layers:
	-	`sha256:748645f9a413db4552bbf182353615a0b12bcd436e3be618d281b3d593030ede`  
		Last Modified: Mon, 25 Aug 2025 21:53:30 GMT  
		Size: 276.9 KB (276903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93bc5bdadeab69d30a633aee167e91118e46d1789c6f0ffd8919e02d2abce29`  
		Last Modified: Mon, 25 Aug 2025 21:53:31 GMT  
		Size: 20.3 KB (20279 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:af183020c3351759ff8b8f4bafc2723eeff7c818144664e3694cc95a57ce5b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70304708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562175980913c7c3795d4d816c57841adf59a5bc12f44a1cd0eeb9e6e600f14a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe3e6d4a1713a75edf1789d38233b2e8d48f54cebae5e9d0789eb1af52023b`  
		Last Modified: Mon, 28 Jul 2025 20:30:54 GMT  
		Size: 285.1 KB (285114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269abe529e66aa5bca30329a5b15eb3b1dc68dbfb72494192487eabaf2c75ea7`  
		Last Modified: Wed, 13 Aug 2025 22:24:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b70f44dd4f808419f6fd44bceba6d166aca8e19f4cc6cbd8b36f33239207db`  
		Last Modified: Mon, 25 Aug 2025 19:50:03 GMT  
		Size: 6.6 MB (6550799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d7bd24bb9deffe0ca1b77e298776a06b4a558884001c7bb47966dadc97ca43`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd6fde2d426e5936d85b957d51eeee4fe29a27e410fcafc97d0874ffda5b0a7`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0aebec967107348a51c2631c5a8092b2a9ddf49e4a53aa5e56b903b7db8da90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 KB (295105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5483635ad7faac1a9e8b342df273f4ba0a4bdbe31f6c156346534eee30d30458`

```dockerfile
```

-	Layers:
	-	`sha256:41a25cf6cf15b6b37e3661b3ac34bd18681863b0b85f51cec56d1d316f0397a5`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 274.9 KB (274920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b02b106246f8f724524bb0de7288d77cf1087c013b38171b388fcaf0f37f9e0`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:28695f2cfaee062b9a0ca60163b294c9aa426d62328db2bface2b85e282b88ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71589730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3295b1278233227188e8477c2827afae51d241b108713916b5ef77d03eb41a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27212710686629ba49777b5e0cccdf04e89cbe41c95c072e1c75381906d724e9`  
		Last Modified: Wed, 13 Aug 2025 22:25:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b7f018e46a54de4eea0e2dad72f4490579e3365d43915d3250d53ae7ec1890`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 6.5 MB (6502043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c049c1b926591fbe94ed04678a617c00476cf93094e56c118b4aa7d5301293`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8d48eb228a3be3c4a90c83ceb3a374f1cbf2cd8b2704f4bfb913c41a3321d`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ffc6ef944b883b81dfd10aedf994982d8dabb9a7bb31e67921f976ef1da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 KB (294963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0eadd91f1fd0a0f91b5c7391ac0c55f701c738d3b6db0537f39f79f0269f79`

```dockerfile
```

-	Layers:
	-	`sha256:518491161b596d1ff8a9f6f9f6edaf63f977efff9396b1be87c42e36e666a14a`  
		Last Modified: Mon, 25 Aug 2025 21:53:42 GMT  
		Size: 274.8 KB (274848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba037ad301b98b30c070866ceb9f8b5b99f8482275c68bd46ba5664c7b6e5e90`  
		Last Modified: Mon, 25 Aug 2025 21:53:43 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-builder` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:f0ecd5bc38691c997cfbb4eaff5bede8b9d25421e5a2fb78b50ac5fbf79f08f5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3615224351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b87c61031d564c20e4c7aadd128b369ac69af5472854d710e6709eec622c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 13 Aug 2025 18:08:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:08:27 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:08:29 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:08:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:08:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:08:50 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:10:07 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:10:07 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:56:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:56:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:56:36 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:56:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:56:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:56:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3329feb8c3f471d93f04a4afc376778f359481b9b10abd677ae7f8105b7a1982`  
		Last Modified: Wed, 13 Aug 2025 18:14:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b683ebca7e697913d8f93eeb03b85a4924fa297a5830b694441bb31e2ef2a8`  
		Last Modified: Wed, 13 Aug 2025 18:14:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a25a1b355f0af537456d6695b8cbf9c0c5582795add71831072b1f2067593`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5469c0152f4c91f8d66bd59239beec913796e4d17d8977dcf67364f6916d3aae`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9e732885c916712df386d920174e3f95dcc40377352391c6f5e8ccc9e59be5`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9ebf49453f4f127c2dffe22dcb483f4eeef5d0260fe4724472d7fc5b89ecaf`  
		Last Modified: Wed, 13 Aug 2025 18:14:25 GMT  
		Size: 51.2 MB (51223826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55bb43d7b4377e022452dadea8a547292c78952945e888b4c3a99193a0e78f`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec885b71c379ce9bdce0b6477ef6652f6b9d9f566e7e571c9863ba6adb40cede`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 351.5 KB (351496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e05cdc4ff30cbd5098771fc7b97628d410fe4d7f2afb43e7ddcd5256d51d407`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5def4f4469cc1db786df7b6975d1fc3c3bd4c534434e05e676d67edd1f0af9f`  
		Last Modified: Wed, 13 Aug 2025 18:14:22 GMT  
		Size: 62.5 MB (62477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dd29c29527d22890d7b81985987d57cceb811888344ca07659b7c0f2e94151`  
		Last Modified: Wed, 13 Aug 2025 18:14:10 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8523736186869f7a49f95f8b318bee25824ebbb010838d15db88667b969e3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb124c01828ece301417db645f6bd33502d9fa4004bbabb93d8483d9adee73fc`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc48728b561dbd7581689079fb9e459be5b1b835c2a19d3e6ad8d63472b2b7b4`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009143406fac9c3402bce23cf7487a8d83bf93fd0dacf936aa17661011450dd`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a06a632575ebdb5c471cc6aeed6865b4ed1bda3ead85aaa00ed5488712d68f3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 2.3 MB (2324141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb76a0655e886937e45d30114efbcbb8b7dcf4f622e834abea3396c37a8494`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.10.2-builder` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:fae8c3555cf3840ff8637313f178c0317b41466226312ea50a9d597b377a982b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2397840105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5006347b108bafda0318a83f34338f8ef74ab52d118e9d335f14fcd1870a70a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 13 Aug 2025 18:06:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:06:54 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:06:55 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:07:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:07:11 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:07:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:07:18 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:08:48 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:49 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:53 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:49:54 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:50:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:50:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9380c184b3613450235fc0562d48b7c1aeb69072e1e188efd675b317114e13`  
		Last Modified: Wed, 13 Aug 2025 18:10:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb25f9f3a6b5b2e582eb535d357af7f125a5eb0d07250886e7275753bba63b`  
		Last Modified: Wed, 13 Aug 2025 18:10:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1b81a88b515880f2398d85c50e12604a0be218b43024e6273e174b171a33`  
		Last Modified: Wed, 13 Aug 2025 18:10:31 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe632c05e48eccbb4f65220b5c6cd3d2c38482c1aff7c8a70dedef13c2d8cde3`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2281e6abc340f61cf79bb6641d015955f72d05413007591f91ca52d8fcb2020b`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6aa352166614c00f1cc5419011f1a211ffaa26ece1203ddb8a7248c0f9dee1`  
		Last Modified: Wed, 13 Aug 2025 18:10:50 GMT  
		Size: 51.2 MB (51199537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36716abacdfd69d4d84aaeb498a02c39e5df07d380dc62c6f93a43dd18bd8b36`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992bb304a4c05d05ad6f9fce52e761eaca24471880c19303b2d27362b731cf77`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 335.3 KB (335287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363744c527b6172af2deba44c4735f38293dd27bc326cde515fa1e40d983cbed`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6c232258d56f8ebfb4d22b50309c11595a9cd50805699bb1edc2ff5cac8dc2`  
		Last Modified: Wed, 13 Aug 2025 18:11:01 GMT  
		Size: 62.3 MB (62261944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318c09560fb6a640397158d02fb52738a3d51b23a8f80d35724a4ece31d4cf72`  
		Last Modified: Wed, 13 Aug 2025 18:10:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1f3385040c90c1ee57f2d21940227c7a049f3442ac13a978b145cf185a15f`  
		Last Modified: Mon, 25 Aug 2025 19:50:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe569c48af273bca5f90b236956c3823ba707807419d4b3d31037b23731ca95`  
		Last Modified: Mon, 25 Aug 2025 19:50:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244ee2fe3346da9436f4b3f9faa2052570d594821c15b4458df33433e70d4cf0`  
		Last Modified: Mon, 25 Aug 2025 19:50:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bbd758a87764c779cea8fe9429c091634198b909b6faadc2c04c4add5049a0`  
		Last Modified: Mon, 25 Aug 2025 19:50:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0dab63cb896e209cbc5b4577e607d35a3df8d9e39d5dca15bc9208710b2ec`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 2.3 MB (2334479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769960fd4bcf873320f369a1ea9ae102548c30a01938b0886cbafefe311b4353`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10.2-builder-alpine`

```console
$ docker pull caddy@sha256:87e38b6488a6a512ce3bd143f66be7184aa7ac411b206815762b82db86ebd980
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

### `caddy:2.10.2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:baa56c9394d7025fb7e344f5a1d52c7d0ae2a428a6d8e4d7acf85480477cf819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72186376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0205b23d29755cb0085885d9fa3ac1ea66ce75020051c0185f423ea947bc24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d4ca09441bdb9129d5708d2aa8802e233b2d11d1797317158c4095e9df8fc`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 282.4 KB (282437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18414ed0f6669fd1d6e137922f2a57e37aaf0a63ae6968c499fe69b17d148d14`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36dd3b7005cdf211c5d6cd7f47820b1ffa15134a87c84b500f754613863411`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.2 MB (6211320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc4a072890c37012160bb87d003d188e34244b09f60d9a7e33a521175aa4914`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.8 MB (1846494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45676fbd1b151c4eb76c6df8afe515dd1b8001736b55aba9841182177b17`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f5d337972eff4ad3e0c109de0443e6695887aae29e94c1df6e6189ef17e777df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3035b7074d5121642859847a37b0e722a8cb9137408b7356cf5e5a79d0a6760c`

```dockerfile
```

-	Layers:
	-	`sha256:f41e395e3e21569a16f8d91a8825c71ee9146373ca8d37c13d6e6de553f55627`  
		Last Modified: Mon, 25 Aug 2025 21:53:16 GMT  
		Size: 276.8 KB (276799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a6e841ccf0c2ac296066a2cd3354ab00dcc598ae922e619237f17aebd1bb82`  
		Last Modified: Mon, 25 Aug 2025 21:53:17 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e1edbceed451136633244ae771982f55dd7d7218a4ffc50369af9eefbb5266a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70630913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8be52c140ce9073b5e99046435e6d10435d169d31239bff87fc88de3e317a56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b30dde5a6a0bd25a99ef148aafdaf794991c98c7b0798149f6d4e21ebc6ccd`  
		Last Modified: Wed, 13 Aug 2025 19:12:26 GMT  
		Size: 59.0 MB (58976836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63714916874ab7e10bdc757c1f8a9e57104a40067c294f970c9d8ff49423866`  
		Last Modified: Wed, 13 Aug 2025 18:04:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96b63bb94735bf5a233756bdc50074d4de4f13340afa4a5b52a444075d8471d`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 6.1 MB (6124248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cae36cb0796b19b218d007f943c4a58a98847586c215d0b9182edb25f4b08`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d14e3b2c944638da45ebffd7d320249acf6ca96e796a9c2aaee17c71e23a4d`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b2b71368948bedcdbe1fe1b49cbffe11bca901b908dde0561b73953dad703bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b200e21ab8337407084c2f915782c003a30ed1b357ddf279a1faf52f479fd277`

```dockerfile
```

-	Layers:
	-	`sha256:995e27d2c9f18e3d1278c03b04caf0d92d8524cca3c1f98d0b486e78c8fdec72`  
		Last Modified: Mon, 25 Aug 2025 21:53:21 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7570894dd8642571d29a3f9a172447dc68c92466e954fbfe509dd4c1002c62d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69821208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303120483e85eaa18d5623ff884d6ba6bc5329cf64792dafc7122ec47e98f1b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0ef49cd2af3f26990fbdb01d76c5d72224144a9082720b843066d506cd46c9`  
		Last Modified: Thu, 14 Aug 2025 04:30:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee18d4be11a0ac51fa3627c2b017b3aef767f70a39ea0d73d6de35cd618a71f`  
		Last Modified: Mon, 25 Aug 2025 19:49:07 GMT  
		Size: 5.6 MB (5603426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6551895b1ab029d74729175b98ce97b83c07b3112d073fc90b8fe101237e63`  
		Last Modified: Mon, 25 Aug 2025 19:49:09 GMT  
		Size: 1.7 MB (1738756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b87d17c36733a93bfd68173426cc2ef130e2195c9c450df58a04dc2c5fab0f`  
		Last Modified: Mon, 25 Aug 2025 19:49:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:55c648a2b1f1e4d6d07485531af3a8734047d606ae8f624a5e55a14a84c3badd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 KB (300079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cdb0bd297a9f9a841359ac15ef57a33be96fe2dae32e84f34341e6fbcf5b69`

```dockerfile
```

-	Layers:
	-	`sha256:8823ee0afb3d9696b6ca5b09a159c39bf7a8fe6690d1fb9851fe5f74584f325f`  
		Last Modified: Mon, 25 Aug 2025 21:53:25 GMT  
		Size: 279.8 KB (279843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486c238d647f7578251e57dd34ce120fb465b25780a1e60cf69ec3bd36b22be4`  
		Last Modified: Mon, 25 Aug 2025 21:53:26 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:32fa6d72e61b79987dd65c0d108e5078c0e0dc93af0460612778e63182c2076c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69951490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9745840960c0e962feb8ce93ade81f3d2d7c4014b1aa7675e1ae02d0a7aff9ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1a427e917c48b164eae3ec3692b4741f5de528261925d2e5efc62a43e5bfc4`  
		Last Modified: Mon, 28 Jul 2025 20:42:19 GMT  
		Size: 284.7 KB (284709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b50d3516e3fbf4aca43b9416e7dd8914c2623a08d12eeb55d98d72b864d50c`  
		Last Modified: Wed, 13 Aug 2025 21:40:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b905d71c6a895e4f8e02255340a28c48f2a71d4744873257004c40c0d2aa00`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.3 MB (6263485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f8b26f147c3aad964c448d6607cf74ae215e3ac1c4cbba753fa3e968275e88`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3231a1494a810504f8b0f942889fffa994e046e8e88d228e3a5088783ce72`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2afba1033f0a6e1546bfc4ba308b2a11e83940382cb23e26214953132de73502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e5578a03d1c8f2a6f8ffcbe41b2176db7f2e9fe34e3740615730082fda76c7`

```dockerfile
```

-	Layers:
	-	`sha256:748645f9a413db4552bbf182353615a0b12bcd436e3be618d281b3d593030ede`  
		Last Modified: Mon, 25 Aug 2025 21:53:30 GMT  
		Size: 276.9 KB (276903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93bc5bdadeab69d30a633aee167e91118e46d1789c6f0ffd8919e02d2abce29`  
		Last Modified: Mon, 25 Aug 2025 21:53:31 GMT  
		Size: 20.3 KB (20279 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:af183020c3351759ff8b8f4bafc2723eeff7c818144664e3694cc95a57ce5b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70304708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562175980913c7c3795d4d816c57841adf59a5bc12f44a1cd0eeb9e6e600f14a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe3e6d4a1713a75edf1789d38233b2e8d48f54cebae5e9d0789eb1af52023b`  
		Last Modified: Mon, 28 Jul 2025 20:30:54 GMT  
		Size: 285.1 KB (285114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269abe529e66aa5bca30329a5b15eb3b1dc68dbfb72494192487eabaf2c75ea7`  
		Last Modified: Wed, 13 Aug 2025 22:24:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b70f44dd4f808419f6fd44bceba6d166aca8e19f4cc6cbd8b36f33239207db`  
		Last Modified: Mon, 25 Aug 2025 19:50:03 GMT  
		Size: 6.6 MB (6550799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d7bd24bb9deffe0ca1b77e298776a06b4a558884001c7bb47966dadc97ca43`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd6fde2d426e5936d85b957d51eeee4fe29a27e410fcafc97d0874ffda5b0a7`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0aebec967107348a51c2631c5a8092b2a9ddf49e4a53aa5e56b903b7db8da90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 KB (295105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5483635ad7faac1a9e8b342df273f4ba0a4bdbe31f6c156346534eee30d30458`

```dockerfile
```

-	Layers:
	-	`sha256:41a25cf6cf15b6b37e3661b3ac34bd18681863b0b85f51cec56d1d316f0397a5`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 274.9 KB (274920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b02b106246f8f724524bb0de7288d77cf1087c013b38171b388fcaf0f37f9e0`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.10.2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:28695f2cfaee062b9a0ca60163b294c9aa426d62328db2bface2b85e282b88ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71589730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3295b1278233227188e8477c2827afae51d241b108713916b5ef77d03eb41a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27212710686629ba49777b5e0cccdf04e89cbe41c95c072e1c75381906d724e9`  
		Last Modified: Wed, 13 Aug 2025 22:25:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b7f018e46a54de4eea0e2dad72f4490579e3365d43915d3250d53ae7ec1890`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 6.5 MB (6502043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c049c1b926591fbe94ed04678a617c00476cf93094e56c118b4aa7d5301293`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8d48eb228a3be3c4a90c83ceb3a374f1cbf2cd8b2704f4bfb913c41a3321d`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.10.2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ffc6ef944b883b81dfd10aedf994982d8dabb9a7bb31e67921f976ef1da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 KB (294963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0eadd91f1fd0a0f91b5c7391ac0c55f701c738d3b6db0537f39f79f0269f79`

```dockerfile
```

-	Layers:
	-	`sha256:518491161b596d1ff8a9f6f9f6edaf63f977efff9396b1be87c42e36e666a14a`  
		Last Modified: Mon, 25 Aug 2025 21:53:42 GMT  
		Size: 274.8 KB (274848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba037ad301b98b30c070866ceb9f8b5b99f8482275c68bd46ba5664c7b6e5e90`  
		Last Modified: Mon, 25 Aug 2025 21:53:43 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.10.2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:f3fcc4c5efa8823e03e7be22f1a617cc774c603b0d8f168c048688337bdeb715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:2.10.2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:fae8c3555cf3840ff8637313f178c0317b41466226312ea50a9d597b377a982b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2397840105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5006347b108bafda0318a83f34338f8ef74ab52d118e9d335f14fcd1870a70a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 13 Aug 2025 18:06:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:06:54 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:06:55 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:07:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:07:11 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:07:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:07:18 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:08:48 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:49 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:53 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:49:54 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:50:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:50:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9380c184b3613450235fc0562d48b7c1aeb69072e1e188efd675b317114e13`  
		Last Modified: Wed, 13 Aug 2025 18:10:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb25f9f3a6b5b2e582eb535d357af7f125a5eb0d07250886e7275753bba63b`  
		Last Modified: Wed, 13 Aug 2025 18:10:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1b81a88b515880f2398d85c50e12604a0be218b43024e6273e174b171a33`  
		Last Modified: Wed, 13 Aug 2025 18:10:31 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe632c05e48eccbb4f65220b5c6cd3d2c38482c1aff7c8a70dedef13c2d8cde3`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2281e6abc340f61cf79bb6641d015955f72d05413007591f91ca52d8fcb2020b`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6aa352166614c00f1cc5419011f1a211ffaa26ece1203ddb8a7248c0f9dee1`  
		Last Modified: Wed, 13 Aug 2025 18:10:50 GMT  
		Size: 51.2 MB (51199537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36716abacdfd69d4d84aaeb498a02c39e5df07d380dc62c6f93a43dd18bd8b36`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992bb304a4c05d05ad6f9fce52e761eaca24471880c19303b2d27362b731cf77`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 335.3 KB (335287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363744c527b6172af2deba44c4735f38293dd27bc326cde515fa1e40d983cbed`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6c232258d56f8ebfb4d22b50309c11595a9cd50805699bb1edc2ff5cac8dc2`  
		Last Modified: Wed, 13 Aug 2025 18:11:01 GMT  
		Size: 62.3 MB (62261944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318c09560fb6a640397158d02fb52738a3d51b23a8f80d35724a4ece31d4cf72`  
		Last Modified: Wed, 13 Aug 2025 18:10:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1f3385040c90c1ee57f2d21940227c7a049f3442ac13a978b145cf185a15f`  
		Last Modified: Mon, 25 Aug 2025 19:50:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe569c48af273bca5f90b236956c3823ba707807419d4b3d31037b23731ca95`  
		Last Modified: Mon, 25 Aug 2025 19:50:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244ee2fe3346da9436f4b3f9faa2052570d594821c15b4458df33433e70d4cf0`  
		Last Modified: Mon, 25 Aug 2025 19:50:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bbd758a87764c779cea8fe9429c091634198b909b6faadc2c04c4add5049a0`  
		Last Modified: Mon, 25 Aug 2025 19:50:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0dab63cb896e209cbc5b4577e607d35a3df8d9e39d5dca15bc9208710b2ec`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 2.3 MB (2334479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769960fd4bcf873320f369a1ea9ae102548c30a01938b0886cbafefe311b4353`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10.2-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:c8f1420ef1f3b2c6beee3989c77169c5b35e505098aecbd8cdf91fa99cc1342e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `caddy:2.10.2-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:f0ecd5bc38691c997cfbb4eaff5bede8b9d25421e5a2fb78b50ac5fbf79f08f5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3615224351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b87c61031d564c20e4c7aadd128b369ac69af5472854d710e6709eec622c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 13 Aug 2025 18:08:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:08:27 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:08:29 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:08:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:08:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:08:50 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:10:07 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:10:07 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:56:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:56:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:56:36 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:56:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:56:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:56:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3329feb8c3f471d93f04a4afc376778f359481b9b10abd677ae7f8105b7a1982`  
		Last Modified: Wed, 13 Aug 2025 18:14:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b683ebca7e697913d8f93eeb03b85a4924fa297a5830b694441bb31e2ef2a8`  
		Last Modified: Wed, 13 Aug 2025 18:14:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a25a1b355f0af537456d6695b8cbf9c0c5582795add71831072b1f2067593`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5469c0152f4c91f8d66bd59239beec913796e4d17d8977dcf67364f6916d3aae`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9e732885c916712df386d920174e3f95dcc40377352391c6f5e8ccc9e59be5`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9ebf49453f4f127c2dffe22dcb483f4eeef5d0260fe4724472d7fc5b89ecaf`  
		Last Modified: Wed, 13 Aug 2025 18:14:25 GMT  
		Size: 51.2 MB (51223826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55bb43d7b4377e022452dadea8a547292c78952945e888b4c3a99193a0e78f`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec885b71c379ce9bdce0b6477ef6652f6b9d9f566e7e571c9863ba6adb40cede`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 351.5 KB (351496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e05cdc4ff30cbd5098771fc7b97628d410fe4d7f2afb43e7ddcd5256d51d407`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5def4f4469cc1db786df7b6975d1fc3c3bd4c534434e05e676d67edd1f0af9f`  
		Last Modified: Wed, 13 Aug 2025 18:14:22 GMT  
		Size: 62.5 MB (62477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dd29c29527d22890d7b81985987d57cceb811888344ca07659b7c0f2e94151`  
		Last Modified: Wed, 13 Aug 2025 18:14:10 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8523736186869f7a49f95f8b318bee25824ebbb010838d15db88667b969e3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb124c01828ece301417db645f6bd33502d9fa4004bbabb93d8483d9adee73fc`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc48728b561dbd7581689079fb9e459be5b1b835c2a19d3e6ad8d63472b2b7b4`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009143406fac9c3402bce23cf7487a8d83bf93fd0dacf936aa17661011450dd`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a06a632575ebdb5c471cc6aeed6865b4ed1bda3ead85aaa00ed5488712d68f3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 2.3 MB (2324141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb76a0655e886937e45d30114efbcbb8b7dcf4f622e834abea3396c37a8494`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10.2-windowsservercore`

```console
$ docker pull caddy@sha256:c2e9243204fd55beead5b9d893a8ca326f04ee4f2331dec60ad5a1d2a6992777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:2.10.2-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.10.2-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10.2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:3ebb7e7a0141c5f1434331567920cb6803bcb77417482786ce8e21cc1efad8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:2.10.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.10.2-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:eadadcb9a4804f2c2f6ace69b31243ddc25d10923eb9d7148361a38dfde75b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `caddy:2.10.2-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:64642fe1e2319c999d20aa489a73e261b5b4ae4fab29385b61e5221287af5c42
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
$ docker pull caddy@sha256:e9fd95fd7cea0c3403c622c5c2457cddcaf355a5eba11048b17cb3d99a828f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20077764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a72cdc384a6f6b8c1d99f569290cee6606bec3cca68812feba43bfda45028`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634211206164759ba5e5df423465aed056f9cc799700d15b89ca49626779515f`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 346.6 KB (346592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edccfae94f0e103409f8c3283a9e19bb7585db1ed9bd9e3a0311de9e0149c1de`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e53616944a4fa3ff99b33d90d938827b7d63bdb00324b94dab3ad40ab166831`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 15.9 MB (15923955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:30f634f6f0e9e39136903c3b81be8f780a4b805b66163bfc0e683fafb62a3f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 KB (314291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d132bcee2e485d83458421325b31111463d1718ccf62b18456e97d495bc57`

```dockerfile
```

-	Layers:
	-	`sha256:91d8c07f79d660b96ebece0d8847c92fd5160edb83b97e31865c2af067eeb8f0`  
		Last Modified: Mon, 25 Aug 2025 21:52:42 GMT  
		Size: 296.0 KB (296013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d27f4d928535909dc6d7b276be2d1e63901b6b627c43a4bfd594a0b899c110`  
		Last Modified: Mon, 25 Aug 2025 21:52:43 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bf497dbd5122b8bce808c55b47aa082eb84d06f77831adf2d8cc0b5f11e66438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18903449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ba67aa2169d0dbd6426eb009d3bd28de88cb829cb8453b2e628f0443f6e9f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8aa6aa6b1802d86bbc73e75216bbb426a1a8ebad8fab1ccf37a1adfdd1b779`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 346.5 KB (346493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3bd303b867cb629d2b99f58967b240f288c9b1dbf712003b3e56200692140c`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e6b087db3bea6b06b1a48ee30c1fc4db8efebe5b0e6670b418e3db437e8c38`  
		Last Modified: Mon, 25 Aug 2025 19:48:46 GMT  
		Size: 15.0 MB (15048518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:286477e027ad1c6350295044f9c520fa196eb08183d4939ae7ed071fc7320c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16e2d2b0cb8b273b15b42a3b1d12c77c076d757e265061f5e61b31763a6a52`

```dockerfile
```

-	Layers:
	-	`sha256:29f2ff0c73ef6349295d38ad6646decc7e0677799f04a1a1ce633e18c85a4327`  
		Last Modified: Mon, 25 Aug 2025 21:52:47 GMT  
		Size: 18.2 KB (18197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d5af7163676df0baffb41f5bce9c4f0775a69609bc2384b101ff4ba749f0050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18601748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e276120a8a2d3df3a422b6d9a2b02c16b9f92c6b28ac595c34fcc06410127c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979c078f866daa2820e22fa7f8a9cc664e49f7d538de1341a2c2c9a60489560`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 343.2 KB (343205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeca689d2f3de3a319b91d9ddb84048521f017d394555aa2ab895ef9cdb98e2`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711aca2485d7f9dfbfccd9cf2a11a6db8015c154383632363d1ac44b755cb55`  
		Last Modified: Mon, 25 Aug 2025 19:48:47 GMT  
		Size: 15.0 MB (15031978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:8049ae7cb8cf21da392232342dd2c386e8e79bb9a7093ef47dec2cd1e4d8d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 KB (314493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b289ec4bc1157ad5848221ba42af4a065fd5af769065351ada6548da41f5c1`

```dockerfile
```

-	Layers:
	-	`sha256:7653918e29fb0de220bc0644efa15394bed69ae8f40081cd705aa96205888b4c`  
		Last Modified: Mon, 25 Aug 2025 21:52:51 GMT  
		Size: 296.1 KB (296081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fb47d806abc1bee7ac987c99961bb2c58274d6cbc04b58ea4c3c026b94f2ce`  
		Last Modified: Mon, 25 Aug 2025 21:52:52 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:4c3be81b7ee70190ce5291230e5a5d4dd8ea998c44cfb5fcc4680a60ea6c5621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19013546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b37c5f2910ca9daf3b5cd9f63bb06d782d2062d4daceced81673d49fe4a1c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ebf372d05e77b4bdc3cea55c048537aaac7759aa0079ed9944004ac30c980c`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 357.7 KB (357727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f163ee242da1ec76c0ab875c407ba39c49aa3eab955a46b9ea14d94a86c4d48e`  
		Last Modified: Mon, 25 Aug 2025 19:48:51 GMT  
		Size: 7.5 KB (7492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225b3b694c911c2a8b8814871c8353f7b7686cc9ea3fc2b02dba2f45803dd75`  
		Last Modified: Mon, 25 Aug 2025 19:48:55 GMT  
		Size: 14.5 MB (14517545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a657dd5aa41ae2796a14d32f91e630f0efcefa03e3261ac63d39793887cea22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 KB (314576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469b3383a6f868625bafb61aa5dd86ccd26899761e2bdb5fafafbc7e250ef24b`

```dockerfile
```

-	Layers:
	-	`sha256:4f49301002ed8e6230d3ea527498b3328f01453f1b0e12e3bbcb7ce771cca15b`  
		Last Modified: Mon, 25 Aug 2025 21:52:55 GMT  
		Size: 296.1 KB (296117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fbb94c8995329e1c4b3235561ee976502480bebaab9183f926bf2529444c9d`  
		Last Modified: Mon, 25 Aug 2025 21:52:56 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:67112be943616a31dfbf0c815ed5325bf71a9d8c6cfe49a1935b244bd3b109e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18591170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f3d87694b9256e003a6824820cec8dfc82ad339b7d3bc41671c4996663a0a3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe739855dbbb9a1403a242cd984b1b9b4439925fb4fcedc9d3d6ade9baf3dd5`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 360.6 KB (360616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab33549ec0ff70ed9ba5ea43079d739e8d6fe698b0578958a9e2675602d1f6`  
		Last Modified: Mon, 25 Aug 2025 19:49:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6276663ba0f6c95bde9cd5440dc7ec15f6e100f8283c704efd10d02181f066dc`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 14.5 MB (14495915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:54c1de5978b47c2325c8f34e5589b9e4befd54792776c52701944ded623d9922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 KB (312470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d525e05914ec596f61ab5f038622c17b75382bd36e15638e19d2ef0b54ab4`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2fa5edceb1da7dbf0f53e0b3b6e55ebdebce9112144575d69508ba7ea1f29`  
		Last Modified: Mon, 25 Aug 2025 21:53:01 GMT  
		Size: 294.1 KB (294120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2488d35b692ff2f9eeccf6177b581e0b4012821bcd0e7079a6755296fdc31433`  
		Last Modified: Mon, 25 Aug 2025 21:53:02 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:fab4c562bd13d4fe11cc47963461b4b2f197e38afa3be8a61b698b6319238f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17956644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c209b028cc287828f645bdd0dc227ee3dbc69f503f5bf1a4ad3a944252b78b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29116abe2cb7489bfe0d514003d7c4822eaf03d2b44e5f1c10c878a603eceb13`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 348.3 KB (348289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ceaafe79989c43b373a7e7780390f12740f15ad106a2c987605998f180cea`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 7.5 KB (7498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9baf51ef7381285244300ec8288209b2b0dc82267a2c3547eb0644ce4c7948`  
		Last Modified: Fri, 18 Jul 2025 07:36:44 GMT  
		Size: 14.3 MB (14251735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:608fabfae5954b1485e44928f39c3844fbdc7de236202d87c4380838c748a018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 KB (303605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff983ccc8020f39b317500f82d9596ad6b4299338ecb828eaa0685950b57aa46`

```dockerfile
```

-	Layers:
	-	`sha256:090b4908e38667b8110e66242c7d88a6c27ba9f8dc2ebc126e04430fcaff531c`  
		Last Modified: Fri, 18 Jul 2025 09:52:30 GMT  
		Size: 285.3 KB (285255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e87f231dbdaabee2c8a7c7375c70ff7387e5d2387ed1a26033f1a9b77c0e427`  
		Last Modified: Fri, 18 Jul 2025 09:52:31 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:df924d28949f8a3be699c88ab40eb6b5ca37234e6af5431cb6a1cca63e58a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19362618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85040edfc178cf9c5de8611792e65c67f07629a5c76b7089bf0828d075163a0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff98415fc23c99d5ff9b731b3ed1f5f263fca7f05ddbb51c47d7d8b6df1f89e8`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 353.5 KB (353456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e6340a3b7a63c6c76d521ec65f90ba0718a26fb02520f02216f158300c89e`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd56c657dc325cdf0a5d0c300a1380b0fe6abd98dcee92bcf38b02d14d579062`  
		Last Modified: Mon, 25 Aug 2025 19:51:46 GMT  
		Size: 15.4 MB (15356663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ce406a252aedd52a38cc6938d993637d83f2aedbe10e9eb385f4b60a12418812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 KB (312340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190d69bf6d55a424c64ecfe71fedbf83d368d2191338ab24083d5426fa60e861`

```dockerfile
```

-	Layers:
	-	`sha256:ea8886b3a4622ffdcc38a8a441716fbb95afc7feb55738ebaae75b137a193925`  
		Last Modified: Mon, 25 Aug 2025 21:53:08 GMT  
		Size: 294.1 KB (294062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5011fab561f7f812f810ba45504c8489c7a5e0383d88863c43b47478a136a21a`  
		Last Modified: Mon, 25 Aug 2025 21:53:09 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder`

```console
$ docker pull caddy@sha256:38708d13dba3aafb83ed97d8b1f9ed00823a6d0eb63de314945a55ada80db2d8
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
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:baa56c9394d7025fb7e344f5a1d52c7d0ae2a428a6d8e4d7acf85480477cf819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72186376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0205b23d29755cb0085885d9fa3ac1ea66ce75020051c0185f423ea947bc24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d4ca09441bdb9129d5708d2aa8802e233b2d11d1797317158c4095e9df8fc`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 282.4 KB (282437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18414ed0f6669fd1d6e137922f2a57e37aaf0a63ae6968c499fe69b17d148d14`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36dd3b7005cdf211c5d6cd7f47820b1ffa15134a87c84b500f754613863411`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.2 MB (6211320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc4a072890c37012160bb87d003d188e34244b09f60d9a7e33a521175aa4914`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.8 MB (1846494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45676fbd1b151c4eb76c6df8afe515dd1b8001736b55aba9841182177b17`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:f5d337972eff4ad3e0c109de0443e6695887aae29e94c1df6e6189ef17e777df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3035b7074d5121642859847a37b0e722a8cb9137408b7356cf5e5a79d0a6760c`

```dockerfile
```

-	Layers:
	-	`sha256:f41e395e3e21569a16f8d91a8825c71ee9146373ca8d37c13d6e6de553f55627`  
		Last Modified: Mon, 25 Aug 2025 21:53:16 GMT  
		Size: 276.8 KB (276799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a6e841ccf0c2ac296066a2cd3354ab00dcc598ae922e619237f17aebd1bb82`  
		Last Modified: Mon, 25 Aug 2025 21:53:17 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e1edbceed451136633244ae771982f55dd7d7218a4ffc50369af9eefbb5266a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70630913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8be52c140ce9073b5e99046435e6d10435d169d31239bff87fc88de3e317a56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b30dde5a6a0bd25a99ef148aafdaf794991c98c7b0798149f6d4e21ebc6ccd`  
		Last Modified: Wed, 13 Aug 2025 19:12:26 GMT  
		Size: 59.0 MB (58976836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63714916874ab7e10bdc757c1f8a9e57104a40067c294f970c9d8ff49423866`  
		Last Modified: Wed, 13 Aug 2025 18:04:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96b63bb94735bf5a233756bdc50074d4de4f13340afa4a5b52a444075d8471d`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 6.1 MB (6124248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cae36cb0796b19b218d007f943c4a58a98847586c215d0b9182edb25f4b08`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d14e3b2c944638da45ebffd7d320249acf6ca96e796a9c2aaee17c71e23a4d`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:b2b71368948bedcdbe1fe1b49cbffe11bca901b908dde0561b73953dad703bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b200e21ab8337407084c2f915782c003a30ed1b357ddf279a1faf52f479fd277`

```dockerfile
```

-	Layers:
	-	`sha256:995e27d2c9f18e3d1278c03b04caf0d92d8524cca3c1f98d0b486e78c8fdec72`  
		Last Modified: Mon, 25 Aug 2025 21:53:21 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7570894dd8642571d29a3f9a172447dc68c92466e954fbfe509dd4c1002c62d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69821208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303120483e85eaa18d5623ff884d6ba6bc5329cf64792dafc7122ec47e98f1b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0ef49cd2af3f26990fbdb01d76c5d72224144a9082720b843066d506cd46c9`  
		Last Modified: Thu, 14 Aug 2025 04:30:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee18d4be11a0ac51fa3627c2b017b3aef767f70a39ea0d73d6de35cd618a71f`  
		Last Modified: Mon, 25 Aug 2025 19:49:07 GMT  
		Size: 5.6 MB (5603426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6551895b1ab029d74729175b98ce97b83c07b3112d073fc90b8fe101237e63`  
		Last Modified: Mon, 25 Aug 2025 19:49:09 GMT  
		Size: 1.7 MB (1738756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b87d17c36733a93bfd68173426cc2ef130e2195c9c450df58a04dc2c5fab0f`  
		Last Modified: Mon, 25 Aug 2025 19:49:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:55c648a2b1f1e4d6d07485531af3a8734047d606ae8f624a5e55a14a84c3badd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 KB (300079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cdb0bd297a9f9a841359ac15ef57a33be96fe2dae32e84f34341e6fbcf5b69`

```dockerfile
```

-	Layers:
	-	`sha256:8823ee0afb3d9696b6ca5b09a159c39bf7a8fe6690d1fb9851fe5f74584f325f`  
		Last Modified: Mon, 25 Aug 2025 21:53:25 GMT  
		Size: 279.8 KB (279843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486c238d647f7578251e57dd34ce120fb465b25780a1e60cf69ec3bd36b22be4`  
		Last Modified: Mon, 25 Aug 2025 21:53:26 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:32fa6d72e61b79987dd65c0d108e5078c0e0dc93af0460612778e63182c2076c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69951490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9745840960c0e962feb8ce93ade81f3d2d7c4014b1aa7675e1ae02d0a7aff9ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1a427e917c48b164eae3ec3692b4741f5de528261925d2e5efc62a43e5bfc4`  
		Last Modified: Mon, 28 Jul 2025 20:42:19 GMT  
		Size: 284.7 KB (284709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b50d3516e3fbf4aca43b9416e7dd8914c2623a08d12eeb55d98d72b864d50c`  
		Last Modified: Wed, 13 Aug 2025 21:40:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b905d71c6a895e4f8e02255340a28c48f2a71d4744873257004c40c0d2aa00`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.3 MB (6263485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f8b26f147c3aad964c448d6607cf74ae215e3ac1c4cbba753fa3e968275e88`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3231a1494a810504f8b0f942889fffa994e046e8e88d228e3a5088783ce72`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:2afba1033f0a6e1546bfc4ba308b2a11e83940382cb23e26214953132de73502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e5578a03d1c8f2a6f8ffcbe41b2176db7f2e9fe34e3740615730082fda76c7`

```dockerfile
```

-	Layers:
	-	`sha256:748645f9a413db4552bbf182353615a0b12bcd436e3be618d281b3d593030ede`  
		Last Modified: Mon, 25 Aug 2025 21:53:30 GMT  
		Size: 276.9 KB (276903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93bc5bdadeab69d30a633aee167e91118e46d1789c6f0ffd8919e02d2abce29`  
		Last Modified: Mon, 25 Aug 2025 21:53:31 GMT  
		Size: 20.3 KB (20279 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:af183020c3351759ff8b8f4bafc2723eeff7c818144664e3694cc95a57ce5b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70304708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562175980913c7c3795d4d816c57841adf59a5bc12f44a1cd0eeb9e6e600f14a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe3e6d4a1713a75edf1789d38233b2e8d48f54cebae5e9d0789eb1af52023b`  
		Last Modified: Mon, 28 Jul 2025 20:30:54 GMT  
		Size: 285.1 KB (285114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269abe529e66aa5bca30329a5b15eb3b1dc68dbfb72494192487eabaf2c75ea7`  
		Last Modified: Wed, 13 Aug 2025 22:24:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b70f44dd4f808419f6fd44bceba6d166aca8e19f4cc6cbd8b36f33239207db`  
		Last Modified: Mon, 25 Aug 2025 19:50:03 GMT  
		Size: 6.6 MB (6550799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d7bd24bb9deffe0ca1b77e298776a06b4a558884001c7bb47966dadc97ca43`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd6fde2d426e5936d85b957d51eeee4fe29a27e410fcafc97d0874ffda5b0a7`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0aebec967107348a51c2631c5a8092b2a9ddf49e4a53aa5e56b903b7db8da90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 KB (295105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5483635ad7faac1a9e8b342df273f4ba0a4bdbe31f6c156346534eee30d30458`

```dockerfile
```

-	Layers:
	-	`sha256:41a25cf6cf15b6b37e3661b3ac34bd18681863b0b85f51cec56d1d316f0397a5`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 274.9 KB (274920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b02b106246f8f724524bb0de7288d77cf1087c013b38171b388fcaf0f37f9e0`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; riscv64

```console
$ docker pull caddy@sha256:fb87571ab0cfe463d5b70a18f7fc659670b5c55747db3031ea04cb59192007d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87901339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc43b273027a52c8474444595317de4089d1356a37708213bb7d600ddde35e7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03fbadbe664ad3d80e3509b96250ae628b3c572ce60e514d1ab20170b9d16f`  
		Last Modified: Wed, 06 Aug 2025 20:35:39 GMT  
		Size: 76.3 MB (76329537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3100604e2ac3ab2afb5cfbb5b614bf8a221677bd8062fec6e7c8d427bd3a227`  
		Last Modified: Wed, 06 Aug 2025 20:38:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7fcb5eb3236cdaf4c847395cb3593f761279c79096d30f3e7cf35380880458`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 6.2 MB (6227728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ffbcd6b9606b2af427eeec605dcacf7cd7d3373be452b10e2bb22f249781e`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 1.7 MB (1711639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cfb2de1c2d535f5db75d479624e79d3c03d09237fa02bfe0e3cdaca96319d6`  
		Last Modified: Wed, 06 Aug 2025 21:55:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e726fabc45a470f841e6101b22886180e210ce12d35e7294ff41bda3d5fca48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 KB (310664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b2a779549901a2e89720d3b51ed603f8cad90098f71519ddbb0679b33cb68`

```dockerfile
```

-	Layers:
	-	`sha256:ccc7ede165f095820a25ffb389a248d0b37c8e904fc5ab03cd1183fef473c6fd`  
		Last Modified: Thu, 07 Aug 2025 00:52:47 GMT  
		Size: 290.5 KB (290479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f30acaaa6bd313ee7a3e5ee0cf46680343b632c7fc49a20989d0b539919b4f`  
		Last Modified: Thu, 07 Aug 2025 00:52:48 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:28695f2cfaee062b9a0ca60163b294c9aa426d62328db2bface2b85e282b88ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71589730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3295b1278233227188e8477c2827afae51d241b108713916b5ef77d03eb41a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27212710686629ba49777b5e0cccdf04e89cbe41c95c072e1c75381906d724e9`  
		Last Modified: Wed, 13 Aug 2025 22:25:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b7f018e46a54de4eea0e2dad72f4490579e3365d43915d3250d53ae7ec1890`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 6.5 MB (6502043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c049c1b926591fbe94ed04678a617c00476cf93094e56c118b4aa7d5301293`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8d48eb228a3be3c4a90c83ceb3a374f1cbf2cd8b2704f4bfb913c41a3321d`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ffc6ef944b883b81dfd10aedf994982d8dabb9a7bb31e67921f976ef1da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 KB (294963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0eadd91f1fd0a0f91b5c7391ac0c55f701c738d3b6db0537f39f79f0269f79`

```dockerfile
```

-	Layers:
	-	`sha256:518491161b596d1ff8a9f6f9f6edaf63f977efff9396b1be87c42e36e666a14a`  
		Last Modified: Mon, 25 Aug 2025 21:53:42 GMT  
		Size: 274.8 KB (274848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba037ad301b98b30c070866ceb9f8b5b99f8482275c68bd46ba5664c7b6e5e90`  
		Last Modified: Mon, 25 Aug 2025 21:53:43 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:f0ecd5bc38691c997cfbb4eaff5bede8b9d25421e5a2fb78b50ac5fbf79f08f5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3615224351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b87c61031d564c20e4c7aadd128b369ac69af5472854d710e6709eec622c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 13 Aug 2025 18:08:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:08:27 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:08:29 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:08:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:08:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:08:50 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:10:07 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:10:07 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:56:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:56:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:56:36 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:56:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:56:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:56:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3329feb8c3f471d93f04a4afc376778f359481b9b10abd677ae7f8105b7a1982`  
		Last Modified: Wed, 13 Aug 2025 18:14:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b683ebca7e697913d8f93eeb03b85a4924fa297a5830b694441bb31e2ef2a8`  
		Last Modified: Wed, 13 Aug 2025 18:14:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a25a1b355f0af537456d6695b8cbf9c0c5582795add71831072b1f2067593`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5469c0152f4c91f8d66bd59239beec913796e4d17d8977dcf67364f6916d3aae`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9e732885c916712df386d920174e3f95dcc40377352391c6f5e8ccc9e59be5`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9ebf49453f4f127c2dffe22dcb483f4eeef5d0260fe4724472d7fc5b89ecaf`  
		Last Modified: Wed, 13 Aug 2025 18:14:25 GMT  
		Size: 51.2 MB (51223826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55bb43d7b4377e022452dadea8a547292c78952945e888b4c3a99193a0e78f`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec885b71c379ce9bdce0b6477ef6652f6b9d9f566e7e571c9863ba6adb40cede`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 351.5 KB (351496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e05cdc4ff30cbd5098771fc7b97628d410fe4d7f2afb43e7ddcd5256d51d407`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5def4f4469cc1db786df7b6975d1fc3c3bd4c534434e05e676d67edd1f0af9f`  
		Last Modified: Wed, 13 Aug 2025 18:14:22 GMT  
		Size: 62.5 MB (62477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dd29c29527d22890d7b81985987d57cceb811888344ca07659b7c0f2e94151`  
		Last Modified: Wed, 13 Aug 2025 18:14:10 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8523736186869f7a49f95f8b318bee25824ebbb010838d15db88667b969e3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb124c01828ece301417db645f6bd33502d9fa4004bbabb93d8483d9adee73fc`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc48728b561dbd7581689079fb9e459be5b1b835c2a19d3e6ad8d63472b2b7b4`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009143406fac9c3402bce23cf7487a8d83bf93fd0dacf936aa17661011450dd`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a06a632575ebdb5c471cc6aeed6865b4ed1bda3ead85aaa00ed5488712d68f3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 2.3 MB (2324141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb76a0655e886937e45d30114efbcbb8b7dcf4f622e834abea3396c37a8494`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:fae8c3555cf3840ff8637313f178c0317b41466226312ea50a9d597b377a982b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2397840105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5006347b108bafda0318a83f34338f8ef74ab52d118e9d335f14fcd1870a70a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 13 Aug 2025 18:06:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:06:54 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:06:55 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:07:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:07:11 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:07:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:07:18 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:08:48 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:49 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:53 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:49:54 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:50:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:50:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9380c184b3613450235fc0562d48b7c1aeb69072e1e188efd675b317114e13`  
		Last Modified: Wed, 13 Aug 2025 18:10:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb25f9f3a6b5b2e582eb535d357af7f125a5eb0d07250886e7275753bba63b`  
		Last Modified: Wed, 13 Aug 2025 18:10:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1b81a88b515880f2398d85c50e12604a0be218b43024e6273e174b171a33`  
		Last Modified: Wed, 13 Aug 2025 18:10:31 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe632c05e48eccbb4f65220b5c6cd3d2c38482c1aff7c8a70dedef13c2d8cde3`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2281e6abc340f61cf79bb6641d015955f72d05413007591f91ca52d8fcb2020b`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6aa352166614c00f1cc5419011f1a211ffaa26ece1203ddb8a7248c0f9dee1`  
		Last Modified: Wed, 13 Aug 2025 18:10:50 GMT  
		Size: 51.2 MB (51199537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36716abacdfd69d4d84aaeb498a02c39e5df07d380dc62c6f93a43dd18bd8b36`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992bb304a4c05d05ad6f9fce52e761eaca24471880c19303b2d27362b731cf77`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 335.3 KB (335287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363744c527b6172af2deba44c4735f38293dd27bc326cde515fa1e40d983cbed`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6c232258d56f8ebfb4d22b50309c11595a9cd50805699bb1edc2ff5cac8dc2`  
		Last Modified: Wed, 13 Aug 2025 18:11:01 GMT  
		Size: 62.3 MB (62261944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318c09560fb6a640397158d02fb52738a3d51b23a8f80d35724a4ece31d4cf72`  
		Last Modified: Wed, 13 Aug 2025 18:10:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1f3385040c90c1ee57f2d21940227c7a049f3442ac13a978b145cf185a15f`  
		Last Modified: Mon, 25 Aug 2025 19:50:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe569c48af273bca5f90b236956c3823ba707807419d4b3d31037b23731ca95`  
		Last Modified: Mon, 25 Aug 2025 19:50:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244ee2fe3346da9436f4b3f9faa2052570d594821c15b4458df33433e70d4cf0`  
		Last Modified: Mon, 25 Aug 2025 19:50:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bbd758a87764c779cea8fe9429c091634198b909b6faadc2c04c4add5049a0`  
		Last Modified: Mon, 25 Aug 2025 19:50:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0dab63cb896e209cbc5b4577e607d35a3df8d9e39d5dca15bc9208710b2ec`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 2.3 MB (2334479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769960fd4bcf873320f369a1ea9ae102548c30a01938b0886cbafefe311b4353`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:2cf9b153f9f65bc7dbaef420968aee70bc0c9e570b2c217777014e1c329de416
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

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:baa56c9394d7025fb7e344f5a1d52c7d0ae2a428a6d8e4d7acf85480477cf819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72186376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0205b23d29755cb0085885d9fa3ac1ea66ce75020051c0185f423ea947bc24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d4ca09441bdb9129d5708d2aa8802e233b2d11d1797317158c4095e9df8fc`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 282.4 KB (282437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8286cb4ece30afb97c398c2b5ac1f35e8f502f758d4ea2fc69e179efdf471ea2`  
		Last Modified: Wed, 13 Aug 2025 18:08:40 GMT  
		Size: 60.0 MB (60045848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18414ed0f6669fd1d6e137922f2a57e37aaf0a63ae6968c499fe69b17d148d14`  
		Last Modified: Wed, 13 Aug 2025 18:04:51 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36dd3b7005cdf211c5d6cd7f47820b1ffa15134a87c84b500f754613863411`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.2 MB (6211320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc4a072890c37012160bb87d003d188e34244b09f60d9a7e33a521175aa4914`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.8 MB (1846494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45676fbd1b151c4eb76c6df8afe515dd1b8001736b55aba9841182177b17`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f5d337972eff4ad3e0c109de0443e6695887aae29e94c1df6e6189ef17e777df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3035b7074d5121642859847a37b0e722a8cb9137408b7356cf5e5a79d0a6760c`

```dockerfile
```

-	Layers:
	-	`sha256:f41e395e3e21569a16f8d91a8825c71ee9146373ca8d37c13d6e6de553f55627`  
		Last Modified: Mon, 25 Aug 2025 21:53:16 GMT  
		Size: 276.8 KB (276799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a6e841ccf0c2ac296066a2cd3354ab00dcc598ae922e619237f17aebd1bb82`  
		Last Modified: Mon, 25 Aug 2025 21:53:17 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e1edbceed451136633244ae771982f55dd7d7218a4ffc50369af9eefbb5266a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70630913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8be52c140ce9073b5e99046435e6d10435d169d31239bff87fc88de3e317a56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b30dde5a6a0bd25a99ef148aafdaf794991c98c7b0798149f6d4e21ebc6ccd`  
		Last Modified: Wed, 13 Aug 2025 19:12:26 GMT  
		Size: 59.0 MB (58976836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63714916874ab7e10bdc757c1f8a9e57104a40067c294f970c9d8ff49423866`  
		Last Modified: Wed, 13 Aug 2025 18:04:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96b63bb94735bf5a233756bdc50074d4de4f13340afa4a5b52a444075d8471d`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 6.1 MB (6124248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cae36cb0796b19b218d007f943c4a58a98847586c215d0b9182edb25f4b08`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d14e3b2c944638da45ebffd7d320249acf6ca96e796a9c2aaee17c71e23a4d`  
		Last Modified: Mon, 25 Aug 2025 19:48:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b2b71368948bedcdbe1fe1b49cbffe11bca901b908dde0561b73953dad703bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b200e21ab8337407084c2f915782c003a30ed1b357ddf279a1faf52f479fd277`

```dockerfile
```

-	Layers:
	-	`sha256:995e27d2c9f18e3d1278c03b04caf0d92d8524cca3c1f98d0b486e78c8fdec72`  
		Last Modified: Mon, 25 Aug 2025 21:53:21 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7570894dd8642571d29a3f9a172447dc68c92466e954fbfe509dd4c1002c62d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69821208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303120483e85eaa18d5623ff884d6ba6bc5329cf64792dafc7122ec47e98f1b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40990d62f227f942f866b61a81f9d06439ba9007695b28805e3327d6605b42`  
		Last Modified: Thu, 14 Aug 2025 05:22:36 GMT  
		Size: 59.0 MB (58976912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0ef49cd2af3f26990fbdb01d76c5d72224144a9082720b843066d506cd46c9`  
		Last Modified: Thu, 14 Aug 2025 04:30:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee18d4be11a0ac51fa3627c2b017b3aef767f70a39ea0d73d6de35cd618a71f`  
		Last Modified: Mon, 25 Aug 2025 19:49:07 GMT  
		Size: 5.6 MB (5603426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6551895b1ab029d74729175b98ce97b83c07b3112d073fc90b8fe101237e63`  
		Last Modified: Mon, 25 Aug 2025 19:49:09 GMT  
		Size: 1.7 MB (1738756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b87d17c36733a93bfd68173426cc2ef130e2195c9c450df58a04dc2c5fab0f`  
		Last Modified: Mon, 25 Aug 2025 19:49:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:55c648a2b1f1e4d6d07485531af3a8734047d606ae8f624a5e55a14a84c3badd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 KB (300079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cdb0bd297a9f9a841359ac15ef57a33be96fe2dae32e84f34341e6fbcf5b69`

```dockerfile
```

-	Layers:
	-	`sha256:8823ee0afb3d9696b6ca5b09a159c39bf7a8fe6690d1fb9851fe5f74584f325f`  
		Last Modified: Mon, 25 Aug 2025 21:53:25 GMT  
		Size: 279.8 KB (279843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486c238d647f7578251e57dd34ce120fb465b25780a1e60cf69ec3bd36b22be4`  
		Last Modified: Mon, 25 Aug 2025 21:53:26 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:32fa6d72e61b79987dd65c0d108e5078c0e0dc93af0460612778e63182c2076c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69951490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9745840960c0e962feb8ce93ade81f3d2d7c4014b1aa7675e1ae02d0a7aff9ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1a427e917c48b164eae3ec3692b4741f5de528261925d2e5efc62a43e5bfc4`  
		Last Modified: Mon, 28 Jul 2025 20:42:19 GMT  
		Size: 284.7 KB (284709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f102543fc427310b92904023d73fa466d96754c15846c2fda90d69bc03afe1`  
		Last Modified: Wed, 13 Aug 2025 20:54:25 GMT  
		Size: 57.6 MB (57555575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b50d3516e3fbf4aca43b9416e7dd8914c2623a08d12eeb55d98d72b864d50c`  
		Last Modified: Wed, 13 Aug 2025 21:40:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b905d71c6a895e4f8e02255340a28c48f2a71d4744873257004c40c0d2aa00`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 6.3 MB (6263485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f8b26f147c3aad964c448d6607cf74ae215e3ac1c4cbba753fa3e968275e88`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3231a1494a810504f8b0f942889fffa994e046e8e88d228e3a5088783ce72`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2afba1033f0a6e1546bfc4ba308b2a11e83940382cb23e26214953132de73502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e5578a03d1c8f2a6f8ffcbe41b2176db7f2e9fe34e3740615730082fda76c7`

```dockerfile
```

-	Layers:
	-	`sha256:748645f9a413db4552bbf182353615a0b12bcd436e3be618d281b3d593030ede`  
		Last Modified: Mon, 25 Aug 2025 21:53:30 GMT  
		Size: 276.9 KB (276903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93bc5bdadeab69d30a633aee167e91118e46d1789c6f0ffd8919e02d2abce29`  
		Last Modified: Mon, 25 Aug 2025 21:53:31 GMT  
		Size: 20.3 KB (20279 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:af183020c3351759ff8b8f4bafc2723eeff7c818144664e3694cc95a57ce5b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70304708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562175980913c7c3795d4d816c57841adf59a5bc12f44a1cd0eeb9e6e600f14a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe3e6d4a1713a75edf1789d38233b2e8d48f54cebae5e9d0789eb1af52023b`  
		Last Modified: Mon, 28 Jul 2025 20:30:54 GMT  
		Size: 285.1 KB (285114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2c76c6195950ea309dc7dfde36fe89df8c2158d0e0ae2a9e7ba3c8dbe9bbe`  
		Last Modified: Wed, 13 Aug 2025 22:24:39 GMT  
		Size: 58.0 MB (58035100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269abe529e66aa5bca30329a5b15eb3b1dc68dbfb72494192487eabaf2c75ea7`  
		Last Modified: Wed, 13 Aug 2025 22:24:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b70f44dd4f808419f6fd44bceba6d166aca8e19f4cc6cbd8b36f33239207db`  
		Last Modified: Mon, 25 Aug 2025 19:50:03 GMT  
		Size: 6.6 MB (6550799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d7bd24bb9deffe0ca1b77e298776a06b4a558884001c7bb47966dadc97ca43`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd6fde2d426e5936d85b957d51eeee4fe29a27e410fcafc97d0874ffda5b0a7`  
		Last Modified: Mon, 25 Aug 2025 19:50:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0aebec967107348a51c2631c5a8092b2a9ddf49e4a53aa5e56b903b7db8da90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 KB (295105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5483635ad7faac1a9e8b342df273f4ba0a4bdbe31f6c156346534eee30d30458`

```dockerfile
```

-	Layers:
	-	`sha256:41a25cf6cf15b6b37e3661b3ac34bd18681863b0b85f51cec56d1d316f0397a5`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 274.9 KB (274920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b02b106246f8f724524bb0de7288d77cf1087c013b38171b388fcaf0f37f9e0`  
		Last Modified: Mon, 25 Aug 2025 21:53:35 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:fb87571ab0cfe463d5b70a18f7fc659670b5c55747db3031ea04cb59192007d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87901339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc43b273027a52c8474444595317de4089d1356a37708213bb7d600ddde35e7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOLANG_VERSION=1.24.6
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOTOOLCHAIN=local
# Sat, 19 Apr 2025 03:51:58 GMT
ENV GOPATH=/go
# Sat, 19 Apr 2025 03:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Apr 2025 03:51:58 GMT
COPY /target/ / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /go
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XCADDY_SETCAP=1
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03fbadbe664ad3d80e3509b96250ae628b3c572ce60e514d1ab20170b9d16f`  
		Last Modified: Wed, 06 Aug 2025 20:35:39 GMT  
		Size: 76.3 MB (76329537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3100604e2ac3ab2afb5cfbb5b614bf8a221677bd8062fec6e7c8d427bd3a227`  
		Last Modified: Wed, 06 Aug 2025 20:38:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7fcb5eb3236cdaf4c847395cb3593f761279c79096d30f3e7cf35380880458`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 6.2 MB (6227728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ffbcd6b9606b2af427eeec605dcacf7cd7d3373be452b10e2bb22f249781e`  
		Last Modified: Wed, 06 Aug 2025 21:55:35 GMT  
		Size: 1.7 MB (1711639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cfb2de1c2d535f5db75d479624e79d3c03d09237fa02bfe0e3cdaca96319d6`  
		Last Modified: Wed, 06 Aug 2025 21:55:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e726fabc45a470f841e6101b22886180e210ce12d35e7294ff41bda3d5fca48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 KB (310664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b2a779549901a2e89720d3b51ed603f8cad90098f71519ddbb0679b33cb68`

```dockerfile
```

-	Layers:
	-	`sha256:ccc7ede165f095820a25ffb389a248d0b37c8e904fc5ab03cd1183fef473c6fd`  
		Last Modified: Thu, 07 Aug 2025 00:52:47 GMT  
		Size: 290.5 KB (290479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f30acaaa6bd313ee7a3e5ee0cf46680343b632c7fc49a20989d0b539919b4f`  
		Last Modified: Thu, 07 Aug 2025 00:52:48 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:28695f2cfaee062b9a0ca60163b294c9aa426d62328db2bface2b85e282b88ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71589730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3295b1278233227188e8477c2827afae51d241b108713916b5ef77d03eb41a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27212710686629ba49777b5e0cccdf04e89cbe41c95c072e1c75381906d724e9`  
		Last Modified: Wed, 13 Aug 2025 22:25:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b7f018e46a54de4eea0e2dad72f4490579e3365d43915d3250d53ae7ec1890`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 6.5 MB (6502043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c049c1b926591fbe94ed04678a617c00476cf93094e56c118b4aa7d5301293`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b8d48eb228a3be3c4a90c83ceb3a374f1cbf2cd8b2704f4bfb913c41a3321d`  
		Last Modified: Mon, 25 Aug 2025 19:52:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ffc6ef944b883b81dfd10aedf994982d8dabb9a7bb31e67921f976ef1da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 KB (294963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0eadd91f1fd0a0f91b5c7391ac0c55f701c738d3b6db0537f39f79f0269f79`

```dockerfile
```

-	Layers:
	-	`sha256:518491161b596d1ff8a9f6f9f6edaf63f977efff9396b1be87c42e36e666a14a`  
		Last Modified: Mon, 25 Aug 2025 21:53:42 GMT  
		Size: 274.8 KB (274848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba037ad301b98b30c070866ceb9f8b5b99f8482275c68bd46ba5664c7b6e5e90`  
		Last Modified: Mon, 25 Aug 2025 21:53:43 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:f3fcc4c5efa8823e03e7be22f1a617cc774c603b0d8f168c048688337bdeb715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:fae8c3555cf3840ff8637313f178c0317b41466226312ea50a9d597b377a982b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2397840105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5006347b108bafda0318a83f34338f8ef74ab52d118e9d335f14fcd1870a70a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 13 Aug 2025 18:06:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:06:54 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:06:55 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:07:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:07:11 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:07:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:07:18 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:08:48 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:49 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:53 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:49:54 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:50:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:50:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9380c184b3613450235fc0562d48b7c1aeb69072e1e188efd675b317114e13`  
		Last Modified: Wed, 13 Aug 2025 18:10:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb25f9f3a6b5b2e582eb535d357af7f125a5eb0d07250886e7275753bba63b`  
		Last Modified: Wed, 13 Aug 2025 18:10:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1b81a88b515880f2398d85c50e12604a0be218b43024e6273e174b171a33`  
		Last Modified: Wed, 13 Aug 2025 18:10:31 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe632c05e48eccbb4f65220b5c6cd3d2c38482c1aff7c8a70dedef13c2d8cde3`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2281e6abc340f61cf79bb6641d015955f72d05413007591f91ca52d8fcb2020b`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6aa352166614c00f1cc5419011f1a211ffaa26ece1203ddb8a7248c0f9dee1`  
		Last Modified: Wed, 13 Aug 2025 18:10:50 GMT  
		Size: 51.2 MB (51199537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36716abacdfd69d4d84aaeb498a02c39e5df07d380dc62c6f93a43dd18bd8b36`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992bb304a4c05d05ad6f9fce52e761eaca24471880c19303b2d27362b731cf77`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 335.3 KB (335287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363744c527b6172af2deba44c4735f38293dd27bc326cde515fa1e40d983cbed`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6c232258d56f8ebfb4d22b50309c11595a9cd50805699bb1edc2ff5cac8dc2`  
		Last Modified: Wed, 13 Aug 2025 18:11:01 GMT  
		Size: 62.3 MB (62261944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318c09560fb6a640397158d02fb52738a3d51b23a8f80d35724a4ece31d4cf72`  
		Last Modified: Wed, 13 Aug 2025 18:10:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1f3385040c90c1ee57f2d21940227c7a049f3442ac13a978b145cf185a15f`  
		Last Modified: Mon, 25 Aug 2025 19:50:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe569c48af273bca5f90b236956c3823ba707807419d4b3d31037b23731ca95`  
		Last Modified: Mon, 25 Aug 2025 19:50:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244ee2fe3346da9436f4b3f9faa2052570d594821c15b4458df33433e70d4cf0`  
		Last Modified: Mon, 25 Aug 2025 19:50:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bbd758a87764c779cea8fe9429c091634198b909b6faadc2c04c4add5049a0`  
		Last Modified: Mon, 25 Aug 2025 19:50:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0dab63cb896e209cbc5b4577e607d35a3df8d9e39d5dca15bc9208710b2ec`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 2.3 MB (2334479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769960fd4bcf873320f369a1ea9ae102548c30a01938b0886cbafefe311b4353`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:c8f1420ef1f3b2c6beee3989c77169c5b35e505098aecbd8cdf91fa99cc1342e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `caddy:builder-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:f0ecd5bc38691c997cfbb4eaff5bede8b9d25421e5a2fb78b50ac5fbf79f08f5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3615224351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b87c61031d564c20e4c7aadd128b369ac69af5472854d710e6709eec622c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 13 Aug 2025 18:08:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:08:27 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:08:29 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:08:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:08:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:08:50 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:10:07 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:10:07 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:56:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:56:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:56:36 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:56:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:56:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:56:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3329feb8c3f471d93f04a4afc376778f359481b9b10abd677ae7f8105b7a1982`  
		Last Modified: Wed, 13 Aug 2025 18:14:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b683ebca7e697913d8f93eeb03b85a4924fa297a5830b694441bb31e2ef2a8`  
		Last Modified: Wed, 13 Aug 2025 18:14:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a25a1b355f0af537456d6695b8cbf9c0c5582795add71831072b1f2067593`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5469c0152f4c91f8d66bd59239beec913796e4d17d8977dcf67364f6916d3aae`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9e732885c916712df386d920174e3f95dcc40377352391c6f5e8ccc9e59be5`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9ebf49453f4f127c2dffe22dcb483f4eeef5d0260fe4724472d7fc5b89ecaf`  
		Last Modified: Wed, 13 Aug 2025 18:14:25 GMT  
		Size: 51.2 MB (51223826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55bb43d7b4377e022452dadea8a547292c78952945e888b4c3a99193a0e78f`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec885b71c379ce9bdce0b6477ef6652f6b9d9f566e7e571c9863ba6adb40cede`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 351.5 KB (351496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e05cdc4ff30cbd5098771fc7b97628d410fe4d7f2afb43e7ddcd5256d51d407`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5def4f4469cc1db786df7b6975d1fc3c3bd4c534434e05e676d67edd1f0af9f`  
		Last Modified: Wed, 13 Aug 2025 18:14:22 GMT  
		Size: 62.5 MB (62477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dd29c29527d22890d7b81985987d57cceb811888344ca07659b7c0f2e94151`  
		Last Modified: Wed, 13 Aug 2025 18:14:10 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8523736186869f7a49f95f8b318bee25824ebbb010838d15db88667b969e3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb124c01828ece301417db645f6bd33502d9fa4004bbabb93d8483d9adee73fc`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc48728b561dbd7581689079fb9e459be5b1b835c2a19d3e6ad8d63472b2b7b4`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009143406fac9c3402bce23cf7487a8d83bf93fd0dacf936aa17661011450dd`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a06a632575ebdb5c471cc6aeed6865b4ed1bda3ead85aaa00ed5488712d68f3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 2.3 MB (2324141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb76a0655e886937e45d30114efbcbb8b7dcf4f622e834abea3396c37a8494`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:73ba793f1b2355cfefe2a7ec53ac2f2db0531bf52679deaf16df087fd35ce4ea
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
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:e9fd95fd7cea0c3403c622c5c2457cddcaf355a5eba11048b17cb3d99a828f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20077764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a72cdc384a6f6b8c1d99f569290cee6606bec3cca68812feba43bfda45028`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634211206164759ba5e5df423465aed056f9cc799700d15b89ca49626779515f`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 346.6 KB (346592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edccfae94f0e103409f8c3283a9e19bb7585db1ed9bd9e3a0311de9e0149c1de`  
		Last Modified: Mon, 25 Aug 2025 19:49:03 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e53616944a4fa3ff99b33d90d938827b7d63bdb00324b94dab3ad40ab166831`  
		Last Modified: Mon, 25 Aug 2025 19:49:04 GMT  
		Size: 15.9 MB (15923955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:30f634f6f0e9e39136903c3b81be8f780a4b805b66163bfc0e683fafb62a3f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 KB (314291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d132bcee2e485d83458421325b31111463d1718ccf62b18456e97d495bc57`

```dockerfile
```

-	Layers:
	-	`sha256:91d8c07f79d660b96ebece0d8847c92fd5160edb83b97e31865c2af067eeb8f0`  
		Last Modified: Mon, 25 Aug 2025 21:52:42 GMT  
		Size: 296.0 KB (296013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d27f4d928535909dc6d7b276be2d1e63901b6b627c43a4bfd594a0b899c110`  
		Last Modified: Mon, 25 Aug 2025 21:52:43 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bf497dbd5122b8bce808c55b47aa082eb84d06f77831adf2d8cc0b5f11e66438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18903449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ba67aa2169d0dbd6426eb009d3bd28de88cb829cb8453b2e628f0443f6e9f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8aa6aa6b1802d86bbc73e75216bbb426a1a8ebad8fab1ccf37a1adfdd1b779`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 346.5 KB (346493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3bd303b867cb629d2b99f58967b240f288c9b1dbf712003b3e56200692140c`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e6b087db3bea6b06b1a48ee30c1fc4db8efebe5b0e6670b418e3db437e8c38`  
		Last Modified: Mon, 25 Aug 2025 19:48:46 GMT  
		Size: 15.0 MB (15048518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:286477e027ad1c6350295044f9c520fa196eb08183d4939ae7ed071fc7320c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16e2d2b0cb8b273b15b42a3b1d12c77c076d757e265061f5e61b31763a6a52`

```dockerfile
```

-	Layers:
	-	`sha256:29f2ff0c73ef6349295d38ad6646decc7e0677799f04a1a1ce633e18c85a4327`  
		Last Modified: Mon, 25 Aug 2025 21:52:47 GMT  
		Size: 18.2 KB (18197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d5af7163676df0baffb41f5bce9c4f0775a69609bc2384b101ff4ba749f0050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18601748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e276120a8a2d3df3a422b6d9a2b02c16b9f92c6b28ac595c34fcc06410127c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979c078f866daa2820e22fa7f8a9cc664e49f7d538de1341a2c2c9a60489560`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 343.2 KB (343205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeca689d2f3de3a319b91d9ddb84048521f017d394555aa2ab895ef9cdb98e2`  
		Last Modified: Mon, 25 Aug 2025 19:48:45 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711aca2485d7f9dfbfccd9cf2a11a6db8015c154383632363d1ac44b755cb55`  
		Last Modified: Mon, 25 Aug 2025 19:48:47 GMT  
		Size: 15.0 MB (15031978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:8049ae7cb8cf21da392232342dd2c386e8e79bb9a7093ef47dec2cd1e4d8d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 KB (314493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b289ec4bc1157ad5848221ba42af4a065fd5af769065351ada6548da41f5c1`

```dockerfile
```

-	Layers:
	-	`sha256:7653918e29fb0de220bc0644efa15394bed69ae8f40081cd705aa96205888b4c`  
		Last Modified: Mon, 25 Aug 2025 21:52:51 GMT  
		Size: 296.1 KB (296081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fb47d806abc1bee7ac987c99961bb2c58274d6cbc04b58ea4c3c026b94f2ce`  
		Last Modified: Mon, 25 Aug 2025 21:52:52 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:4c3be81b7ee70190ce5291230e5a5d4dd8ea998c44cfb5fcc4680a60ea6c5621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19013546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b37c5f2910ca9daf3b5cd9f63bb06d782d2062d4daceced81673d49fe4a1c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ebf372d05e77b4bdc3cea55c048537aaac7759aa0079ed9944004ac30c980c`  
		Last Modified: Mon, 25 Aug 2025 19:48:50 GMT  
		Size: 357.7 KB (357727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f163ee242da1ec76c0ab875c407ba39c49aa3eab955a46b9ea14d94a86c4d48e`  
		Last Modified: Mon, 25 Aug 2025 19:48:51 GMT  
		Size: 7.5 KB (7492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225b3b694c911c2a8b8814871c8353f7b7686cc9ea3fc2b02dba2f45803dd75`  
		Last Modified: Mon, 25 Aug 2025 19:48:55 GMT  
		Size: 14.5 MB (14517545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:a657dd5aa41ae2796a14d32f91e630f0efcefa03e3261ac63d39793887cea22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 KB (314576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469b3383a6f868625bafb61aa5dd86ccd26899761e2bdb5fafafbc7e250ef24b`

```dockerfile
```

-	Layers:
	-	`sha256:4f49301002ed8e6230d3ea527498b3328f01453f1b0e12e3bbcb7ce771cca15b`  
		Last Modified: Mon, 25 Aug 2025 21:52:55 GMT  
		Size: 296.1 KB (296117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fbb94c8995329e1c4b3235561ee976502480bebaab9183f926bf2529444c9d`  
		Last Modified: Mon, 25 Aug 2025 21:52:56 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:67112be943616a31dfbf0c815ed5325bf71a9d8c6cfe49a1935b244bd3b109e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18591170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f3d87694b9256e003a6824820cec8dfc82ad339b7d3bc41671c4996663a0a3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe739855dbbb9a1403a242cd984b1b9b4439925fb4fcedc9d3d6ade9baf3dd5`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 360.6 KB (360616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab33549ec0ff70ed9ba5ea43079d739e8d6fe698b0578958a9e2675602d1f6`  
		Last Modified: Mon, 25 Aug 2025 19:49:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6276663ba0f6c95bde9cd5440dc7ec15f6e100f8283c704efd10d02181f066dc`  
		Last Modified: Mon, 25 Aug 2025 19:49:46 GMT  
		Size: 14.5 MB (14495915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:54c1de5978b47c2325c8f34e5589b9e4befd54792776c52701944ded623d9922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 KB (312470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d525e05914ec596f61ab5f038622c17b75382bd36e15638e19d2ef0b54ab4`

```dockerfile
```

-	Layers:
	-	`sha256:c9a2fa5edceb1da7dbf0f53e0b3b6e55ebdebce9112144575d69508ba7ea1f29`  
		Last Modified: Mon, 25 Aug 2025 21:53:01 GMT  
		Size: 294.1 KB (294120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2488d35b692ff2f9eeccf6177b581e0b4012821bcd0e7079a6755296fdc31433`  
		Last Modified: Mon, 25 Aug 2025 21:53:02 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; riscv64

```console
$ docker pull caddy@sha256:fab4c562bd13d4fe11cc47963461b4b2f197e38afa3be8a61b698b6319238f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17956644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c209b028cc287828f645bdd0dc227ee3dbc69f503f5bf1a4ad3a944252b78b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29116abe2cb7489bfe0d514003d7c4822eaf03d2b44e5f1c10c878a603eceb13`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 348.3 KB (348289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ceaafe79989c43b373a7e7780390f12740f15ad106a2c987605998f180cea`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 7.5 KB (7498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9baf51ef7381285244300ec8288209b2b0dc82267a2c3547eb0644ce4c7948`  
		Last Modified: Fri, 18 Jul 2025 07:36:44 GMT  
		Size: 14.3 MB (14251735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:608fabfae5954b1485e44928f39c3844fbdc7de236202d87c4380838c748a018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 KB (303605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff983ccc8020f39b317500f82d9596ad6b4299338ecb828eaa0685950b57aa46`

```dockerfile
```

-	Layers:
	-	`sha256:090b4908e38667b8110e66242c7d88a6c27ba9f8dc2ebc126e04430fcaff531c`  
		Last Modified: Fri, 18 Jul 2025 09:52:30 GMT  
		Size: 285.3 KB (285255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e87f231dbdaabee2c8a7c7375c70ff7387e5d2387ed1a26033f1a9b77c0e427`  
		Last Modified: Fri, 18 Jul 2025 09:52:31 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:df924d28949f8a3be699c88ab40eb6b5ca37234e6af5431cb6a1cca63e58a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19362618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85040edfc178cf9c5de8611792e65c67f07629a5c76b7089bf0828d075163a0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff98415fc23c99d5ff9b731b3ed1f5f263fca7f05ddbb51c47d7d8b6df1f89e8`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 353.5 KB (353456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e6340a3b7a63c6c76d521ec65f90ba0718a26fb02520f02216f158300c89e`  
		Last Modified: Mon, 25 Aug 2025 19:51:45 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd56c657dc325cdf0a5d0c300a1380b0fe6abd98dcee92bcf38b02d14d579062`  
		Last Modified: Mon, 25 Aug 2025 19:51:46 GMT  
		Size: 15.4 MB (15356663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:ce406a252aedd52a38cc6938d993637d83f2aedbe10e9eb385f4b60a12418812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 KB (312340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190d69bf6d55a424c64ecfe71fedbf83d368d2191338ab24083d5426fa60e861`

```dockerfile
```

-	Layers:
	-	`sha256:ea8886b3a4622ffdcc38a8a441716fbb95afc7feb55738ebaae75b137a193925`  
		Last Modified: Mon, 25 Aug 2025 21:53:08 GMT  
		Size: 294.1 KB (294062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5011fab561f7f812f810ba45504c8489c7a5e0383d88863c43b47478a136a21a`  
		Last Modified: Mon, 25 Aug 2025 21:53:09 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:c2e9243204fd55beead5b9d893a8ca326f04ee4f2331dec60ad5a1d2a6992777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:3ebb7e7a0141c5f1434331567920cb6803bcb77417482786ce8e21cc1efad8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:eadadcb9a4804f2c2f6ace69b31243ddc25d10923eb9d7148361a38dfde75b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `caddy:windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:e2c0eb26a9afb56a702b4ac92173453870f232d8017fca3ef7d89f3bddd87325
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3516255218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc5ad3f54ca8aebbd4c61a8ba0cf1912e9c99bf255a1e41811d7ad458629a80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 19:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:54:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:54:52 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:55:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:55:04 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:55:05 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:55:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:55:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:55:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:55:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:55:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:55:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:55:12 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:55:13 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:55:14 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:55:15 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:55:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:55:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f399e79f5032340187f62a207687b064b769695af504ac62767001f38265d90`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb898c8e6c19bec5870def544459e0e0932f68789f735efee5aef9fbb363e60`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 401.7 KB (401711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e39b932c97202b44b0a0228a9d7a619d87e4851cd9592b42ecef2c0bda666d0`  
		Last Modified: Mon, 25 Aug 2025 19:59:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7dbbc88168ac1915c1a86d493057f0c5d9164625d3fe4a86650cfe5abf0fe2`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 16.6 MB (16610173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08638818c0d66701b430def7afb95f1fdacedc40765bab57cf02932a0e7a8a8`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164f8d482a92a2186718540a60e2e9e69b31d1e66b0eab010fcb4b90b6e48e5`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c801eab31e04440b9fab2bca0ffb8d9716d2195dd5eead1cbe1bab01f993461`  
		Last Modified: Mon, 25 Aug 2025 19:59:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4db49813ba10a2de3b7f4ece5816265f3ee82f4e03a4a41a62dfbdfd9b14d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45bbda1bb51d2d319bfe743d7272fe2e9d7fafd4b846ff4460463de0023135`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9256723510fcfbcb0bff01d6447d68a46441428cca4d32ce97dfac8f689bf2`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ea9b7dcb9b3b136b6b6af2fe7d804e65618e72bae1c2701fb1578f4710989d`  
		Last Modified: Mon, 25 Aug 2025 19:59:04 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf85861f20e037bf88b624fc08226d79b5a88bca7a106885498a15adb4cb804e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6599feb960b40842670982ecf866d0a86db7f6e0df56819bf8287e49fe4e6ad`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0735f4a2f580b4145501d52edfe406e5e63cee4bd777419ca0efe88d567137`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bef5cf9619f57f3ac1e1be8c6cf0c947f4a46b686598608386a5c3e90e2e596`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a87bd32083fcdbefbfed89c192d81796812f880aa9c13bd08642a3a76d1d7`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6671170553d289b3aa717f7a303cd34a867c4893034d3d8f6397ad0a4a05225`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7345acb994a0b74ee4eaad4ca9d0fdecfe4a43d8c3dd349f2aae4357f91e2f0e`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4caa810c9ecf60b6882e9f838b7c91d7c3baa28373c618d8e0dc6660536fd6`  
		Last Modified: Mon, 25 Aug 2025 19:59:05 GMT  
		Size: 390.6 KB (390608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b8942983782461ae5cd76b3af44aa0aec4c8a6d4c378b2e2dfcda79c9ac2ca`  
		Last Modified: Mon, 25 Aug 2025 19:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
