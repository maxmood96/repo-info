## `caddy:latest`

```console
$ docker pull caddy@sha256:ef6ed6e22b469efd5051e1c4cee221d3a0ebebea14bbb5898c8fb4dc70d12d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4377; amd64
	-	windows version 10.0.20348.1726; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:5acae6b87b26a591d6d14ec2704b7f2cd94b888ad62af16a02356d3124198ede
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17449151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ab4e60cac2e943fc115f5a9ec4f7b91ee165fbabc01b3f00963ce6319d1101`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:40:48 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Wed, 29 Mar 2023 19:40:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 29 Mar 2023 19:40:49 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 29 Mar 2023 19:40:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 29 Mar 2023 19:40:51 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 Mar 2023 19:40:51 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 Mar 2023 19:40:51 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 29 Mar 2023 19:40:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 Mar 2023 19:40:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 Mar 2023 19:40:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 Mar 2023 19:40:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 Mar 2023 19:40:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 Mar 2023 19:40:52 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 Mar 2023 19:40:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 Mar 2023 19:40:52 GMT
EXPOSE 80
# Wed, 29 Mar 2023 19:40:52 GMT
EXPOSE 443
# Wed, 29 Mar 2023 19:40:52 GMT
EXPOSE 443/udp
# Wed, 29 Mar 2023 19:40:52 GMT
EXPOSE 2019
# Wed, 29 Mar 2023 19:40:52 GMT
WORKDIR /srv
# Wed, 29 Mar 2023 19:40:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f137c1fd65aa258552c9e586c735e093ab17bfd56f8b955a45368f75d9dd186`  
		Last Modified: Wed, 29 Mar 2023 19:41:06 GMT  
		Size: 351.2 KB (351170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123731571dfc917eae08527f983c1f454a9fed97dd0454272dbd89c24e8a32c7`  
		Last Modified: Wed, 29 Mar 2023 19:41:06 GMT  
		Size: 7.6 KB (7556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab4cbb8b7b7cfb79fecb20ac12ecf5d3d8cc9c9fe1d05c4dad071564f4748b6`  
		Last Modified: Wed, 29 Mar 2023 19:41:08 GMT  
		Size: 14.3 MB (14282622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:b27532c3b8bee89c27501e93b81d69b60f2bab459e9b967f39d2ccec151c93b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16582574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe9d5fca028312523db46b46629b828c790b9f89b13f31b434725f6232a15c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Wed, 29 Mar 2023 18:46:54 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 29 Mar 2023 18:46:54 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 29 Mar 2023 18:46:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 29 Mar 2023 18:46:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 Mar 2023 18:46:56 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 Mar 2023 18:46:57 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 29 Mar 2023 18:46:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 Mar 2023 18:46:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 Mar 2023 18:46:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 Mar 2023 18:46:57 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 Mar 2023 18:46:57 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 Mar 2023 18:46:57 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 Mar 2023 18:46:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 Mar 2023 18:46:57 GMT
EXPOSE 80
# Wed, 29 Mar 2023 18:46:57 GMT
EXPOSE 443
# Wed, 29 Mar 2023 18:46:57 GMT
EXPOSE 443/udp
# Wed, 29 Mar 2023 18:46:57 GMT
EXPOSE 2019
# Wed, 29 Mar 2023 18:46:58 GMT
WORKDIR /srv
# Wed, 29 Mar 2023 18:46:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4f04d50a24d37f7e9368a95cb9088fa7d5bf8cdfbe3929c8765c4f954507d2`  
		Last Modified: Wed, 29 Mar 2023 18:53:24 GMT  
		Size: 345.9 KB (345890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5a70f8f2e1b052396c9849792ea86786d09a1ff21867462d2a06d4985f9d65`  
		Last Modified: Wed, 29 Mar 2023 18:53:24 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b1bd3eb25fd6c488f51f95377dc1d17fdcc2c687a3042c82d99a84c306137d`  
		Last Modified: Wed, 29 Mar 2023 18:53:26 GMT  
		Size: 13.6 MB (13612281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:4ad2390026191553fc198da4f8d3c9addb4d24b46d2f92e23195a022ba52a1d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16365735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f58ffc22bc39150d1ac5af1b1b8490dc499fc410a2eef48a01d0c7c8cb2c978`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 29 Mar 2023 18:04:21 GMT
ADD file:68992157dbe7c3a454c26656c7bcb497794c1008ead5e078b2928ce165cd65cd in / 
# Wed, 29 Mar 2023 18:04:21 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:39:33 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 30 Mar 2023 00:39:34 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Thu, 30 Mar 2023 00:39:34 GMT
ENV CADDY_VERSION=v2.6.4
# Thu, 30 Mar 2023 00:39:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 30 Mar 2023 00:39:36 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 30 Mar 2023 00:39:37 GMT
ENV XDG_DATA_HOME=/data
# Thu, 30 Mar 2023 00:39:37 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Thu, 30 Mar 2023 00:39:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 Mar 2023 00:39:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 Mar 2023 00:39:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 Mar 2023 00:39:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 Mar 2023 00:39:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 Mar 2023 00:39:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 Mar 2023 00:39:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 Mar 2023 00:39:37 GMT
EXPOSE 80
# Thu, 30 Mar 2023 00:39:37 GMT
EXPOSE 443
# Thu, 30 Mar 2023 00:39:37 GMT
EXPOSE 443/udp
# Thu, 30 Mar 2023 00:39:37 GMT
EXPOSE 2019
# Thu, 30 Mar 2023 00:39:38 GMT
WORKDIR /srv
# Thu, 30 Mar 2023 00:39:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d378ffb313542b797defad9ec843de710c353f40e17e124e74f7e874971429ee`  
		Last Modified: Wed, 29 Mar 2023 18:07:08 GMT  
		Size: 2.4 MB (2420546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b21b970f1be3dd1f6ad93f4233bb05eebdbc1caebe8ab6c769093da8666c467`  
		Last Modified: Thu, 30 Mar 2023 00:40:05 GMT  
		Size: 342.7 KB (342668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ac71d5cd008392394c1e0bec73660595a0e8a2dbe6ab5083c202f2c8a32f06`  
		Last Modified: Thu, 30 Mar 2023 00:40:05 GMT  
		Size: 7.6 KB (7556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7d87e28f1b54178ce40ce4129f58954d0716466859c7cef74b3db045ce73e`  
		Last Modified: Thu, 30 Mar 2023 00:40:07 GMT  
		Size: 13.6 MB (13594965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:5c676a59917cfb48a9c8a8a60df8314bddbde15524450db55f25e2aa598850ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16130847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cac8e331cadbcef5644aae5d39704fc6ec4c5d6c734c2458509675805ca9b1f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 03:54:55 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 30 Mar 2023 03:54:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Thu, 30 Mar 2023 03:54:56 GMT
ENV CADDY_VERSION=v2.6.4
# Thu, 30 Mar 2023 03:54:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 30 Mar 2023 03:54:58 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 30 Mar 2023 03:54:58 GMT
ENV XDG_DATA_HOME=/data
# Thu, 30 Mar 2023 03:54:58 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Thu, 30 Mar 2023 03:54:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 Mar 2023 03:54:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 Mar 2023 03:54:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 Mar 2023 03:54:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 Mar 2023 03:54:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 Mar 2023 03:54:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 Mar 2023 03:54:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 Mar 2023 03:54:59 GMT
EXPOSE 80
# Thu, 30 Mar 2023 03:54:59 GMT
EXPOSE 443
# Thu, 30 Mar 2023 03:54:59 GMT
EXPOSE 443/udp
# Thu, 30 Mar 2023 03:54:59 GMT
EXPOSE 2019
# Thu, 30 Mar 2023 03:54:59 GMT
WORKDIR /srv
# Thu, 30 Mar 2023 03:54:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0f047cc7662980b0739593b7d9ae110e54e817ec4cf6b890d854e1321705cc`  
		Last Modified: Thu, 30 Mar 2023 03:55:11 GMT  
		Size: 350.2 KB (350158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0176485b11b9294cec973ec9fc20ff1a0caf1c601f31cdf81400b26bdc0236`  
		Last Modified: Thu, 30 Mar 2023 03:55:11 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e02e2e7f6d534004c3e59c7fbbe30bc0b90cdea9aa850214e9db3cfd927bf2a`  
		Last Modified: Thu, 30 Mar 2023 03:55:13 GMT  
		Size: 13.1 MB (13063787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:962bb98297c84cbd2004b63e0d4f8f728fb3282162b62031a2728af1d5c95d72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15955238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59a35c3b20b118606a348555696e80b6f71a180fe66b154f37be4495ef06245`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 29 Mar 2023 18:16:34 GMT
ADD file:00a20a25a46ff8ebd9bc78b5b8c6fc5b1dc8ae73d5a42048fa5769a2b2e717c7 in / 
# Wed, 29 Mar 2023 18:16:34 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:39:08 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 30 Mar 2023 04:39:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Thu, 30 Mar 2023 04:39:11 GMT
ENV CADDY_VERSION=v2.6.4
# Thu, 30 Mar 2023 04:39:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 30 Mar 2023 04:39:15 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 30 Mar 2023 04:39:16 GMT
ENV XDG_DATA_HOME=/data
# Thu, 30 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Thu, 30 Mar 2023 04:39:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 Mar 2023 04:39:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 Mar 2023 04:39:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 Mar 2023 04:39:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 Mar 2023 04:39:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 Mar 2023 04:39:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 Mar 2023 04:39:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 Mar 2023 04:39:20 GMT
EXPOSE 80
# Thu, 30 Mar 2023 04:39:20 GMT
EXPOSE 443
# Thu, 30 Mar 2023 04:39:20 GMT
EXPOSE 443/udp
# Thu, 30 Mar 2023 04:39:21 GMT
EXPOSE 2019
# Thu, 30 Mar 2023 04:39:21 GMT
WORKDIR /srv
# Thu, 30 Mar 2023 04:39:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d80736dee7a63492583c90bab1ab07f987ed5e10dfb16fd3f025df3a2d65f1c6`  
		Last Modified: Wed, 29 Mar 2023 18:17:28 GMT  
		Size: 2.8 MB (2804670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ab2c4253c7f672d14502ad6ef639d71074661b50b2e1e71c3318ba0518fe3b`  
		Last Modified: Thu, 30 Mar 2023 04:39:41 GMT  
		Size: 363.1 KB (363089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8b24f9438070c6ab529ee112a06a2e1977b8ad4d29346c3e6dbac9f2f2d9cb`  
		Last Modified: Thu, 30 Mar 2023 04:39:40 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0187deee60d8aeabef55a6a1ef80e48ab121f0ada5f727166d9369521a5f15`  
		Last Modified: Thu, 30 Mar 2023 04:39:43 GMT  
		Size: 12.8 MB (12779922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:2a8d2350281c0b34e785a3822691c36f0d13e1a82038999f993ceaaeb903d652
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16792548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1dee5e3b9e398104c8af3eb418c10a7603849782d837613c4cafe9aca18346`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Tue, 02 May 2023 19:12:39 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Tue, 02 May 2023 19:12:40 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Tue, 02 May 2023 19:12:41 GMT
ENV CADDY_VERSION=v2.6.4
# Tue, 02 May 2023 19:12:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 02 May 2023 19:12:46 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 02 May 2023 19:12:46 GMT
ENV XDG_DATA_HOME=/data
# Tue, 02 May 2023 19:12:46 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Tue, 02 May 2023 19:12:47 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 02 May 2023 19:12:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 02 May 2023 19:12:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 02 May 2023 19:12:48 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 02 May 2023 19:12:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 02 May 2023 19:12:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 02 May 2023 19:12:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 02 May 2023 19:12:48 GMT
EXPOSE 80
# Tue, 02 May 2023 19:12:49 GMT
EXPOSE 443
# Tue, 02 May 2023 19:12:49 GMT
EXPOSE 443/udp
# Tue, 02 May 2023 19:12:49 GMT
EXPOSE 2019
# Tue, 02 May 2023 19:12:49 GMT
WORKDIR /srv
# Tue, 02 May 2023 19:12:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67198d339fb89cea75684337f899057b33b31485993389f2b580d32bc2049bca`  
		Last Modified: Tue, 02 May 2023 19:13:18 GMT  
		Size: 352.8 KB (352796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e681c779f6227da94de2c84d6c813597a989bf4818df00dea18da899298abfd5`  
		Last Modified: Tue, 02 May 2023 19:13:18 GMT  
		Size: 7.6 KB (7560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252df245f95deab402a183510f19ee42e7bc7181cfc7d295c5c6c0385b066624`  
		Last Modified: Tue, 02 May 2023 19:13:20 GMT  
		Size: 13.8 MB (13838803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.4377; amd64

```console
$ docker pull caddy@sha256:bc2d7d1e02ad50bc714bfa3a7ad743b15df542e0364dc6187b0c70a3b1c109e1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087419273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6165e59977df255c3b106cb268a3def0bf7e12ae3bd8d33dff28d04fe72ceb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 May 2023 23:16:14 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 17 May 2023 23:16:15 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 17 May 2023 23:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 17 May 2023 23:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 17 May 2023 23:17:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 17 May 2023 23:17:34 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 17 May 2023 23:17:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 17 May 2023 23:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 17 May 2023 23:17:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 17 May 2023 23:17:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 17 May 2023 23:17:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 17 May 2023 23:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 17 May 2023 23:17:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 17 May 2023 23:17:40 GMT
EXPOSE 80
# Wed, 17 May 2023 23:17:41 GMT
EXPOSE 443
# Wed, 17 May 2023 23:17:41 GMT
EXPOSE 443/udp
# Wed, 17 May 2023 23:17:42 GMT
EXPOSE 2019
# Wed, 17 May 2023 23:18:37 GMT
RUN caddy version
# Wed, 17 May 2023 23:18:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176b87fc080ca7fdc7c92ea024e1c90497e654c4de204eb0b03a6d0ed4bd78d2`  
		Last Modified: Wed, 17 May 2023 23:28:22 GMT  
		Size: 469.2 KB (469175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf87003061971e671f1a695d424921685acd171bab98a88dce4f156d008cbb87`  
		Last Modified: Wed, 17 May 2023 23:28:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357cc2d732a2a48400f8bad2d651c60f2b5cab56e3d10e576eff8f901214242d`  
		Last Modified: Wed, 17 May 2023 23:28:24 GMT  
		Size: 14.6 MB (14624891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44155d97ea1e8d69a6ee8a8bbaaf8afea0f60fae2ea43bbce300825f847b945a`  
		Last Modified: Wed, 17 May 2023 23:28:20 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea7ca6fa2bf47d4c37bf6fbc84178fd9d11dd862036d7bdb83e2ab01f4e42d2`  
		Last Modified: Wed, 17 May 2023 23:28:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdb435e74c32ad492b5c1cb2a48b919e72d5a37629b7a50a8d475656a13be6b`  
		Last Modified: Wed, 17 May 2023 23:28:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254b46732bde7148fc9f8c7e760811c3ae961b0e59baff330c5fd392ecb793ff`  
		Last Modified: Wed, 17 May 2023 23:28:19 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f34bbd5e9b88858e03e38b0c3dd51e6e6d96828ec25fdf49c4f00da99a06a97`  
		Last Modified: Wed, 17 May 2023 23:28:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe6cbca1e8a0e014a3aa7f53fbaf98b521752a9b673657afdb2166e0a4c4fbc`  
		Last Modified: Wed, 17 May 2023 23:28:18 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9f1e8cc1950b9657bca07616003482d380f7183d61a8478d7e3046d7369132`  
		Last Modified: Wed, 17 May 2023 23:28:17 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bf22752b7c25e0936ff2aabc54a4ff7f67a6544be3adff169538e367aecfc8`  
		Last Modified: Wed, 17 May 2023 23:28:17 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c449edb91fa14248bafb2488618627619b724dde19fb336721f4833771bc6ee`  
		Last Modified: Wed, 17 May 2023 23:28:17 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c39a8161d3e4f149bbcdf6f07c177345e446b34d639a62d9688256e265d9bb`  
		Last Modified: Wed, 17 May 2023 23:28:17 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab1a614dc590ee19903d852ff78fc5ba7098a8adcec44af16003b3779d4e308`  
		Last Modified: Wed, 17 May 2023 23:28:16 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd4597bf64cb26d63076b99f65d92175f2951c9ade2979d670e4107048be729`  
		Last Modified: Wed, 17 May 2023 23:28:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c905d64752165883c52beb325f18e8d45997da51a27f42ea1b0c47b3ae0291`  
		Last Modified: Wed, 17 May 2023 23:28:15 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774e79b05989de52e015e3b7456af65d625344730dfe23524f53a642187e793a`  
		Last Modified: Wed, 17 May 2023 23:28:15 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0adf7a67ab73101838663ed8f0c1b78ebdf5c219d8260d00d5ac991a156c143`  
		Last Modified: Wed, 17 May 2023 23:28:15 GMT  
		Size: 266.1 KB (266080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ee3a15ab0ed08997c3e2bdbc39531275d7f4f3d6ade0ac5c0fbb5926d1cf4a`  
		Last Modified: Wed, 17 May 2023 23:28:15 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.1726; amd64

```console
$ docker pull caddy@sha256:2c2b2cee149cf16c7a5e73056128c864b9e4ecec264c94da750e6cb9efbbb70b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1790373055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3612f2107a3cbf6f6483ca6ab233e9cfc4bceed17e966aedafa1afc405080d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 May 2023 23:19:11 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 17 May 2023 23:19:12 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 17 May 2023 23:19:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 17 May 2023 23:19:38 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 17 May 2023 23:19:39 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 17 May 2023 23:19:39 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 17 May 2023 23:19:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 17 May 2023 23:19:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 17 May 2023 23:19:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 17 May 2023 23:19:48 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 17 May 2023 23:19:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 17 May 2023 23:19:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 17 May 2023 23:19:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 17 May 2023 23:19:51 GMT
EXPOSE 80
# Wed, 17 May 2023 23:19:52 GMT
EXPOSE 443
# Wed, 17 May 2023 23:19:53 GMT
EXPOSE 443/udp
# Wed, 17 May 2023 23:19:54 GMT
EXPOSE 2019
# Wed, 17 May 2023 23:20:09 GMT
RUN caddy version
# Wed, 17 May 2023 23:20:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773e7289297a0b670dd0f5b459e443d0fc67abfb369f11bbd6b9443350ca64e5`  
		Last Modified: Wed, 17 May 2023 23:28:46 GMT  
		Size: 465.9 KB (465938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94af1d117cf76c9b6562f1bf3bb48068106a82dd2f1337feb41d90c77db77ab9`  
		Last Modified: Wed, 17 May 2023 23:28:46 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b8a45cf51a4263ef838742c93a2c11d2a9503240c858bffe2fbfd7ad01ec49`  
		Last Modified: Wed, 17 May 2023 23:28:49 GMT  
		Size: 14.6 MB (14615239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c4c68a46692cb9e7c9359ed822b2a67e50a90b978a45f2279bb84d764ee162`  
		Last Modified: Wed, 17 May 2023 23:28:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c9b768fff03f66352a27dae03c8444b146313c11096f83f580e2b541475499`  
		Last Modified: Wed, 17 May 2023 23:28:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532f4b22d25a67fe100c3530f29074d3f3405213dd63f45d4b49376cb265c0a`  
		Last Modified: Wed, 17 May 2023 23:28:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d798b31fccdd732e7d90632a5935e62d21822df0c7d76391503e0fe1c584526`  
		Last Modified: Wed, 17 May 2023 23:28:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd5527e7c7321520aa3e9f8652c3e10918cb8b88cfa5fe5f47caf8930cb03ad`  
		Last Modified: Wed, 17 May 2023 23:28:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6581610a4eeffb57b8289ca72c2fe7e34e2719a97b819bd3422156d0d5611e`  
		Last Modified: Wed, 17 May 2023 23:28:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19fdcf10e626d335dc37d46bdb8e0f84d6a1b3e6d431ae68ad05080beebe08`  
		Last Modified: Wed, 17 May 2023 23:28:43 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343daf867b19c635e13ad92d4343f1ba1742005df62e0be0634dfd3852472831`  
		Last Modified: Wed, 17 May 2023 23:28:42 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debb6649a6130da8389dc7046c8ccf4f2137238de5f6b7862bfb6c19d339acb7`  
		Last Modified: Wed, 17 May 2023 23:28:42 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5320194029403b147910476f029af57fd84deded14e1cc5cc50487fb657a18eb`  
		Last Modified: Wed, 17 May 2023 23:28:42 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159258e57541ba556d195797c078d89804128bb14f4ff8fa91626cf81720e5b2`  
		Last Modified: Wed, 17 May 2023 23:28:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2a7b4b8871c0cda5d19f702ba1b0cbbb8a6b32f6a30767da107f20a2402875`  
		Last Modified: Wed, 17 May 2023 23:28:40 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b857a3a45246a5bbb59fdfe43bc40b06f7e738e6b3d0ecf05ab3208773b4a46`  
		Last Modified: Wed, 17 May 2023 23:28:40 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edcd27ca1e9f7c57518df882d84a4a7220c32187184b74909056355ba5f8f7e`  
		Last Modified: Wed, 17 May 2023 23:28:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fc296cd3515b886a31e9f122eba2e9132ae76437ef43a124fe6ebde52a30db`  
		Last Modified: Wed, 17 May 2023 23:28:41 GMT  
		Size: 288.1 KB (288051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cf4a5a2e6444ddce694b57e8588d1bda0e8ed08cd034125b6277ea824ff6d4`  
		Last Modified: Wed, 17 May 2023 23:28:40 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
