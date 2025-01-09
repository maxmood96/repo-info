## `caddy:alpine`

```console
$ docker pull caddy@sha256:22f8ff07c79bde0ef1c000f04e70f45ac03a448c43d58113a27ff6b92e260315
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
$ docker pull caddy@sha256:c1b2ca303d5fe9c33f74c571066b35a087c3d2501463454cc02e252371222d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18373058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7d0a82297a0ab4d6f0a855f790d0208a975163c02e307c171de9674d23a4a0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='0412057ba591c33bdb66034d7f32209619ce635147dac3084c79abcbc118a761145e695199f57c6798d88fab077f2b0d9cb999f52ded904c6d464a4eba202932' ;; 		armhf)   binArch='armv6'; checksum='4553157b1b3b9e82cd5f6ce7dd5a960927c8a9f96d1c6bfb376be80407a494c9d487377d8c6f77a82e80066f052d8b4f9e2640615f9c3c855e3f53314044d565' ;; 		armv7)   binArch='armv7'; checksum='9650abc74b2a2f014a086536fd52f0c6827adc36e27e82ee3edd8ed2ee82c8bb8f274b5d829be1a809c632214b7d931bd5e760f4cbf87d7d31e3e8ec5f934652' ;; 		aarch64) binArch='arm64'; checksum='80b917c2bd8aa0892f1386ff97af9e776067dd8cdc4793238869aca7e13f7280f89d1799a1fef08b49af92dbd86684c3ba7a38b9d44afc55ef2eeb33b49e1cbd' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='93383bc8f231028810019db624e7be16754db1f3d84f6b9455f3b53275129f208f1ba3a02ee98ebd6b45e61263208d61ecb1b451c429c841988202a373423a34' ;; 		riscv64) binArch='riscv64'; checksum='f6707928f9b2ece9d82a6a1f9ae2154662b79bc9a0747bb0ecb0971b368a4afb1f78b44cda6a6914bc0fdbdeac601d037d5c767801dd41441377d508cf5cd3bd' ;; 		s390x)   binArch='s390x'; checksum='0211cfb04d172eba794831e01273414f983b2c1b28ce3c0b4e5ca829579fdbe43ec2df163f9cb951b778d8ac3579fbcb873b33963b98504fd1d0191e3866b2ac' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XDG_DATA_HOME=/data
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 17:30:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 08 Jan 2025 17:30:49 GMT
EXPOSE map[443/tcp:{}]
# Wed, 08 Jan 2025 17:30:49 GMT
EXPOSE map[443/udp:{}]
# Wed, 08 Jan 2025 17:30:49 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /srv
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb01e15d1864a38be41f49f39a622b31434210052f931f9e9197363f1da47b2`  
		Last Modified: Wed, 08 Jan 2025 23:31:42 GMT  
		Size: 359.2 KB (359195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638a7610da93c8e5c2485069dfc98b710644ee74a110786155db6ae7f3aab06a`  
		Last Modified: Wed, 08 Jan 2025 23:31:42 GMT  
		Size: 7.5 KB (7494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785d93e6656c9f15f1630bc96799a8bf04b324e1156ff8441c617fc0d9ad8017`  
		Last Modified: Wed, 08 Jan 2025 23:31:42 GMT  
		Size: 14.4 MB (14380077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2641a239d15eef321d68d8d7ca1b73192ed9c1e9e0fd1f250b1fafb2216b2694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 KB (299451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738024187bed93f45b724f15a90697820ae731c9347fd4ae138eb79368943e58`

```dockerfile
```

-	Layers:
	-	`sha256:f2c61879a04791f64b48cfee08bee7f37dd3d6dd3fde20dd596fb56b1e7c93d2`  
		Last Modified: Wed, 08 Jan 2025 23:31:42 GMT  
		Size: 281.2 KB (281195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc453f5f784cfd137e11d31187df648a6af38d28fe8915a9c4f5ca6f95ffff8f`  
		Last Modified: Wed, 08 Jan 2025 23:31:42 GMT  
		Size: 18.3 KB (18256 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:c15bc3678d5f0c127a07d06bd56e6f993a0172a127488ca39541930447df9056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17480733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edea398f9d6816860b5a8d61aa07d7b518c1cbefefb78575364a00740d7a9c2a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635f5b2fc88a27638f00b895bb643de7d08b27d0b684fa1cea1ca40b436f34b8`  
		Last Modified: Tue, 07 Jan 2025 18:09:55 GMT  
		Size: 343.5 KB (343475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8fbc790861f95c5dc2696a20d1cc676b86432cf1b370b1592df816c155f9d5`  
		Last Modified: Tue, 07 Jan 2025 18:10:11 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae92bb59d07a7d6ef0d7ae7ec8f78e314f0aca7deefec5fec1c9f83ff634288`  
		Last Modified: Tue, 07 Jan 2025 18:10:11 GMT  
		Size: 13.8 MB (13765832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:976eac6cdbaa639555fae3ef35a38eedca83e0fd6599878e40f50b5a677cb1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a549990c334e258e58bd9a4cbc29e3abe61abf6ed0d10f676cc8e6e38756bc45`

```dockerfile
```

-	Layers:
	-	`sha256:e87c2adb0bdca2402072bd6171f6e2763ff9e8f1f505da019353c428094603ac`  
		Last Modified: Tue, 07 Jan 2025 18:10:11 GMT  
		Size: 18.2 KB (18176 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e6b0d674849e83830e802a07ca1065e5b864ef2438c3c73febe0b51e6735d0a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17178911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c67079080f3e78abb6f193e697714d8a69c5fd049f9beb9f78db4652c7817bb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53bf021d99fe966b28264d81b1aa18a57a08c960444fdad5a10117cbce80e4d`  
		Last Modified: Tue, 07 Jan 2025 18:01:57 GMT  
		Size: 340.3 KB (340284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0307cf68affcc31e4302ecc814c02e02594f39c7d6934b591eaf49bd14b9540`  
		Last Modified: Tue, 07 Jan 2025 18:02:17 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa542a65e90bcf75e8a596866aff58146eca34e685352e478504df4208227378`  
		Last Modified: Tue, 07 Jan 2025 18:02:18 GMT  
		Size: 13.7 MB (13739856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3fb64809bd1e8244f7bea0c9d329f0c26d2910cd02a8b988927c6abd0922b785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 KB (300217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f4115d9aee3c623f4f6d643c154b8f1913d25f7ea7707b125be6374598d618`

```dockerfile
```

-	Layers:
	-	`sha256:a53f829bd6daf9a10115b0219176747b1690d4680412ec511557753fcb4d954c`  
		Last Modified: Tue, 07 Jan 2025 18:02:17 GMT  
		Size: 281.8 KB (281827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fe9fb18c2280ac1d537c60eba015680b6e3435c0e3cd9e9ad5252c2145d372b`  
		Last Modified: Tue, 07 Jan 2025 18:02:17 GMT  
		Size: 18.4 KB (18390 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:5657118a3d299143bc752384baae7324472946ce650c4ad923c010a1f781b1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18001540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8bf58dbe5eb8f8a505de5a8ee2109985d575327366fb40dcc5556277803ed7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c05a3621831e54621e4f1acaf4a8bb5e55116191284ce77a083cabdc4a93fe`  
		Last Modified: Tue, 07 Jan 2025 15:32:47 GMT  
		Size: 356.3 KB (356309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dac5f58ddd3d404206dade70635464b77bcdc1ff2e477103abf966fe860e273`  
		Last Modified: Tue, 07 Jan 2025 15:33:10 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7d82f2281e8decc12a3b38d20d52ed889057e373b3285ca5fbdedc2eeeae7f`  
		Last Modified: Tue, 07 Jan 2025 15:33:11 GMT  
		Size: 13.6 MB (13551061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:47b0b28886df8ba75888966ab5dc81c7bc9f95f23c3dd8d9070bbf104abd9cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 KB (300300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96459bf8f4fac461936d236a0c7bd2ff8b96ddb7f005c529e3da82bb6dbed7f`

```dockerfile
```

-	Layers:
	-	`sha256:706156a27a7bbdab530d5719d0c440aa4df8c9de663a0f118101792896572061`  
		Last Modified: Tue, 07 Jan 2025 15:33:10 GMT  
		Size: 281.9 KB (281863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c79827874ccb509ba3537735c8c3de7cd7aa90854d4700510a93d31a9b2603a`  
		Last Modified: Tue, 07 Jan 2025 15:33:10 GMT  
		Size: 18.4 KB (18437 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8e83bf20b5c34c087f8391c0cc51cf77cf967bf4da2fb96298fbb17df70604eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17014983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d611b6be70adf2fc5d580d3bf2422d16569ee0fb6da9e20d4d5013ddcbdfa2ce`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='0412057ba591c33bdb66034d7f32209619ce635147dac3084c79abcbc118a761145e695199f57c6798d88fab077f2b0d9cb999f52ded904c6d464a4eba202932' ;; 		armhf)   binArch='armv6'; checksum='4553157b1b3b9e82cd5f6ce7dd5a960927c8a9f96d1c6bfb376be80407a494c9d487377d8c6f77a82e80066f052d8b4f9e2640615f9c3c855e3f53314044d565' ;; 		armv7)   binArch='armv7'; checksum='9650abc74b2a2f014a086536fd52f0c6827adc36e27e82ee3edd8ed2ee82c8bb8f274b5d829be1a809c632214b7d931bd5e760f4cbf87d7d31e3e8ec5f934652' ;; 		aarch64) binArch='arm64'; checksum='80b917c2bd8aa0892f1386ff97af9e776067dd8cdc4793238869aca7e13f7280f89d1799a1fef08b49af92dbd86684c3ba7a38b9d44afc55ef2eeb33b49e1cbd' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='93383bc8f231028810019db624e7be16754db1f3d84f6b9455f3b53275129f208f1ba3a02ee98ebd6b45e61263208d61ecb1b451c429c841988202a373423a34' ;; 		riscv64) binArch='riscv64'; checksum='f6707928f9b2ece9d82a6a1f9ae2154662b79bc9a0747bb0ecb0971b368a4afb1f78b44cda6a6914bc0fdbdeac601d037d5c767801dd41441377d508cf5cd3bd' ;; 		s390x)   binArch='s390x'; checksum='0211cfb04d172eba794831e01273414f983b2c1b28ce3c0b4e5ca829579fdbe43ec2df163f9cb951b778d8ac3579fbcb873b33963b98504fd1d0191e3866b2ac' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XDG_DATA_HOME=/data
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 17:30:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 17:30:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 08 Jan 2025 17:30:49 GMT
EXPOSE map[443/tcp:{}]
# Wed, 08 Jan 2025 17:30:49 GMT
EXPOSE map[443/udp:{}]
# Wed, 08 Jan 2025 17:30:49 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /srv
# Wed, 08 Jan 2025 17:30:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44035813f3e40c9fd67013ddcfefa99f2379704c4b3dc5387a296468c08ea254`  
		Last Modified: Thu, 09 Jan 2025 03:29:42 GMT  
		Size: 371.8 KB (371842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96d3541da14a2b1b5783599b6a3eaa159ae44b7cd8e576858c00a4c3c417999`  
		Last Modified: Thu, 09 Jan 2025 03:29:42 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1140b69493877dc8576266826460e30e1e204eb3f77ee8be0f39702af89d4aef`  
		Last Modified: Thu, 09 Jan 2025 03:29:43 GMT  
		Size: 13.1 MB (13061208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:8c18f13b97985ee6daafad560f9ce058e2710fad6bc9dbe26b5084d7f5be050c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 KB (297631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90723c4da0c073abf8a6224813f86454a62adc92c52b5513f578057c8b027ee8`

```dockerfile
```

-	Layers:
	-	`sha256:d76402dbaf498cf028104cfeba5c8317b20d6c10904cec5a926eb01bd9c88bb6`  
		Last Modified: Thu, 09 Jan 2025 03:29:42 GMT  
		Size: 279.3 KB (279302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:784f695b96895edbef7707a7b4d57fa4e574ccf68d069381a4d4a4827b3a733d`  
		Last Modified: Thu, 09 Jan 2025 03:29:42 GMT  
		Size: 18.3 KB (18329 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:f70704a0c9b4084b305b581c3a123df1e333782a5724a474a82fca9e223f4656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17597056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3e0caf24dfdbb872ea87925f2f2939d4653769cae723611b072bb9814a13c0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e4791757fafc8d5ec76994945b7f221ee3a7f72dce5e8491588396b4fd14a`  
		Last Modified: Wed, 13 Nov 2024 11:39:51 GMT  
		Size: 359.1 KB (359083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc9a07b9f1eb5b75ed09670e492ddfe159df28c722bc5037b4baa2b69a079a4`  
		Last Modified: Wed, 13 Nov 2024 11:41:05 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20d0a82f11dde912d4a6d263412df88a3100e9cbc82d72f893baae5f5de6c1`  
		Last Modified: Wed, 13 Nov 2024 11:41:08 GMT  
		Size: 13.9 MB (13859007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e512d9e3dcfdfc8eaefc5fd9e4d36efc271021f1f32f26df279c06c42cb45341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 KB (301862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11891f5e5a63f816a6c4a701994757464a3dd559545082ca5a0327bc2adf4fcf`

```dockerfile
```

-	Layers:
	-	`sha256:a54c64a9e3f6af4b319410f1ab337d6211aff9d5544b7a7f05bddd04002d169e`  
		Last Modified: Wed, 13 Nov 2024 11:41:06 GMT  
		Size: 283.5 KB (283533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa2b6c9c4d6cedf08e5cf26aa83277da3d69b5368c604ef630a28b87d692d86`  
		Last Modified: Wed, 13 Nov 2024 11:41:05 GMT  
		Size: 18.3 KB (18329 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:8d7d5c4e5cfe38c53bcc5e847c8a45f2b6c8eead064debea454713f1dfc2aff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17972902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349053d4302f1752309988239d69475f0d862eecebff62c008a5788d43ca32c1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904289d136591d99b76dcee7d9e790a2a0fa92d4b2ee2c75116aa973eb3bcb6f`  
		Last Modified: Tue, 07 Jan 2025 15:22:21 GMT  
		Size: 350.1 KB (350119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9b0cae016959640155a6057e6e4130c31ab5e9f01713d75495b38f10b087f5`  
		Last Modified: Tue, 07 Jan 2025 15:23:00 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e76b694d641c135ce2727cdefb904a69fbeeea7f887661eee5c7ea3ff4266e`  
		Last Modified: Tue, 07 Jan 2025 15:23:01 GMT  
		Size: 14.2 MB (14156122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:6c293f9356c44565f9e68224d87a776d5df60e340fbbb5366c998a10a529103f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 KB (298065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd7295ff3c920d7453fac1349c2fd05d0ddc3fe610ecbf0950e7a51dab094f9`

```dockerfile
```

-	Layers:
	-	`sha256:5e8aef810fdc6f7efead4b2c3f9a83e859920e11ac7ad981d96c306fb28181b5`  
		Last Modified: Tue, 07 Jan 2025 15:23:00 GMT  
		Size: 279.8 KB (279808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add19e6151e398dd26a8d51fe39889bf6502d6aa540819f597471ec3eef11768`  
		Last Modified: Tue, 07 Jan 2025 15:23:00 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json
