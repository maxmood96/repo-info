## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:834468128c7696cec0ceea6172f7d692daf645ae51983ca76e39da54a97c570d
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
$ docker pull caddy@sha256:6d125e80883be8a2bef5f088c7535945b42cdbb8a0f5471bf36eaf18dc0638f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23755423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad4f81b9a44d531eff80b8d8c65c495c8a867648dc9a3e3720224d7418b3f90`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:05:28 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 15 Apr 2026 21:05:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 15 Apr 2026 21:05:30 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 15 Apr 2026 21:05:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2513b289054386b76642a9e8bfc10d217df2b5361e4cdd0c72672b0eeab57ae737d57466eb70f1a44233cbcc697ecf21de88137ca45ef4b64f150a32b58f5f14' ;; 		armhf)   binArch='armv6'; checksum='bdce2a9c07a17d1ef36fd81cbfcae282de5b5ecc1b911592463e9f06033ff395bbbc2322bff557d086a614223c005f046cc0d5679b70813a8da3c2e2a93463de' ;; 		armv7)   binArch='armv7'; checksum='acb0dc3ece97922b374fef492682b7ecd6d302a417e01abd12570360f055ebe1673d6032a987525475c1181eee7ea7c2efc0b17f1aeec1799303a1efa57deabd' ;; 		aarch64) binArch='arm64'; checksum='630d1e096e3c9594fd2f4f7129356ee5d6c7e53d0ca1b9a0c7486612c6d752ff355c96738c7a28c60367a5f1da4b51afca731bb745fb0b97cda4c811214cdc48' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2f885d026be962b3959cb24adc2294c30f4a385b111216d8aa4296adf700854065c62b4bae7b32228176c8c26ac97193db3a7a38fdffaf74cadde1293ad2e304' ;; 		riscv64) binArch='riscv64'; checksum='4fd9ed8feaa3f239901fd3376897a132ee05c467d73c8b448163cb341c570208b9907ca316a1e475a5b8d4594507a1c5cf65d6cbe2e309af81f7b8a620b3796b' ;; 		s390x)   binArch='s390x'; checksum='d9f6b53330aa36badcde1cce49f38e4e577c24b91ea522eb6680fb49e07cda3b2ee83de83a7e253c3ebf8f2ec38f7de16f75c09a8590c1bf126bdc67df576185' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 15 Apr 2026 21:05:30 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Apr 2026 21:05:30 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Apr 2026 21:05:30 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Wed, 15 Apr 2026 21:05:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Apr 2026 21:05:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Apr 2026 21:05:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Apr 2026 21:05:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Apr 2026 21:05:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Apr 2026 21:05:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Apr 2026 21:05:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Apr 2026 21:05:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 21:05:30 GMT
EXPOSE map[443/tcp:{}]
# Wed, 15 Apr 2026 21:05:30 GMT
EXPOSE map[443/udp:{}]
# Wed, 15 Apr 2026 21:05:30 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 15 Apr 2026 21:05:30 GMT
WORKDIR /srv
# Wed, 15 Apr 2026 21:05:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd08a3fe88bb7e7563b8f138581963f397fb7399862b4879d7fbe1ff6bafce54`  
		Last Modified: Wed, 15 Apr 2026 21:05:38 GMT  
		Size: 2.9 MB (2886734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5a7c34098263ed15f38850e585c7b34edcd871248867cfede711684a39d4dc`  
		Last Modified: Wed, 15 Apr 2026 21:05:38 GMT  
		Size: 7.5 KB (7500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387d6e14b64bd2e00ed062eac5345854cad58a845d4c140d1346d93804b09b9f`  
		Last Modified: Wed, 15 Apr 2026 21:05:38 GMT  
		Size: 17.0 MB (16996968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:abc55c929d940af7df0b360ca8a2209936091ec2533d5305b90bacbe32b6fe35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 KB (351387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cea8aab928821dc8bc52cb203dcfc5889d673223218b119797641412b2bdadf`

```dockerfile
```

-	Layers:
	-	`sha256:2bb97d90f2cc55062405a1c189dc11cbaf07df7f03464d18c90c0e10f1ab80f9`  
		Last Modified: Wed, 15 Apr 2026 21:05:38 GMT  
		Size: 333.0 KB (332957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8905cf2b212dcd2349528eac9a5528d7e3e779700f73a2c7e2bd68a80a6593bb`  
		Last Modified: Wed, 15 Apr 2026 21:05:38 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d9c20c5a5bc0bda14696aa0b66d61edb1be91d462bf55688ec5b9a098933b8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22531783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6e913cfcc72ef8bfc79c14192e95f1c07e35815442ebf40fc38ddfb4592f75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:42:07 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 15 Apr 2026 20:42:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 15 Apr 2026 20:42:10 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 15 Apr 2026 20:42:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2513b289054386b76642a9e8bfc10d217df2b5361e4cdd0c72672b0eeab57ae737d57466eb70f1a44233cbcc697ecf21de88137ca45ef4b64f150a32b58f5f14' ;; 		armhf)   binArch='armv6'; checksum='bdce2a9c07a17d1ef36fd81cbfcae282de5b5ecc1b911592463e9f06033ff395bbbc2322bff557d086a614223c005f046cc0d5679b70813a8da3c2e2a93463de' ;; 		armv7)   binArch='armv7'; checksum='acb0dc3ece97922b374fef492682b7ecd6d302a417e01abd12570360f055ebe1673d6032a987525475c1181eee7ea7c2efc0b17f1aeec1799303a1efa57deabd' ;; 		aarch64) binArch='arm64'; checksum='630d1e096e3c9594fd2f4f7129356ee5d6c7e53d0ca1b9a0c7486612c6d752ff355c96738c7a28c60367a5f1da4b51afca731bb745fb0b97cda4c811214cdc48' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2f885d026be962b3959cb24adc2294c30f4a385b111216d8aa4296adf700854065c62b4bae7b32228176c8c26ac97193db3a7a38fdffaf74cadde1293ad2e304' ;; 		riscv64) binArch='riscv64'; checksum='4fd9ed8feaa3f239901fd3376897a132ee05c467d73c8b448163cb341c570208b9907ca316a1e475a5b8d4594507a1c5cf65d6cbe2e309af81f7b8a620b3796b' ;; 		s390x)   binArch='s390x'; checksum='d9f6b53330aa36badcde1cce49f38e4e577c24b91ea522eb6680fb49e07cda3b2ee83de83a7e253c3ebf8f2ec38f7de16f75c09a8590c1bf126bdc67df576185' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 15 Apr 2026 20:42:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Apr 2026 20:42:10 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Apr 2026 20:42:10 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Wed, 15 Apr 2026 20:42:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Apr 2026 20:42:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Apr 2026 20:42:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Apr 2026 20:42:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Apr 2026 20:42:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Apr 2026 20:42:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Apr 2026 20:42:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Apr 2026 20:42:10 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:42:10 GMT
EXPOSE map[443/tcp:{}]
# Wed, 15 Apr 2026 20:42:10 GMT
EXPOSE map[443/udp:{}]
# Wed, 15 Apr 2026 20:42:10 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 15 Apr 2026 20:42:10 GMT
WORKDIR /srv
# Wed, 15 Apr 2026 20:42:10 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754bf18d6f55658d372ce865b47cf4bff3c9febfaa138e2f5d432bce0eac85d8`  
		Last Modified: Wed, 15 Apr 2026 20:42:15 GMT  
		Size: 2.8 MB (2818744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f43db31aac352e2f2529e0ef6f08be679eae0533ab4f3287f30fe27a501a815`  
		Last Modified: Wed, 15 Apr 2026 20:42:15 GMT  
		Size: 7.5 KB (7501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0369c5706ea08a0dd92c62b30c75b78cf1906a7263dda56ee57393df25cbe9`  
		Last Modified: Wed, 15 Apr 2026 20:42:16 GMT  
		Size: 16.1 MB (16133643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a462bd2b7ce951db47c9a3153d6a501515664b9c98ae60e5e11d31a12221b9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bf5a1382a756bfe878f7b6bf2bf1ed1c9fda66ad57a2fb67e56cde529c91a5`

```dockerfile
```

-	Layers:
	-	`sha256:9ab7f488db1da4a42b4434c77103996854653a050be4a30ec30d88e2f0b30d99`  
		Last Modified: Wed, 15 Apr 2026 20:42:15 GMT  
		Size: 18.4 KB (18353 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:80c19a8c6ce727670ab25eec18e5a3a32076b7c064748b2bf1e36a70b277e227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22092926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2de4a4653874872d6ee8651fa394793c908194e1f71f2ff0526107e2f52aa6c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:54:07 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 15 Apr 2026 20:54:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 15 Apr 2026 20:54:10 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 15 Apr 2026 20:54:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2513b289054386b76642a9e8bfc10d217df2b5361e4cdd0c72672b0eeab57ae737d57466eb70f1a44233cbcc697ecf21de88137ca45ef4b64f150a32b58f5f14' ;; 		armhf)   binArch='armv6'; checksum='bdce2a9c07a17d1ef36fd81cbfcae282de5b5ecc1b911592463e9f06033ff395bbbc2322bff557d086a614223c005f046cc0d5679b70813a8da3c2e2a93463de' ;; 		armv7)   binArch='armv7'; checksum='acb0dc3ece97922b374fef492682b7ecd6d302a417e01abd12570360f055ebe1673d6032a987525475c1181eee7ea7c2efc0b17f1aeec1799303a1efa57deabd' ;; 		aarch64) binArch='arm64'; checksum='630d1e096e3c9594fd2f4f7129356ee5d6c7e53d0ca1b9a0c7486612c6d752ff355c96738c7a28c60367a5f1da4b51afca731bb745fb0b97cda4c811214cdc48' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2f885d026be962b3959cb24adc2294c30f4a385b111216d8aa4296adf700854065c62b4bae7b32228176c8c26ac97193db3a7a38fdffaf74cadde1293ad2e304' ;; 		riscv64) binArch='riscv64'; checksum='4fd9ed8feaa3f239901fd3376897a132ee05c467d73c8b448163cb341c570208b9907ca316a1e475a5b8d4594507a1c5cf65d6cbe2e309af81f7b8a620b3796b' ;; 		s390x)   binArch='s390x'; checksum='d9f6b53330aa36badcde1cce49f38e4e577c24b91ea522eb6680fb49e07cda3b2ee83de83a7e253c3ebf8f2ec38f7de16f75c09a8590c1bf126bdc67df576185' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 15 Apr 2026 20:54:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Apr 2026 20:54:10 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Apr 2026 20:54:10 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Wed, 15 Apr 2026 20:54:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Apr 2026 20:54:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Apr 2026 20:54:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Apr 2026 20:54:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Apr 2026 20:54:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Apr 2026 20:54:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Apr 2026 20:54:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Apr 2026 20:54:10 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:54:10 GMT
EXPOSE map[443/tcp:{}]
# Wed, 15 Apr 2026 20:54:10 GMT
EXPOSE map[443/udp:{}]
# Wed, 15 Apr 2026 20:54:10 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 15 Apr 2026 20:54:10 GMT
WORKDIR /srv
# Wed, 15 Apr 2026 20:54:10 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a4555ae664df5ef7a3a79604bc4c4775ffb3c730e8c84b26ef789e1452839d`  
		Last Modified: Wed, 15 Apr 2026 20:54:16 GMT  
		Size: 2.7 MB (2681342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47a89247b423d7187c0757beecb6a3dc8a57af90c35d6b9502ba415b3f16af7`  
		Last Modified: Wed, 15 Apr 2026 20:54:16 GMT  
		Size: 7.5 KB (7501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e261602ef670734761b84317e2a2a3fb05e911c0c86bb60c33e5ddca506f13c`  
		Last Modified: Wed, 15 Apr 2026 20:54:17 GMT  
		Size: 16.1 MB (16120928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:bdba640f7d67cf4be7e9757e6ba4f31832161d27d601ff08e2655d244d988326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d708c4cf5ef25957502946ab169ff7ca4ce5b2c7e465a99933e89131f6405e`

```dockerfile
```

-	Layers:
	-	`sha256:f35dda686a6b0b0d396a76ddbbdfea98b4e1b6558a82fa1eb17f915a0bc2155a`  
		Last Modified: Wed, 15 Apr 2026 20:54:16 GMT  
		Size: 332.4 KB (332375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5e82525266179f1b3564186be8dfb161de3dc05c9d24e8cd3cf7d0341b49dc4`  
		Last Modified: Wed, 15 Apr 2026 20:54:16 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:df9781ddd351c310248024d964065cd8d41b11fb5d238256d55d30925e8b6ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22603337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e5d14867528ed7ac3dbcea6e8d99be33be0e41d34ada04cab1a7587360810d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:16:46 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 15 Apr 2026 21:16:48 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 15 Apr 2026 21:16:49 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 15 Apr 2026 21:16:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2513b289054386b76642a9e8bfc10d217df2b5361e4cdd0c72672b0eeab57ae737d57466eb70f1a44233cbcc697ecf21de88137ca45ef4b64f150a32b58f5f14' ;; 		armhf)   binArch='armv6'; checksum='bdce2a9c07a17d1ef36fd81cbfcae282de5b5ecc1b911592463e9f06033ff395bbbc2322bff557d086a614223c005f046cc0d5679b70813a8da3c2e2a93463de' ;; 		armv7)   binArch='armv7'; checksum='acb0dc3ece97922b374fef492682b7ecd6d302a417e01abd12570360f055ebe1673d6032a987525475c1181eee7ea7c2efc0b17f1aeec1799303a1efa57deabd' ;; 		aarch64) binArch='arm64'; checksum='630d1e096e3c9594fd2f4f7129356ee5d6c7e53d0ca1b9a0c7486612c6d752ff355c96738c7a28c60367a5f1da4b51afca731bb745fb0b97cda4c811214cdc48' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2f885d026be962b3959cb24adc2294c30f4a385b111216d8aa4296adf700854065c62b4bae7b32228176c8c26ac97193db3a7a38fdffaf74cadde1293ad2e304' ;; 		riscv64) binArch='riscv64'; checksum='4fd9ed8feaa3f239901fd3376897a132ee05c467d73c8b448163cb341c570208b9907ca316a1e475a5b8d4594507a1c5cf65d6cbe2e309af81f7b8a620b3796b' ;; 		s390x)   binArch='s390x'; checksum='d9f6b53330aa36badcde1cce49f38e4e577c24b91ea522eb6680fb49e07cda3b2ee83de83a7e253c3ebf8f2ec38f7de16f75c09a8590c1bf126bdc67df576185' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 15 Apr 2026 21:16:49 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Apr 2026 21:16:49 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Apr 2026 21:16:49 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Wed, 15 Apr 2026 21:16:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Apr 2026 21:16:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Apr 2026 21:16:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Apr 2026 21:16:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Apr 2026 21:16:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Apr 2026 21:16:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Apr 2026 21:16:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Apr 2026 21:16:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 21:16:49 GMT
EXPOSE map[443/tcp:{}]
# Wed, 15 Apr 2026 21:16:49 GMT
EXPOSE map[443/udp:{}]
# Wed, 15 Apr 2026 21:16:49 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 15 Apr 2026 21:16:49 GMT
WORKDIR /srv
# Wed, 15 Apr 2026 21:16:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4607461e91f7ecbaef87742feea979cfc75586911d2d0b5101f937a6fbe4517`  
		Last Modified: Wed, 15 Apr 2026 21:16:57 GMT  
		Size: 2.9 MB (2900897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee22bd3a2003e9e5b25a9bfcf9537e45d7522c3e6151297c9038e27329c6b02`  
		Last Modified: Wed, 15 Apr 2026 21:16:57 GMT  
		Size: 7.5 KB (7500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ed9c85c980fc5c0563c4d3a14afb2ca32965af12d861ff00dd57d2b9bc23b7`  
		Last Modified: Wed, 15 Apr 2026 21:16:57 GMT  
		Size: 15.5 MB (15495038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9a72ae7971e8782e85c3963db8f359ff866dc5b9e5c42c82a2c843e02ad2b519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 KB (351022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cef9b30623372269d1cb6efbba939b0e1055b07e967b2db3bfd67397a6f79d4`

```dockerfile
```

-	Layers:
	-	`sha256:d72cf8e0580700c6cd43110c0f942e38ef9aff664c8f78239e921d6cd43eeae8`  
		Last Modified: Wed, 15 Apr 2026 21:16:57 GMT  
		Size: 332.4 KB (332411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd9565d690a468d34cce75b694dc720deecc349714867a71cae9fa0458c948e`  
		Last Modified: Wed, 15 Apr 2026 21:16:57 GMT  
		Size: 18.6 KB (18611 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:316f585950869019b7d63d84f970bc2dfe49eb42ecc6097f91bf07e6a9eb0abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22350288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4ee2f8221a1a248c2dc2a428bb4c358b9fa361b6a71e9d0b59a85d06072517`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:46:21 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 15 Apr 2026 23:46:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 15 Apr 2026 23:46:26 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 15 Apr 2026 23:46:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2513b289054386b76642a9e8bfc10d217df2b5361e4cdd0c72672b0eeab57ae737d57466eb70f1a44233cbcc697ecf21de88137ca45ef4b64f150a32b58f5f14' ;; 		armhf)   binArch='armv6'; checksum='bdce2a9c07a17d1ef36fd81cbfcae282de5b5ecc1b911592463e9f06033ff395bbbc2322bff557d086a614223c005f046cc0d5679b70813a8da3c2e2a93463de' ;; 		armv7)   binArch='armv7'; checksum='acb0dc3ece97922b374fef492682b7ecd6d302a417e01abd12570360f055ebe1673d6032a987525475c1181eee7ea7c2efc0b17f1aeec1799303a1efa57deabd' ;; 		aarch64) binArch='arm64'; checksum='630d1e096e3c9594fd2f4f7129356ee5d6c7e53d0ca1b9a0c7486612c6d752ff355c96738c7a28c60367a5f1da4b51afca731bb745fb0b97cda4c811214cdc48' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2f885d026be962b3959cb24adc2294c30f4a385b111216d8aa4296adf700854065c62b4bae7b32228176c8c26ac97193db3a7a38fdffaf74cadde1293ad2e304' ;; 		riscv64) binArch='riscv64'; checksum='4fd9ed8feaa3f239901fd3376897a132ee05c467d73c8b448163cb341c570208b9907ca316a1e475a5b8d4594507a1c5cf65d6cbe2e309af81f7b8a620b3796b' ;; 		s390x)   binArch='s390x'; checksum='d9f6b53330aa36badcde1cce49f38e4e577c24b91ea522eb6680fb49e07cda3b2ee83de83a7e253c3ebf8f2ec38f7de16f75c09a8590c1bf126bdc67df576185' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 15 Apr 2026 23:46:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Apr 2026 23:46:26 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Apr 2026 23:46:26 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Wed, 15 Apr 2026 23:46:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Apr 2026 23:46:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Apr 2026 23:46:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Apr 2026 23:46:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Apr 2026 23:46:26 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Apr 2026 23:46:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Apr 2026 23:46:26 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Apr 2026 23:46:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 23:46:26 GMT
EXPOSE map[443/tcp:{}]
# Wed, 15 Apr 2026 23:46:26 GMT
EXPOSE map[443/udp:{}]
# Wed, 15 Apr 2026 23:46:26 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 15 Apr 2026 23:46:26 GMT
WORKDIR /srv
# Wed, 15 Apr 2026 23:46:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617dd572ebb320108a94308d43117f1a1d75991a158c273dc5eb0d16259de3fd`  
		Last Modified: Wed, 15 Apr 2026 23:46:42 GMT  
		Size: 3.0 MB (3024033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6f34265235fcd52bb7b03ebccc54f384853f62bd71763b7d4cfbab93036afa`  
		Last Modified: Wed, 15 Apr 2026 23:46:42 GMT  
		Size: 7.5 KB (7501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd4a1e54ebcb42fb2b8c4b9e536d2d035818d2cf2c4737eebbde97e12aadca`  
		Last Modified: Wed, 15 Apr 2026 23:46:42 GMT  
		Size: 15.5 MB (15487793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7d3e6e045c7691c653a3f9f57118386bb7aa0baa1abcb9158c64f317c8f1e987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ca3344770df97ce63e68cd0aa133fddbb19fd9cd04e11e665263ac7553708d`

```dockerfile
```

-	Layers:
	-	`sha256:e41954236f10bfbcb3fb4c9ef6bc378b8554a0535d570885615efc60fab45007`  
		Last Modified: Wed, 15 Apr 2026 23:46:42 GMT  
		Size: 332.4 KB (332364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f97cee678d723d019d900c88bb7d284bf5ba87965115953869e966e803f5fb5`  
		Last Modified: Wed, 15 Apr 2026 23:46:42 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:7260463ad61733ff5f6f59f878486624bbd2a9b4272518ac08c116c975bec166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22649843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1a8cd86ebff26a92c1450ba06041bbb070b5680a8ea42d13336c38486362a0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 07:16:52 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Fri, 17 Apr 2026 07:16:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Fri, 17 Apr 2026 07:17:01 GMT
ENV CADDY_VERSION=v2.11.2
# Fri, 17 Apr 2026 07:17:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2513b289054386b76642a9e8bfc10d217df2b5361e4cdd0c72672b0eeab57ae737d57466eb70f1a44233cbcc697ecf21de88137ca45ef4b64f150a32b58f5f14' ;; 		armhf)   binArch='armv6'; checksum='bdce2a9c07a17d1ef36fd81cbfcae282de5b5ecc1b911592463e9f06033ff395bbbc2322bff557d086a614223c005f046cc0d5679b70813a8da3c2e2a93463de' ;; 		armv7)   binArch='armv7'; checksum='acb0dc3ece97922b374fef492682b7ecd6d302a417e01abd12570360f055ebe1673d6032a987525475c1181eee7ea7c2efc0b17f1aeec1799303a1efa57deabd' ;; 		aarch64) binArch='arm64'; checksum='630d1e096e3c9594fd2f4f7129356ee5d6c7e53d0ca1b9a0c7486612c6d752ff355c96738c7a28c60367a5f1da4b51afca731bb745fb0b97cda4c811214cdc48' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2f885d026be962b3959cb24adc2294c30f4a385b111216d8aa4296adf700854065c62b4bae7b32228176c8c26ac97193db3a7a38fdffaf74cadde1293ad2e304' ;; 		riscv64) binArch='riscv64'; checksum='4fd9ed8feaa3f239901fd3376897a132ee05c467d73c8b448163cb341c570208b9907ca316a1e475a5b8d4594507a1c5cf65d6cbe2e309af81f7b8a620b3796b' ;; 		s390x)   binArch='s390x'; checksum='d9f6b53330aa36badcde1cce49f38e4e577c24b91ea522eb6680fb49e07cda3b2ee83de83a7e253c3ebf8f2ec38f7de16f75c09a8590c1bf126bdc67df576185' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 17 Apr 2026 07:17:01 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 17 Apr 2026 07:17:01 GMT
ENV XDG_DATA_HOME=/data
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 17 Apr 2026 07:17:01 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Apr 2026 07:17:01 GMT
EXPOSE map[443/tcp:{}]
# Fri, 17 Apr 2026 07:17:01 GMT
EXPOSE map[443/udp:{}]
# Fri, 17 Apr 2026 07:17:01 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 17 Apr 2026 07:17:01 GMT
WORKDIR /srv
# Fri, 17 Apr 2026 07:17:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218bd489171f8531b5e25c99a8157d3b666349873396cc06bbc5ba06381d7d03`  
		Last Modified: Fri, 17 Apr 2026 07:17:48 GMT  
		Size: 3.0 MB (3024643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92411b5bbb77817778886815977dc6ed7c75809299e34e4d778a2b7a4d621f1`  
		Last Modified: Fri, 17 Apr 2026 07:17:47 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8071266f877b5adc028242f20e06c6519af755b22e85e6c83dda823a1e9f8d`  
		Last Modified: Fri, 17 Apr 2026 07:17:50 GMT  
		Size: 16.0 MB (16030001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:5683d2f88f26b57f115706a618e2e3f6979b05adbd4e9b6ec3479953c14139fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64a36beba079609ff2e8ca9f5462b1c9c83de54a347c79d1711addde2dfcff1`

```dockerfile
```

-	Layers:
	-	`sha256:9a67824e1f9bf4caa331a77e012a1ec5ca808374fba22ae8b6f002d139af5c31`  
		Last Modified: Fri, 17 Apr 2026 07:17:47 GMT  
		Size: 332.4 KB (332360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90887d3a5a531e740d5d7de9677bd6c552e11be06d922bb3b262b6a788cc51bb`  
		Last Modified: Fri, 17 Apr 2026 07:17:47 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:244070181a6b00b888a8b5db7a2d203b0c0cf1834fb10051dc0f87f7e2b8d9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23123360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31f0380372448077ca9aff2940b3fce65cc18ca8f0e817c2ecbcc1d96850462`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:34:24 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 15 Apr 2026 23:34:30 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 15 Apr 2026 23:34:35 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 15 Apr 2026 23:34:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2513b289054386b76642a9e8bfc10d217df2b5361e4cdd0c72672b0eeab57ae737d57466eb70f1a44233cbcc697ecf21de88137ca45ef4b64f150a32b58f5f14' ;; 		armhf)   binArch='armv6'; checksum='bdce2a9c07a17d1ef36fd81cbfcae282de5b5ecc1b911592463e9f06033ff395bbbc2322bff557d086a614223c005f046cc0d5679b70813a8da3c2e2a93463de' ;; 		armv7)   binArch='armv7'; checksum='acb0dc3ece97922b374fef492682b7ecd6d302a417e01abd12570360f055ebe1673d6032a987525475c1181eee7ea7c2efc0b17f1aeec1799303a1efa57deabd' ;; 		aarch64) binArch='arm64'; checksum='630d1e096e3c9594fd2f4f7129356ee5d6c7e53d0ca1b9a0c7486612c6d752ff355c96738c7a28c60367a5f1da4b51afca731bb745fb0b97cda4c811214cdc48' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2f885d026be962b3959cb24adc2294c30f4a385b111216d8aa4296adf700854065c62b4bae7b32228176c8c26ac97193db3a7a38fdffaf74cadde1293ad2e304' ;; 		riscv64) binArch='riscv64'; checksum='4fd9ed8feaa3f239901fd3376897a132ee05c467d73c8b448163cb341c570208b9907ca316a1e475a5b8d4594507a1c5cf65d6cbe2e309af81f7b8a620b3796b' ;; 		s390x)   binArch='s390x'; checksum='d9f6b53330aa36badcde1cce49f38e4e577c24b91ea522eb6680fb49e07cda3b2ee83de83a7e253c3ebf8f2ec38f7de16f75c09a8590c1bf126bdc67df576185' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 15 Apr 2026 23:34:35 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Apr 2026 23:34:35 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Apr 2026 23:34:35 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Wed, 15 Apr 2026 23:34:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Apr 2026 23:34:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Apr 2026 23:34:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Apr 2026 23:34:35 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Apr 2026 23:34:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Apr 2026 23:34:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Apr 2026 23:34:35 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Apr 2026 23:34:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 23:34:35 GMT
EXPOSE map[443/tcp:{}]
# Wed, 15 Apr 2026 23:34:35 GMT
EXPOSE map[443/udp:{}]
# Wed, 15 Apr 2026 23:34:35 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 15 Apr 2026 23:34:37 GMT
WORKDIR /srv
# Wed, 15 Apr 2026 23:34:37 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad724463715e239ba7700af915df2b82bc6636bdfae69112f356743dedb4ed9`  
		Last Modified: Wed, 15 Apr 2026 23:35:03 GMT  
		Size: 3.0 MB (3010305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4ae6aabaead9f70c5c505ff0ccda78bd4dbf13b49034ed5a0eeb060e8ce943`  
		Last Modified: Wed, 15 Apr 2026 23:35:03 GMT  
		Size: 7.5 KB (7506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bda9c8ea864d92c0e5830910ae450b3313b061bfb3bb03ae7d54d5b4b089ac`  
		Last Modified: Wed, 15 Apr 2026 23:35:03 GMT  
		Size: 16.4 MB (16378985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f144cd583b99c3c743d7084e00be83c3b0d76563933cfebed993d8b1c46f277a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 KB (350735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e20adf98523adba5d2d766b2a8c200036f2e9b8933c73b63025ffb5526b48c`

```dockerfile
```

-	Layers:
	-	`sha256:66ae81a15a04ae4948c79df788718fe268f1e9b3a3fb13d4d39039a233cb8891`  
		Last Modified: Wed, 15 Apr 2026 23:35:03 GMT  
		Size: 332.3 KB (332306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90f993d512f00938940f624beaf2bfc13879effe0d0ce2fdbcfe76e0f2c1655`  
		Last Modified: Wed, 15 Apr 2026 23:35:02 GMT  
		Size: 18.4 KB (18429 bytes)  
		MIME: application/vnd.in-toto+json
