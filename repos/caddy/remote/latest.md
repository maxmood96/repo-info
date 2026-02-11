## `caddy:latest`

```console
$ docker pull caddy@sha256:c3d7ee5d2b11f9dc54f947f68a734c84e9c9666c92c88a7f30b9cba5da182adb
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
$ docker pull caddy@sha256:d8c17a862962def15cde69863a3a463f25a2664942eafd7bdbf050e9c3116b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22502233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac61abc4024c323602ccb9ee38bd68b147601f518626b2a055e06944e01c510`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:04 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 11 Feb 2026 18:28:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 11 Feb 2026 18:28:06 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:28:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 11 Feb 2026 18:28:06 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 11 Feb 2026 18:28:06 GMT
ENV XDG_DATA_HOME=/data
# Wed, 11 Feb 2026 18:28:06 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 11 Feb 2026 18:28:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Feb 2026 18:28:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Feb 2026 18:28:06 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Feb 2026 18:28:06 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Feb 2026 18:28:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Feb 2026 18:28:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Feb 2026 18:28:06 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Feb 2026 18:28:06 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:06 GMT
EXPOSE map[443/tcp:{}]
# Wed, 11 Feb 2026 18:28:06 GMT
EXPOSE map[443/udp:{}]
# Wed, 11 Feb 2026 18:28:06 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 11 Feb 2026 18:28:06 GMT
WORKDIR /srv
# Wed, 11 Feb 2026 18:28:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dab9c579893913f1dde3163b96d3e03f06a907b3ddfe78f71ca73f5f5eceb4`  
		Last Modified: Wed, 11 Feb 2026 18:28:13 GMT  
		Size: 2.8 MB (2765852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c108b7dc59eb05d618e1ee8803e793ce44eed9e2967c6cef39210d81d8a4b4fc`  
		Last Modified: Wed, 11 Feb 2026 18:28:13 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b2460369730f1bee18fea5bf1b63d3d5f17fda1aabbdbbd86cf5ae49ab9f7`  
		Last Modified: Wed, 11 Feb 2026 18:28:13 GMT  
		Size: 15.9 MB (15923972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:9bf62326d17e2d12bd78896ca26795658390afa9a084d73d2e17e19f857e6b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 KB (338247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f903377ee1e8980222c6a4a82a38fada4c0ece88d070b143ab9c10bc702f7`

```dockerfile
```

-	Layers:
	-	`sha256:7441b80a9e3047487c48861615f701777a276077b175961acedc637131ce77ee`  
		Last Modified: Wed, 11 Feb 2026 18:28:12 GMT  
		Size: 319.8 KB (319817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfa8d6bed7122e99c1c6112f5fb281c2c9f18c7b12d8b6e38580fa35aa7bd9da`  
		Last Modified: Wed, 11 Feb 2026 18:28:12 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:9ecaeae5e5f991362a14bdbe172ce9e4ccfcd2a54a6880235d058e1bae5f9dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21262102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5057486781bba2aa134b55bf15efb632802277ecb6b2ecfee7718605a548772`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:27:52 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 11 Feb 2026 18:27:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 11 Feb 2026 18:27:55 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:27:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 11 Feb 2026 18:27:55 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 11 Feb 2026 18:27:55 GMT
ENV XDG_DATA_HOME=/data
# Wed, 11 Feb 2026 18:27:55 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 11 Feb 2026 18:27:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Feb 2026 18:27:55 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Feb 2026 18:27:55 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Feb 2026 18:27:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Feb 2026 18:27:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Feb 2026 18:27:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Feb 2026 18:27:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Feb 2026 18:27:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:27:55 GMT
EXPOSE map[443/tcp:{}]
# Wed, 11 Feb 2026 18:27:55 GMT
EXPOSE map[443/udp:{}]
# Wed, 11 Feb 2026 18:27:55 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 11 Feb 2026 18:27:55 GMT
WORKDIR /srv
# Wed, 11 Feb 2026 18:27:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb36d754087d032991d07bd6218a70e64a62efb46fc8211eac1646177cf117`  
		Last Modified: Wed, 11 Feb 2026 18:28:00 GMT  
		Size: 2.7 MB (2701014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8861e21dd5b23b79650aab26d3ca3b677338d29b6fbf0d6757b5fce8f2f81940`  
		Last Modified: Wed, 11 Feb 2026 18:28:00 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f107fd2b74d1aedf31c08a0c8608d5ac2d25d4fce1ca4b5e1c30611bca24f79`  
		Last Modified: Wed, 11 Feb 2026 18:28:01 GMT  
		Size: 15.0 MB (15048508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:b5ab879815f6f5034ce0d5871adced94b922fbb5d52557e6bab03f7392e5c698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cf80da8b0fed9de1d466a0afe6460222cc490e680336ae510ef0ad3d3b9232`

```dockerfile
```

-	Layers:
	-	`sha256:2bbb1a0d07ee1c68f2c43aa4c419a5f770b8a13c83b6546258617368abc2744c`  
		Last Modified: Wed, 11 Feb 2026 18:28:00 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:333ca049d81a3087c296aab37f2c427cfa66c021d0d1e25678ae6f72354fe05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20846093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988cb43ba100d8a655c29c2570abab52aeadb39cd0b8cfadfdb117fbf7019db0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:05 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 11 Feb 2026 18:28:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 11 Feb 2026 18:28:08 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:28:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 11 Feb 2026 18:28:08 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 11 Feb 2026 18:28:08 GMT
ENV XDG_DATA_HOME=/data
# Wed, 11 Feb 2026 18:28:08 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 11 Feb 2026 18:28:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Feb 2026 18:28:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Feb 2026 18:28:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Feb 2026 18:28:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Feb 2026 18:28:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Feb 2026 18:28:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Feb 2026 18:28:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Feb 2026 18:28:08 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:08 GMT
EXPOSE map[443/tcp:{}]
# Wed, 11 Feb 2026 18:28:08 GMT
EXPOSE map[443/udp:{}]
# Wed, 11 Feb 2026 18:28:08 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 11 Feb 2026 18:28:08 GMT
WORKDIR /srv
# Wed, 11 Feb 2026 18:28:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a8dc4bf5ef8679228e59e257f69f56002f85e1f5c3051475b0c92a9bf18c41`  
		Last Modified: Wed, 11 Feb 2026 18:28:15 GMT  
		Size: 2.6 MB (2582962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f8288f423cc5eac63e0085dd3206645c51adb8e92c5f3b81ca9c03df9884ab`  
		Last Modified: Wed, 11 Feb 2026 18:28:15 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496d053975af5a85f2af4f7b61237009d4f3523d85020b94eff08ecb33da9de4`  
		Last Modified: Wed, 11 Feb 2026 18:28:16 GMT  
		Size: 15.0 MB (15031968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:955eaabbcd743d314213481554249593c3b5f166230f24a44b43a74eb36e4a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 KB (338453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896f84ebdb86f050e613a3412afcd2484d39acdb729e20eb89bf06bfee0fc812`

```dockerfile
```

-	Layers:
	-	`sha256:ff9f6018061c048c4365d3b62bdffdef030ceb156378793e7ba84b220f9519c0`  
		Last Modified: Wed, 11 Feb 2026 18:28:15 GMT  
		Size: 319.9 KB (319885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7025a5a10aec7c89ebb925ba9fa25891fa3edd22bb2ffa8fffac4b135a6e7da2`  
		Last Modified: Wed, 11 Feb 2026 18:28:15 GMT  
		Size: 18.6 KB (18568 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:8dbca3525dd8dce671e495665a0eb297a83ec87ee30f373947d0ea93115949db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21437645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5619aac3ed45304632491507becd99711bcaed375aee3e6317c7b703902969`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:10 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 11 Feb 2026 18:28:11 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 11 Feb 2026 18:28:13 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:28:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 11 Feb 2026 18:28:13 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 11 Feb 2026 18:28:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 11 Feb 2026 18:28:13 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 11 Feb 2026 18:28:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Feb 2026 18:28:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Feb 2026 18:28:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Feb 2026 18:28:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Feb 2026 18:28:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Feb 2026 18:28:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Feb 2026 18:28:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Feb 2026 18:28:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:13 GMT
EXPOSE map[443/tcp:{}]
# Wed, 11 Feb 2026 18:28:13 GMT
EXPOSE map[443/udp:{}]
# Wed, 11 Feb 2026 18:28:13 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 11 Feb 2026 18:28:13 GMT
WORKDIR /srv
# Wed, 11 Feb 2026 18:28:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ebfda0e505485ef95f60e534995ad2bcabbb9cff62daf895e3b59336c7aa74`  
		Last Modified: Wed, 11 Feb 2026 18:28:19 GMT  
		Size: 2.8 MB (2773036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b34d3207db036802002fb1608c601936bed033b2792d4f647e3f162bb34d732`  
		Last Modified: Wed, 11 Feb 2026 18:28:19 GMT  
		Size: 7.5 KB (7501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c15ff4d11340915795742fed835f3d8bc78e96613874ca09f9e29695bf6007`  
		Last Modified: Wed, 11 Feb 2026 18:28:19 GMT  
		Size: 14.5 MB (14517557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:e5971226841ae8f2c264754492e9b5ee9199f127f2f42b15516546dd1d8a92e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 KB (338533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186cc4b2a6c9e26a3c5c77305d73f2b883a1ecf740a7b99586c96e8fab5bfc73`

```dockerfile
```

-	Layers:
	-	`sha256:e5866770164465cb45ba4de02fcb134141bde0d9d0a2ce47e47a81633e585a51`  
		Last Modified: Wed, 11 Feb 2026 18:28:19 GMT  
		Size: 319.9 KB (319921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1e1d83ff540591d6ad49ad3d3badca5203ac4d71296854a367d259defa2450`  
		Last Modified: Wed, 11 Feb 2026 18:28:19 GMT  
		Size: 18.6 KB (18612 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:a46a0437eea0157f60ba2b825c100d99c8de8d8259be657c0a0f5e1642cc79a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21118783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf9acff086125d9ab87614878ba1305a69d8278aeb1983f17a99331f63d3643`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:27:28 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 11 Feb 2026 18:27:34 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 11 Feb 2026 18:27:37 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:27:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 11 Feb 2026 18:27:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 11 Feb 2026 18:27:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 11 Feb 2026 18:27:37 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 11 Feb 2026 18:27:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Feb 2026 18:27:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Feb 2026 18:27:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Feb 2026 18:27:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Feb 2026 18:27:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Feb 2026 18:27:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Feb 2026 18:27:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Feb 2026 18:27:37 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:27:37 GMT
EXPOSE map[443/tcp:{}]
# Wed, 11 Feb 2026 18:27:37 GMT
EXPOSE map[443/udp:{}]
# Wed, 11 Feb 2026 18:27:37 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 11 Feb 2026 18:27:38 GMT
WORKDIR /srv
# Wed, 11 Feb 2026 18:27:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7864d6549a2b53f840d1440abade9446c57b3468579c1ec854a87da6aec204c5`  
		Last Modified: Wed, 11 Feb 2026 18:28:01 GMT  
		Size: 2.9 MB (2881032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5426e3ea259dc024f23bc42ded4d9d2d337021c7fd2ec8fd146faf97c6c72770`  
		Last Modified: Wed, 11 Feb 2026 18:28:00 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41552e2382f48cfbea18e439bd4351a3a3e1bfd3d70c4f7b54c4ef81e972ae`  
		Last Modified: Wed, 11 Feb 2026 18:28:01 GMT  
		Size: 14.5 MB (14495920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:1a54918ff31dbab2a37f4c0492593ad5968822607ced04808de2ce2cbb58cab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 KB (336426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae071f325c167d4e910a0525563964a9ecee2a31e0b8eb11d59f5646a3eae8d1`

```dockerfile
```

-	Layers:
	-	`sha256:38622a7848eac88be53d1a9e8cecdf8ee13666dfe7c632b781a71ebd6a550605`  
		Last Modified: Wed, 11 Feb 2026 18:28:01 GMT  
		Size: 317.9 KB (317924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7dcc280b87b5cb8360bbd52edc278dd880a713c70e0d2536bed0908f7375f2`  
		Last Modified: Wed, 11 Feb 2026 18:28:00 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; riscv64

```console
$ docker pull caddy@sha256:5f7460b231a9ab96dbfdd726882bb4982f6ac9e06b90a914c06f5c56aa1971c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21544385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f640965574b52988d512a8801903fe382031536e0bbce761fcd7b9b2f20832`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:33:01 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 11 Feb 2026 18:33:04 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 11 Feb 2026 18:33:10 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:33:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 11 Feb 2026 18:33:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 11 Feb 2026 18:33:10 GMT
ENV XDG_DATA_HOME=/data
# Wed, 11 Feb 2026 18:33:10 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 11 Feb 2026 18:33:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Feb 2026 18:33:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Feb 2026 18:33:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Feb 2026 18:33:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Feb 2026 18:33:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Feb 2026 18:33:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Feb 2026 18:33:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Feb 2026 18:33:10 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:33:10 GMT
EXPOSE map[443/tcp:{}]
# Wed, 11 Feb 2026 18:33:10 GMT
EXPOSE map[443/udp:{}]
# Wed, 11 Feb 2026 18:33:10 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 11 Feb 2026 18:33:10 GMT
WORKDIR /srv
# Wed, 11 Feb 2026 18:33:10 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8d6bf106e09b4cc1b2fd338f879a46c5152ae2f1b33dede297d1a112a1d164`  
		Last Modified: Wed, 11 Feb 2026 18:34:07 GMT  
		Size: 2.9 MB (2889137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949285627dfc0d00f5b84ff6052bdf47dfc55ab69fd377ecf8b35438a657c0c6`  
		Last Modified: Wed, 11 Feb 2026 18:34:06 GMT  
		Size: 7.5 KB (7506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b93a31c9478898562c01c24dc2fc7e96384cf488b22a0bd936cd58e04c7f22`  
		Last Modified: Wed, 11 Feb 2026 18:34:09 GMT  
		Size: 15.1 MB (15130288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:a294ea2d7ceef07a1ab06086e906644f7eaeb586c3b7001074af35af345e1256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 KB (336422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7079125e27f040dc8631ff78c9928cfcf9511a871384821a371c36f3b5543c2`

```dockerfile
```

-	Layers:
	-	`sha256:2d853812d9c40ef4ea0b4012abe80a8e452c8851fa73a2a27073d95041ff1abd`  
		Last Modified: Wed, 11 Feb 2026 18:34:06 GMT  
		Size: 317.9 KB (317920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7562a4d727b4f5e2f892ca1b559a5d77f183640be5a4f4d988a13b8576759a`  
		Last Modified: Wed, 11 Feb 2026 18:34:06 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:19c924462b6e2ecf2f226a10a96b66c715c17f2b44e9f8e4c82336a0bb07227c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21926310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064189306bffb91bddbc2d07e115f02a062b0cfe34808938f0a49cd840e66d7b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:26:14 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 11 Feb 2026 18:26:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 11 Feb 2026 18:26:16 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 11 Feb 2026 18:26:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='747df7ee74de188485157a383633a1a963fd9233b71fbb4a69ddcbcc589ce4e2cc82dacf5dbbe136cb51d17e14c59daeb5d9bc92487610b0f3b93680b2646546' ;; 		armhf)   binArch='armv6'; checksum='95b71fd99595018eebf4890782de63018ee86455531380b2a83a1814bb09c2588c0a531c877a26ba8a16a5b78072a1c26f7548bdec0e18abcef423fcc31a2e0e' ;; 		armv7)   binArch='armv7'; checksum='215af42cf952726d962c9753a12c04248781221b66df8b7110726fa7905d7a5c2e50056e0b47ab3c709d3dcfb48fde0f11e184a6950de0a2ddf941d3e503d07b' ;; 		aarch64) binArch='arm64'; checksum='6ce061a690312ab38367df3c5d5f89a2e4a263e7300d300d87356211bb81e79b15933e6d6203e03fbf26f15cc0311f264805f336147dbdd24938d84b57a4421c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ab286a51e0e8ce79393519b0c7ebe99075f4539b57f6a34fe555ba8060f8fbaee36197a1e8e49d0050ab5d6a783253839bc2675137635f8d252aea27f2ca5a85' ;; 		riscv64) binArch='riscv64'; checksum='e71c8ba2462990e0d8a67c544b694446ad36d045bf40ce641fae6774181677457f6ae8ed0b5c4c927ef8302d91c587074b6001318f377d7054113b5da6dee6df' ;; 		s390x)   binArch='s390x'; checksum='b8aaa737b63308fac14cf84d7a658d9a0d74d2fe5f6a2eb57ca3ce7c52a73bea702c95da73ebfd20b3206bfb7b71ac8613aef9797e0f7a2c2a04bf5083092c2b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 11 Feb 2026 18:26:16 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 11 Feb 2026 18:26:16 GMT
ENV XDG_DATA_HOME=/data
# Wed, 11 Feb 2026 18:26:16 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Wed, 11 Feb 2026 18:26:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Feb 2026 18:26:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Feb 2026 18:26:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Feb 2026 18:26:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Feb 2026 18:26:16 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Feb 2026 18:26:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Feb 2026 18:26:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Feb 2026 18:26:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:26:16 GMT
EXPOSE map[443/tcp:{}]
# Wed, 11 Feb 2026 18:26:16 GMT
EXPOSE map[443/udp:{}]
# Wed, 11 Feb 2026 18:26:16 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 11 Feb 2026 18:26:16 GMT
WORKDIR /srv
# Wed, 11 Feb 2026 18:26:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac40e8c5d2249dfceb36f54c730ad1fffa323f5f3a6bf6cb829994b96476ac5f`  
		Last Modified: Wed, 11 Feb 2026 18:26:27 GMT  
		Size: 2.9 MB (2911686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaf09939bee32daceccfa9f95f37b36f56a6aaaa2338c1bbd565f1ab00a079e`  
		Last Modified: Wed, 11 Feb 2026 18:26:27 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2091d513078a4e912fac628ad319687e80eba7f02e1da3b71416a9737b6e58`  
		Last Modified: Wed, 11 Feb 2026 18:26:28 GMT  
		Size: 15.4 MB (15356656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:6025e42ea5ce4478e9069c2326b03ffccfdb39791bea3b54696deea897ae55e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 KB (336296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e164b3da5220ffbae6f09f7605fe6dccbffb5932491b5e98ece5de02e273fd`

```dockerfile
```

-	Layers:
	-	`sha256:43ef93f6ae083690726d2b020f4aa6d30644c1702681e5438bfcfcfe9e562270`  
		Last Modified: Wed, 11 Feb 2026 18:26:27 GMT  
		Size: 317.9 KB (317866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb4db0f5f7c724cd4c8b771a4fa16f31e501c6371a78811f59ca9140bbcf412f`  
		Last Modified: Wed, 11 Feb 2026 18:26:27 GMT  
		Size: 18.4 KB (18430 bytes)  
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
