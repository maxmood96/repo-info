## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:7b1bcdd6a0c132849ff0be6cc662df5e5a7791c826cb389ecbe5f2d10da07f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:2728a7a5cc9045d475a134f9230565677fe26deb5306060a0ab766d8449f6ba4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17013282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d954b31fe122c95e58bd7257e100408c9a17c064b065f4c723b46640b61d150c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 00:21:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 19 Jul 2022 00:21:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Tue, 19 Jul 2022 00:21:05 GMT
ENV CADDY_VERSION=v2.5.2
# Tue, 19 Jul 2022 00:21:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 19 Jul 2022 00:21:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 00:21:08 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 19 Jul 2022 00:21:08 GMT
ENV XDG_DATA_HOME=/data
# Tue, 19 Jul 2022 00:21:08 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Tue, 19 Jul 2022 00:21:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 19 Jul 2022 00:21:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 19 Jul 2022 00:21:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 19 Jul 2022 00:21:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 19 Jul 2022 00:21:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 19 Jul 2022 00:21:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 19 Jul 2022 00:21:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 19 Jul 2022 00:21:09 GMT
EXPOSE 80
# Tue, 19 Jul 2022 00:21:09 GMT
EXPOSE 443
# Tue, 19 Jul 2022 00:21:09 GMT
EXPOSE 2019
# Tue, 19 Jul 2022 00:21:09 GMT
WORKDIR /srv
# Tue, 19 Jul 2022 00:21:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0a25d662370cef41a6edf3bceddbd2bda0675eb94f8568d038b7356230396`  
		Last Modified: Tue, 19 Jul 2022 00:21:33 GMT  
		Size: 291.6 KB (291612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a501877fabbb599942a33a45603240e372d191f8322b000c5aafec5a5090c4e`  
		Last Modified: Tue, 19 Jul 2022 00:21:33 GMT  
		Size: 5.8 KB (5825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c62335257e66d56f8fe9203793fb935200c4788ae2328fc7820374794f3d56`  
		Last Modified: Tue, 19 Jul 2022 00:21:36 GMT  
		Size: 13.9 MB (13916885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4608ab095ff261532ff3818afb28725d2548a4d242c96ba13bd0e268249e6a`  
		Last Modified: Tue, 19 Jul 2022 00:21:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a4faffc4f2a46ebc00ece376d805f6be85e994de0d8d98175f84c9ab7e568ee0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16281124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f6682a24f2943790bb0fa25e153cbf1e6b2710c492901e466766ee30b8107d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Mon, 01 Aug 2022 17:53:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 01 Aug 2022 17:53:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Mon, 01 Aug 2022 17:53:17 GMT
ENV CADDY_VERSION=v2.5.2
# Mon, 01 Aug 2022 17:53:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 01 Aug 2022 17:53:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 01 Aug 2022 17:53:20 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 01 Aug 2022 17:53:20 GMT
ENV XDG_DATA_HOME=/data
# Mon, 01 Aug 2022 17:53:20 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Mon, 01 Aug 2022 17:53:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 01 Aug 2022 17:53:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 01 Aug 2022 17:53:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 01 Aug 2022 17:53:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 01 Aug 2022 17:53:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 01 Aug 2022 17:53:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 01 Aug 2022 17:53:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 01 Aug 2022 17:53:21 GMT
EXPOSE 80
# Mon, 01 Aug 2022 17:53:21 GMT
EXPOSE 443
# Mon, 01 Aug 2022 17:53:21 GMT
EXPOSE 2019
# Mon, 01 Aug 2022 17:53:21 GMT
WORKDIR /srv
# Mon, 01 Aug 2022 17:53:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf198df6d3b9a14a8c1f9d5cff7ff7e837de2bf2fda4e86bc7ad4162f7bf558`  
		Last Modified: Mon, 01 Aug 2022 17:54:07 GMT  
		Size: 304.5 KB (304528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a58eb272d93ebe45b0a46f034b4330a4ede9d459fc6770dfa28bc676000379e`  
		Last Modified: Mon, 01 Aug 2022 17:54:06 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cce94f3d2ebd2f4f137aef8435742860d4af63c0f7ef8b7895f74526230be2`  
		Last Modified: Mon, 01 Aug 2022 17:54:09 GMT  
		Size: 13.4 MB (13364178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ce8d08db4149d1084772ab0eae3b77b4e98b15ae51c7b7d9269bd2646a4717`  
		Last Modified: Mon, 01 Aug 2022 17:54:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:980e9f462eee7a087aa262df7c59289cadc189060b5c9d5bd4ba6f5bf0c74229
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16074411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5dd1b61e629ea324876f6a8e52a369f7690d4d0c156f13e7959338e456b3b8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 17:38:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 09 Aug 2022 17:38:04 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Tue, 09 Aug 2022 17:38:04 GMT
ENV CADDY_VERSION=v2.5.2
# Tue, 09 Aug 2022 17:38:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Aug 2022 17:38:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 17:38:08 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Aug 2022 17:38:08 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Aug 2022 17:38:08 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Tue, 09 Aug 2022 17:38:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Aug 2022 17:38:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Aug 2022 17:38:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Aug 2022 17:38:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Aug 2022 17:38:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Aug 2022 17:38:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Aug 2022 17:38:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Aug 2022 17:38:09 GMT
EXPOSE 80
# Tue, 09 Aug 2022 17:38:09 GMT
EXPOSE 443
# Tue, 09 Aug 2022 17:38:09 GMT
EXPOSE 2019
# Tue, 09 Aug 2022 17:38:09 GMT
WORKDIR /srv
# Tue, 09 Aug 2022 17:38:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a152bedd5e8d32263f18ecbb89c23375b9f8ff9de1f90018eb566f96d2fff82`  
		Last Modified: Tue, 09 Aug 2022 17:38:50 GMT  
		Size: 303.6 KB (303607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af139d15b005159bcdde44df64eff617b34ba1611c67bedc740bd59c0eca563`  
		Last Modified: Tue, 09 Aug 2022 17:38:50 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3c3ea87c04a2baa15fec00d92b71ab100e02ba4f48ad59985b92dd61c11524`  
		Last Modified: Tue, 09 Aug 2022 17:38:52 GMT  
		Size: 13.3 MB (13347756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bcfe8f96baeba662c26746cab98fae41f81fbc694fb9f62efa260a82ea4927`  
		Last Modified: Tue, 09 Aug 2022 17:38:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f0a1658deb0cebfeb8d7fe8c239240c1f6481e159a868d065f83e75fe7423faf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15747027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74559eb4a47283b65dda99bf1d258f4d6c6c3e16aa70eb68bf7dcdef174c01a7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:20:53 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 09 Aug 2022 18:20:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Tue, 09 Aug 2022 18:20:56 GMT
ENV CADDY_VERSION=v2.5.2
# Tue, 09 Aug 2022 18:20:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Aug 2022 18:20:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:21:00 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Aug 2022 18:21:01 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Aug 2022 18:21:02 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Tue, 09 Aug 2022 18:21:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Aug 2022 18:21:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Aug 2022 18:21:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Aug 2022 18:21:06 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Aug 2022 18:21:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Aug 2022 18:21:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Aug 2022 18:21:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Aug 2022 18:21:10 GMT
EXPOSE 80
# Tue, 09 Aug 2022 18:21:11 GMT
EXPOSE 443
# Tue, 09 Aug 2022 18:21:12 GMT
EXPOSE 2019
# Tue, 09 Aug 2022 18:21:13 GMT
WORKDIR /srv
# Tue, 09 Aug 2022 18:21:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3baea3c3431660a1c20a2c9648914cc3b5c3bbbcde4e05a678a4b48033bd12`  
		Last Modified: Tue, 09 Aug 2022 18:21:50 GMT  
		Size: 304.3 KB (304299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f196f799aa76056c71d2afcdceb8f201428a6414a77c19e2690acc6b6f6988d`  
		Last Modified: Tue, 09 Aug 2022 18:21:50 GMT  
		Size: 5.8 KB (5750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba74d0141bf051d97aa61935f807fedf17533fdbc3a5eb08ac0ee1c98c8648b`  
		Last Modified: Tue, 09 Aug 2022 18:21:52 GMT  
		Size: 12.7 MB (12729161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4cb521865ac8487439b62e9f1706da781874a29fe38a9aba5b376b968e4c120`  
		Last Modified: Tue, 09 Aug 2022 18:21:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:bf7667d542a7f55a0f6c6f0f8a523c944f34bbf661068697e61dc23672573bc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15425336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc24d4466b7ad1dc55d7eff8335992e5031fe433446a2fe6470133606dedfae`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:00:50 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 09 Aug 2022 18:00:52 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Tue, 09 Aug 2022 18:00:52 GMT
ENV CADDY_VERSION=v2.5.2
# Tue, 09 Aug 2022 18:00:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Aug 2022 18:00:58 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:00:58 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Aug 2022 18:00:58 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Aug 2022 18:00:59 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Tue, 09 Aug 2022 18:01:00 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Aug 2022 18:01:00 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Aug 2022 18:01:01 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Aug 2022 18:01:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Aug 2022 18:01:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Aug 2022 18:01:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Aug 2022 18:01:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Aug 2022 18:01:04 GMT
EXPOSE 80
# Tue, 09 Aug 2022 18:01:04 GMT
EXPOSE 443
# Tue, 09 Aug 2022 18:01:04 GMT
EXPOSE 2019
# Tue, 09 Aug 2022 18:01:04 GMT
WORKDIR /srv
# Tue, 09 Aug 2022 18:01:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d130c379cf611096c8b251962793f03fb6b19d393f7488871a0731fc026264b0`  
		Last Modified: Tue, 09 Aug 2022 18:01:46 GMT  
		Size: 306.5 KB (306509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78df06f4f1ddcab0c1a0a3c315fd94c5b6574d58fa3eec8616d7f3fb75c6f8d1`  
		Last Modified: Tue, 09 Aug 2022 18:01:46 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da367b908cafa68846ec3a4c8b9660b96a6901e3d16e3595b5f1e56caa8c1fd`  
		Last Modified: Tue, 09 Aug 2022 18:01:49 GMT  
		Size: 12.3 MB (12309522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a906ddd96d31e91eedb99d93eb0fb5609cf655ad3cc03c6a885f8a9da37d629d`  
		Last Modified: Tue, 09 Aug 2022 18:01:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bb10dd6ab6ab4e01320b6fdb037c4a4c28dafadffb1348a03b240164034cb99f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16362019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933df8c88011db8f5ddce6060398445ea8b3139efe974c45d3a811acddf8731f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 09 Aug 2022 18:15:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Tue, 09 Aug 2022 18:15:06 GMT
ENV CADDY_VERSION=v2.5.2
# Tue, 09 Aug 2022 18:15:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Aug 2022 18:15:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:15:10 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Aug 2022 18:15:10 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Aug 2022 18:15:10 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Tue, 09 Aug 2022 18:15:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Aug 2022 18:15:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Aug 2022 18:15:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Aug 2022 18:15:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Aug 2022 18:15:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Aug 2022 18:15:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Aug 2022 18:15:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Aug 2022 18:15:11 GMT
EXPOSE 80
# Tue, 09 Aug 2022 18:15:11 GMT
EXPOSE 443
# Tue, 09 Aug 2022 18:15:11 GMT
EXPOSE 2019
# Tue, 09 Aug 2022 18:15:11 GMT
WORKDIR /srv
# Tue, 09 Aug 2022 18:15:11 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75905bff4d3de6daed73e1c8f83d37ce44f2a30ebc2a9764fb82f89c1344ac7e`  
		Last Modified: Tue, 09 Aug 2022 18:15:53 GMT  
		Size: 304.7 KB (304742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352ba655d1c5ab97f65a61931fb410d5dbb71a2aa01bf2c610156fb2c4f76fce`  
		Last Modified: Tue, 09 Aug 2022 18:15:53 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4337a42e49a276ba328d45c8af4bbc1b56c3c67edc730259d1d218a31e263ce`  
		Last Modified: Tue, 09 Aug 2022 18:15:55 GMT  
		Size: 13.5 MB (13460699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73809ed76eaa5655558127e091c5a214118515f72d7c9e085c171a7cc64ae1dd`  
		Last Modified: Tue, 09 Aug 2022 18:15:53 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
