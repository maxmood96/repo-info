## `caddy:latest`

```console
$ docker pull caddy@sha256:aa07c7478466e3d6c94a74a02375c3fe57a8332226348bc0c6f594eb08dfdc8a
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
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:b0780a47e6f7502610d16fa177a8bfe8e3229fe3f1e5b8dd1b040f2f917af7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22502235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aed261b9d04b08cca89b6076e336af590dbedcd5178dfd6d490cf26da61debf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:54 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 03:49:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 03:49:56 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 03:49:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 03:49:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 03:49:56 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 03:49:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 03:49:56 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:49:56 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 03:49:56 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 03:49:56 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 03:49:56 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 03:49:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b233224cdc908851482adf1d142dd77f697a4f320d7457a26f80b3bf886ac7fe`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.8 MB (2765883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241bbfa4875f6e97ad2966d2bd1439109ea867cbf0f8fa492e8009727c8fa24f`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 7.5 KB (7491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099e4eae307f3fc3ce28f54f0db4e8b41dc7318ca249bb01d6582ffd10553ac`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 15.9 MB (15923954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:9785eb8268d98a9552e6819607bf1f6eea78128ca7462857af529637b9eb78ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.1 KB (338111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4df38ee34b1810d3aa6fdf9b998b95c534c1a7c917cd79469c6197df576b11c`

```dockerfile
```

-	Layers:
	-	`sha256:33d6adb97eb48edcc7c7f797ff67ad2623a563a4d5bcb2cf9d70c96ef83b4e7a`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 319.8 KB (319817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada840fbfb4c1f7df3285d88f6cceb573c1d019c2ab5b155d2457b7c7f9138ba`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 18.3 KB (18294 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:3419b51f2f4bec4bbe037d4b791e372ff2b097e3b52ed0525be98e700cc2db22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21262107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2432c4b853c3b89fc0bf1ebe0da7ca65af4ab689000e914d736e3e4e0ab409fd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:47:11 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 03:47:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 03:47:13 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 03:47:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 03:47:13 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 03:47:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 03:47:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 03:47:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:47:13 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 03:47:13 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 03:47:13 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 03:47:13 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 03:47:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8969decbc3ab02b36d50abd17e14a3ec76d9d0875f458282904dbc4d433620`  
		Last Modified: Wed, 28 Jan 2026 03:47:18 GMT  
		Size: 2.7 MB (2701019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d2210b20920ce47f06b5b9224c5ac24a919b97dfa2a7c33e358c796161ef6f`  
		Last Modified: Wed, 28 Jan 2026 03:47:18 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ce2074fc6d422debb8e9dc0252c4351f76bfc53d6046bb62f5f6fbf0c4fb54`  
		Last Modified: Wed, 28 Jan 2026 03:47:19 GMT  
		Size: 15.0 MB (15048515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:05353075c91eaba3720ad6ede7dee390b43cbd3d6a4a60ebfd3b2c58ec3f9e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7631f81fdf869e51a88d9588466aa7e9715aeafff7267b0edb6a44816f5c30e`

```dockerfile
```

-	Layers:
	-	`sha256:c271ce95b8e40d3e390f1d17f5a16676f1a3e7007c72350eec7fc6a64937fa67`  
		Last Modified: Wed, 28 Jan 2026 03:47:18 GMT  
		Size: 18.2 KB (18217 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d7a1b9d635ed7d40e18f9ee9a568c934561c7f9902eb0e9518e8e92c36b84522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20846091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771cfd473aae0e709970ec8b291a37c66196741dba8c8c59c582c6780e557282`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:47:16 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 03:47:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 03:47:19 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 03:47:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 03:47:19 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 03:47:19 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 03:47:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 03:47:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:47:19 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 03:47:19 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 03:47:19 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 03:47:19 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 03:47:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d66e158a340bf7d4b009a721892d22cc3cc5cc845422607af9493396d7c2c72`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 2.6 MB (2582948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a03a4daa4c354fc55dc9c81a61b67eea5edf8fa9a73ba3f0e44d90f2660767`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 7.5 KB (7491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e328cf0b856f1ba40061d5cf56f24ec2aa0d25139cc1194105429e044f1fb15`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 15.0 MB (15031991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:b8b93790f88082ce3ccde72eb3384be67aec300dd12a54c033fd4b46765b4b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 KB (338317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36607589a513a3c6dc5b10983d83716ea59be30c7fa8e41263c8c3507da4ffa4`

```dockerfile
```

-	Layers:
	-	`sha256:ac333ae5fa9c8b09feb252e4dee352c2f18c56cddb7dde60679a574eb14b5c62`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 319.9 KB (319885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96b25c2b9628d351706780289b7ecf7d51a5284bd7af2eb448f363e1db913fd5`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 18.4 KB (18432 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:41a99e75650213d76ff63fd49ab58a02a9ce4f1129a6985661659993c91a5bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21437628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209ef7854fc1f0fa74146feafca79a016a61f4f6b20f4457e5f0ad3b228d9c7e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:38 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 03:56:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 03:56:40 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 03:56:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 03:56:40 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 03:56:40 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 03:56:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 03:56:40 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:56:40 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 03:56:40 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 03:56:40 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 03:56:40 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 03:56:40 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4faa3274f6632949d447e44d107d209b567d1828ad37406becdeb78faf2a292`  
		Last Modified: Wed, 28 Jan 2026 03:56:46 GMT  
		Size: 2.8 MB (2773038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5082e1f85493f22e64b9374824aa63a8038a94a642fa4e7cc905e7cdeb68146d`  
		Last Modified: Wed, 28 Jan 2026 03:56:46 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb0c9b27be6cd7db5b535fc1ad267ab4bdcac9fdca2fb884e4934e2f2ac6197`  
		Last Modified: Wed, 28 Jan 2026 03:56:46 GMT  
		Size: 14.5 MB (14517544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:52b102a611855f2fe509a00f862e994e6e9a4d0590e0e391c7bf3a1bac048439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 KB (338397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24dd8d17c272b00c9b2e7251aaf4b9de16b50176dfa477aafb62d2b7cd36e14b`

```dockerfile
```

-	Layers:
	-	`sha256:4fc8976f2cb69754ae5dbe18a0d3a1d4ed5e705b410c8a24e70658ecd1579a7e`  
		Last Modified: Wed, 28 Jan 2026 03:56:46 GMT  
		Size: 319.9 KB (319921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:546f85385a3d95ce6ea0511f6ca5ac562c9160782c0c2a94faeef33ffc6e89e5`  
		Last Modified: Wed, 28 Jan 2026 03:56:46 GMT  
		Size: 18.5 KB (18476 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:7945eecf0567a8d377392a010929755ac9edc7983a719595b0abcaad99a4f958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21118744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029c041718cba83f3f73c7a03b122bf79ca74256ef4cf6aef5eb8501ec80cf89`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 05:49:42 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 05:49:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 05:49:46 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 05:49:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 05:49:46 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 05:49:46 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 05:49:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 05:49:46 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 05:49:46 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 05:49:46 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 05:49:46 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 05:49:47 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 05:49:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d27a1cebfcd5c7d19f815a118a939680dd7f17dbe0fc6708fdf8e18b4e08e7`  
		Last Modified: Wed, 28 Jan 2026 05:50:00 GMT  
		Size: 2.9 MB (2881009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f8f91b00c9d5bdabdab56b6356d32076ea61820c67088dfcd4f4c82365b386`  
		Last Modified: Wed, 28 Jan 2026 05:50:00 GMT  
		Size: 7.5 KB (7490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580f1b75e743904245a014c656f0ceb2811c2afdf316017a02d11c36cc218310`  
		Last Modified: Wed, 28 Jan 2026 05:50:00 GMT  
		Size: 14.5 MB (14495916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:0bd47765d347cae743b21d5ed9be391f310153dde547e1f2bbaff1cf00ea134e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 KB (336290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debc9b84c0deb0ebe3efa50b31be33c0777f74907e84ff1039fe412913794c3e`

```dockerfile
```

-	Layers:
	-	`sha256:49e53b3c2722757ce8c4b2dd55a232215d5d433643ae22f1f0abb6b235d7d624`  
		Last Modified: Wed, 28 Jan 2026 05:50:00 GMT  
		Size: 317.9 KB (317924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed2654dd3697cf27c7a6fd105274d11114c040a4b4defe2ea7bab4f331b3b97`  
		Last Modified: Wed, 28 Jan 2026 05:49:59 GMT  
		Size: 18.4 KB (18366 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; riscv64

```console
$ docker pull caddy@sha256:1fda1ea60041573a7343d9ac09c2a671487373eb2a0d4ac02cc97547b12b2a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21544363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62c731a67a2fa983f6002abe485198b41b427d959dc968ed8de8cea26f525d3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Sun, 01 Feb 2026 05:41:40 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Sun, 01 Feb 2026 05:41:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sun, 01 Feb 2026 05:41:48 GMT
ENV CADDY_VERSION=v2.10.2
# Sun, 01 Feb 2026 05:41:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sun, 01 Feb 2026 05:41:48 GMT
ENV XDG_CONFIG_HOME=/config
# Sun, 01 Feb 2026 05:41:48 GMT
ENV XDG_DATA_HOME=/data
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sun, 01 Feb 2026 05:41:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sun, 01 Feb 2026 05:41:48 GMT
EXPOSE map[80/tcp:{}]
# Sun, 01 Feb 2026 05:41:48 GMT
EXPOSE map[443/tcp:{}]
# Sun, 01 Feb 2026 05:41:48 GMT
EXPOSE map[443/udp:{}]
# Sun, 01 Feb 2026 05:41:48 GMT
EXPOSE map[2019/tcp:{}]
# Sun, 01 Feb 2026 05:41:48 GMT
WORKDIR /srv
# Sun, 01 Feb 2026 05:41:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef112d08d3a9af3893edd8085873b635eee17016e49d660415dc2cfeebc479f`  
		Last Modified: Sun, 01 Feb 2026 05:42:36 GMT  
		Size: 2.9 MB (2889122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca694903ff86ed9e688cb7279ee66be7051ee75d68985f3e91357c272429930`  
		Last Modified: Sun, 01 Feb 2026 05:42:35 GMT  
		Size: 7.5 KB (7499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedcddfcab535731a9ccef4307b226a59163e16bfe92a64e874e915c3eec6e7d`  
		Last Modified: Sun, 01 Feb 2026 05:42:38 GMT  
		Size: 15.1 MB (15130288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:9f9cbee6a0b56e542b332fbc0e236e739648db71f558354d8296faea82884caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 KB (336285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844bfad8fd9f088a8dc30158b09e2c9848ef781d54245826d1f6adad34ee9790`

```dockerfile
```

-	Layers:
	-	`sha256:16d5726973f883ab398894a3869d4a5248698374baa15d7982703c4d163ec0ac`  
		Last Modified: Sun, 01 Feb 2026 05:42:35 GMT  
		Size: 317.9 KB (317920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:765de01d9208844588ac004d7160d42c5563721efc204013dbe00b2d04ad4773`  
		Last Modified: Sun, 01 Feb 2026 05:42:35 GMT  
		Size: 18.4 KB (18365 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:6f5897a40ba331b6168ead40cc1af5e38d20ff4f363a5ea3672f58da1a39e857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21926347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07127a3343ffee00e7caa9b9ea8e566a208a7195571afd0c3984d8519c94fd4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:57:07 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 28 Jan 2026 06:57:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 28 Jan 2026 06:57:09 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 28 Jan 2026 06:57:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 28 Jan 2026 06:57:09 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 28 Jan 2026 06:57:09 GMT
ENV XDG_DATA_HOME=/data
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 28 Jan 2026 06:57:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 28 Jan 2026 06:57:09 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 06:57:09 GMT
EXPOSE map[443/tcp:{}]
# Wed, 28 Jan 2026 06:57:09 GMT
EXPOSE map[443/udp:{}]
# Wed, 28 Jan 2026 06:57:09 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 28 Jan 2026 06:57:09 GMT
WORKDIR /srv
# Wed, 28 Jan 2026 06:57:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7491ee627d96375c3d815309c875024be98d4a23e338476433fbc9f131035055`  
		Last Modified: Wed, 28 Jan 2026 06:57:20 GMT  
		Size: 2.9 MB (2911727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4823f0238a3307d087b783a0492fa37ed26d107fb428f910c8771cbef1344c`  
		Last Modified: Wed, 28 Jan 2026 06:57:20 GMT  
		Size: 7.5 KB (7491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de39d52dda6fcb149d5fe9c9951b9fc4c5c79f388084ec63dd96ee2882e58fa`  
		Last Modified: Wed, 28 Jan 2026 06:57:20 GMT  
		Size: 15.4 MB (15356663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:db77930a68a31e89d2f36104e852747509c1f6b1082face89d2b33fbf3f614e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.2 KB (336159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f090c6a9bd1993a4fbd1e66e29403c3e7237a50bec7bad331499fb801bc7da44`

```dockerfile
```

-	Layers:
	-	`sha256:434937b4ed21587a7eda92958eefa3639edbcf2f48ad5f213902681f388f2997`  
		Last Modified: Wed, 28 Jan 2026 06:57:20 GMT  
		Size: 317.9 KB (317866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9e0fdbcd0818a0e579184915c7ad2a64145583ea09f562a0fdf920d923d86f`  
		Last Modified: Wed, 28 Jan 2026 06:57:20 GMT  
		Size: 18.3 KB (18293 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - windows version 10.0.26100.32370; amd64

```console
$ docker pull caddy@sha256:6e7c66c6099d6bc6b5ff906bf6058dd563458ab0007857e97f1e784e2043981f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1982152977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d760c474d4157d97b21a9ee980079e935b92d3ef301e884742c9ce09a3f1aa00`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:51:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:01:15 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 10 Feb 2026 23:01:16 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 10 Feb 2026 23:01:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 10 Feb 2026 23:01:24 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 10 Feb 2026 23:01:25 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 10 Feb 2026 23:01:25 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 10 Feb 2026 23:01:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 10 Feb 2026 23:01:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 10 Feb 2026 23:01:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 10 Feb 2026 23:01:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 10 Feb 2026 23:01:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 10 Feb 2026 23:01:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 10 Feb 2026 23:01:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 10 Feb 2026 23:01:30 GMT
EXPOSE 80
# Tue, 10 Feb 2026 23:01:31 GMT
EXPOSE 443
# Tue, 10 Feb 2026 23:01:32 GMT
EXPOSE 443/udp
# Tue, 10 Feb 2026 23:01:32 GMT
EXPOSE 2019
# Tue, 10 Feb 2026 23:01:37 GMT
RUN caddy version
# Tue, 10 Feb 2026 23:01:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f3641b48551abf691e707ba76f8b07a225d509249237749ad0c13cbcab89a6`  
		Last Modified: Tue, 10 Feb 2026 22:52:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f276061a0e9fd62b5f026c0e8e20432c3c2bed55b1a283749156d4d1a6554fa`  
		Last Modified: Tue, 10 Feb 2026 23:01:47 GMT  
		Size: 391.7 KB (391713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5e15a2289d59d7eca1d6ce05af1d24eee8fa054736c6158129fff6955994b1`  
		Last Modified: Tue, 10 Feb 2026 23:01:47 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cfe98cc5e37fd25c0affc79b51ba982cae3f772287787b68c942b4fa6774b1c`  
		Last Modified: Tue, 10 Feb 2026 23:01:50 GMT  
		Size: 16.6 MB (16603432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979824b982ef69c03807cc87e8a18aad10bd24a1641d9bc1653d483b06549ccf`  
		Last Modified: Tue, 10 Feb 2026 23:01:47 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab9d90cdf8fee003148ca90b1fb97207cdaaeaf6367a1c754fe9c05a39b7d0f`  
		Last Modified: Tue, 10 Feb 2026 23:01:46 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a0ea0b8e74e83e98e2ce6827eec442564643af8bc41baddffeb2d5c49e079`  
		Last Modified: Tue, 10 Feb 2026 23:01:46 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5e19df1d353e82803821837599cc670b39c65461dade76e4f723e582dbbbb9`  
		Last Modified: Tue, 10 Feb 2026 23:01:46 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc4512c1e5582c86ad4877934fd342dfdc2da294e2bbe6c23179c1b7543306b`  
		Last Modified: Tue, 10 Feb 2026 23:01:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3975ec9242bbc052bdb5d57efd0756f45acfcf99094e2805356d46959ed6cbe6`  
		Last Modified: Tue, 10 Feb 2026 23:01:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a604552550aaf7489aa0e405ad7aa48c1122509c898547a94a6ca8f0461b6d`  
		Last Modified: Tue, 10 Feb 2026 23:01:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10c6859a9b1be1ccd1f4f75655019335d457f8ce3ba20b1d3cac9590f0db6cf`  
		Last Modified: Tue, 10 Feb 2026 23:01:44 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d940e6676ac8b98f5e03a964e6156d51cea11a5dcceb7f5d1e6fbfc32b88f2c2`  
		Last Modified: Tue, 10 Feb 2026 23:01:44 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec3a6e40fa5748b341cd6e5d1d2d1766a866b0fad1a1983c7b3904010db56d`  
		Last Modified: Tue, 10 Feb 2026 23:01:44 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e2a8335a8bcd0f09b8881e1aceb0256a1f4ca5cf783ed1f59b3830ac4dfc63`  
		Last Modified: Tue, 10 Feb 2026 23:01:44 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458431ca1f11a4a4821a1f1664937c2030ca380b87fb6f5fbffefd6ca8d7b445`  
		Last Modified: Tue, 10 Feb 2026 23:01:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20910b219f8574e2733678cb3c1aa9cff159182d4d5ea6c6389d1c2062748fee`  
		Last Modified: Tue, 10 Feb 2026 23:01:42 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fae5cf857cd8bbb242ce433c3df4346052140c08697dbf1461654829aabd2f`  
		Last Modified: Tue, 10 Feb 2026 23:01:43 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fafec4cb7000cfd389b9271fa8dcb290d829f68afbbde11c803f8c26840536`  
		Last Modified: Tue, 10 Feb 2026 23:01:42 GMT  
		Size: 375.4 KB (375425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f5cd22343f6e63b3b23bcf0c1877f9b7532439c621b30e43bc13999985be8b`  
		Last Modified: Tue, 10 Feb 2026 23:01:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.4773; amd64

```console
$ docker pull caddy@sha256:a3837d693358af45d4af020a98c9ab64bc3d8890cc718b4d71b218ca8a7ed1ab
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1880077650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2080fbc82fecf316257b929e2f540b8338fc2e29dc8f0db452c61bd770358c18`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 23:14:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:14:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 10 Feb 2026 23:14:56 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 10 Feb 2026 23:15:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 10 Feb 2026 23:15:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 10 Feb 2026 23:15:08 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 10 Feb 2026 23:15:10 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 10 Feb 2026 23:15:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 10 Feb 2026 23:15:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 10 Feb 2026 23:15:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 10 Feb 2026 23:15:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 10 Feb 2026 23:15:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 10 Feb 2026 23:15:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 10 Feb 2026 23:15:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 10 Feb 2026 23:15:17 GMT
EXPOSE 80
# Tue, 10 Feb 2026 23:15:18 GMT
EXPOSE 443
# Tue, 10 Feb 2026 23:15:18 GMT
EXPOSE 443/udp
# Tue, 10 Feb 2026 23:15:19 GMT
EXPOSE 2019
# Tue, 10 Feb 2026 23:15:26 GMT
RUN caddy version
# Tue, 10 Feb 2026 23:15:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c42f97ad258a14a6dbdcb82f4db240ae770d130ae690da2e4abf30e29919a5`  
		Last Modified: Tue, 10 Feb 2026 23:15:36 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5986a92d2c4741f2d28228dfd7c6283deb455ea86d2277d16fb73c24469e3a0`  
		Last Modified: Tue, 10 Feb 2026 23:15:36 GMT  
		Size: 490.0 KB (490008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffe8601c9aac4730bf36d72767be0c5c461ca36d50bfb8380a36ae220fa964d`  
		Last Modified: Tue, 10 Feb 2026 23:15:36 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cec3a97816b7253b9f0536e61523f608fc9eb09c9a133f2352d36f0a61f5c9`  
		Last Modified: Tue, 10 Feb 2026 23:15:38 GMT  
		Size: 16.6 MB (16564778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8f492e3a72bf1cf6c7a83d87fbb56c36ff7e10b88f13ceda98762c52348c56`  
		Last Modified: Tue, 10 Feb 2026 23:15:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b98fdede264784e07b9b871ad56349fd7a48bdd3f9d86f60cf9d6bd650d859`  
		Last Modified: Tue, 10 Feb 2026 23:15:34 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b55dea49a860842e60026ffb1310e79dabbec2b6249df94e93d8136289f8ef8`  
		Last Modified: Tue, 10 Feb 2026 23:15:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650f6d3b28ea2fe1efd0b1d9bde43dc991ac946aad84ccff96d6dd8b5702571b`  
		Last Modified: Tue, 10 Feb 2026 23:15:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a04551dc3e2993d1de700b6ad8232cde96a5d6ae10c35f486e40b92da1fe8b`  
		Last Modified: Tue, 10 Feb 2026 23:15:34 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a400410fea1a3a7c70fddc7a2f628361172c51b475c190eb11d1ad25b934294`  
		Last Modified: Tue, 10 Feb 2026 23:15:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e0cc6d534bc45b036852067fc9056ce0509bcb90c81a20a403a84f555b3048`  
		Last Modified: Tue, 10 Feb 2026 23:15:33 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca018aa6e7136f3713a12b83fb8886c6ae355bbbad49ee98329bd3062436822`  
		Last Modified: Tue, 10 Feb 2026 23:15:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1047b0c70acde50333d760c4e87b61c55868ac5237207fa7a613adb45053b3c0`  
		Last Modified: Tue, 10 Feb 2026 23:15:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84591cbe17431834bfc10ea86327744d33121c0361e17a9663ff5bc383c92b8`  
		Last Modified: Tue, 10 Feb 2026 23:15:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e6b047f1cb496104ea8b755e7c91d0e112cab0d516c2fa1a117978e0e8bd1c`  
		Last Modified: Tue, 10 Feb 2026 23:15:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d7d061fb740099a287a80e83018e4415a8aafc72a068d2649e1ba8456aaf6d`  
		Last Modified: Tue, 10 Feb 2026 23:15:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9c9ffc4b188fae0c18c88003323717c2e39d96579ad89bb1160b06dac6d9a`  
		Last Modified: Tue, 10 Feb 2026 23:15:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce7a8989b632d092c616b346647bbf444cfb19f2cd9278aeb477632e2cd672`  
		Last Modified: Tue, 10 Feb 2026 23:15:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b865b67def9a31372e40fda32211a379e86e79ea86c1950799f589b9ebb3706f`  
		Last Modified: Tue, 10 Feb 2026 23:15:31 GMT  
		Size: 343.4 KB (343398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496d68ffbd692e3de604600d4afb7e38c8f40f772e9ffd34e8c8cc57b4dd8f20`  
		Last Modified: Tue, 10 Feb 2026 23:15:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
