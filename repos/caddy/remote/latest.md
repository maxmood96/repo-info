## `caddy:latest`

```console
$ docker pull caddy@sha256:4163a5c7b7631707956db4057720ec75de429992d5e3aa518d54872c01644dbe
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
$ docker pull caddy@sha256:0176aa805baa6fbe392cd36b97a1ce0c9d5e27f7e27251e5f618ed7b7010fede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18998682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f79be0e1ff95297cbf4dbb0b9bea2ecc5919dd6ded4dd0d32a28ba89c55ccb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea837a568c1c4711a071cc4239433fa9789705d31332b1a13e3cef54c856d5b`  
		Last Modified: Wed, 27 Aug 2025 08:50:03 GMT  
		Size: 348.1 KB (348063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59929409f754f48bad95c6194c278ec227960781da35d8cd486d382fd4efa6a`  
		Last Modified: Wed, 27 Aug 2025 08:50:04 GMT  
		Size: 7.5 KB (7500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d190d238a064f111e2d7726465b3f31be8c281d77ed3d09193d2160094cc17`  
		Last Modified: Wed, 27 Aug 2025 08:50:06 GMT  
		Size: 15.1 MB (15130286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:a01d2b50764efbaa83304652a87d88e07d3243e4cee4e5b28f8f90f55300f07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 KB (312466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9617077f5127f21daf0565d36e2e94f75ebb71930be2afc9d60b2c56f1e76b6`

```dockerfile
```

-	Layers:
	-	`sha256:341fe15f1cc50733e07da2a443602db6757895d6f8269b17685ad8626e0c5648`  
		Last Modified: Wed, 27 Aug 2025 09:52:28 GMT  
		Size: 294.1 KB (294116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e524d25326989b1e2d68427c6c9c084445869032636c7bd9c573880cc0c96f1`  
		Last Modified: Wed, 27 Aug 2025 09:52:28 GMT  
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
