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
