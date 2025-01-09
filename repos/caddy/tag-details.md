<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-1809`](#caddy2-builder-windowsservercore-1809)
-	[`caddy:2-builder-windowsservercore-ltsc2022`](#caddy2-builder-windowsservercore-ltsc2022)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-1809`](#caddy2-windowsservercore-1809)
-	[`caddy:2-windowsservercore-ltsc2022`](#caddy2-windowsservercore-ltsc2022)
-	[`caddy:2.9`](#caddy29)
-	[`caddy:2.9-alpine`](#caddy29-alpine)
-	[`caddy:2.9-builder`](#caddy29-builder)
-	[`caddy:2.9-builder-alpine`](#caddy29-builder-alpine)
-	[`caddy:2.9-builder-windowsservercore-1809`](#caddy29-builder-windowsservercore-1809)
-	[`caddy:2.9-builder-windowsservercore-ltsc2022`](#caddy29-builder-windowsservercore-ltsc2022)
-	[`caddy:2.9-windowsservercore`](#caddy29-windowsservercore)
-	[`caddy:2.9-windowsservercore-1809`](#caddy29-windowsservercore-1809)
-	[`caddy:2.9-windowsservercore-ltsc2022`](#caddy29-windowsservercore-ltsc2022)
-	[`caddy:2.9.1`](#caddy291)
-	[`caddy:2.9.1-alpine`](#caddy291-alpine)
-	[`caddy:2.9.1-builder`](#caddy291-builder)
-	[`caddy:2.9.1-builder-alpine`](#caddy291-builder-alpine)
-	[`caddy:2.9.1-builder-windowsservercore-1809`](#caddy291-builder-windowsservercore-1809)
-	[`caddy:2.9.1-builder-windowsservercore-ltsc2022`](#caddy291-builder-windowsservercore-ltsc2022)
-	[`caddy:2.9.1-windowsservercore`](#caddy291-windowsservercore)
-	[`caddy:2.9.1-windowsservercore-1809`](#caddy291-windowsservercore-1809)
-	[`caddy:2.9.1-windowsservercore-ltsc2022`](#caddy291-windowsservercore-ltsc2022)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:builder-alpine`](#caddybuilder-alpine)
-	[`caddy:builder-windowsservercore-1809`](#caddybuilder-windowsservercore-1809)
-	[`caddy:builder-windowsservercore-ltsc2022`](#caddybuilder-windowsservercore-ltsc2022)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-1809`](#caddywindowsservercore-1809)
-	[`caddy:windowsservercore-ltsc2022`](#caddywindowsservercore-ltsc2022)

## `caddy:2`

```console
$ docker pull caddy@sha256:65955e6725e3f743e57534af15c6efab98b7d6978b5be2efa21cbe8e24bbfaa3
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:2` - linux; amd64

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

### `caddy:2` - unknown; unknown

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

### `caddy:2` - linux; arm variant v6

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

### `caddy:2` - unknown; unknown

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

### `caddy:2` - linux; arm variant v7

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

### `caddy:2` - unknown; unknown

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

### `caddy:2` - linux; arm64 variant v8

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

### `caddy:2` - unknown; unknown

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

### `caddy:2` - linux; ppc64le

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

### `caddy:2` - unknown; unknown

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

### `caddy:2` - linux; riscv64

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

### `caddy:2` - unknown; unknown

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

### `caddy:2` - linux; s390x

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

### `caddy:2` - unknown; unknown

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

### `caddy:2` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

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

### `caddy:2-alpine` - linux; amd64

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

### `caddy:2-alpine` - unknown; unknown

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

### `caddy:2-alpine` - linux; arm variant v6

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

### `caddy:2-alpine` - unknown; unknown

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

### `caddy:2-alpine` - linux; arm variant v7

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

### `caddy:2-alpine` - unknown; unknown

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

### `caddy:2-alpine` - linux; arm64 variant v8

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

### `caddy:2-alpine` - unknown; unknown

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

### `caddy:2-alpine` - linux; ppc64le

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

### `caddy:2-alpine` - unknown; unknown

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

### `caddy:2-alpine` - linux; riscv64

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

### `caddy:2-alpine` - unknown; unknown

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

### `caddy:2-alpine` - linux; s390x

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

### `caddy:2-alpine` - unknown; unknown

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

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:427ad6e5dacffe5577d77e3307fef61efdba832b6a78cc80e6f226975b56e1f1
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:db250d8ac333dbfb36d2082ae73b39f21d1316e42d441199f8fdef60aa578773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4fed372693e3e094c6ca0f1a55f4d71f8e0ce8f751c7a4158a8ad487996162`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe7652777a557be7320acd6bafa585a401104296826b9790d94fa35f28480d`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 294.4 KB (294368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda4308841a6cc675c32eadc7ca82f1f5916886229ff6efcbc6e0f9015d73c80`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f167cb8105c9df8315499305c0ce83016c842a6c68f1e4424182dce22a3fe6d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 5.9 MB (5939538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf2b30687fe7e3fa4f927c76a4e43b2db14a66b0e42a32ea9ddcdfa17e0c7d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed24074f0fd5dc780dad0af8b4260d4205b3b89d7a666396c5b415abc85f2a8`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:75e70c9bd28699ef12d45bf9f03e28ff90a8d151d65e788697b9a7d7af5fe398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fc11bbdfee02d4bdc1dbac347ca232538947335e5e4d6788952c5a38c2494`

```dockerfile
```

-	Layers:
	-	`sha256:a19c370ffc738c2bca6c09b72807b6a1244b6294e4ba0df6aa29eaa2aac91efc`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff92b5cdde37260cee10c8515c7ddc7fe46ee4c87c0b3cbfb1b3cf2f34be315`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ec24df61bf7606d181ee40ab713e0df69a89173fe117883dee14f1e0f8cd9bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83456315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc5eb1a64f9004a10a99b5a85fe75b0f0e58290eeb650f976d94e56f143fe3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ab5d3af8a0c99d02e713511deb39821a107d6d0ba6be4b2f6b0843085aea2a`  
		Last Modified: Tue, 07 Jan 2025 06:50:36 GMT  
		Size: 280.0 KB (279984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868f7227e5c7c8b4bac84441ac5dd24dd837136b8721a4f792daa15e57a2e9ea`  
		Last Modified: Tue, 07 Jan 2025 06:51:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8716a3e393f5147708dc6ab75310ace0722971636dcd1e92fc18a1a08d4310`  
		Last Modified: Tue, 07 Jan 2025 19:16:28 GMT  
		Size: 5.9 MB (5882962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d46024c53346834045856881a3323c9ccff4bd71a3f3f4c6064639d6e1706dc`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 1.7 MB (1730294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12c0eba9000c85b2d1a02d8937fcd9c09c11ce473890d5e26a88237e4ce970d`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:52a385666c18fcec928e4c9dffda6c64c1da8483006166e1b8efc40f8f5bbb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02875baa9933babea5658c74ce320bc6e424b75883b7c032f466e85cdafb1ce8`

```dockerfile
```

-	Layers:
	-	`sha256:86ac3110d2be76dee5e418e092a98d1bfceb80f4af3c2e8eb67b6d8ac5bef969`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:711550b3390725d352325fd551c237a75924d3a4d378d0a8c17d834d6bcae853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82660656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6208081873046fa65434043c2e1dd3a2966207bb5ade720526b54fb97606bfdd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb23a6598e9680ccc41dbb603b77f496c80c87db84ee993d3585d4db8daebd2e`  
		Last Modified: Tue, 07 Jan 2025 06:39:22 GMT  
		Size: 279.2 KB (279170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb64175fa34d7385f5a0720c5acb4845fb41cfffcdb03493609e11dc37a6fd3`  
		Last Modified: Tue, 07 Jan 2025 06:40:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfe46e461df3fdecb8a562830ba9b12245936fb2791b9cedbd7a8ca36b20058`  
		Last Modified: Tue, 07 Jan 2025 19:38:26 GMT  
		Size: 5.4 MB (5366898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84596fbb855fcd21b6ca4c90bd456908377d74cffb2445f95237309d2a484c32`  
		Last Modified: Tue, 07 Jan 2025 19:38:57 GMT  
		Size: 1.7 MB (1724266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a624d5a8ac42b5c2c1445a69ab87ced9badec3de749d9b8599880570b3cb273f`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a8a75354935bc0c2b56ea5d8b81443bde300dba8442dd8b1af1d3b9a109e7839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 KB (310762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb03932eed79a6f6239c181f8ae39f1ac887fb5e37423392abb9df355f32f6d`

```dockerfile
```

-	Layers:
	-	`sha256:ff2ed6da1cb98be75248ee79a7a9982cac41e1383ac1c44a37c63f2d2da0d5bf`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 290.5 KB (290538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e990bba3a097819e2870500e1ffb95d24a29d5089876af934f56a1f29952b84`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c11ef1d0a5c9ed229f43082f29f8ecf422a72aa72bdac93e7b6abc8706f8f7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82800608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce92f6eb0f78cd92a5b165889654838a71ce963d7d0eba1d64d0073ae223be0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4f93e44bdb513724a186600fdec99e49dc6de485ed4757e27b16ec93cbf7b4`  
		Last Modified: Tue, 07 Jan 2025 07:41:57 GMT  
		Size: 281.4 KB (281389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7497157ade0eb8e27bb99f1d2cbe466a3b159a321b071ec86638aa51639752f7`  
		Last Modified: Tue, 07 Jan 2025 07:42:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e208341eb37c26d31056e7b9148bfdf952c929003ac80f238023004a70d9fa`  
		Last Modified: Tue, 07 Jan 2025 17:23:51 GMT  
		Size: 6.1 MB (6057100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3a64dbd3a39b6007f76c39b6ee0c0720d4f4a40cc9dcc8dda3d042db4d37a0`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 1.7 MB (1701424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23ad2d83091707b797b9ad6a73c160439fe1e6ee21e669643988449af62b5e`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ccda48881787a1a9e2e973d61572f691776fed4ffd4e9b624b6bb0b73c9875b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 KB (308018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd4cc2f180b6209f339c8c9c89535d12602c5c9bb3a47255f9e1401e1f98fdd`

```dockerfile
```

-	Layers:
	-	`sha256:2d5335a62a98cd1fb5b9c13a01293700177a9dcae5897f6131a2f51a0de0c371`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 287.7 KB (287749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:509d779c7eb8321ae849c288781db7054c0c756218e63f2864a669f57f982089`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 20.3 KB (20269 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ae070d55ed734bb9f26b8bd370a2505a74b68f8258358df545af4f86f19decf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82669759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d45931cb6f86cb49eb2a88c2fb65ea04da6b51a5931231776eaa748c76c32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10173039484873ca3979a3698ef22d1edfdf1fb0aeabab8ad8b5abf80e36c0b`  
		Last Modified: Wed, 08 Jan 2025 21:52:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e90046d3ba1afd50a6d4a5c6c40609982d2342f650d63e92845f9680191fc04`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 6.3 MB (6261729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6020e3492fb8731819fb401ebf9bea060d1dba0da112cc369801cc6f75181`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 1.7 MB (1695595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31426252091c11d90ffd2cb5692a5923c31dae3911af16cc2973b5164e1ef2`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e0dbaba01b809b9974e5b39e1949a4eba4c650e9c8add5d4940186740ae9c274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6003454eef73ebaabead0aaf06b619bc1eccee16eaf04558aacc5148fc2e00f7`

```dockerfile
```

-	Layers:
	-	`sha256:5ef66216d744cfcfafeb2f64c715c6d373ca1dee38c77308d694033c36689144`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a85f55b9730ad2b1de1532bd27f9a27055fa947fee10a1e04c3641ae2965051`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:6526b547f327fdad247225ea542b9ce1cc77d687884dde4b14b75241e63aa3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82770124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bdb944f99feaf2e305e0d10a42df1c2bf6de1bd0d6138ea9f253171ca76699`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9da01c4ee7a2864330da14801bdf35f981730b5e2ffea0588c9ac48734e26b`  
		Last Modified: Wed, 13 Nov 2024 01:22:36 GMT  
		Size: 291.7 KB (291671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Last Modified: Tue, 03 Dec 2024 22:32:57 GMT  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ab90a88816114ae116bd757c876eb44413901c2699659dffc92325a8501bb`  
		Last Modified: Tue, 03 Dec 2024 22:32:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb90820f994a13ba411ce9f13382e83c031ed0b2d2219db34d7e121af2ca4e4`  
		Last Modified: Tue, 03 Dec 2024 23:30:22 GMT  
		Size: 6.2 MB (6153816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755a3f609dacb1c3c9cfd444c8e0e17d3164ff984a8c8b256ca23bfb5285abd`  
		Last Modified: Tue, 03 Dec 2024 23:32:07 GMT  
		Size: 1.7 MB (1711642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca049294665a12d4c46195094fc9caab2fe1dd23f4387a0bcafa5d4554ad85fc`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:d34f32e4efec0fe90fb35c9ea61321bb53cbd7830923f55f6994fee7e22b2fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3ff966024ddcb0d6b64a1ee4c2603f448aa7bb698535cc33c4fa10b1bde26d`

```dockerfile
```

-	Layers:
	-	`sha256:f83d644b47cbf45f33c3427c879684d93be2f3bb6a034dd204d813c0a3ad241a`  
		Last Modified: Tue, 03 Dec 2024 23:32:07 GMT  
		Size: 290.4 KB (290442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9073f9e18b020a4a883d3c1b52d5b8511b42396b8eb9972a0e5fc216f03d47ce`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:6aa66a7c188127cf3b1d74c61ea008b95a1bdd86535cba563f3582710b036d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84682121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29cc61277738cb7914c72ff20d3bfd79b577ba6b5d721daae3058dc1dfa8244`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141e3fcf5173977fad664af74a255a69a2749551008af76945b144725f228f5f`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 280.2 KB (280152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9039b3f81c901f7abad17b0429809aa980ff70f25d072c8d64ee71f7db3e045`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8aa38916b9a65afe6d745bc7b4405235419055139a947defb9ce792bb28b73`  
		Last Modified: Tue, 07 Jan 2025 16:55:39 GMT  
		Size: 6.2 MB (6200978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8fb1e6bc0540f6045137dc3088acea82454684beb33b47125d22823982d437`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 1.8 MB (1771406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788488d4f2b594a7b69ffa9ada90972f2be7de5973303ff5d5d6dee1ddb5270f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:224cde432b86d4943a06974721e702e3be7c1723fd153c64411a1070d8127f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 KB (305797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914a49da35ae3856968dab023e6d0459b952fca4d12749f61dcda3b1a4bee0cc`

```dockerfile
```

-	Layers:
	-	`sha256:c767f61505dfabedc5ae5df8b49499a6c8fd64d5a2735c26bd1820abd6c01d2f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 285.7 KB (285694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfeae3b8d465e03c17edddbdf5a198fd4d9a0c9a0c78e30622b17a5255100765`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:0189cfa4a4c02a3bb800a7e32a588f1264aa3f8eafa4b94e6ed4129cbe3ff2a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2359343914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d72f15e0f30165074557b2b759d5db3e5947c39aee860af1bdf1e3877f65413`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:29 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:41:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:41:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:41:51 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:41:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:41:57 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:43:05 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:43:07 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:48 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:48 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:34:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:34:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2203f205368ce649ffd4367d83cb7d0e0f349edd4a73d17bf72e1d1fd45547`  
		Last Modified: Wed, 11 Dec 2024 20:43:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a929050203563fde4afe1d48374621524ea8726dc8ca55d3c22d0ac7a798594`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1be8f168e721557e602e0b7a3a7cb7e068d12e159af7b67cbd570277d67b6d3`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a047a2e43f164719e30219f432eae6c44e556b5a49ad8de5c356eef5ceb9f2`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538affaf25305d64f324539f173d0eb2d2dd465cb1762b082450ad4c797f27c`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c69a8ef4d7541c4f17aa73bdd2bc059fbf9e06bb80dba0c6780214385b946`  
		Last Modified: Wed, 11 Dec 2024 20:43:13 GMT  
		Size: 25.4 MB (25433638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8adf8499c2eb9b67d228fba4c9e69a29a2d7060f8b7c5592eacc3be4421710`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb262fe2ef81142570e16f48f8f03d4031993f7f4bdd1e8ddc6130f5ac401023`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 339.0 KB (338961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b81c31620602735496201938ab0373d338f5d0422cdb2fe31bf91e703561180`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a3cd836a09077c7888a8a16d4e7bdf054357c81b2dfc19d8a0d373c88f51d`  
		Last Modified: Wed, 11 Dec 2024 20:43:22 GMT  
		Size: 77.3 MB (77349783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6072f4215eedb6bd6a3744f556ae0cd5807bf437d9168f5f06a714a4935e11ad`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddd9caf64ad2db2b643ff3a12c821a4568fb6cab42c886d58ec94c55611183`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9ad2ce3c975bdb8bb5a956ddacab8f088540115a28bdc8d3c28beab4329aec`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b21bef77b61f0857b5cfc4fdb89f2c1c74d5346d5c5813e145c298a5b86642`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b2d84d7d2cf78270c6457f8ab87188b8d84fcbe934749c67f5a31364f3a84`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f1f09b1a52df9107d2afb46ee59d7d749f2b38fb8bf1a07b9e0ba04de6e6e`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 2.3 MB (2331000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450a1c75f8730f0ad6bb33eaa49034a16cc2b79db5b5098a4afd873dcc3ed769`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:ea06d27be71f8ef91c6d6f553d93e6261efe59e77edf8ca72c562150017510d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2119855201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688816f8244428a55ae1ec4bd192c597ce0f04d19edda948e46a80ecfd9bf8ce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:39:37 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:39:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:40:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:40:47 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:40:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:40:54 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:42:12 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:42:13 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:32 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:32 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:35:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:35:04 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f3bbeb4e2782220c87261e5e9d61855baf0ace86081d92be83026dd5e8fcc2`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241e544e87d299e404e0055ac6a3d562110f5dbac92ab40f5274757c352361`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d65d85ef63918a2fe84d0a5c56c3c6b83838ea5060fc445cb586acaa3fc316`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d89f6bf6b5749f5d1a48d1e66e0f5882aa8e07e2d3218b9a7e1f59c2dda0c`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54a47581ed1b6b7629a8abc75e2e6e45c36975a21ec95b65e8106e75c34aafa`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81645ff46b23f2588b64411ee4dd209ad3383c3b4376b70fa25b258296a5d05`  
		Last Modified: Wed, 11 Dec 2024 20:42:19 GMT  
		Size: 25.6 MB (25561663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619f9252e7182af97b30c9a01c651c8a8f83c521db1c842279b8adaf45bc17ac`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e01c2f476af7e5c6236de3ec31577c6d3d4491c44d2e5cce185341f9d8a19`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 328.3 KB (328344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd74620f512254e194320e032040d3c01472e9f9c304c960171132f8a838cb7`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05934960da5aa39d60d727548d37d080612ea4164a25e09b3c3d9e310f6fa14f`  
		Last Modified: Wed, 11 Dec 2024 20:42:28 GMT  
		Size: 77.5 MB (77463395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d829f35d8061698251f21a9c2ad8cb0d344ddb5465b577017415f89f82d50aa`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0302b0fa76f2e0e3678e4ec6e3a77b56966df7cbd7788ff083f096d58f66eb9`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b2e9a08ab9b486a49339207a0e3c35851ead887e82207dabf747c69de0ef9`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb03d015e74d14f0a3566de1e456b2c92453ba713a378af8d0608061e2f9d06`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7da9a44214dc454bfc9248a3e2db15fda48ce69c4c8f426122a25540d604d20`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0fc2d732d66c3b5aeb005f494441963afb2427e6b8eb07d9f0e0855a328c31`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 2.3 MB (2314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c45570296cf141f1579eb94ca900ddea076099f18b3f5e5dedf41c600a449`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:04a9a96806361a24024ae9331926cc4adf2e3a8e75d71428535293d01173dfd0
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
$ docker pull caddy@sha256:db250d8ac333dbfb36d2082ae73b39f21d1316e42d441199f8fdef60aa578773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4fed372693e3e094c6ca0f1a55f4d71f8e0ce8f751c7a4158a8ad487996162`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe7652777a557be7320acd6bafa585a401104296826b9790d94fa35f28480d`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 294.4 KB (294368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda4308841a6cc675c32eadc7ca82f1f5916886229ff6efcbc6e0f9015d73c80`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f167cb8105c9df8315499305c0ce83016c842a6c68f1e4424182dce22a3fe6d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 5.9 MB (5939538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf2b30687fe7e3fa4f927c76a4e43b2db14a66b0e42a32ea9ddcdfa17e0c7d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed24074f0fd5dc780dad0af8b4260d4205b3b89d7a666396c5b415abc85f2a8`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:75e70c9bd28699ef12d45bf9f03e28ff90a8d151d65e788697b9a7d7af5fe398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fc11bbdfee02d4bdc1dbac347ca232538947335e5e4d6788952c5a38c2494`

```dockerfile
```

-	Layers:
	-	`sha256:a19c370ffc738c2bca6c09b72807b6a1244b6294e4ba0df6aa29eaa2aac91efc`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff92b5cdde37260cee10c8515c7ddc7fe46ee4c87c0b3cbfb1b3cf2f34be315`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ec24df61bf7606d181ee40ab713e0df69a89173fe117883dee14f1e0f8cd9bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83456315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc5eb1a64f9004a10a99b5a85fe75b0f0e58290eeb650f976d94e56f143fe3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ab5d3af8a0c99d02e713511deb39821a107d6d0ba6be4b2f6b0843085aea2a`  
		Last Modified: Tue, 07 Jan 2025 06:50:36 GMT  
		Size: 280.0 KB (279984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868f7227e5c7c8b4bac84441ac5dd24dd837136b8721a4f792daa15e57a2e9ea`  
		Last Modified: Tue, 07 Jan 2025 06:51:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8716a3e393f5147708dc6ab75310ace0722971636dcd1e92fc18a1a08d4310`  
		Last Modified: Tue, 07 Jan 2025 19:16:28 GMT  
		Size: 5.9 MB (5882962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d46024c53346834045856881a3323c9ccff4bd71a3f3f4c6064639d6e1706dc`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 1.7 MB (1730294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12c0eba9000c85b2d1a02d8937fcd9c09c11ce473890d5e26a88237e4ce970d`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:52a385666c18fcec928e4c9dffda6c64c1da8483006166e1b8efc40f8f5bbb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02875baa9933babea5658c74ce320bc6e424b75883b7c032f466e85cdafb1ce8`

```dockerfile
```

-	Layers:
	-	`sha256:86ac3110d2be76dee5e418e092a98d1bfceb80f4af3c2e8eb67b6d8ac5bef969`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:711550b3390725d352325fd551c237a75924d3a4d378d0a8c17d834d6bcae853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82660656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6208081873046fa65434043c2e1dd3a2966207bb5ade720526b54fb97606bfdd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb23a6598e9680ccc41dbb603b77f496c80c87db84ee993d3585d4db8daebd2e`  
		Last Modified: Tue, 07 Jan 2025 06:39:22 GMT  
		Size: 279.2 KB (279170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb64175fa34d7385f5a0720c5acb4845fb41cfffcdb03493609e11dc37a6fd3`  
		Last Modified: Tue, 07 Jan 2025 06:40:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfe46e461df3fdecb8a562830ba9b12245936fb2791b9cedbd7a8ca36b20058`  
		Last Modified: Tue, 07 Jan 2025 19:38:26 GMT  
		Size: 5.4 MB (5366898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84596fbb855fcd21b6ca4c90bd456908377d74cffb2445f95237309d2a484c32`  
		Last Modified: Tue, 07 Jan 2025 19:38:57 GMT  
		Size: 1.7 MB (1724266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a624d5a8ac42b5c2c1445a69ab87ced9badec3de749d9b8599880570b3cb273f`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a8a75354935bc0c2b56ea5d8b81443bde300dba8442dd8b1af1d3b9a109e7839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 KB (310762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb03932eed79a6f6239c181f8ae39f1ac887fb5e37423392abb9df355f32f6d`

```dockerfile
```

-	Layers:
	-	`sha256:ff2ed6da1cb98be75248ee79a7a9982cac41e1383ac1c44a37c63f2d2da0d5bf`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 290.5 KB (290538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e990bba3a097819e2870500e1ffb95d24a29d5089876af934f56a1f29952b84`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c11ef1d0a5c9ed229f43082f29f8ecf422a72aa72bdac93e7b6abc8706f8f7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82800608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce92f6eb0f78cd92a5b165889654838a71ce963d7d0eba1d64d0073ae223be0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4f93e44bdb513724a186600fdec99e49dc6de485ed4757e27b16ec93cbf7b4`  
		Last Modified: Tue, 07 Jan 2025 07:41:57 GMT  
		Size: 281.4 KB (281389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7497157ade0eb8e27bb99f1d2cbe466a3b159a321b071ec86638aa51639752f7`  
		Last Modified: Tue, 07 Jan 2025 07:42:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e208341eb37c26d31056e7b9148bfdf952c929003ac80f238023004a70d9fa`  
		Last Modified: Tue, 07 Jan 2025 17:23:51 GMT  
		Size: 6.1 MB (6057100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3a64dbd3a39b6007f76c39b6ee0c0720d4f4a40cc9dcc8dda3d042db4d37a0`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 1.7 MB (1701424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23ad2d83091707b797b9ad6a73c160439fe1e6ee21e669643988449af62b5e`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ccda48881787a1a9e2e973d61572f691776fed4ffd4e9b624b6bb0b73c9875b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 KB (308018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd4cc2f180b6209f339c8c9c89535d12602c5c9bb3a47255f9e1401e1f98fdd`

```dockerfile
```

-	Layers:
	-	`sha256:2d5335a62a98cd1fb5b9c13a01293700177a9dcae5897f6131a2f51a0de0c371`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 287.7 KB (287749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:509d779c7eb8321ae849c288781db7054c0c756218e63f2864a669f57f982089`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 20.3 KB (20269 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ae070d55ed734bb9f26b8bd370a2505a74b68f8258358df545af4f86f19decf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82669759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d45931cb6f86cb49eb2a88c2fb65ea04da6b51a5931231776eaa748c76c32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10173039484873ca3979a3698ef22d1edfdf1fb0aeabab8ad8b5abf80e36c0b`  
		Last Modified: Wed, 08 Jan 2025 21:52:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e90046d3ba1afd50a6d4a5c6c40609982d2342f650d63e92845f9680191fc04`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 6.3 MB (6261729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6020e3492fb8731819fb401ebf9bea060d1dba0da112cc369801cc6f75181`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 1.7 MB (1695595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31426252091c11d90ffd2cb5692a5923c31dae3911af16cc2973b5164e1ef2`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e0dbaba01b809b9974e5b39e1949a4eba4c650e9c8add5d4940186740ae9c274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6003454eef73ebaabead0aaf06b619bc1eccee16eaf04558aacc5148fc2e00f7`

```dockerfile
```

-	Layers:
	-	`sha256:5ef66216d744cfcfafeb2f64c715c6d373ca1dee38c77308d694033c36689144`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a85f55b9730ad2b1de1532bd27f9a27055fa947fee10a1e04c3641ae2965051`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:6526b547f327fdad247225ea542b9ce1cc77d687884dde4b14b75241e63aa3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82770124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bdb944f99feaf2e305e0d10a42df1c2bf6de1bd0d6138ea9f253171ca76699`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9da01c4ee7a2864330da14801bdf35f981730b5e2ffea0588c9ac48734e26b`  
		Last Modified: Wed, 13 Nov 2024 01:22:36 GMT  
		Size: 291.7 KB (291671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Last Modified: Tue, 03 Dec 2024 22:32:57 GMT  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ab90a88816114ae116bd757c876eb44413901c2699659dffc92325a8501bb`  
		Last Modified: Tue, 03 Dec 2024 22:32:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb90820f994a13ba411ce9f13382e83c031ed0b2d2219db34d7e121af2ca4e4`  
		Last Modified: Tue, 03 Dec 2024 23:30:22 GMT  
		Size: 6.2 MB (6153816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755a3f609dacb1c3c9cfd444c8e0e17d3164ff984a8c8b256ca23bfb5285abd`  
		Last Modified: Tue, 03 Dec 2024 23:32:07 GMT  
		Size: 1.7 MB (1711642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca049294665a12d4c46195094fc9caab2fe1dd23f4387a0bcafa5d4554ad85fc`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:d34f32e4efec0fe90fb35c9ea61321bb53cbd7830923f55f6994fee7e22b2fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3ff966024ddcb0d6b64a1ee4c2603f448aa7bb698535cc33c4fa10b1bde26d`

```dockerfile
```

-	Layers:
	-	`sha256:f83d644b47cbf45f33c3427c879684d93be2f3bb6a034dd204d813c0a3ad241a`  
		Last Modified: Tue, 03 Dec 2024 23:32:07 GMT  
		Size: 290.4 KB (290442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9073f9e18b020a4a883d3c1b52d5b8511b42396b8eb9972a0e5fc216f03d47ce`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:6aa66a7c188127cf3b1d74c61ea008b95a1bdd86535cba563f3582710b036d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84682121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29cc61277738cb7914c72ff20d3bfd79b577ba6b5d721daae3058dc1dfa8244`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141e3fcf5173977fad664af74a255a69a2749551008af76945b144725f228f5f`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 280.2 KB (280152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9039b3f81c901f7abad17b0429809aa980ff70f25d072c8d64ee71f7db3e045`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8aa38916b9a65afe6d745bc7b4405235419055139a947defb9ce792bb28b73`  
		Last Modified: Tue, 07 Jan 2025 16:55:39 GMT  
		Size: 6.2 MB (6200978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8fb1e6bc0540f6045137dc3088acea82454684beb33b47125d22823982d437`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 1.8 MB (1771406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788488d4f2b594a7b69ffa9ada90972f2be7de5973303ff5d5d6dee1ddb5270f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:224cde432b86d4943a06974721e702e3be7c1723fd153c64411a1070d8127f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 KB (305797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914a49da35ae3856968dab023e6d0459b952fca4d12749f61dcda3b1a4bee0cc`

```dockerfile
```

-	Layers:
	-	`sha256:c767f61505dfabedc5ae5df8b49499a6c8fd64d5a2735c26bd1820abd6c01d2f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 285.7 KB (285694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfeae3b8d465e03c17edddbdf5a198fd4d9a0c9a0c78e30622b17a5255100765`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ba8e01cd3489a6d329519bd950beb8f983734752aeb472b4ef6eb1ee8711a7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:ea06d27be71f8ef91c6d6f553d93e6261efe59e77edf8ca72c562150017510d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2119855201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688816f8244428a55ae1ec4bd192c597ce0f04d19edda948e46a80ecfd9bf8ce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:39:37 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:39:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:40:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:40:47 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:40:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:40:54 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:42:12 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:42:13 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:32 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:32 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:35:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:35:04 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f3bbeb4e2782220c87261e5e9d61855baf0ace86081d92be83026dd5e8fcc2`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241e544e87d299e404e0055ac6a3d562110f5dbac92ab40f5274757c352361`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d65d85ef63918a2fe84d0a5c56c3c6b83838ea5060fc445cb586acaa3fc316`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d89f6bf6b5749f5d1a48d1e66e0f5882aa8e07e2d3218b9a7e1f59c2dda0c`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54a47581ed1b6b7629a8abc75e2e6e45c36975a21ec95b65e8106e75c34aafa`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81645ff46b23f2588b64411ee4dd209ad3383c3b4376b70fa25b258296a5d05`  
		Last Modified: Wed, 11 Dec 2024 20:42:19 GMT  
		Size: 25.6 MB (25561663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619f9252e7182af97b30c9a01c651c8a8f83c521db1c842279b8adaf45bc17ac`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e01c2f476af7e5c6236de3ec31577c6d3d4491c44d2e5cce185341f9d8a19`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 328.3 KB (328344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd74620f512254e194320e032040d3c01472e9f9c304c960171132f8a838cb7`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05934960da5aa39d60d727548d37d080612ea4164a25e09b3c3d9e310f6fa14f`  
		Last Modified: Wed, 11 Dec 2024 20:42:28 GMT  
		Size: 77.5 MB (77463395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d829f35d8061698251f21a9c2ad8cb0d344ddb5465b577017415f89f82d50aa`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0302b0fa76f2e0e3678e4ec6e3a77b56966df7cbd7788ff083f096d58f66eb9`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b2e9a08ab9b486a49339207a0e3c35851ead887e82207dabf747c69de0ef9`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb03d015e74d14f0a3566de1e456b2c92453ba713a378af8d0608061e2f9d06`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7da9a44214dc454bfc9248a3e2db15fda48ce69c4c8f426122a25540d604d20`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0fc2d732d66c3b5aeb005f494441963afb2427e6b8eb07d9f0e0855a328c31`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 2.3 MB (2314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c45570296cf141f1579eb94ca900ddea076099f18b3f5e5dedf41c600a449`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:af2dcf0d4a7eae883882f2a63357f55bc484ef53386cb5ceb912e92631130a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:0189cfa4a4c02a3bb800a7e32a588f1264aa3f8eafa4b94e6ed4129cbe3ff2a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2359343914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d72f15e0f30165074557b2b759d5db3e5947c39aee860af1bdf1e3877f65413`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:29 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:41:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:41:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:41:51 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:41:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:41:57 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:43:05 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:43:07 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:48 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:48 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:34:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:34:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2203f205368ce649ffd4367d83cb7d0e0f349edd4a73d17bf72e1d1fd45547`  
		Last Modified: Wed, 11 Dec 2024 20:43:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a929050203563fde4afe1d48374621524ea8726dc8ca55d3c22d0ac7a798594`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1be8f168e721557e602e0b7a3a7cb7e068d12e159af7b67cbd570277d67b6d3`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a047a2e43f164719e30219f432eae6c44e556b5a49ad8de5c356eef5ceb9f2`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538affaf25305d64f324539f173d0eb2d2dd465cb1762b082450ad4c797f27c`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c69a8ef4d7541c4f17aa73bdd2bc059fbf9e06bb80dba0c6780214385b946`  
		Last Modified: Wed, 11 Dec 2024 20:43:13 GMT  
		Size: 25.4 MB (25433638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8adf8499c2eb9b67d228fba4c9e69a29a2d7060f8b7c5592eacc3be4421710`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb262fe2ef81142570e16f48f8f03d4031993f7f4bdd1e8ddc6130f5ac401023`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 339.0 KB (338961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b81c31620602735496201938ab0373d338f5d0422cdb2fe31bf91e703561180`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a3cd836a09077c7888a8a16d4e7bdf054357c81b2dfc19d8a0d373c88f51d`  
		Last Modified: Wed, 11 Dec 2024 20:43:22 GMT  
		Size: 77.3 MB (77349783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6072f4215eedb6bd6a3744f556ae0cd5807bf437d9168f5f06a714a4935e11ad`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddd9caf64ad2db2b643ff3a12c821a4568fb6cab42c886d58ec94c55611183`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9ad2ce3c975bdb8bb5a956ddacab8f088540115a28bdc8d3c28beab4329aec`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b21bef77b61f0857b5cfc4fdb89f2c1c74d5346d5c5813e145c298a5b86642`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b2d84d7d2cf78270c6457f8ab87188b8d84fcbe934749c67f5a31364f3a84`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f1f09b1a52df9107d2afb46ee59d7d749f2b38fb8bf1a07b9e0ba04de6e6e`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 2.3 MB (2331000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450a1c75f8730f0ad6bb33eaa49034a16cc2b79db5b5098a4afd873dcc3ed769`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:8e842a56471df259c7282c7827f1a7c4b8f24de694d1892428bd6c421d29052a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:1307996d1255d8cba23d2b956a5f47525051154fc907edffeafbdc9ce01b6460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:4d4fc4b1242a7788c646c9d733cf131cea76ed6ee655570a41d2ea783cb56e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9`

```console
$ docker pull caddy@sha256:8ea64c7494ad8d8029ddee2752423cc897e498556075363f68d4dede01b5bd26
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:2.9` - linux; amd64

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

### `caddy:2.9` - unknown; unknown

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

### `caddy:2.9` - linux; arm variant v6

```console
$ docker pull caddy@sha256:198f5cf6d36d2d05c8f6ec2093da8d2dac7b6e0f99654344d02db48d533e4bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17181573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bf8f149075c5e5a0c7627452917bbbd4ff1ea416f1163bbddf8a57540f45ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='c38d63d3dc58e50cf6bb9af873f61c265624dcdaf5eb2de834f309148d0faed162f83d27b073e729318e63f28cd2958c93a5e0467fbbaf82624b54925dec97dc' ;; 		armhf)   binArch='armv6'; checksum='aadf515dc43ab035d75595414560c8d9168e4b5823feef441b7846170ac5c9d4ed382c2024b8c8fab2cb4000cb89612870aae9a15f355b15f5931c63b75e06b5' ;; 		armv7)   binArch='armv7'; checksum='c9a189a4d92c4872d429a6f5dffb12a53237dbf8a98c45985d531ab71200d84a49c9d120026799035cb03cc8c75a37be07e65d590900976a82cdf6355f7872aa' ;; 		aarch64) binArch='arm64'; checksum='094c0f5a82dabafb707f050d637a2858f3ec0a4865d99f51808a76a30e4e2e466d4534ec48fd830b369c7c9e2bcdfb9fe3132fdbcf94dd3256d5f0bcc6b0b062' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3dca4a42a50540f5256a49528dffcf6456a571392ac6bab628933e5dde0b344eca39920625982d426e741c4af3bc38a8a20373a082d9cd332a19e293c60738e5' ;; 		riscv64) binArch='riscv64'; checksum='ba28761fa1809061884dea5487f23b4aae19ce02902982ae424f1916489a7934056f2a18cff1a08808d545c5ea97022e3f5ca9a28e23aa9aa90a775a50fd93dc' ;; 		s390x)   binArch='s390x'; checksum='fcd39452bd96f952eb66035acf1d3493a6f4884fcedcc52fae3dc700e3a1e280b862facf2d4a6a0150d652116796e368e73756169ca8924c34e102be4b0ab24f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.0-beta.3/caddy_2.9.0-beta.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.version=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/udp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /srv
# Wed, 06 Nov 2024 00:46:53 GMT
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
	-	`sha256:8636d8c0a0412c886be4c5464e9c925bc0b84582fbeeff786318b8594ad8b644`  
		Last Modified: Tue, 07 Jan 2025 18:09:55 GMT  
		Size: 7.5 KB (7494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8271ef57e6364dad36f9bbbd8ddd3fb86d434ade7b979cb1c6f7390375a7e7be`  
		Last Modified: Tue, 07 Jan 2025 18:09:56 GMT  
		Size: 13.5 MB (13466628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9` - unknown; unknown

```console
$ docker pull caddy@sha256:dac82d85902e5d580e62b334d937e2786c1c08753b2297c962271a41a2fc5b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac6a6bb84a3202e863ac4d690ecfc50e46a5c62421d9e07d5980fd511310187`

```dockerfile
```

-	Layers:
	-	`sha256:e8312d3fbbf21ef5472da9398438c68719bf76714a2b3da154862b2e352a5b10`  
		Last Modified: Tue, 07 Jan 2025 18:09:55 GMT  
		Size: 17.1 KB (17055 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9` - linux; arm variant v7

```console
$ docker pull caddy@sha256:62e03ee28c3f4d5a07ba6bf07af06e1079d0c568cb42ff81fb3e4bcf730fc280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16882779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256ec7ac02b34c237540328123dcbccc949b63da81e02164b667e9742b37cd80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='c38d63d3dc58e50cf6bb9af873f61c265624dcdaf5eb2de834f309148d0faed162f83d27b073e729318e63f28cd2958c93a5e0467fbbaf82624b54925dec97dc' ;; 		armhf)   binArch='armv6'; checksum='aadf515dc43ab035d75595414560c8d9168e4b5823feef441b7846170ac5c9d4ed382c2024b8c8fab2cb4000cb89612870aae9a15f355b15f5931c63b75e06b5' ;; 		armv7)   binArch='armv7'; checksum='c9a189a4d92c4872d429a6f5dffb12a53237dbf8a98c45985d531ab71200d84a49c9d120026799035cb03cc8c75a37be07e65d590900976a82cdf6355f7872aa' ;; 		aarch64) binArch='arm64'; checksum='094c0f5a82dabafb707f050d637a2858f3ec0a4865d99f51808a76a30e4e2e466d4534ec48fd830b369c7c9e2bcdfb9fe3132fdbcf94dd3256d5f0bcc6b0b062' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3dca4a42a50540f5256a49528dffcf6456a571392ac6bab628933e5dde0b344eca39920625982d426e741c4af3bc38a8a20373a082d9cd332a19e293c60738e5' ;; 		riscv64) binArch='riscv64'; checksum='ba28761fa1809061884dea5487f23b4aae19ce02902982ae424f1916489a7934056f2a18cff1a08808d545c5ea97022e3f5ca9a28e23aa9aa90a775a50fd93dc' ;; 		s390x)   binArch='s390x'; checksum='fcd39452bd96f952eb66035acf1d3493a6f4884fcedcc52fae3dc700e3a1e280b862facf2d4a6a0150d652116796e368e73756169ca8924c34e102be4b0ab24f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.0-beta.3/caddy_2.9.0-beta.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.version=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/udp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /srv
# Wed, 06 Nov 2024 00:46:53 GMT
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
	-	`sha256:317c0da0ddb915b7add373210ff06bc64713614c79fe3757b0a49a7bf2abe589`  
		Last Modified: Tue, 07 Jan 2025 18:01:57 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7472f4d325291ebe610120edadea45b41de79e18a7c84cb432ae097b00a9ea`  
		Last Modified: Tue, 07 Jan 2025 18:01:58 GMT  
		Size: 13.4 MB (13443680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9` - unknown; unknown

```console
$ docker pull caddy@sha256:b275d562b1fc6008c5367cb5b51df9aa96aa2274e684a47898a3cfa9e9cf2f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 KB (291545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7978c2a0e95deebfe3927edc895acf91eb20b467a1d771d95f3ba17b46a859cf`

```dockerfile
```

-	Layers:
	-	`sha256:cbf4425cb8c0f03ac9355df7c11c9defa9a32293659d9b66950a30266b76ff1c`  
		Last Modified: Tue, 07 Jan 2025 18:01:58 GMT  
		Size: 274.3 KB (274275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e3d2ca686fde12105443de703f340794105db1a037974d35fb2aad35b8e13d`  
		Last Modified: Tue, 07 Jan 2025 18:01:57 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:11c2112e19ae9416eb6c7597049dcbb2932e23a0e93e81f8e060048de6b69024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17731085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a408719370529fe4726b8f8487d05ace34d721fb3c4009df2e014e29d47263b9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='c38d63d3dc58e50cf6bb9af873f61c265624dcdaf5eb2de834f309148d0faed162f83d27b073e729318e63f28cd2958c93a5e0467fbbaf82624b54925dec97dc' ;; 		armhf)   binArch='armv6'; checksum='aadf515dc43ab035d75595414560c8d9168e4b5823feef441b7846170ac5c9d4ed382c2024b8c8fab2cb4000cb89612870aae9a15f355b15f5931c63b75e06b5' ;; 		armv7)   binArch='armv7'; checksum='c9a189a4d92c4872d429a6f5dffb12a53237dbf8a98c45985d531ab71200d84a49c9d120026799035cb03cc8c75a37be07e65d590900976a82cdf6355f7872aa' ;; 		aarch64) binArch='arm64'; checksum='094c0f5a82dabafb707f050d637a2858f3ec0a4865d99f51808a76a30e4e2e466d4534ec48fd830b369c7c9e2bcdfb9fe3132fdbcf94dd3256d5f0bcc6b0b062' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3dca4a42a50540f5256a49528dffcf6456a571392ac6bab628933e5dde0b344eca39920625982d426e741c4af3bc38a8a20373a082d9cd332a19e293c60738e5' ;; 		riscv64) binArch='riscv64'; checksum='ba28761fa1809061884dea5487f23b4aae19ce02902982ae424f1916489a7934056f2a18cff1a08808d545c5ea97022e3f5ca9a28e23aa9aa90a775a50fd93dc' ;; 		s390x)   binArch='s390x'; checksum='fcd39452bd96f952eb66035acf1d3493a6f4884fcedcc52fae3dc700e3a1e280b862facf2d4a6a0150d652116796e368e73756169ca8924c34e102be4b0ab24f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.0-beta.3/caddy_2.9.0-beta.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.version=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/udp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /srv
# Wed, 06 Nov 2024 00:46:53 GMT
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
	-	`sha256:eaacdf1a6fde8b871875870aaf4d793c6b91563aa00668695c8dcd4142ea0148`  
		Last Modified: Tue, 07 Jan 2025 15:32:47 GMT  
		Size: 7.5 KB (7494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f47beb7e07cb73063aecaca18464c8b05c3fa5cdf27beeb5b15363d8c7c1777`  
		Last Modified: Tue, 07 Jan 2025 15:32:48 GMT  
		Size: 13.3 MB (13280564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9` - unknown; unknown

```console
$ docker pull caddy@sha256:c8380cc4ed3c6e449c2f7c8c5442d23be2f2cdc38abcc3f74a067193f3e6f536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 KB (291596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9002f15c4637d2c3efb3e4b3adeb7ff095bd00ebfa5c4101472532a296caac7f`

```dockerfile
```

-	Layers:
	-	`sha256:a03b40200c3923c13e281a7e9cd6eb77a202e3c96c82aa670e8aaf8b3e946496`  
		Last Modified: Tue, 07 Jan 2025 15:32:47 GMT  
		Size: 274.3 KB (274295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5928092abe4f042ec931d57713ce6b356e27e9693324cbe4c3bfb84a74616e35`  
		Last Modified: Tue, 07 Jan 2025 15:32:47 GMT  
		Size: 17.3 KB (17301 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9` - linux; ppc64le

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

### `caddy:2.9` - unknown; unknown

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

### `caddy:2.9` - linux; riscv64

```console
$ docker pull caddy@sha256:7d9bd476ef3f431062a744e7f0de2332a7b39cbf57805d245fe57be20ecd9109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17301241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3f2170681d8025cfcdff5f402fc6a717bbd27e0f5b87c88d6f0186be13ad65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='c38d63d3dc58e50cf6bb9af873f61c265624dcdaf5eb2de834f309148d0faed162f83d27b073e729318e63f28cd2958c93a5e0467fbbaf82624b54925dec97dc' ;; 		armhf)   binArch='armv6'; checksum='aadf515dc43ab035d75595414560c8d9168e4b5823feef441b7846170ac5c9d4ed382c2024b8c8fab2cb4000cb89612870aae9a15f355b15f5931c63b75e06b5' ;; 		armv7)   binArch='armv7'; checksum='c9a189a4d92c4872d429a6f5dffb12a53237dbf8a98c45985d531ab71200d84a49c9d120026799035cb03cc8c75a37be07e65d590900976a82cdf6355f7872aa' ;; 		aarch64) binArch='arm64'; checksum='094c0f5a82dabafb707f050d637a2858f3ec0a4865d99f51808a76a30e4e2e466d4534ec48fd830b369c7c9e2bcdfb9fe3132fdbcf94dd3256d5f0bcc6b0b062' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3dca4a42a50540f5256a49528dffcf6456a571392ac6bab628933e5dde0b344eca39920625982d426e741c4af3bc38a8a20373a082d9cd332a19e293c60738e5' ;; 		riscv64) binArch='riscv64'; checksum='ba28761fa1809061884dea5487f23b4aae19ce02902982ae424f1916489a7934056f2a18cff1a08808d545c5ea97022e3f5ca9a28e23aa9aa90a775a50fd93dc' ;; 		s390x)   binArch='s390x'; checksum='fcd39452bd96f952eb66035acf1d3493a6f4884fcedcc52fae3dc700e3a1e280b862facf2d4a6a0150d652116796e368e73756169ca8924c34e102be4b0ab24f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.0-beta.3/caddy_2.9.0-beta.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.version=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/udp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /srv
# Wed, 06 Nov 2024 00:46:53 GMT
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
	-	`sha256:9b6ef700caede266aef2cc62c4fbf5a5f6a0bc48a15c2693d05d4635e3ca797c`  
		Last Modified: Wed, 13 Nov 2024 11:39:51 GMT  
		Size: 7.5 KB (7501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629938f93af507c1f047311af8acd8fee6f2aa5552c195a4e4e93e5649ee514f`  
		Last Modified: Wed, 13 Nov 2024 11:39:53 GMT  
		Size: 13.6 MB (13563143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9` - unknown; unknown

```console
$ docker pull caddy@sha256:323aba930db4a7d30652e64d4cbe281170294aec3915ddcc9216a208fcbed65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 KB (293285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3553f46ef399f4be4b0391e5e5fff8a9a7e374b4d9092921b5e1fb1ad6d89c`

```dockerfile
```

-	Layers:
	-	`sha256:6b4f991765394c1cfd7f786746d782e9f000e506510074fff8959ff4e8054488`  
		Last Modified: Wed, 13 Nov 2024 11:39:51 GMT  
		Size: 276.1 KB (276069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6485cd41c07abb11b5e157d58186623602bd31856ef44f271dcfb7cf0ce3ffb0`  
		Last Modified: Wed, 13 Nov 2024 11:39:51 GMT  
		Size: 17.2 KB (17216 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9` - linux; s390x

```console
$ docker pull caddy@sha256:8a7fed27787a43cdd9ef39298717912aabb77afacd7b3b671c19b596f81fadbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17699443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5166a134ea20426be43d3bcd07a11c755e09f50664b97d712dac55688a20a7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='c38d63d3dc58e50cf6bb9af873f61c265624dcdaf5eb2de834f309148d0faed162f83d27b073e729318e63f28cd2958c93a5e0467fbbaf82624b54925dec97dc' ;; 		armhf)   binArch='armv6'; checksum='aadf515dc43ab035d75595414560c8d9168e4b5823feef441b7846170ac5c9d4ed382c2024b8c8fab2cb4000cb89612870aae9a15f355b15f5931c63b75e06b5' ;; 		armv7)   binArch='armv7'; checksum='c9a189a4d92c4872d429a6f5dffb12a53237dbf8a98c45985d531ab71200d84a49c9d120026799035cb03cc8c75a37be07e65d590900976a82cdf6355f7872aa' ;; 		aarch64) binArch='arm64'; checksum='094c0f5a82dabafb707f050d637a2858f3ec0a4865d99f51808a76a30e4e2e466d4534ec48fd830b369c7c9e2bcdfb9fe3132fdbcf94dd3256d5f0bcc6b0b062' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3dca4a42a50540f5256a49528dffcf6456a571392ac6bab628933e5dde0b344eca39920625982d426e741c4af3bc38a8a20373a082d9cd332a19e293c60738e5' ;; 		riscv64) binArch='riscv64'; checksum='ba28761fa1809061884dea5487f23b4aae19ce02902982ae424f1916489a7934056f2a18cff1a08808d545c5ea97022e3f5ca9a28e23aa9aa90a775a50fd93dc' ;; 		s390x)   binArch='s390x'; checksum='fcd39452bd96f952eb66035acf1d3493a6f4884fcedcc52fae3dc700e3a1e280b862facf2d4a6a0150d652116796e368e73756169ca8924c34e102be4b0ab24f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.0-beta.3/caddy_2.9.0-beta.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.version=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/udp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /srv
# Wed, 06 Nov 2024 00:46:53 GMT
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
	-	`sha256:dc0ee0d94997080e20e286c8a3a7b7242d694857672d9ad4d2b2809822b22a4b`  
		Last Modified: Tue, 07 Jan 2025 15:22:21 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a41a9ae157a31dfdf986fad7ca834c843d5e41af937c653771868ce51c4669a`  
		Last Modified: Tue, 07 Jan 2025 15:22:21 GMT  
		Size: 13.9 MB (13882618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9` - unknown; unknown

```console
$ docker pull caddy@sha256:9df73e5fefd9555c98cd7c361fee1cf9ec1e2c02001444999fe1bd890c2d8d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 KB (289456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc05fcbbf1541be33b258f35634e9140b55cf6aea4185d86df044edad79fbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bcf8eebf1154a2ed42df8c7e483c59936e81d7934cdfa9e575ede8cdc385301e`  
		Last Modified: Tue, 07 Jan 2025 15:22:21 GMT  
		Size: 272.3 KB (272288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d378b24c1e681fc9bd132702f72f844b68128941b4e030cfd1f388f5cb496b9`  
		Last Modified: Tue, 07 Jan 2025 15:22:21 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.9` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9-alpine`

```console
$ docker pull caddy@sha256:c0b125c11b119457bb08f832a4bfa75e3a03ef63f8a256d9712a599868026c31
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

### `caddy:2.9-alpine` - linux; amd64

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

### `caddy:2.9-alpine` - unknown; unknown

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

### `caddy:2.9-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:198f5cf6d36d2d05c8f6ec2093da8d2dac7b6e0f99654344d02db48d533e4bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17181573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bf8f149075c5e5a0c7627452917bbbd4ff1ea416f1163bbddf8a57540f45ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='c38d63d3dc58e50cf6bb9af873f61c265624dcdaf5eb2de834f309148d0faed162f83d27b073e729318e63f28cd2958c93a5e0467fbbaf82624b54925dec97dc' ;; 		armhf)   binArch='armv6'; checksum='aadf515dc43ab035d75595414560c8d9168e4b5823feef441b7846170ac5c9d4ed382c2024b8c8fab2cb4000cb89612870aae9a15f355b15f5931c63b75e06b5' ;; 		armv7)   binArch='armv7'; checksum='c9a189a4d92c4872d429a6f5dffb12a53237dbf8a98c45985d531ab71200d84a49c9d120026799035cb03cc8c75a37be07e65d590900976a82cdf6355f7872aa' ;; 		aarch64) binArch='arm64'; checksum='094c0f5a82dabafb707f050d637a2858f3ec0a4865d99f51808a76a30e4e2e466d4534ec48fd830b369c7c9e2bcdfb9fe3132fdbcf94dd3256d5f0bcc6b0b062' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3dca4a42a50540f5256a49528dffcf6456a571392ac6bab628933e5dde0b344eca39920625982d426e741c4af3bc38a8a20373a082d9cd332a19e293c60738e5' ;; 		riscv64) binArch='riscv64'; checksum='ba28761fa1809061884dea5487f23b4aae19ce02902982ae424f1916489a7934056f2a18cff1a08808d545c5ea97022e3f5ca9a28e23aa9aa90a775a50fd93dc' ;; 		s390x)   binArch='s390x'; checksum='fcd39452bd96f952eb66035acf1d3493a6f4884fcedcc52fae3dc700e3a1e280b862facf2d4a6a0150d652116796e368e73756169ca8924c34e102be4b0ab24f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.0-beta.3/caddy_2.9.0-beta.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.version=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/udp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /srv
# Wed, 06 Nov 2024 00:46:53 GMT
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
	-	`sha256:8636d8c0a0412c886be4c5464e9c925bc0b84582fbeeff786318b8594ad8b644`  
		Last Modified: Tue, 07 Jan 2025 18:09:55 GMT  
		Size: 7.5 KB (7494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8271ef57e6364dad36f9bbbd8ddd3fb86d434ade7b979cb1c6f7390375a7e7be`  
		Last Modified: Tue, 07 Jan 2025 18:09:56 GMT  
		Size: 13.5 MB (13466628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:dac82d85902e5d580e62b334d937e2786c1c08753b2297c962271a41a2fc5b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac6a6bb84a3202e863ac4d690ecfc50e46a5c62421d9e07d5980fd511310187`

```dockerfile
```

-	Layers:
	-	`sha256:e8312d3fbbf21ef5472da9398438c68719bf76714a2b3da154862b2e352a5b10`  
		Last Modified: Tue, 07 Jan 2025 18:09:55 GMT  
		Size: 17.1 KB (17055 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:62e03ee28c3f4d5a07ba6bf07af06e1079d0c568cb42ff81fb3e4bcf730fc280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16882779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256ec7ac02b34c237540328123dcbccc949b63da81e02164b667e9742b37cd80`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='c38d63d3dc58e50cf6bb9af873f61c265624dcdaf5eb2de834f309148d0faed162f83d27b073e729318e63f28cd2958c93a5e0467fbbaf82624b54925dec97dc' ;; 		armhf)   binArch='armv6'; checksum='aadf515dc43ab035d75595414560c8d9168e4b5823feef441b7846170ac5c9d4ed382c2024b8c8fab2cb4000cb89612870aae9a15f355b15f5931c63b75e06b5' ;; 		armv7)   binArch='armv7'; checksum='c9a189a4d92c4872d429a6f5dffb12a53237dbf8a98c45985d531ab71200d84a49c9d120026799035cb03cc8c75a37be07e65d590900976a82cdf6355f7872aa' ;; 		aarch64) binArch='arm64'; checksum='094c0f5a82dabafb707f050d637a2858f3ec0a4865d99f51808a76a30e4e2e466d4534ec48fd830b369c7c9e2bcdfb9fe3132fdbcf94dd3256d5f0bcc6b0b062' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3dca4a42a50540f5256a49528dffcf6456a571392ac6bab628933e5dde0b344eca39920625982d426e741c4af3bc38a8a20373a082d9cd332a19e293c60738e5' ;; 		riscv64) binArch='riscv64'; checksum='ba28761fa1809061884dea5487f23b4aae19ce02902982ae424f1916489a7934056f2a18cff1a08808d545c5ea97022e3f5ca9a28e23aa9aa90a775a50fd93dc' ;; 		s390x)   binArch='s390x'; checksum='fcd39452bd96f952eb66035acf1d3493a6f4884fcedcc52fae3dc700e3a1e280b862facf2d4a6a0150d652116796e368e73756169ca8924c34e102be4b0ab24f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.0-beta.3/caddy_2.9.0-beta.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.version=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/udp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /srv
# Wed, 06 Nov 2024 00:46:53 GMT
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
	-	`sha256:317c0da0ddb915b7add373210ff06bc64713614c79fe3757b0a49a7bf2abe589`  
		Last Modified: Tue, 07 Jan 2025 18:01:57 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7472f4d325291ebe610120edadea45b41de79e18a7c84cb432ae097b00a9ea`  
		Last Modified: Tue, 07 Jan 2025 18:01:58 GMT  
		Size: 13.4 MB (13443680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b275d562b1fc6008c5367cb5b51df9aa96aa2274e684a47898a3cfa9e9cf2f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 KB (291545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7978c2a0e95deebfe3927edc895acf91eb20b467a1d771d95f3ba17b46a859cf`

```dockerfile
```

-	Layers:
	-	`sha256:cbf4425cb8c0f03ac9355df7c11c9defa9a32293659d9b66950a30266b76ff1c`  
		Last Modified: Tue, 07 Jan 2025 18:01:58 GMT  
		Size: 274.3 KB (274275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e3d2ca686fde12105443de703f340794105db1a037974d35fb2aad35b8e13d`  
		Last Modified: Tue, 07 Jan 2025 18:01:57 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:11c2112e19ae9416eb6c7597049dcbb2932e23a0e93e81f8e060048de6b69024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17731085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a408719370529fe4726b8f8487d05ace34d721fb3c4009df2e014e29d47263b9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='c38d63d3dc58e50cf6bb9af873f61c265624dcdaf5eb2de834f309148d0faed162f83d27b073e729318e63f28cd2958c93a5e0467fbbaf82624b54925dec97dc' ;; 		armhf)   binArch='armv6'; checksum='aadf515dc43ab035d75595414560c8d9168e4b5823feef441b7846170ac5c9d4ed382c2024b8c8fab2cb4000cb89612870aae9a15f355b15f5931c63b75e06b5' ;; 		armv7)   binArch='armv7'; checksum='c9a189a4d92c4872d429a6f5dffb12a53237dbf8a98c45985d531ab71200d84a49c9d120026799035cb03cc8c75a37be07e65d590900976a82cdf6355f7872aa' ;; 		aarch64) binArch='arm64'; checksum='094c0f5a82dabafb707f050d637a2858f3ec0a4865d99f51808a76a30e4e2e466d4534ec48fd830b369c7c9e2bcdfb9fe3132fdbcf94dd3256d5f0bcc6b0b062' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3dca4a42a50540f5256a49528dffcf6456a571392ac6bab628933e5dde0b344eca39920625982d426e741c4af3bc38a8a20373a082d9cd332a19e293c60738e5' ;; 		riscv64) binArch='riscv64'; checksum='ba28761fa1809061884dea5487f23b4aae19ce02902982ae424f1916489a7934056f2a18cff1a08808d545c5ea97022e3f5ca9a28e23aa9aa90a775a50fd93dc' ;; 		s390x)   binArch='s390x'; checksum='fcd39452bd96f952eb66035acf1d3493a6f4884fcedcc52fae3dc700e3a1e280b862facf2d4a6a0150d652116796e368e73756169ca8924c34e102be4b0ab24f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.0-beta.3/caddy_2.9.0-beta.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.version=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/udp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /srv
# Wed, 06 Nov 2024 00:46:53 GMT
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
	-	`sha256:eaacdf1a6fde8b871875870aaf4d793c6b91563aa00668695c8dcd4142ea0148`  
		Last Modified: Tue, 07 Jan 2025 15:32:47 GMT  
		Size: 7.5 KB (7494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f47beb7e07cb73063aecaca18464c8b05c3fa5cdf27beeb5b15363d8c7c1777`  
		Last Modified: Tue, 07 Jan 2025 15:32:48 GMT  
		Size: 13.3 MB (13280564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c8380cc4ed3c6e449c2f7c8c5442d23be2f2cdc38abcc3f74a067193f3e6f536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 KB (291596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9002f15c4637d2c3efb3e4b3adeb7ff095bd00ebfa5c4101472532a296caac7f`

```dockerfile
```

-	Layers:
	-	`sha256:a03b40200c3923c13e281a7e9cd6eb77a202e3c96c82aa670e8aaf8b3e946496`  
		Last Modified: Tue, 07 Jan 2025 15:32:47 GMT  
		Size: 274.3 KB (274295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5928092abe4f042ec931d57713ce6b356e27e9693324cbe4c3bfb84a74616e35`  
		Last Modified: Tue, 07 Jan 2025 15:32:47 GMT  
		Size: 17.3 KB (17301 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-alpine` - linux; ppc64le

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

### `caddy:2.9-alpine` - unknown; unknown

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

### `caddy:2.9-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:7d9bd476ef3f431062a744e7f0de2332a7b39cbf57805d245fe57be20ecd9109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17301241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3f2170681d8025cfcdff5f402fc6a717bbd27e0f5b87c88d6f0186be13ad65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='c38d63d3dc58e50cf6bb9af873f61c265624dcdaf5eb2de834f309148d0faed162f83d27b073e729318e63f28cd2958c93a5e0467fbbaf82624b54925dec97dc' ;; 		armhf)   binArch='armv6'; checksum='aadf515dc43ab035d75595414560c8d9168e4b5823feef441b7846170ac5c9d4ed382c2024b8c8fab2cb4000cb89612870aae9a15f355b15f5931c63b75e06b5' ;; 		armv7)   binArch='armv7'; checksum='c9a189a4d92c4872d429a6f5dffb12a53237dbf8a98c45985d531ab71200d84a49c9d120026799035cb03cc8c75a37be07e65d590900976a82cdf6355f7872aa' ;; 		aarch64) binArch='arm64'; checksum='094c0f5a82dabafb707f050d637a2858f3ec0a4865d99f51808a76a30e4e2e466d4534ec48fd830b369c7c9e2bcdfb9fe3132fdbcf94dd3256d5f0bcc6b0b062' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3dca4a42a50540f5256a49528dffcf6456a571392ac6bab628933e5dde0b344eca39920625982d426e741c4af3bc38a8a20373a082d9cd332a19e293c60738e5' ;; 		riscv64) binArch='riscv64'; checksum='ba28761fa1809061884dea5487f23b4aae19ce02902982ae424f1916489a7934056f2a18cff1a08808d545c5ea97022e3f5ca9a28e23aa9aa90a775a50fd93dc' ;; 		s390x)   binArch='s390x'; checksum='fcd39452bd96f952eb66035acf1d3493a6f4884fcedcc52fae3dc700e3a1e280b862facf2d4a6a0150d652116796e368e73756169ca8924c34e102be4b0ab24f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.0-beta.3/caddy_2.9.0-beta.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.version=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/udp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /srv
# Wed, 06 Nov 2024 00:46:53 GMT
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
	-	`sha256:9b6ef700caede266aef2cc62c4fbf5a5f6a0bc48a15c2693d05d4635e3ca797c`  
		Last Modified: Wed, 13 Nov 2024 11:39:51 GMT  
		Size: 7.5 KB (7501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629938f93af507c1f047311af8acd8fee6f2aa5552c195a4e4e93e5649ee514f`  
		Last Modified: Wed, 13 Nov 2024 11:39:53 GMT  
		Size: 13.6 MB (13563143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:323aba930db4a7d30652e64d4cbe281170294aec3915ddcc9216a208fcbed65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 KB (293285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3553f46ef399f4be4b0391e5e5fff8a9a7e374b4d9092921b5e1fb1ad6d89c`

```dockerfile
```

-	Layers:
	-	`sha256:6b4f991765394c1cfd7f786746d782e9f000e506510074fff8959ff4e8054488`  
		Last Modified: Wed, 13 Nov 2024 11:39:51 GMT  
		Size: 276.1 KB (276069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6485cd41c07abb11b5e157d58186623602bd31856ef44f271dcfb7cf0ce3ffb0`  
		Last Modified: Wed, 13 Nov 2024 11:39:51 GMT  
		Size: 17.2 KB (17216 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:8a7fed27787a43cdd9ef39298717912aabb77afacd7b3b671c19b596f81fadbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17699443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5166a134ea20426be43d3bcd07a11c755e09f50664b97d712dac55688a20a7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='c38d63d3dc58e50cf6bb9af873f61c265624dcdaf5eb2de834f309148d0faed162f83d27b073e729318e63f28cd2958c93a5e0467fbbaf82624b54925dec97dc' ;; 		armhf)   binArch='armv6'; checksum='aadf515dc43ab035d75595414560c8d9168e4b5823feef441b7846170ac5c9d4ed382c2024b8c8fab2cb4000cb89612870aae9a15f355b15f5931c63b75e06b5' ;; 		armv7)   binArch='armv7'; checksum='c9a189a4d92c4872d429a6f5dffb12a53237dbf8a98c45985d531ab71200d84a49c9d120026799035cb03cc8c75a37be07e65d590900976a82cdf6355f7872aa' ;; 		aarch64) binArch='arm64'; checksum='094c0f5a82dabafb707f050d637a2858f3ec0a4865d99f51808a76a30e4e2e466d4534ec48fd830b369c7c9e2bcdfb9fe3132fdbcf94dd3256d5f0bcc6b0b062' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3dca4a42a50540f5256a49528dffcf6456a571392ac6bab628933e5dde0b344eca39920625982d426e741c4af3bc38a8a20373a082d9cd332a19e293c60738e5' ;; 		riscv64) binArch='riscv64'; checksum='ba28761fa1809061884dea5487f23b4aae19ce02902982ae424f1916489a7934056f2a18cff1a08808d545c5ea97022e3f5ca9a28e23aa9aa90a775a50fd93dc' ;; 		s390x)   binArch='s390x'; checksum='fcd39452bd96f952eb66035acf1d3493a6f4884fcedcc52fae3dc700e3a1e280b862facf2d4a6a0150d652116796e368e73756169ca8924c34e102be4b0ab24f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.9.0-beta.3/caddy_2.9.0-beta.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.version=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 Nov 2024 00:46:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[443/udp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /srv
# Wed, 06 Nov 2024 00:46:53 GMT
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
	-	`sha256:dc0ee0d94997080e20e286c8a3a7b7242d694857672d9ad4d2b2809822b22a4b`  
		Last Modified: Tue, 07 Jan 2025 15:22:21 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a41a9ae157a31dfdf986fad7ca834c843d5e41af937c653771868ce51c4669a`  
		Last Modified: Tue, 07 Jan 2025 15:22:21 GMT  
		Size: 13.9 MB (13882618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9df73e5fefd9555c98cd7c361fee1cf9ec1e2c02001444999fe1bd890c2d8d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 KB (289456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc05fcbbf1541be33b258f35634e9140b55cf6aea4185d86df044edad79fbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bcf8eebf1154a2ed42df8c7e483c59936e81d7934cdfa9e575ede8cdc385301e`  
		Last Modified: Tue, 07 Jan 2025 15:22:21 GMT  
		Size: 272.3 KB (272288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d378b24c1e681fc9bd132702f72f844b68128941b4e030cfd1f388f5cb496b9`  
		Last Modified: Tue, 07 Jan 2025 15:22:21 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.9-builder`

```console
$ docker pull caddy@sha256:57e9424fad50d900db8cb4873d93208967d2d573da51695cf369cdf718de2bae
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:2.9-builder` - linux; amd64

```console
$ docker pull caddy@sha256:db250d8ac333dbfb36d2082ae73b39f21d1316e42d441199f8fdef60aa578773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4fed372693e3e094c6ca0f1a55f4d71f8e0ce8f751c7a4158a8ad487996162`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe7652777a557be7320acd6bafa585a401104296826b9790d94fa35f28480d`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 294.4 KB (294368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda4308841a6cc675c32eadc7ca82f1f5916886229ff6efcbc6e0f9015d73c80`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f167cb8105c9df8315499305c0ce83016c842a6c68f1e4424182dce22a3fe6d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 5.9 MB (5939538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf2b30687fe7e3fa4f927c76a4e43b2db14a66b0e42a32ea9ddcdfa17e0c7d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed24074f0fd5dc780dad0af8b4260d4205b3b89d7a666396c5b415abc85f2a8`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:75e70c9bd28699ef12d45bf9f03e28ff90a8d151d65e788697b9a7d7af5fe398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fc11bbdfee02d4bdc1dbac347ca232538947335e5e4d6788952c5a38c2494`

```dockerfile
```

-	Layers:
	-	`sha256:a19c370ffc738c2bca6c09b72807b6a1244b6294e4ba0df6aa29eaa2aac91efc`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff92b5cdde37260cee10c8515c7ddc7fe46ee4c87c0b3cbfb1b3cf2f34be315`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:09330ddca8ff56a6486098ba6c3277ae0efdeb584e30208cb42d917f6475e7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83456311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751c85b57ea579ea3860bf3dc947281387591caca52f0e32766a2c5613ebfefd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ab5d3af8a0c99d02e713511deb39821a107d6d0ba6be4b2f6b0843085aea2a`  
		Last Modified: Tue, 07 Jan 2025 06:50:36 GMT  
		Size: 280.0 KB (279984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868f7227e5c7c8b4bac84441ac5dd24dd837136b8721a4f792daa15e57a2e9ea`  
		Last Modified: Tue, 07 Jan 2025 06:51:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8716a3e393f5147708dc6ab75310ace0722971636dcd1e92fc18a1a08d4310`  
		Last Modified: Tue, 07 Jan 2025 19:16:28 GMT  
		Size: 5.9 MB (5882962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b791cc5e080049e1ae7394580757166567bd0900cebac904cbbe64920e61b8ce`  
		Last Modified: Tue, 07 Jan 2025 19:16:28 GMT  
		Size: 1.7 MB (1730291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c93fc685d7f2433fa6daa535ca47228c9b866aea7f896fbd6a4af465210e19`  
		Last Modified: Tue, 07 Jan 2025 19:16:27 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:5ad045ccd0150d4e833f0663f82a40c69dbb28885bff74445a19290cd060c19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b03d5bf2a398ad9a9638bb96afe77e56f97aec261f3b53aab2351fe2995fc`

```dockerfile
```

-	Layers:
	-	`sha256:0a2381e192ef9ee724bf077a91e8e453aa0ea4f94bca3403ec500eb41cda2234`  
		Last Modified: Tue, 07 Jan 2025 19:16:27 GMT  
		Size: 18.8 KB (18792 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:a43b680920ae7ce72f20c75410ed1915cd5337f427f081c4f9aafd782eccc247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82660655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3feebdc1caa9b4f9be9ab4b8c66fb328f6f7749ff4c0432805b32939ef94c06`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb23a6598e9680ccc41dbb603b77f496c80c87db84ee993d3585d4db8daebd2e`  
		Last Modified: Tue, 07 Jan 2025 06:39:22 GMT  
		Size: 279.2 KB (279170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb64175fa34d7385f5a0720c5acb4845fb41cfffcdb03493609e11dc37a6fd3`  
		Last Modified: Tue, 07 Jan 2025 06:40:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfe46e461df3fdecb8a562830ba9b12245936fb2791b9cedbd7a8ca36b20058`  
		Last Modified: Tue, 07 Jan 2025 19:38:26 GMT  
		Size: 5.4 MB (5366898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac0e00af9653bd3b25707483c4a95af230aaeea0a62545f418a0617f136fa80`  
		Last Modified: Tue, 07 Jan 2025 19:38:26 GMT  
		Size: 1.7 MB (1724267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1d7c1b83cfb35c4fac7d1d3a5684133edf1b75046ce0c4697a3ba5460e44ed`  
		Last Modified: Tue, 07 Jan 2025 19:38:25 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:7c774b05333c78f6c7901c3a00226289799ab4ad5a6d821bb333d761e5b9045d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.3 KB (308313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fd39b958d6e8c399a32dbaeab787d0a8733f087faa9c07f32e5e65b2615b08`

```dockerfile
```

-	Layers:
	-	`sha256:0350cf0d76397eaf7c63deb656fe10134f07ffaf92aee7d4315b210474bcd8e9`  
		Last Modified: Tue, 07 Jan 2025 19:38:25 GMT  
		Size: 289.3 KB (289306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4ff90f1724255f049592f7adf6e634b4cc180ec375532b3453c045d6b98b798`  
		Last Modified: Tue, 07 Jan 2025 19:38:25 GMT  
		Size: 19.0 KB (19007 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:474e710cd83284b6db2ad59f067baa0e9790caaf47b89525f221e74ade964642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82800613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8af4f266f7b4f0b896f9670b8829fea8b9172101f3f30bede770d4899ce7f07`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4f93e44bdb513724a186600fdec99e49dc6de485ed4757e27b16ec93cbf7b4`  
		Last Modified: Tue, 07 Jan 2025 07:41:57 GMT  
		Size: 281.4 KB (281389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7497157ade0eb8e27bb99f1d2cbe466a3b159a321b071ec86638aa51639752f7`  
		Last Modified: Tue, 07 Jan 2025 07:42:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e208341eb37c26d31056e7b9148bfdf952c929003ac80f238023004a70d9fa`  
		Last Modified: Tue, 07 Jan 2025 17:23:51 GMT  
		Size: 6.1 MB (6057100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6dc413d4affbe37787424ac7d057da6e6afeb908288f6ce62ac22d05808ef0`  
		Last Modified: Tue, 07 Jan 2025 17:23:50 GMT  
		Size: 1.7 MB (1701429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec712f8533244d901d3393884856e673bb162a3c03deb8f4d31befd8fa7fd88`  
		Last Modified: Tue, 07 Jan 2025 17:23:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0c44fadb78fcd06c24a8331f3a8b79ea8e73621c8adee909a3d17986ba5f8099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 KB (305538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e81047a49deb2ea96f23a111ecbf19465632b128694e422731373ebcef85f7f`

```dockerfile
```

-	Layers:
	-	`sha256:ee1c13b13592116d1311711b0e3d3b018efc3977c577cfd36415cc11b366cefb`  
		Last Modified: Tue, 07 Jan 2025 17:23:50 GMT  
		Size: 286.5 KB (286501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:669dc151c1da53d095f1afd2778cd824c5469271fdff75f39c926f2f541b20f0`  
		Last Modified: Tue, 07 Jan 2025 17:23:50 GMT  
		Size: 19.0 KB (19037 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ae070d55ed734bb9f26b8bd370a2505a74b68f8258358df545af4f86f19decf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82669759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d45931cb6f86cb49eb2a88c2fb65ea04da6b51a5931231776eaa748c76c32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10173039484873ca3979a3698ef22d1edfdf1fb0aeabab8ad8b5abf80e36c0b`  
		Last Modified: Wed, 08 Jan 2025 21:52:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e90046d3ba1afd50a6d4a5c6c40609982d2342f650d63e92845f9680191fc04`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 6.3 MB (6261729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6020e3492fb8731819fb401ebf9bea060d1dba0da112cc369801cc6f75181`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 1.7 MB (1695595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31426252091c11d90ffd2cb5692a5923c31dae3911af16cc2973b5164e1ef2`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e0dbaba01b809b9974e5b39e1949a4eba4c650e9c8add5d4940186740ae9c274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6003454eef73ebaabead0aaf06b619bc1eccee16eaf04558aacc5148fc2e00f7`

```dockerfile
```

-	Layers:
	-	`sha256:5ef66216d744cfcfafeb2f64c715c6d373ca1dee38c77308d694033c36689144`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a85f55b9730ad2b1de1532bd27f9a27055fa947fee10a1e04c3641ae2965051`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:6afa7e0d3a3a59e9aa6b882701099bb44f36f58e99e8b43a8ea2f18ea1f2efb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82770126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc71d7aee6212a3e843f53252ff6932022464a9aa8b435298b8ae8047a54f109`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9da01c4ee7a2864330da14801bdf35f981730b5e2ffea0588c9ac48734e26b`  
		Last Modified: Wed, 13 Nov 2024 01:22:36 GMT  
		Size: 291.7 KB (291671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Last Modified: Tue, 03 Dec 2024 22:32:57 GMT  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ab90a88816114ae116bd757c876eb44413901c2699659dffc92325a8501bb`  
		Last Modified: Tue, 03 Dec 2024 22:32:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb90820f994a13ba411ce9f13382e83c031ed0b2d2219db34d7e121af2ca4e4`  
		Last Modified: Tue, 03 Dec 2024 23:30:22 GMT  
		Size: 6.2 MB (6153816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fefb8feb2de35a5a9f20a0a493bcd74d7b0922eea5b2ccbd6439c5247f800fb`  
		Last Modified: Tue, 03 Dec 2024 23:30:22 GMT  
		Size: 1.7 MB (1711645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b660586a9723f7ff2e532fbfca97d106664e20e2b69f3774fa623074229c26`  
		Last Modified: Tue, 03 Dec 2024 23:30:21 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:06dc52055ac5b600dedff75602a67e06fa9c731601d5482188ce6d1652bf14a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 KB (308181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5aa093c47d4ed1cebd96cde24099a78cb7a52d417440f9025f8c21c96c5860`

```dockerfile
```

-	Layers:
	-	`sha256:9e4d4e124bb432701401ba103ada3c94d54e668da406553a63886f0fb6fe6408`  
		Last Modified: Tue, 03 Dec 2024 23:30:21 GMT  
		Size: 289.2 KB (289218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c41b3804a8ea2f8ff3a53d9621af2e336a055789acc0de82092ed8a058f074`  
		Last Modified: Tue, 03 Dec 2024 23:30:21 GMT  
		Size: 19.0 KB (18963 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder` - linux; s390x

```console
$ docker pull caddy@sha256:b92d612a4f737a37ff72d49a9efc34962ca64cfc5efc9c811eeb732075bcc3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84682122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442f99a42eb84e1bc22c8a5e0a86fccc3a40598b04888451d70c2880385bfcc4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141e3fcf5173977fad664af74a255a69a2749551008af76945b144725f228f5f`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 280.2 KB (280152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9039b3f81c901f7abad17b0429809aa980ff70f25d072c8d64ee71f7db3e045`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8aa38916b9a65afe6d745bc7b4405235419055139a947defb9ce792bb28b73`  
		Last Modified: Tue, 07 Jan 2025 16:55:39 GMT  
		Size: 6.2 MB (6200978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec7fab0d7b3e909f9d604c7d5db4d6c5d148a5621f917ae64d47527ac04dd6c`  
		Last Modified: Tue, 07 Jan 2025 16:55:38 GMT  
		Size: 1.8 MB (1771408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7c25ff35fc2bf5b4e68e2b04fceec185b05f8e45c0c41b9692e8e59cd1c262`  
		Last Modified: Tue, 07 Jan 2025 16:55:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:070946d4d8fef9dca3ce28916561a1f7ddefdbb80cede999c36e8f11e6ed7421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 KB (303412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86eaf1bb01e5d3120194465338ce9ec4b323ee8b6dff4cd3ebf865ccc2d8db24`

```dockerfile
```

-	Layers:
	-	`sha256:34663bb74e1afda9d0c0a26834b5e61abda8e0ae78019db79650699ea054aec5`  
		Last Modified: Tue, 07 Jan 2025 16:55:38 GMT  
		Size: 284.5 KB (284494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eced6039cdcb97b7decd611ac9ad736effc3f5018cfe2d10b5c484bf2b455642`  
		Last Modified: Tue, 07 Jan 2025 16:55:38 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:0189cfa4a4c02a3bb800a7e32a588f1264aa3f8eafa4b94e6ed4129cbe3ff2a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2359343914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d72f15e0f30165074557b2b759d5db3e5947c39aee860af1bdf1e3877f65413`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:29 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:41:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:41:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:41:51 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:41:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:41:57 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:43:05 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:43:07 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:48 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:48 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:34:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:34:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2203f205368ce649ffd4367d83cb7d0e0f349edd4a73d17bf72e1d1fd45547`  
		Last Modified: Wed, 11 Dec 2024 20:43:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a929050203563fde4afe1d48374621524ea8726dc8ca55d3c22d0ac7a798594`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1be8f168e721557e602e0b7a3a7cb7e068d12e159af7b67cbd570277d67b6d3`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a047a2e43f164719e30219f432eae6c44e556b5a49ad8de5c356eef5ceb9f2`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538affaf25305d64f324539f173d0eb2d2dd465cb1762b082450ad4c797f27c`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c69a8ef4d7541c4f17aa73bdd2bc059fbf9e06bb80dba0c6780214385b946`  
		Last Modified: Wed, 11 Dec 2024 20:43:13 GMT  
		Size: 25.4 MB (25433638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8adf8499c2eb9b67d228fba4c9e69a29a2d7060f8b7c5592eacc3be4421710`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb262fe2ef81142570e16f48f8f03d4031993f7f4bdd1e8ddc6130f5ac401023`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 339.0 KB (338961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b81c31620602735496201938ab0373d338f5d0422cdb2fe31bf91e703561180`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a3cd836a09077c7888a8a16d4e7bdf054357c81b2dfc19d8a0d373c88f51d`  
		Last Modified: Wed, 11 Dec 2024 20:43:22 GMT  
		Size: 77.3 MB (77349783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6072f4215eedb6bd6a3744f556ae0cd5807bf437d9168f5f06a714a4935e11ad`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddd9caf64ad2db2b643ff3a12c821a4568fb6cab42c886d58ec94c55611183`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9ad2ce3c975bdb8bb5a956ddacab8f088540115a28bdc8d3c28beab4329aec`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b21bef77b61f0857b5cfc4fdb89f2c1c74d5346d5c5813e145c298a5b86642`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b2d84d7d2cf78270c6457f8ab87188b8d84fcbe934749c67f5a31364f3a84`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f1f09b1a52df9107d2afb46ee59d7d749f2b38fb8bf1a07b9e0ba04de6e6e`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 2.3 MB (2331000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450a1c75f8730f0ad6bb33eaa49034a16cc2b79db5b5098a4afd873dcc3ed769`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.9-builder` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:ea06d27be71f8ef91c6d6f553d93e6261efe59e77edf8ca72c562150017510d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2119855201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688816f8244428a55ae1ec4bd192c597ce0f04d19edda948e46a80ecfd9bf8ce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:39:37 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:39:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:40:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:40:47 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:40:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:40:54 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:42:12 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:42:13 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:32 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:32 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:35:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:35:04 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f3bbeb4e2782220c87261e5e9d61855baf0ace86081d92be83026dd5e8fcc2`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241e544e87d299e404e0055ac6a3d562110f5dbac92ab40f5274757c352361`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d65d85ef63918a2fe84d0a5c56c3c6b83838ea5060fc445cb586acaa3fc316`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d89f6bf6b5749f5d1a48d1e66e0f5882aa8e07e2d3218b9a7e1f59c2dda0c`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54a47581ed1b6b7629a8abc75e2e6e45c36975a21ec95b65e8106e75c34aafa`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81645ff46b23f2588b64411ee4dd209ad3383c3b4376b70fa25b258296a5d05`  
		Last Modified: Wed, 11 Dec 2024 20:42:19 GMT  
		Size: 25.6 MB (25561663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619f9252e7182af97b30c9a01c651c8a8f83c521db1c842279b8adaf45bc17ac`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e01c2f476af7e5c6236de3ec31577c6d3d4491c44d2e5cce185341f9d8a19`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 328.3 KB (328344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd74620f512254e194320e032040d3c01472e9f9c304c960171132f8a838cb7`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05934960da5aa39d60d727548d37d080612ea4164a25e09b3c3d9e310f6fa14f`  
		Last Modified: Wed, 11 Dec 2024 20:42:28 GMT  
		Size: 77.5 MB (77463395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d829f35d8061698251f21a9c2ad8cb0d344ddb5465b577017415f89f82d50aa`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0302b0fa76f2e0e3678e4ec6e3a77b56966df7cbd7788ff083f096d58f66eb9`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b2e9a08ab9b486a49339207a0e3c35851ead887e82207dabf747c69de0ef9`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb03d015e74d14f0a3566de1e456b2c92453ba713a378af8d0608061e2f9d06`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7da9a44214dc454bfc9248a3e2db15fda48ce69c4c8f426122a25540d604d20`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0fc2d732d66c3b5aeb005f494441963afb2427e6b8eb07d9f0e0855a328c31`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 2.3 MB (2314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c45570296cf141f1579eb94ca900ddea076099f18b3f5e5dedf41c600a449`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9-builder-alpine`

```console
$ docker pull caddy@sha256:122e6fbfb29765833e69b91d7b7bdf7df78a202a266c3c3610e09b278a31ad4f
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

### `caddy:2.9-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:db250d8ac333dbfb36d2082ae73b39f21d1316e42d441199f8fdef60aa578773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4fed372693e3e094c6ca0f1a55f4d71f8e0ce8f751c7a4158a8ad487996162`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe7652777a557be7320acd6bafa585a401104296826b9790d94fa35f28480d`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 294.4 KB (294368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda4308841a6cc675c32eadc7ca82f1f5916886229ff6efcbc6e0f9015d73c80`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f167cb8105c9df8315499305c0ce83016c842a6c68f1e4424182dce22a3fe6d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 5.9 MB (5939538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf2b30687fe7e3fa4f927c76a4e43b2db14a66b0e42a32ea9ddcdfa17e0c7d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed24074f0fd5dc780dad0af8b4260d4205b3b89d7a666396c5b415abc85f2a8`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:75e70c9bd28699ef12d45bf9f03e28ff90a8d151d65e788697b9a7d7af5fe398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fc11bbdfee02d4bdc1dbac347ca232538947335e5e4d6788952c5a38c2494`

```dockerfile
```

-	Layers:
	-	`sha256:a19c370ffc738c2bca6c09b72807b6a1244b6294e4ba0df6aa29eaa2aac91efc`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff92b5cdde37260cee10c8515c7ddc7fe46ee4c87c0b3cbfb1b3cf2f34be315`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:09330ddca8ff56a6486098ba6c3277ae0efdeb584e30208cb42d917f6475e7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83456311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751c85b57ea579ea3860bf3dc947281387591caca52f0e32766a2c5613ebfefd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ab5d3af8a0c99d02e713511deb39821a107d6d0ba6be4b2f6b0843085aea2a`  
		Last Modified: Tue, 07 Jan 2025 06:50:36 GMT  
		Size: 280.0 KB (279984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868f7227e5c7c8b4bac84441ac5dd24dd837136b8721a4f792daa15e57a2e9ea`  
		Last Modified: Tue, 07 Jan 2025 06:51:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8716a3e393f5147708dc6ab75310ace0722971636dcd1e92fc18a1a08d4310`  
		Last Modified: Tue, 07 Jan 2025 19:16:28 GMT  
		Size: 5.9 MB (5882962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b791cc5e080049e1ae7394580757166567bd0900cebac904cbbe64920e61b8ce`  
		Last Modified: Tue, 07 Jan 2025 19:16:28 GMT  
		Size: 1.7 MB (1730291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c93fc685d7f2433fa6daa535ca47228c9b866aea7f896fbd6a4af465210e19`  
		Last Modified: Tue, 07 Jan 2025 19:16:27 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:5ad045ccd0150d4e833f0663f82a40c69dbb28885bff74445a19290cd060c19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b03d5bf2a398ad9a9638bb96afe77e56f97aec261f3b53aab2351fe2995fc`

```dockerfile
```

-	Layers:
	-	`sha256:0a2381e192ef9ee724bf077a91e8e453aa0ea4f94bca3403ec500eb41cda2234`  
		Last Modified: Tue, 07 Jan 2025 19:16:27 GMT  
		Size: 18.8 KB (18792 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:a43b680920ae7ce72f20c75410ed1915cd5337f427f081c4f9aafd782eccc247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82660655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3feebdc1caa9b4f9be9ab4b8c66fb328f6f7749ff4c0432805b32939ef94c06`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb23a6598e9680ccc41dbb603b77f496c80c87db84ee993d3585d4db8daebd2e`  
		Last Modified: Tue, 07 Jan 2025 06:39:22 GMT  
		Size: 279.2 KB (279170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb64175fa34d7385f5a0720c5acb4845fb41cfffcdb03493609e11dc37a6fd3`  
		Last Modified: Tue, 07 Jan 2025 06:40:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfe46e461df3fdecb8a562830ba9b12245936fb2791b9cedbd7a8ca36b20058`  
		Last Modified: Tue, 07 Jan 2025 19:38:26 GMT  
		Size: 5.4 MB (5366898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac0e00af9653bd3b25707483c4a95af230aaeea0a62545f418a0617f136fa80`  
		Last Modified: Tue, 07 Jan 2025 19:38:26 GMT  
		Size: 1.7 MB (1724267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1d7c1b83cfb35c4fac7d1d3a5684133edf1b75046ce0c4697a3ba5460e44ed`  
		Last Modified: Tue, 07 Jan 2025 19:38:25 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7c774b05333c78f6c7901c3a00226289799ab4ad5a6d821bb333d761e5b9045d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.3 KB (308313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fd39b958d6e8c399a32dbaeab787d0a8733f087faa9c07f32e5e65b2615b08`

```dockerfile
```

-	Layers:
	-	`sha256:0350cf0d76397eaf7c63deb656fe10134f07ffaf92aee7d4315b210474bcd8e9`  
		Last Modified: Tue, 07 Jan 2025 19:38:25 GMT  
		Size: 289.3 KB (289306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4ff90f1724255f049592f7adf6e634b4cc180ec375532b3453c045d6b98b798`  
		Last Modified: Tue, 07 Jan 2025 19:38:25 GMT  
		Size: 19.0 KB (19007 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:474e710cd83284b6db2ad59f067baa0e9790caaf47b89525f221e74ade964642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82800613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8af4f266f7b4f0b896f9670b8829fea8b9172101f3f30bede770d4899ce7f07`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4f93e44bdb513724a186600fdec99e49dc6de485ed4757e27b16ec93cbf7b4`  
		Last Modified: Tue, 07 Jan 2025 07:41:57 GMT  
		Size: 281.4 KB (281389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7497157ade0eb8e27bb99f1d2cbe466a3b159a321b071ec86638aa51639752f7`  
		Last Modified: Tue, 07 Jan 2025 07:42:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e208341eb37c26d31056e7b9148bfdf952c929003ac80f238023004a70d9fa`  
		Last Modified: Tue, 07 Jan 2025 17:23:51 GMT  
		Size: 6.1 MB (6057100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6dc413d4affbe37787424ac7d057da6e6afeb908288f6ce62ac22d05808ef0`  
		Last Modified: Tue, 07 Jan 2025 17:23:50 GMT  
		Size: 1.7 MB (1701429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec712f8533244d901d3393884856e673bb162a3c03deb8f4d31befd8fa7fd88`  
		Last Modified: Tue, 07 Jan 2025 17:23:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0c44fadb78fcd06c24a8331f3a8b79ea8e73621c8adee909a3d17986ba5f8099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 KB (305538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e81047a49deb2ea96f23a111ecbf19465632b128694e422731373ebcef85f7f`

```dockerfile
```

-	Layers:
	-	`sha256:ee1c13b13592116d1311711b0e3d3b018efc3977c577cfd36415cc11b366cefb`  
		Last Modified: Tue, 07 Jan 2025 17:23:50 GMT  
		Size: 286.5 KB (286501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:669dc151c1da53d095f1afd2778cd824c5469271fdff75f39c926f2f541b20f0`  
		Last Modified: Tue, 07 Jan 2025 17:23:50 GMT  
		Size: 19.0 KB (19037 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ae070d55ed734bb9f26b8bd370a2505a74b68f8258358df545af4f86f19decf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82669759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d45931cb6f86cb49eb2a88c2fb65ea04da6b51a5931231776eaa748c76c32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10173039484873ca3979a3698ef22d1edfdf1fb0aeabab8ad8b5abf80e36c0b`  
		Last Modified: Wed, 08 Jan 2025 21:52:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e90046d3ba1afd50a6d4a5c6c40609982d2342f650d63e92845f9680191fc04`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 6.3 MB (6261729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6020e3492fb8731819fb401ebf9bea060d1dba0da112cc369801cc6f75181`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 1.7 MB (1695595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31426252091c11d90ffd2cb5692a5923c31dae3911af16cc2973b5164e1ef2`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e0dbaba01b809b9974e5b39e1949a4eba4c650e9c8add5d4940186740ae9c274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6003454eef73ebaabead0aaf06b619bc1eccee16eaf04558aacc5148fc2e00f7`

```dockerfile
```

-	Layers:
	-	`sha256:5ef66216d744cfcfafeb2f64c715c6d373ca1dee38c77308d694033c36689144`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a85f55b9730ad2b1de1532bd27f9a27055fa947fee10a1e04c3641ae2965051`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:6afa7e0d3a3a59e9aa6b882701099bb44f36f58e99e8b43a8ea2f18ea1f2efb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82770126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc71d7aee6212a3e843f53252ff6932022464a9aa8b435298b8ae8047a54f109`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9da01c4ee7a2864330da14801bdf35f981730b5e2ffea0588c9ac48734e26b`  
		Last Modified: Wed, 13 Nov 2024 01:22:36 GMT  
		Size: 291.7 KB (291671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Last Modified: Tue, 03 Dec 2024 22:32:57 GMT  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ab90a88816114ae116bd757c876eb44413901c2699659dffc92325a8501bb`  
		Last Modified: Tue, 03 Dec 2024 22:32:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb90820f994a13ba411ce9f13382e83c031ed0b2d2219db34d7e121af2ca4e4`  
		Last Modified: Tue, 03 Dec 2024 23:30:22 GMT  
		Size: 6.2 MB (6153816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fefb8feb2de35a5a9f20a0a493bcd74d7b0922eea5b2ccbd6439c5247f800fb`  
		Last Modified: Tue, 03 Dec 2024 23:30:22 GMT  
		Size: 1.7 MB (1711645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b660586a9723f7ff2e532fbfca97d106664e20e2b69f3774fa623074229c26`  
		Last Modified: Tue, 03 Dec 2024 23:30:21 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:06dc52055ac5b600dedff75602a67e06fa9c731601d5482188ce6d1652bf14a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 KB (308181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5aa093c47d4ed1cebd96cde24099a78cb7a52d417440f9025f8c21c96c5860`

```dockerfile
```

-	Layers:
	-	`sha256:9e4d4e124bb432701401ba103ada3c94d54e668da406553a63886f0fb6fe6408`  
		Last Modified: Tue, 03 Dec 2024 23:30:21 GMT  
		Size: 289.2 KB (289218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c41b3804a8ea2f8ff3a53d9621af2e336a055789acc0de82092ed8a058f074`  
		Last Modified: Tue, 03 Dec 2024 23:30:21 GMT  
		Size: 19.0 KB (18963 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:b92d612a4f737a37ff72d49a9efc34962ca64cfc5efc9c811eeb732075bcc3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84682122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442f99a42eb84e1bc22c8a5e0a86fccc3a40598b04888451d70c2880385bfcc4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.9.0-beta.3
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141e3fcf5173977fad664af74a255a69a2749551008af76945b144725f228f5f`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 280.2 KB (280152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9039b3f81c901f7abad17b0429809aa980ff70f25d072c8d64ee71f7db3e045`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8aa38916b9a65afe6d745bc7b4405235419055139a947defb9ce792bb28b73`  
		Last Modified: Tue, 07 Jan 2025 16:55:39 GMT  
		Size: 6.2 MB (6200978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec7fab0d7b3e909f9d604c7d5db4d6c5d148a5621f917ae64d47527ac04dd6c`  
		Last Modified: Tue, 07 Jan 2025 16:55:38 GMT  
		Size: 1.8 MB (1771408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7c25ff35fc2bf5b4e68e2b04fceec185b05f8e45c0c41b9692e8e59cd1c262`  
		Last Modified: Tue, 07 Jan 2025 16:55:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:070946d4d8fef9dca3ce28916561a1f7ddefdbb80cede999c36e8f11e6ed7421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 KB (303412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86eaf1bb01e5d3120194465338ce9ec4b323ee8b6dff4cd3ebf865ccc2d8db24`

```dockerfile
```

-	Layers:
	-	`sha256:34663bb74e1afda9d0c0a26834b5e61abda8e0ae78019db79650699ea054aec5`  
		Last Modified: Tue, 07 Jan 2025 16:55:38 GMT  
		Size: 284.5 KB (284494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eced6039cdcb97b7decd611ac9ad736effc3f5018cfe2d10b5c484bf2b455642`  
		Last Modified: Tue, 07 Jan 2025 16:55:38 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.9-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ba8e01cd3489a6d329519bd950beb8f983734752aeb472b4ef6eb1ee8711a7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `caddy:2.9-builder-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:ea06d27be71f8ef91c6d6f553d93e6261efe59e77edf8ca72c562150017510d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2119855201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688816f8244428a55ae1ec4bd192c597ce0f04d19edda948e46a80ecfd9bf8ce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:39:37 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:39:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:40:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:40:47 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:40:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:40:54 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:42:12 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:42:13 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:32 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:32 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:35:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:35:04 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f3bbeb4e2782220c87261e5e9d61855baf0ace86081d92be83026dd5e8fcc2`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241e544e87d299e404e0055ac6a3d562110f5dbac92ab40f5274757c352361`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d65d85ef63918a2fe84d0a5c56c3c6b83838ea5060fc445cb586acaa3fc316`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d89f6bf6b5749f5d1a48d1e66e0f5882aa8e07e2d3218b9a7e1f59c2dda0c`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54a47581ed1b6b7629a8abc75e2e6e45c36975a21ec95b65e8106e75c34aafa`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81645ff46b23f2588b64411ee4dd209ad3383c3b4376b70fa25b258296a5d05`  
		Last Modified: Wed, 11 Dec 2024 20:42:19 GMT  
		Size: 25.6 MB (25561663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619f9252e7182af97b30c9a01c651c8a8f83c521db1c842279b8adaf45bc17ac`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e01c2f476af7e5c6236de3ec31577c6d3d4491c44d2e5cce185341f9d8a19`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 328.3 KB (328344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd74620f512254e194320e032040d3c01472e9f9c304c960171132f8a838cb7`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05934960da5aa39d60d727548d37d080612ea4164a25e09b3c3d9e310f6fa14f`  
		Last Modified: Wed, 11 Dec 2024 20:42:28 GMT  
		Size: 77.5 MB (77463395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d829f35d8061698251f21a9c2ad8cb0d344ddb5465b577017415f89f82d50aa`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0302b0fa76f2e0e3678e4ec6e3a77b56966df7cbd7788ff083f096d58f66eb9`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b2e9a08ab9b486a49339207a0e3c35851ead887e82207dabf747c69de0ef9`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb03d015e74d14f0a3566de1e456b2c92453ba713a378af8d0608061e2f9d06`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7da9a44214dc454bfc9248a3e2db15fda48ce69c4c8f426122a25540d604d20`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0fc2d732d66c3b5aeb005f494441963afb2427e6b8eb07d9f0e0855a328c31`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 2.3 MB (2314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c45570296cf141f1579eb94ca900ddea076099f18b3f5e5dedf41c600a449`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:af2dcf0d4a7eae883882f2a63357f55bc484ef53386cb5ceb912e92631130a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `caddy:2.9-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:0189cfa4a4c02a3bb800a7e32a588f1264aa3f8eafa4b94e6ed4129cbe3ff2a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2359343914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d72f15e0f30165074557b2b759d5db3e5947c39aee860af1bdf1e3877f65413`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:29 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:41:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:41:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:41:51 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:41:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:41:57 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:43:05 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:43:07 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:48 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:48 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:34:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:34:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2203f205368ce649ffd4367d83cb7d0e0f349edd4a73d17bf72e1d1fd45547`  
		Last Modified: Wed, 11 Dec 2024 20:43:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a929050203563fde4afe1d48374621524ea8726dc8ca55d3c22d0ac7a798594`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1be8f168e721557e602e0b7a3a7cb7e068d12e159af7b67cbd570277d67b6d3`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a047a2e43f164719e30219f432eae6c44e556b5a49ad8de5c356eef5ceb9f2`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538affaf25305d64f324539f173d0eb2d2dd465cb1762b082450ad4c797f27c`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c69a8ef4d7541c4f17aa73bdd2bc059fbf9e06bb80dba0c6780214385b946`  
		Last Modified: Wed, 11 Dec 2024 20:43:13 GMT  
		Size: 25.4 MB (25433638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8adf8499c2eb9b67d228fba4c9e69a29a2d7060f8b7c5592eacc3be4421710`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb262fe2ef81142570e16f48f8f03d4031993f7f4bdd1e8ddc6130f5ac401023`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 339.0 KB (338961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b81c31620602735496201938ab0373d338f5d0422cdb2fe31bf91e703561180`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a3cd836a09077c7888a8a16d4e7bdf054357c81b2dfc19d8a0d373c88f51d`  
		Last Modified: Wed, 11 Dec 2024 20:43:22 GMT  
		Size: 77.3 MB (77349783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6072f4215eedb6bd6a3744f556ae0cd5807bf437d9168f5f06a714a4935e11ad`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddd9caf64ad2db2b643ff3a12c821a4568fb6cab42c886d58ec94c55611183`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9ad2ce3c975bdb8bb5a956ddacab8f088540115a28bdc8d3c28beab4329aec`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b21bef77b61f0857b5cfc4fdb89f2c1c74d5346d5c5813e145c298a5b86642`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b2d84d7d2cf78270c6457f8ab87188b8d84fcbe934749c67f5a31364f3a84`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f1f09b1a52df9107d2afb46ee59d7d749f2b38fb8bf1a07b9e0ba04de6e6e`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 2.3 MB (2331000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450a1c75f8730f0ad6bb33eaa49034a16cc2b79db5b5098a4afd873dcc3ed769`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9-windowsservercore`

```console
$ docker pull caddy@sha256:8e842a56471df259c7282c7827f1a7c4b8f24de694d1892428bd6c421d29052a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:2.9-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.9-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9-windowsservercore-1809`

```console
$ docker pull caddy@sha256:1307996d1255d8cba23d2b956a5f47525051154fc907edffeafbdc9ce01b6460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `caddy:2.9-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:4d4fc4b1242a7788c646c9d733cf131cea76ed6ee655570a41d2ea783cb56e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `caddy:2.9-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9.1`

```console
$ docker pull caddy@sha256:948b33a1ec78d0eb22c39dd6543de3647c215f823277fe9529f73a847d920102
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:2.9.1` - linux; amd64

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

### `caddy:2.9.1` - unknown; unknown

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

### `caddy:2.9.1` - linux; ppc64le

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

### `caddy:2.9.1` - unknown; unknown

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

### `caddy:2.9.1` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.9.1` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9.1-alpine`

```console
$ docker pull caddy@sha256:e70ccf0c9821a88303671ef22d7b5e2d2b6057a8b18703022d755ba4d5fd35cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `caddy:2.9.1-alpine` - linux; amd64

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

### `caddy:2.9.1-alpine` - unknown; unknown

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

### `caddy:2.9.1-alpine` - linux; ppc64le

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

### `caddy:2.9.1-alpine` - unknown; unknown

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

## `caddy:2.9.1-builder`

```console
$ docker pull caddy@sha256:8d36ec89c6a433669dcca365176c679ea2d45b7e3659d4a4766456508d1e31d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:2.9.1-builder` - linux; amd64

```console
$ docker pull caddy@sha256:db250d8ac333dbfb36d2082ae73b39f21d1316e42d441199f8fdef60aa578773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4fed372693e3e094c6ca0f1a55f4d71f8e0ce8f751c7a4158a8ad487996162`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe7652777a557be7320acd6bafa585a401104296826b9790d94fa35f28480d`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 294.4 KB (294368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda4308841a6cc675c32eadc7ca82f1f5916886229ff6efcbc6e0f9015d73c80`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f167cb8105c9df8315499305c0ce83016c842a6c68f1e4424182dce22a3fe6d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 5.9 MB (5939538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf2b30687fe7e3fa4f927c76a4e43b2db14a66b0e42a32ea9ddcdfa17e0c7d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed24074f0fd5dc780dad0af8b4260d4205b3b89d7a666396c5b415abc85f2a8`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9.1-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:75e70c9bd28699ef12d45bf9f03e28ff90a8d151d65e788697b9a7d7af5fe398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fc11bbdfee02d4bdc1dbac347ca232538947335e5e4d6788952c5a38c2494`

```dockerfile
```

-	Layers:
	-	`sha256:a19c370ffc738c2bca6c09b72807b6a1244b6294e4ba0df6aa29eaa2aac91efc`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff92b5cdde37260cee10c8515c7ddc7fe46ee4c87c0b3cbfb1b3cf2f34be315`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9.1-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ae070d55ed734bb9f26b8bd370a2505a74b68f8258358df545af4f86f19decf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82669759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d45931cb6f86cb49eb2a88c2fb65ea04da6b51a5931231776eaa748c76c32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10173039484873ca3979a3698ef22d1edfdf1fb0aeabab8ad8b5abf80e36c0b`  
		Last Modified: Wed, 08 Jan 2025 21:52:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e90046d3ba1afd50a6d4a5c6c40609982d2342f650d63e92845f9680191fc04`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 6.3 MB (6261729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6020e3492fb8731819fb401ebf9bea060d1dba0da112cc369801cc6f75181`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 1.7 MB (1695595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31426252091c11d90ffd2cb5692a5923c31dae3911af16cc2973b5164e1ef2`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9.1-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e0dbaba01b809b9974e5b39e1949a4eba4c650e9c8add5d4940186740ae9c274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6003454eef73ebaabead0aaf06b619bc1eccee16eaf04558aacc5148fc2e00f7`

```dockerfile
```

-	Layers:
	-	`sha256:5ef66216d744cfcfafeb2f64c715c6d373ca1dee38c77308d694033c36689144`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a85f55b9730ad2b1de1532bd27f9a27055fa947fee10a1e04c3641ae2965051`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9.1-builder` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:0189cfa4a4c02a3bb800a7e32a588f1264aa3f8eafa4b94e6ed4129cbe3ff2a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2359343914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d72f15e0f30165074557b2b759d5db3e5947c39aee860af1bdf1e3877f65413`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:29 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:41:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:41:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:41:51 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:41:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:41:57 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:43:05 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:43:07 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:48 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:48 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:34:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:34:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2203f205368ce649ffd4367d83cb7d0e0f349edd4a73d17bf72e1d1fd45547`  
		Last Modified: Wed, 11 Dec 2024 20:43:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a929050203563fde4afe1d48374621524ea8726dc8ca55d3c22d0ac7a798594`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1be8f168e721557e602e0b7a3a7cb7e068d12e159af7b67cbd570277d67b6d3`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a047a2e43f164719e30219f432eae6c44e556b5a49ad8de5c356eef5ceb9f2`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538affaf25305d64f324539f173d0eb2d2dd465cb1762b082450ad4c797f27c`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c69a8ef4d7541c4f17aa73bdd2bc059fbf9e06bb80dba0c6780214385b946`  
		Last Modified: Wed, 11 Dec 2024 20:43:13 GMT  
		Size: 25.4 MB (25433638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8adf8499c2eb9b67d228fba4c9e69a29a2d7060f8b7c5592eacc3be4421710`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb262fe2ef81142570e16f48f8f03d4031993f7f4bdd1e8ddc6130f5ac401023`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 339.0 KB (338961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b81c31620602735496201938ab0373d338f5d0422cdb2fe31bf91e703561180`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a3cd836a09077c7888a8a16d4e7bdf054357c81b2dfc19d8a0d373c88f51d`  
		Last Modified: Wed, 11 Dec 2024 20:43:22 GMT  
		Size: 77.3 MB (77349783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6072f4215eedb6bd6a3744f556ae0cd5807bf437d9168f5f06a714a4935e11ad`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddd9caf64ad2db2b643ff3a12c821a4568fb6cab42c886d58ec94c55611183`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9ad2ce3c975bdb8bb5a956ddacab8f088540115a28bdc8d3c28beab4329aec`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b21bef77b61f0857b5cfc4fdb89f2c1c74d5346d5c5813e145c298a5b86642`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b2d84d7d2cf78270c6457f8ab87188b8d84fcbe934749c67f5a31364f3a84`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f1f09b1a52df9107d2afb46ee59d7d749f2b38fb8bf1a07b9e0ba04de6e6e`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 2.3 MB (2331000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450a1c75f8730f0ad6bb33eaa49034a16cc2b79db5b5098a4afd873dcc3ed769`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.9.1-builder` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:ea06d27be71f8ef91c6d6f553d93e6261efe59e77edf8ca72c562150017510d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2119855201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688816f8244428a55ae1ec4bd192c597ce0f04d19edda948e46a80ecfd9bf8ce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:39:37 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:39:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:40:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:40:47 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:40:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:40:54 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:42:12 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:42:13 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:32 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:32 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:35:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:35:04 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f3bbeb4e2782220c87261e5e9d61855baf0ace86081d92be83026dd5e8fcc2`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241e544e87d299e404e0055ac6a3d562110f5dbac92ab40f5274757c352361`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d65d85ef63918a2fe84d0a5c56c3c6b83838ea5060fc445cb586acaa3fc316`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d89f6bf6b5749f5d1a48d1e66e0f5882aa8e07e2d3218b9a7e1f59c2dda0c`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54a47581ed1b6b7629a8abc75e2e6e45c36975a21ec95b65e8106e75c34aafa`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81645ff46b23f2588b64411ee4dd209ad3383c3b4376b70fa25b258296a5d05`  
		Last Modified: Wed, 11 Dec 2024 20:42:19 GMT  
		Size: 25.6 MB (25561663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619f9252e7182af97b30c9a01c651c8a8f83c521db1c842279b8adaf45bc17ac`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e01c2f476af7e5c6236de3ec31577c6d3d4491c44d2e5cce185341f9d8a19`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 328.3 KB (328344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd74620f512254e194320e032040d3c01472e9f9c304c960171132f8a838cb7`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05934960da5aa39d60d727548d37d080612ea4164a25e09b3c3d9e310f6fa14f`  
		Last Modified: Wed, 11 Dec 2024 20:42:28 GMT  
		Size: 77.5 MB (77463395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d829f35d8061698251f21a9c2ad8cb0d344ddb5465b577017415f89f82d50aa`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0302b0fa76f2e0e3678e4ec6e3a77b56966df7cbd7788ff083f096d58f66eb9`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b2e9a08ab9b486a49339207a0e3c35851ead887e82207dabf747c69de0ef9`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb03d015e74d14f0a3566de1e456b2c92453ba713a378af8d0608061e2f9d06`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7da9a44214dc454bfc9248a3e2db15fda48ce69c4c8f426122a25540d604d20`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0fc2d732d66c3b5aeb005f494441963afb2427e6b8eb07d9f0e0855a328c31`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 2.3 MB (2314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c45570296cf141f1579eb94ca900ddea076099f18b3f5e5dedf41c600a449`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9.1-builder-alpine`

```console
$ docker pull caddy@sha256:bfa436d2711d1294501ba0f72f149d8c5dad237fc8e9c9b9aec682df8438ec73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `caddy:2.9.1-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:db250d8ac333dbfb36d2082ae73b39f21d1316e42d441199f8fdef60aa578773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4fed372693e3e094c6ca0f1a55f4d71f8e0ce8f751c7a4158a8ad487996162`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe7652777a557be7320acd6bafa585a401104296826b9790d94fa35f28480d`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 294.4 KB (294368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda4308841a6cc675c32eadc7ca82f1f5916886229ff6efcbc6e0f9015d73c80`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f167cb8105c9df8315499305c0ce83016c842a6c68f1e4424182dce22a3fe6d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 5.9 MB (5939538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf2b30687fe7e3fa4f927c76a4e43b2db14a66b0e42a32ea9ddcdfa17e0c7d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed24074f0fd5dc780dad0af8b4260d4205b3b89d7a666396c5b415abc85f2a8`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9.1-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:75e70c9bd28699ef12d45bf9f03e28ff90a8d151d65e788697b9a7d7af5fe398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fc11bbdfee02d4bdc1dbac347ca232538947335e5e4d6788952c5a38c2494`

```dockerfile
```

-	Layers:
	-	`sha256:a19c370ffc738c2bca6c09b72807b6a1244b6294e4ba0df6aa29eaa2aac91efc`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff92b5cdde37260cee10c8515c7ddc7fe46ee4c87c0b3cbfb1b3cf2f34be315`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.9.1-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ae070d55ed734bb9f26b8bd370a2505a74b68f8258358df545af4f86f19decf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82669759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d45931cb6f86cb49eb2a88c2fb65ea04da6b51a5931231776eaa748c76c32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10173039484873ca3979a3698ef22d1edfdf1fb0aeabab8ad8b5abf80e36c0b`  
		Last Modified: Wed, 08 Jan 2025 21:52:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e90046d3ba1afd50a6d4a5c6c40609982d2342f650d63e92845f9680191fc04`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 6.3 MB (6261729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6020e3492fb8731819fb401ebf9bea060d1dba0da112cc369801cc6f75181`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 1.7 MB (1695595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31426252091c11d90ffd2cb5692a5923c31dae3911af16cc2973b5164e1ef2`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.9.1-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e0dbaba01b809b9974e5b39e1949a4eba4c650e9c8add5d4940186740ae9c274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6003454eef73ebaabead0aaf06b619bc1eccee16eaf04558aacc5148fc2e00f7`

```dockerfile
```

-	Layers:
	-	`sha256:5ef66216d744cfcfafeb2f64c715c6d373ca1dee38c77308d694033c36689144`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a85f55b9730ad2b1de1532bd27f9a27055fa947fee10a1e04c3641ae2965051`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.9.1-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ba8e01cd3489a6d329519bd950beb8f983734752aeb472b4ef6eb1ee8711a7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `caddy:2.9.1-builder-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:ea06d27be71f8ef91c6d6f553d93e6261efe59e77edf8ca72c562150017510d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2119855201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688816f8244428a55ae1ec4bd192c597ce0f04d19edda948e46a80ecfd9bf8ce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:39:37 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:39:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:40:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:40:47 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:40:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:40:54 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:42:12 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:42:13 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:32 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:32 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:35:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:35:04 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f3bbeb4e2782220c87261e5e9d61855baf0ace86081d92be83026dd5e8fcc2`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241e544e87d299e404e0055ac6a3d562110f5dbac92ab40f5274757c352361`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d65d85ef63918a2fe84d0a5c56c3c6b83838ea5060fc445cb586acaa3fc316`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d89f6bf6b5749f5d1a48d1e66e0f5882aa8e07e2d3218b9a7e1f59c2dda0c`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54a47581ed1b6b7629a8abc75e2e6e45c36975a21ec95b65e8106e75c34aafa`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81645ff46b23f2588b64411ee4dd209ad3383c3b4376b70fa25b258296a5d05`  
		Last Modified: Wed, 11 Dec 2024 20:42:19 GMT  
		Size: 25.6 MB (25561663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619f9252e7182af97b30c9a01c651c8a8f83c521db1c842279b8adaf45bc17ac`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e01c2f476af7e5c6236de3ec31577c6d3d4491c44d2e5cce185341f9d8a19`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 328.3 KB (328344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd74620f512254e194320e032040d3c01472e9f9c304c960171132f8a838cb7`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05934960da5aa39d60d727548d37d080612ea4164a25e09b3c3d9e310f6fa14f`  
		Last Modified: Wed, 11 Dec 2024 20:42:28 GMT  
		Size: 77.5 MB (77463395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d829f35d8061698251f21a9c2ad8cb0d344ddb5465b577017415f89f82d50aa`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0302b0fa76f2e0e3678e4ec6e3a77b56966df7cbd7788ff083f096d58f66eb9`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b2e9a08ab9b486a49339207a0e3c35851ead887e82207dabf747c69de0ef9`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb03d015e74d14f0a3566de1e456b2c92453ba713a378af8d0608061e2f9d06`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7da9a44214dc454bfc9248a3e2db15fda48ce69c4c8f426122a25540d604d20`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0fc2d732d66c3b5aeb005f494441963afb2427e6b8eb07d9f0e0855a328c31`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 2.3 MB (2314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c45570296cf141f1579eb94ca900ddea076099f18b3f5e5dedf41c600a449`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9.1-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:af2dcf0d4a7eae883882f2a63357f55bc484ef53386cb5ceb912e92631130a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `caddy:2.9.1-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:0189cfa4a4c02a3bb800a7e32a588f1264aa3f8eafa4b94e6ed4129cbe3ff2a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2359343914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d72f15e0f30165074557b2b759d5db3e5947c39aee860af1bdf1e3877f65413`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:29 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:41:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:41:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:41:51 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:41:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:41:57 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:43:05 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:43:07 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:48 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:48 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:34:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:34:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2203f205368ce649ffd4367d83cb7d0e0f349edd4a73d17bf72e1d1fd45547`  
		Last Modified: Wed, 11 Dec 2024 20:43:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a929050203563fde4afe1d48374621524ea8726dc8ca55d3c22d0ac7a798594`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1be8f168e721557e602e0b7a3a7cb7e068d12e159af7b67cbd570277d67b6d3`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a047a2e43f164719e30219f432eae6c44e556b5a49ad8de5c356eef5ceb9f2`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538affaf25305d64f324539f173d0eb2d2dd465cb1762b082450ad4c797f27c`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c69a8ef4d7541c4f17aa73bdd2bc059fbf9e06bb80dba0c6780214385b946`  
		Last Modified: Wed, 11 Dec 2024 20:43:13 GMT  
		Size: 25.4 MB (25433638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8adf8499c2eb9b67d228fba4c9e69a29a2d7060f8b7c5592eacc3be4421710`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb262fe2ef81142570e16f48f8f03d4031993f7f4bdd1e8ddc6130f5ac401023`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 339.0 KB (338961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b81c31620602735496201938ab0373d338f5d0422cdb2fe31bf91e703561180`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a3cd836a09077c7888a8a16d4e7bdf054357c81b2dfc19d8a0d373c88f51d`  
		Last Modified: Wed, 11 Dec 2024 20:43:22 GMT  
		Size: 77.3 MB (77349783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6072f4215eedb6bd6a3744f556ae0cd5807bf437d9168f5f06a714a4935e11ad`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddd9caf64ad2db2b643ff3a12c821a4568fb6cab42c886d58ec94c55611183`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9ad2ce3c975bdb8bb5a956ddacab8f088540115a28bdc8d3c28beab4329aec`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b21bef77b61f0857b5cfc4fdb89f2c1c74d5346d5c5813e145c298a5b86642`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b2d84d7d2cf78270c6457f8ab87188b8d84fcbe934749c67f5a31364f3a84`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f1f09b1a52df9107d2afb46ee59d7d749f2b38fb8bf1a07b9e0ba04de6e6e`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 2.3 MB (2331000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450a1c75f8730f0ad6bb33eaa49034a16cc2b79db5b5098a4afd873dcc3ed769`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9.1-windowsservercore`

```console
$ docker pull caddy@sha256:8e842a56471df259c7282c7827f1a7c4b8f24de694d1892428bd6c421d29052a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:2.9.1-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.9.1-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9.1-windowsservercore-1809`

```console
$ docker pull caddy@sha256:1307996d1255d8cba23d2b956a5f47525051154fc907edffeafbdc9ce01b6460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `caddy:2.9.1-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.9.1-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:4d4fc4b1242a7788c646c9d733cf131cea76ed6ee655570a41d2ea783cb56e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `caddy:2.9.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `caddy:builder`

```console
$ docker pull caddy@sha256:427ad6e5dacffe5577d77e3307fef61efdba832b6a78cc80e6f226975b56e1f1
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:db250d8ac333dbfb36d2082ae73b39f21d1316e42d441199f8fdef60aa578773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4fed372693e3e094c6ca0f1a55f4d71f8e0ce8f751c7a4158a8ad487996162`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe7652777a557be7320acd6bafa585a401104296826b9790d94fa35f28480d`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 294.4 KB (294368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda4308841a6cc675c32eadc7ca82f1f5916886229ff6efcbc6e0f9015d73c80`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f167cb8105c9df8315499305c0ce83016c842a6c68f1e4424182dce22a3fe6d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 5.9 MB (5939538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf2b30687fe7e3fa4f927c76a4e43b2db14a66b0e42a32ea9ddcdfa17e0c7d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed24074f0fd5dc780dad0af8b4260d4205b3b89d7a666396c5b415abc85f2a8`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:75e70c9bd28699ef12d45bf9f03e28ff90a8d151d65e788697b9a7d7af5fe398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fc11bbdfee02d4bdc1dbac347ca232538947335e5e4d6788952c5a38c2494`

```dockerfile
```

-	Layers:
	-	`sha256:a19c370ffc738c2bca6c09b72807b6a1244b6294e4ba0df6aa29eaa2aac91efc`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff92b5cdde37260cee10c8515c7ddc7fe46ee4c87c0b3cbfb1b3cf2f34be315`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ec24df61bf7606d181ee40ab713e0df69a89173fe117883dee14f1e0f8cd9bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83456315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc5eb1a64f9004a10a99b5a85fe75b0f0e58290eeb650f976d94e56f143fe3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ab5d3af8a0c99d02e713511deb39821a107d6d0ba6be4b2f6b0843085aea2a`  
		Last Modified: Tue, 07 Jan 2025 06:50:36 GMT  
		Size: 280.0 KB (279984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868f7227e5c7c8b4bac84441ac5dd24dd837136b8721a4f792daa15e57a2e9ea`  
		Last Modified: Tue, 07 Jan 2025 06:51:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8716a3e393f5147708dc6ab75310ace0722971636dcd1e92fc18a1a08d4310`  
		Last Modified: Tue, 07 Jan 2025 19:16:28 GMT  
		Size: 5.9 MB (5882962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d46024c53346834045856881a3323c9ccff4bd71a3f3f4c6064639d6e1706dc`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 1.7 MB (1730294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12c0eba9000c85b2d1a02d8937fcd9c09c11ce473890d5e26a88237e4ce970d`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:52a385666c18fcec928e4c9dffda6c64c1da8483006166e1b8efc40f8f5bbb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02875baa9933babea5658c74ce320bc6e424b75883b7c032f466e85cdafb1ce8`

```dockerfile
```

-	Layers:
	-	`sha256:86ac3110d2be76dee5e418e092a98d1bfceb80f4af3c2e8eb67b6d8ac5bef969`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:711550b3390725d352325fd551c237a75924d3a4d378d0a8c17d834d6bcae853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82660656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6208081873046fa65434043c2e1dd3a2966207bb5ade720526b54fb97606bfdd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb23a6598e9680ccc41dbb603b77f496c80c87db84ee993d3585d4db8daebd2e`  
		Last Modified: Tue, 07 Jan 2025 06:39:22 GMT  
		Size: 279.2 KB (279170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb64175fa34d7385f5a0720c5acb4845fb41cfffcdb03493609e11dc37a6fd3`  
		Last Modified: Tue, 07 Jan 2025 06:40:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfe46e461df3fdecb8a562830ba9b12245936fb2791b9cedbd7a8ca36b20058`  
		Last Modified: Tue, 07 Jan 2025 19:38:26 GMT  
		Size: 5.4 MB (5366898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84596fbb855fcd21b6ca4c90bd456908377d74cffb2445f95237309d2a484c32`  
		Last Modified: Tue, 07 Jan 2025 19:38:57 GMT  
		Size: 1.7 MB (1724266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a624d5a8ac42b5c2c1445a69ab87ced9badec3de749d9b8599880570b3cb273f`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a8a75354935bc0c2b56ea5d8b81443bde300dba8442dd8b1af1d3b9a109e7839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 KB (310762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb03932eed79a6f6239c181f8ae39f1ac887fb5e37423392abb9df355f32f6d`

```dockerfile
```

-	Layers:
	-	`sha256:ff2ed6da1cb98be75248ee79a7a9982cac41e1383ac1c44a37c63f2d2da0d5bf`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 290.5 KB (290538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e990bba3a097819e2870500e1ffb95d24a29d5089876af934f56a1f29952b84`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c11ef1d0a5c9ed229f43082f29f8ecf422a72aa72bdac93e7b6abc8706f8f7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82800608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce92f6eb0f78cd92a5b165889654838a71ce963d7d0eba1d64d0073ae223be0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4f93e44bdb513724a186600fdec99e49dc6de485ed4757e27b16ec93cbf7b4`  
		Last Modified: Tue, 07 Jan 2025 07:41:57 GMT  
		Size: 281.4 KB (281389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7497157ade0eb8e27bb99f1d2cbe466a3b159a321b071ec86638aa51639752f7`  
		Last Modified: Tue, 07 Jan 2025 07:42:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e208341eb37c26d31056e7b9148bfdf952c929003ac80f238023004a70d9fa`  
		Last Modified: Tue, 07 Jan 2025 17:23:51 GMT  
		Size: 6.1 MB (6057100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3a64dbd3a39b6007f76c39b6ee0c0720d4f4a40cc9dcc8dda3d042db4d37a0`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 1.7 MB (1701424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23ad2d83091707b797b9ad6a73c160439fe1e6ee21e669643988449af62b5e`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ccda48881787a1a9e2e973d61572f691776fed4ffd4e9b624b6bb0b73c9875b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 KB (308018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd4cc2f180b6209f339c8c9c89535d12602c5c9bb3a47255f9e1401e1f98fdd`

```dockerfile
```

-	Layers:
	-	`sha256:2d5335a62a98cd1fb5b9c13a01293700177a9dcae5897f6131a2f51a0de0c371`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 287.7 KB (287749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:509d779c7eb8321ae849c288781db7054c0c756218e63f2864a669f57f982089`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 20.3 KB (20269 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ae070d55ed734bb9f26b8bd370a2505a74b68f8258358df545af4f86f19decf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82669759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d45931cb6f86cb49eb2a88c2fb65ea04da6b51a5931231776eaa748c76c32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10173039484873ca3979a3698ef22d1edfdf1fb0aeabab8ad8b5abf80e36c0b`  
		Last Modified: Wed, 08 Jan 2025 21:52:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e90046d3ba1afd50a6d4a5c6c40609982d2342f650d63e92845f9680191fc04`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 6.3 MB (6261729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6020e3492fb8731819fb401ebf9bea060d1dba0da112cc369801cc6f75181`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 1.7 MB (1695595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31426252091c11d90ffd2cb5692a5923c31dae3911af16cc2973b5164e1ef2`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e0dbaba01b809b9974e5b39e1949a4eba4c650e9c8add5d4940186740ae9c274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6003454eef73ebaabead0aaf06b619bc1eccee16eaf04558aacc5148fc2e00f7`

```dockerfile
```

-	Layers:
	-	`sha256:5ef66216d744cfcfafeb2f64c715c6d373ca1dee38c77308d694033c36689144`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a85f55b9730ad2b1de1532bd27f9a27055fa947fee10a1e04c3641ae2965051`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; riscv64

```console
$ docker pull caddy@sha256:6526b547f327fdad247225ea542b9ce1cc77d687884dde4b14b75241e63aa3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82770124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bdb944f99feaf2e305e0d10a42df1c2bf6de1bd0d6138ea9f253171ca76699`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9da01c4ee7a2864330da14801bdf35f981730b5e2ffea0588c9ac48734e26b`  
		Last Modified: Wed, 13 Nov 2024 01:22:36 GMT  
		Size: 291.7 KB (291671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Last Modified: Tue, 03 Dec 2024 22:32:57 GMT  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ab90a88816114ae116bd757c876eb44413901c2699659dffc92325a8501bb`  
		Last Modified: Tue, 03 Dec 2024 22:32:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb90820f994a13ba411ce9f13382e83c031ed0b2d2219db34d7e121af2ca4e4`  
		Last Modified: Tue, 03 Dec 2024 23:30:22 GMT  
		Size: 6.2 MB (6153816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755a3f609dacb1c3c9cfd444c8e0e17d3164ff984a8c8b256ca23bfb5285abd`  
		Last Modified: Tue, 03 Dec 2024 23:32:07 GMT  
		Size: 1.7 MB (1711642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca049294665a12d4c46195094fc9caab2fe1dd23f4387a0bcafa5d4554ad85fc`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:d34f32e4efec0fe90fb35c9ea61321bb53cbd7830923f55f6994fee7e22b2fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3ff966024ddcb0d6b64a1ee4c2603f448aa7bb698535cc33c4fa10b1bde26d`

```dockerfile
```

-	Layers:
	-	`sha256:f83d644b47cbf45f33c3427c879684d93be2f3bb6a034dd204d813c0a3ad241a`  
		Last Modified: Tue, 03 Dec 2024 23:32:07 GMT  
		Size: 290.4 KB (290442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9073f9e18b020a4a883d3c1b52d5b8511b42396b8eb9972a0e5fc216f03d47ce`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:6aa66a7c188127cf3b1d74c61ea008b95a1bdd86535cba563f3582710b036d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84682121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29cc61277738cb7914c72ff20d3bfd79b577ba6b5d721daae3058dc1dfa8244`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141e3fcf5173977fad664af74a255a69a2749551008af76945b144725f228f5f`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 280.2 KB (280152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9039b3f81c901f7abad17b0429809aa980ff70f25d072c8d64ee71f7db3e045`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8aa38916b9a65afe6d745bc7b4405235419055139a947defb9ce792bb28b73`  
		Last Modified: Tue, 07 Jan 2025 16:55:39 GMT  
		Size: 6.2 MB (6200978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8fb1e6bc0540f6045137dc3088acea82454684beb33b47125d22823982d437`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 1.8 MB (1771406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788488d4f2b594a7b69ffa9ada90972f2be7de5973303ff5d5d6dee1ddb5270f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:224cde432b86d4943a06974721e702e3be7c1723fd153c64411a1070d8127f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 KB (305797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914a49da35ae3856968dab023e6d0459b952fca4d12749f61dcda3b1a4bee0cc`

```dockerfile
```

-	Layers:
	-	`sha256:c767f61505dfabedc5ae5df8b49499a6c8fd64d5a2735c26bd1820abd6c01d2f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 285.7 KB (285694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfeae3b8d465e03c17edddbdf5a198fd4d9a0c9a0c78e30622b17a5255100765`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:0189cfa4a4c02a3bb800a7e32a588f1264aa3f8eafa4b94e6ed4129cbe3ff2a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2359343914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d72f15e0f30165074557b2b759d5db3e5947c39aee860af1bdf1e3877f65413`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:29 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:41:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:41:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:41:51 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:41:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:41:57 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:43:05 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:43:07 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:48 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:48 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:34:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:34:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2203f205368ce649ffd4367d83cb7d0e0f349edd4a73d17bf72e1d1fd45547`  
		Last Modified: Wed, 11 Dec 2024 20:43:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a929050203563fde4afe1d48374621524ea8726dc8ca55d3c22d0ac7a798594`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1be8f168e721557e602e0b7a3a7cb7e068d12e159af7b67cbd570277d67b6d3`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a047a2e43f164719e30219f432eae6c44e556b5a49ad8de5c356eef5ceb9f2`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538affaf25305d64f324539f173d0eb2d2dd465cb1762b082450ad4c797f27c`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c69a8ef4d7541c4f17aa73bdd2bc059fbf9e06bb80dba0c6780214385b946`  
		Last Modified: Wed, 11 Dec 2024 20:43:13 GMT  
		Size: 25.4 MB (25433638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8adf8499c2eb9b67d228fba4c9e69a29a2d7060f8b7c5592eacc3be4421710`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb262fe2ef81142570e16f48f8f03d4031993f7f4bdd1e8ddc6130f5ac401023`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 339.0 KB (338961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b81c31620602735496201938ab0373d338f5d0422cdb2fe31bf91e703561180`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a3cd836a09077c7888a8a16d4e7bdf054357c81b2dfc19d8a0d373c88f51d`  
		Last Modified: Wed, 11 Dec 2024 20:43:22 GMT  
		Size: 77.3 MB (77349783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6072f4215eedb6bd6a3744f556ae0cd5807bf437d9168f5f06a714a4935e11ad`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddd9caf64ad2db2b643ff3a12c821a4568fb6cab42c886d58ec94c55611183`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9ad2ce3c975bdb8bb5a956ddacab8f088540115a28bdc8d3c28beab4329aec`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b21bef77b61f0857b5cfc4fdb89f2c1c74d5346d5c5813e145c298a5b86642`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b2d84d7d2cf78270c6457f8ab87188b8d84fcbe934749c67f5a31364f3a84`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f1f09b1a52df9107d2afb46ee59d7d749f2b38fb8bf1a07b9e0ba04de6e6e`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 2.3 MB (2331000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450a1c75f8730f0ad6bb33eaa49034a16cc2b79db5b5098a4afd873dcc3ed769`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:ea06d27be71f8ef91c6d6f553d93e6261efe59e77edf8ca72c562150017510d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2119855201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688816f8244428a55ae1ec4bd192c597ce0f04d19edda948e46a80ecfd9bf8ce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:39:37 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:39:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:40:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:40:47 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:40:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:40:54 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:42:12 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:42:13 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:32 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:32 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:35:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:35:04 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f3bbeb4e2782220c87261e5e9d61855baf0ace86081d92be83026dd5e8fcc2`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241e544e87d299e404e0055ac6a3d562110f5dbac92ab40f5274757c352361`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d65d85ef63918a2fe84d0a5c56c3c6b83838ea5060fc445cb586acaa3fc316`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d89f6bf6b5749f5d1a48d1e66e0f5882aa8e07e2d3218b9a7e1f59c2dda0c`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54a47581ed1b6b7629a8abc75e2e6e45c36975a21ec95b65e8106e75c34aafa`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81645ff46b23f2588b64411ee4dd209ad3383c3b4376b70fa25b258296a5d05`  
		Last Modified: Wed, 11 Dec 2024 20:42:19 GMT  
		Size: 25.6 MB (25561663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619f9252e7182af97b30c9a01c651c8a8f83c521db1c842279b8adaf45bc17ac`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e01c2f476af7e5c6236de3ec31577c6d3d4491c44d2e5cce185341f9d8a19`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 328.3 KB (328344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd74620f512254e194320e032040d3c01472e9f9c304c960171132f8a838cb7`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05934960da5aa39d60d727548d37d080612ea4164a25e09b3c3d9e310f6fa14f`  
		Last Modified: Wed, 11 Dec 2024 20:42:28 GMT  
		Size: 77.5 MB (77463395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d829f35d8061698251f21a9c2ad8cb0d344ddb5465b577017415f89f82d50aa`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0302b0fa76f2e0e3678e4ec6e3a77b56966df7cbd7788ff083f096d58f66eb9`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b2e9a08ab9b486a49339207a0e3c35851ead887e82207dabf747c69de0ef9`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb03d015e74d14f0a3566de1e456b2c92453ba713a378af8d0608061e2f9d06`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7da9a44214dc454bfc9248a3e2db15fda48ce69c4c8f426122a25540d604d20`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0fc2d732d66c3b5aeb005f494441963afb2427e6b8eb07d9f0e0855a328c31`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 2.3 MB (2314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c45570296cf141f1579eb94ca900ddea076099f18b3f5e5dedf41c600a449`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:04a9a96806361a24024ae9331926cc4adf2e3a8e75d71428535293d01173dfd0
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
$ docker pull caddy@sha256:db250d8ac333dbfb36d2082ae73b39f21d1316e42d441199f8fdef60aa578773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4fed372693e3e094c6ca0f1a55f4d71f8e0ce8f751c7a4158a8ad487996162`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe7652777a557be7320acd6bafa585a401104296826b9790d94fa35f28480d`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 294.4 KB (294368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda4308841a6cc675c32eadc7ca82f1f5916886229ff6efcbc6e0f9015d73c80`  
		Last Modified: Wed, 08 Jan 2025 18:15:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f167cb8105c9df8315499305c0ce83016c842a6c68f1e4424182dce22a3fe6d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 5.9 MB (5939538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf2b30687fe7e3fa4f927c76a4e43b2db14a66b0e42a32ea9ddcdfa17e0c7d`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 1.8 MB (1835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed24074f0fd5dc780dad0af8b4260d4205b3b89d7a666396c5b415abc85f2a8`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:75e70c9bd28699ef12d45bf9f03e28ff90a8d151d65e788697b9a7d7af5fe398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 KB (313626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fc11bbdfee02d4bdc1dbac347ca232538947335e5e4d6788952c5a38c2494`

```dockerfile
```

-	Layers:
	-	`sha256:a19c370ffc738c2bca6c09b72807b6a1244b6294e4ba0df6aa29eaa2aac91efc`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 293.5 KB (293523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff92b5cdde37260cee10c8515c7ddc7fe46ee4c87c0b3cbfb1b3cf2f34be315`  
		Last Modified: Wed, 08 Jan 2025 23:31:57 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ec24df61bf7606d181ee40ab713e0df69a89173fe117883dee14f1e0f8cd9bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83456315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc5eb1a64f9004a10a99b5a85fe75b0f0e58290eeb650f976d94e56f143fe3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ab5d3af8a0c99d02e713511deb39821a107d6d0ba6be4b2f6b0843085aea2a`  
		Last Modified: Tue, 07 Jan 2025 06:50:36 GMT  
		Size: 280.0 KB (279984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868f7227e5c7c8b4bac84441ac5dd24dd837136b8721a4f792daa15e57a2e9ea`  
		Last Modified: Tue, 07 Jan 2025 06:51:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8716a3e393f5147708dc6ab75310ace0722971636dcd1e92fc18a1a08d4310`  
		Last Modified: Tue, 07 Jan 2025 19:16:28 GMT  
		Size: 5.9 MB (5882962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d46024c53346834045856881a3323c9ccff4bd71a3f3f4c6064639d6e1706dc`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 1.7 MB (1730294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12c0eba9000c85b2d1a02d8937fcd9c09c11ce473890d5e26a88237e4ce970d`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:52a385666c18fcec928e4c9dffda6c64c1da8483006166e1b8efc40f8f5bbb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02875baa9933babea5658c74ce320bc6e424b75883b7c032f466e85cdafb1ce8`

```dockerfile
```

-	Layers:
	-	`sha256:86ac3110d2be76dee5e418e092a98d1bfceb80f4af3c2e8eb67b6d8ac5bef969`  
		Last Modified: Tue, 07 Jan 2025 19:16:39 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:711550b3390725d352325fd551c237a75924d3a4d378d0a8c17d834d6bcae853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82660656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6208081873046fa65434043c2e1dd3a2966207bb5ade720526b54fb97606bfdd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb23a6598e9680ccc41dbb603b77f496c80c87db84ee993d3585d4db8daebd2e`  
		Last Modified: Tue, 07 Jan 2025 06:39:22 GMT  
		Size: 279.2 KB (279170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb64175fa34d7385f5a0720c5acb4845fb41cfffcdb03493609e11dc37a6fd3`  
		Last Modified: Tue, 07 Jan 2025 06:40:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfe46e461df3fdecb8a562830ba9b12245936fb2791b9cedbd7a8ca36b20058`  
		Last Modified: Tue, 07 Jan 2025 19:38:26 GMT  
		Size: 5.4 MB (5366898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84596fbb855fcd21b6ca4c90bd456908377d74cffb2445f95237309d2a484c32`  
		Last Modified: Tue, 07 Jan 2025 19:38:57 GMT  
		Size: 1.7 MB (1724266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a624d5a8ac42b5c2c1445a69ab87ced9badec3de749d9b8599880570b3cb273f`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a8a75354935bc0c2b56ea5d8b81443bde300dba8442dd8b1af1d3b9a109e7839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 KB (310762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb03932eed79a6f6239c181f8ae39f1ac887fb5e37423392abb9df355f32f6d`

```dockerfile
```

-	Layers:
	-	`sha256:ff2ed6da1cb98be75248ee79a7a9982cac41e1383ac1c44a37c63f2d2da0d5bf`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 290.5 KB (290538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e990bba3a097819e2870500e1ffb95d24a29d5089876af934f56a1f29952b84`  
		Last Modified: Tue, 07 Jan 2025 19:38:56 GMT  
		Size: 20.2 KB (20224 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c11ef1d0a5c9ed229f43082f29f8ecf422a72aa72bdac93e7b6abc8706f8f7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82800608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce92f6eb0f78cd92a5b165889654838a71ce963d7d0eba1d64d0073ae223be0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4f93e44bdb513724a186600fdec99e49dc6de485ed4757e27b16ec93cbf7b4`  
		Last Modified: Tue, 07 Jan 2025 07:41:57 GMT  
		Size: 281.4 KB (281389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7497157ade0eb8e27bb99f1d2cbe466a3b159a321b071ec86638aa51639752f7`  
		Last Modified: Tue, 07 Jan 2025 07:42:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e208341eb37c26d31056e7b9148bfdf952c929003ac80f238023004a70d9fa`  
		Last Modified: Tue, 07 Jan 2025 17:23:51 GMT  
		Size: 6.1 MB (6057100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3a64dbd3a39b6007f76c39b6ee0c0720d4f4a40cc9dcc8dda3d042db4d37a0`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 1.7 MB (1701424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23ad2d83091707b797b9ad6a73c160439fe1e6ee21e669643988449af62b5e`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ccda48881787a1a9e2e973d61572f691776fed4ffd4e9b624b6bb0b73c9875b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 KB (308018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd4cc2f180b6209f339c8c9c89535d12602c5c9bb3a47255f9e1401e1f98fdd`

```dockerfile
```

-	Layers:
	-	`sha256:2d5335a62a98cd1fb5b9c13a01293700177a9dcae5897f6131a2f51a0de0c371`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 287.7 KB (287749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:509d779c7eb8321ae849c288781db7054c0c756218e63f2864a669f57f982089`  
		Last Modified: Tue, 07 Jan 2025 17:24:04 GMT  
		Size: 20.3 KB (20269 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ae070d55ed734bb9f26b8bd370a2505a74b68f8258358df545af4f86f19decf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82669759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d45931cb6f86cb49eb2a88c2fb65ea04da6b51a5931231776eaa748c76c32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 03 Dec 2024 19:01:46 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
# Wed, 08 Jan 2025 17:30:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 17:30:49 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 17:30:49 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Jan 2025 17:30:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Jan 2025 17:30:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536d34381fd9ad3cee58f53559c0874fc783fd9067870f324d9d4e8f092a0015`  
		Last Modified: Wed, 08 Jan 2025 21:50:14 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10173039484873ca3979a3698ef22d1edfdf1fb0aeabab8ad8b5abf80e36c0b`  
		Last Modified: Wed, 08 Jan 2025 21:52:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e90046d3ba1afd50a6d4a5c6c40609982d2342f650d63e92845f9680191fc04`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 6.3 MB (6261729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6020e3492fb8731819fb401ebf9bea060d1dba0da112cc369801cc6f75181`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 1.7 MB (1695595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31426252091c11d90ffd2cb5692a5923c31dae3911af16cc2973b5164e1ef2`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e0dbaba01b809b9974e5b39e1949a4eba4c650e9c8add5d4940186740ae9c274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 KB (311839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6003454eef73ebaabead0aaf06b619bc1eccee16eaf04558aacc5148fc2e00f7`

```dockerfile
```

-	Layers:
	-	`sha256:5ef66216d744cfcfafeb2f64c715c6d373ca1dee38c77308d694033c36689144`  
		Last Modified: Thu, 09 Jan 2025 03:30:26 GMT  
		Size: 291.7 KB (291666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a85f55b9730ad2b1de1532bd27f9a27055fa947fee10a1e04c3641ae2965051`  
		Last Modified: Thu, 09 Jan 2025 03:30:25 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:6526b547f327fdad247225ea542b9ce1cc77d687884dde4b14b75241e63aa3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82770124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bdb944f99feaf2e305e0d10a42df1c2bf6de1bd0d6138ea9f253171ca76699`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9da01c4ee7a2864330da14801bdf35f981730b5e2ffea0588c9ac48734e26b`  
		Last Modified: Wed, 13 Nov 2024 01:22:36 GMT  
		Size: 291.7 KB (291671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Last Modified: Tue, 03 Dec 2024 22:32:57 GMT  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ab90a88816114ae116bd757c876eb44413901c2699659dffc92325a8501bb`  
		Last Modified: Tue, 03 Dec 2024 22:32:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb90820f994a13ba411ce9f13382e83c031ed0b2d2219db34d7e121af2ca4e4`  
		Last Modified: Tue, 03 Dec 2024 23:30:22 GMT  
		Size: 6.2 MB (6153816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755a3f609dacb1c3c9cfd444c8e0e17d3164ff984a8c8b256ca23bfb5285abd`  
		Last Modified: Tue, 03 Dec 2024 23:32:07 GMT  
		Size: 1.7 MB (1711642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca049294665a12d4c46195094fc9caab2fe1dd23f4387a0bcafa5d4554ad85fc`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:d34f32e4efec0fe90fb35c9ea61321bb53cbd7830923f55f6994fee7e22b2fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 KB (310615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3ff966024ddcb0d6b64a1ee4c2603f448aa7bb698535cc33c4fa10b1bde26d`

```dockerfile
```

-	Layers:
	-	`sha256:f83d644b47cbf45f33c3427c879684d93be2f3bb6a034dd204d813c0a3ad241a`  
		Last Modified: Tue, 03 Dec 2024 23:32:07 GMT  
		Size: 290.4 KB (290442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9073f9e18b020a4a883d3c1b52d5b8511b42396b8eb9972a0e5fc216f03d47ce`  
		Last Modified: Tue, 03 Dec 2024 23:32:06 GMT  
		Size: 20.2 KB (20173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:6aa66a7c188127cf3b1d74c61ea008b95a1bdd86535cba563f3582710b036d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84682121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29cc61277738cb7914c72ff20d3bfd79b577ba6b5d721daae3058dc1dfa8244`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 06 Nov 2024 00:46:53 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 Nov 2024 00:46:53 GMT
ENV GOPATH=/go
# Wed, 06 Nov 2024 00:46:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 00:46:53 GMT
COPY /target/ / # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /go
# Wed, 06 Nov 2024 00:46:53 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Nov 2024 00:46:53 GMT
ENV XCADDY_SETCAP=1
# Wed, 06 Nov 2024 00:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='09b0bd09c879c2985c562deec675da074f896c9e114717d07f11bdb2714b7e9ecbb26748431732469c245e1517cde6e78ee6b0f6e839de3992d22a3d474188fe' ;; 		armhf)   binArch='armv6'; checksum='dd1ee3d27bb9f0c2b6b900e19e779398c972fc7a0affaf19ee64fb01689cdd18e2df1429251607dbdeca1ad57d1851317c9f0c0c4c4ead3aa2b9e68678a62d52' ;; 		armv7)   binArch='armv7'; checksum='e13003e727c228e84b1abb72db3f92362dd232087256ea51249002d4d0a17d002760123a33dafb8d47553d54c7d821f3d3dee419347a61f967ea4617abaef46a' ;; 		aarch64) binArch='arm64'; checksum='c04464f944ebad714ded44691d359cf27109f5e088f7ee7ed5b49941c88382b0d31c91b81cb1c11444371abe7c491df06aba7306503a17627a7826ac8992e02a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c05c883e3a6162b77454ed4efa1e28278d0624a53bb096dced95e27b61f60fdcc0a40e90524806fa07e2da654c6420995fede7077c2c2319351f8f0bc1855cd9' ;; 		riscv64) binArch='riscv64'; checksum='84d1e61330aed77373ffa91dcfda5e20757372fb6ec204e33916a78d864aeb5e0560b2a8aad3166a91311110cb41fce4684a5731cf0d738780f11ee7838811de' ;; 		s390x)   binArch='s390x'; checksum='93ff65601c255e9a2910b8ccfd3bcd4765ea6e5261fab31918e8bef0ffa37bcfaf45e2311fd43f9d9a13751102c3644d107d463fdb64d05c2af02307b96e9772' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 06 Nov 2024 00:46:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141e3fcf5173977fad664af74a255a69a2749551008af76945b144725f228f5f`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 280.2 KB (280152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9039b3f81c901f7abad17b0429809aa980ff70f25d072c8d64ee71f7db3e045`  
		Last Modified: Tue, 07 Jan 2025 06:42:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8aa38916b9a65afe6d745bc7b4405235419055139a947defb9ce792bb28b73`  
		Last Modified: Tue, 07 Jan 2025 16:55:39 GMT  
		Size: 6.2 MB (6200978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8fb1e6bc0540f6045137dc3088acea82454684beb33b47125d22823982d437`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 1.8 MB (1771406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788488d4f2b594a7b69ffa9ada90972f2be7de5973303ff5d5d6dee1ddb5270f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:224cde432b86d4943a06974721e702e3be7c1723fd153c64411a1070d8127f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 KB (305797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914a49da35ae3856968dab023e6d0459b952fca4d12749f61dcda3b1a4bee0cc`

```dockerfile
```

-	Layers:
	-	`sha256:c767f61505dfabedc5ae5df8b49499a6c8fd64d5a2735c26bd1820abd6c01d2f`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 285.7 KB (285694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfeae3b8d465e03c17edddbdf5a198fd4d9a0c9a0c78e30622b17a5255100765`  
		Last Modified: Tue, 07 Jan 2025 16:56:28 GMT  
		Size: 20.1 KB (20103 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ba8e01cd3489a6d329519bd950beb8f983734752aeb472b4ef6eb1ee8711a7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:ea06d27be71f8ef91c6d6f553d93e6261efe59e77edf8ca72c562150017510d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2119855201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688816f8244428a55ae1ec4bd192c597ce0f04d19edda948e46a80ecfd9bf8ce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:39:36 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:39:37 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:39:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:40:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:40:47 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:40:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:40:54 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:42:12 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:42:13 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:32 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:32 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:35:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:35:04 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f3bbeb4e2782220c87261e5e9d61855baf0ace86081d92be83026dd5e8fcc2`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241e544e87d299e404e0055ac6a3d562110f5dbac92ab40f5274757c352361`  
		Last Modified: Wed, 11 Dec 2024 20:42:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d65d85ef63918a2fe84d0a5c56c3c6b83838ea5060fc445cb586acaa3fc316`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3d89f6bf6b5749f5d1a48d1e66e0f5882aa8e07e2d3218b9a7e1f59c2dda0c`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54a47581ed1b6b7629a8abc75e2e6e45c36975a21ec95b65e8106e75c34aafa`  
		Last Modified: Wed, 11 Dec 2024 20:42:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81645ff46b23f2588b64411ee4dd209ad3383c3b4376b70fa25b258296a5d05`  
		Last Modified: Wed, 11 Dec 2024 20:42:19 GMT  
		Size: 25.6 MB (25561663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619f9252e7182af97b30c9a01c651c8a8f83c521db1c842279b8adaf45bc17ac`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e01c2f476af7e5c6236de3ec31577c6d3d4491c44d2e5cce185341f9d8a19`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 328.3 KB (328344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd74620f512254e194320e032040d3c01472e9f9c304c960171132f8a838cb7`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05934960da5aa39d60d727548d37d080612ea4164a25e09b3c3d9e310f6fa14f`  
		Last Modified: Wed, 11 Dec 2024 20:42:28 GMT  
		Size: 77.5 MB (77463395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d829f35d8061698251f21a9c2ad8cb0d344ddb5465b577017415f89f82d50aa`  
		Last Modified: Wed, 11 Dec 2024 20:42:16 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0302b0fa76f2e0e3678e4ec6e3a77b56966df7cbd7788ff083f096d58f66eb9`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153b2e9a08ab9b486a49339207a0e3c35851ead887e82207dabf747c69de0ef9`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb03d015e74d14f0a3566de1e456b2c92453ba713a378af8d0608061e2f9d06`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7da9a44214dc454bfc9248a3e2db15fda48ce69c4c8f426122a25540d604d20`  
		Last Modified: Wed, 08 Jan 2025 23:35:06 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0fc2d732d66c3b5aeb005f494441963afb2427e6b8eb07d9f0e0855a328c31`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 2.3 MB (2314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c45570296cf141f1579eb94ca900ddea076099f18b3f5e5dedf41c600a449`  
		Last Modified: Wed, 08 Jan 2025 23:35:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:af2dcf0d4a7eae883882f2a63357f55bc484ef53386cb5ceb912e92631130a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:0189cfa4a4c02a3bb800a7e32a588f1264aa3f8eafa4b94e6ed4129cbe3ff2a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2359343914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d72f15e0f30165074557b2b759d5db3e5947c39aee860af1bdf1e3877f65413`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:29 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:41:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:41:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:41:51 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:41:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:41:57 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:43:05 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:43:07 GMT
WORKDIR C:\go
# Wed, 08 Jan 2025 23:33:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:48 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 08 Jan 2025 23:33:48 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:49 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Jan 2025 23:34:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 08 Jan 2025 23:34:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2203f205368ce649ffd4367d83cb7d0e0f349edd4a73d17bf72e1d1fd45547`  
		Last Modified: Wed, 11 Dec 2024 20:43:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a929050203563fde4afe1d48374621524ea8726dc8ca55d3c22d0ac7a798594`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1be8f168e721557e602e0b7a3a7cb7e068d12e159af7b67cbd570277d67b6d3`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a047a2e43f164719e30219f432eae6c44e556b5a49ad8de5c356eef5ceb9f2`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538affaf25305d64f324539f173d0eb2d2dd465cb1762b082450ad4c797f27c`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c69a8ef4d7541c4f17aa73bdd2bc059fbf9e06bb80dba0c6780214385b946`  
		Last Modified: Wed, 11 Dec 2024 20:43:13 GMT  
		Size: 25.4 MB (25433638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8adf8499c2eb9b67d228fba4c9e69a29a2d7060f8b7c5592eacc3be4421710`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb262fe2ef81142570e16f48f8f03d4031993f7f4bdd1e8ddc6130f5ac401023`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 339.0 KB (338961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b81c31620602735496201938ab0373d338f5d0422cdb2fe31bf91e703561180`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a3cd836a09077c7888a8a16d4e7bdf054357c81b2dfc19d8a0d373c88f51d`  
		Last Modified: Wed, 11 Dec 2024 20:43:22 GMT  
		Size: 77.3 MB (77349783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6072f4215eedb6bd6a3744f556ae0cd5807bf437d9168f5f06a714a4935e11ad`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ddd9caf64ad2db2b643ff3a12c821a4568fb6cab42c886d58ec94c55611183`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9ad2ce3c975bdb8bb5a956ddacab8f088540115a28bdc8d3c28beab4329aec`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b21bef77b61f0857b5cfc4fdb89f2c1c74d5346d5c5813e145c298a5b86642`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b2d84d7d2cf78270c6457f8ab87188b8d84fcbe934749c67f5a31364f3a84`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f1f09b1a52df9107d2afb46ee59d7d749f2b38fb8bf1a07b9e0ba04de6e6e`  
		Last Modified: Wed, 08 Jan 2025 23:35:01 GMT  
		Size: 2.3 MB (2331000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450a1c75f8730f0ad6bb33eaa49034a16cc2b79db5b5098a4afd873dcc3ed769`  
		Last Modified: Wed, 08 Jan 2025 23:35:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:65955e6725e3f743e57534af15c6efab98b7d6978b5be2efa21cbe8e24bbfaa3
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:latest` - linux; amd64

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

### `caddy:latest` - unknown; unknown

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

### `caddy:latest` - linux; arm variant v6

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

### `caddy:latest` - unknown; unknown

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

### `caddy:latest` - linux; arm variant v7

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

### `caddy:latest` - unknown; unknown

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

### `caddy:latest` - linux; arm64 variant v8

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

### `caddy:latest` - unknown; unknown

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

### `caddy:latest` - linux; ppc64le

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

### `caddy:latest` - unknown; unknown

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

### `caddy:latest` - linux; riscv64

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

### `caddy:latest` - unknown; unknown

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

### `caddy:latest` - linux; s390x

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

### `caddy:latest` - unknown; unknown

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

### `caddy:latest` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:8e842a56471df259c7282c7827f1a7c4b8f24de694d1892428bd6c421d29052a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:1307996d1255d8cba23d2b956a5f47525051154fc907edffeafbdc9ce01b6460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7a447d4f0bb560a73ebf3865e078499a05fb05a559cf6714420bb186dc664c9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289f6cbd1eeb7288428d139f00af4e989aa61bf9354a160eb2d3b11da6c7def`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 08 Jan 2025 23:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:33:13 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:33:14 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:33:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:33:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:33:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:33:35 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:33:36 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:33:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:33:38 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:33:39 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:33:48 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:33:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b620f9a6697835bfd46ef7b1b8ae27a2e0a803920052df330f74e9d1ee39068`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976271a1747188d6c7a9131edcb20594bdcfb076f60002abb928a61c285024a5`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 475.0 KB (475029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed716727b5e0f596e97933ecab793b52651957b6a2c4bf2eb32beadbdfc36d0`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5688658385fc13ab372cb697684be4012af55b052f8399e4825756621545f4`  
		Last Modified: Wed, 08 Jan 2025 23:33:56 GMT  
		Size: 15.0 MB (15003697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b559f4c0076cff6af782c9712176d4f67015b33144e21ec0b29dadf1983cee`  
		Last Modified: Wed, 08 Jan 2025 23:33:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446028551343f8378bcf51426dd1c151fbb46c8138c5599b71214aa03464210`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d8e2af17abe0e34b75b26da85230a496c0d9d21ad0cdbbc35b2a4289c196b9`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5506f302e6d4cb49be05c835e53db9493b96d324f3323bee83cf1b84c0ee189`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b9be9b57118a0f5813565a85e432ee5d6ad18d1d344a2bbefa8c5e9633241`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ee3111b192a449165b71e1c9f3ef84b3749fc9e5b6f42fe02ca48df98a10e`  
		Last Modified: Wed, 08 Jan 2025 23:33:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40b25bb82f87082711b7ff0afdbda24c5c24be0536bd14e7352035048a257e3`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61464acfb070bcace25523faa516cc934ab0d5bb0ae8342705b76bf96a2f5bed`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611aad391dd1f97e7ac6f2cd747b1850ced5667ce0e44a60c28cc694f7d3ae8`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa230aa23918f507c7c3b99d9ed901c8e69c4f66248aa7f583aa6c31cbc9f`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ce3bb0ff5249426301a8d894ae1f2c9924570ef17e6e0dbc6e26abb21cc5`  
		Last Modified: Wed, 08 Jan 2025 23:33:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e5711f940fb9d28039ac6410e99d9bb58139647d7286c67d1d8af5bb9c99c6`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077818ed9b43bda9f8dd86690fdb89fb1d8d8ce8000c7f58918840af4959675f`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc835b76ee8e009bb6299f8ca0ef857cb0fa82fd25201d77f652c737f422598`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df951891f56cd6bd74df0ac5e2ffcd23fb4926ffde8a717e5ce61464d31d59`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 337.7 KB (337694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70638838d599fd2fb85bf21029df97af06822219ac4f8196684c69ce10a16603`  
		Last Modified: Wed, 08 Jan 2025 23:33:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:4d4fc4b1242a7788c646c9d733cf131cea76ed6ee655570a41d2ea783cb56e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:56c41ce28bd71deed123237c5ccad4bcb2e75cefa1cc83f50934431f754898b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269648313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e673d78eb576696f429fcb8037be7a928126308758a8d7f01b4edc41f8f9e8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 08 Jan 2025 23:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Jan 2025 23:32:18 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 08 Jan 2025 23:32:18 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 08 Jan 2025 23:32:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 08 Jan 2025 23:32:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 08 Jan 2025 23:32:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 08 Jan 2025 23:32:34 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 08 Jan 2025 23:32:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 08 Jan 2025 23:32:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 08 Jan 2025 23:32:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 08 Jan 2025 23:32:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 08 Jan 2025 23:32:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 08 Jan 2025 23:32:39 GMT
EXPOSE 80
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443
# Wed, 08 Jan 2025 23:32:40 GMT
EXPOSE 443/udp
# Wed, 08 Jan 2025 23:32:41 GMT
EXPOSE 2019
# Wed, 08 Jan 2025 23:32:46 GMT
RUN caddy version
# Wed, 08 Jan 2025 23:32:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042d18fb8683285697559e73cf74aeef0c8a08f9315bb518e5e3a9bee608aa8`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095376267f84cb3f81d900e0aa588d4a676110ea800da2c966dc31bdcfda6849`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 369.6 KB (369626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40af7f69b729ba457e22d4c258942b0e9ba55aad071c02851490628a9dc0e29`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19359de01ce18a398018bff964ffac6e17d57873939a38cb2bed7ae94c477dee`  
		Last Modified: Wed, 08 Jan 2025 23:32:54 GMT  
		Size: 15.0 MB (15020893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c432a0ce2d7b884d62e387761503f71c77992ee8e3b67178c7d07714cb24385`  
		Last Modified: Wed, 08 Jan 2025 23:32:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810aa041d9e2b10e4afbecb82dfdc23e3153aee8365e6e273cbc4a5084d9d67`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594fb8b58f33ce0d2733acf23484cc35d1e1f1e74818993953063066e0ac12e`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb726a2aae3e529211313e9c317c354f9e5019b9398fb43b8279de811c8b4e7`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9f25566dc57e22fd9869aa43110ed993010b3327aa1b94766139b4886e550c`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e6518d0c8a8caa9aea40aba7f422aa00934d1f63eebde9d7c8625c8fbba140`  
		Last Modified: Wed, 08 Jan 2025 23:32:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56d2e1abbf379532e617d59db773b4242dea07354b6596b4a7075a3fcf8ecf2`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b612812d8d9a05a7aece9c59b6bf041d593d0269b5829a3663df750baaafe`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c93d9ea6936ab90e3d698344de15aa396b30101cc8f53d01519a769dd9f5e4`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848574a2d0f941f796997862219f22e1a2c7350a48314676a585b3dd87369465`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421bb87e2bbe43daed75d8c4c0984c892858c5cc14b90a665e53730131b34e0`  
		Last Modified: Wed, 08 Jan 2025 23:32:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a960d19f1b123d25bf6d5e8150adbe2192e29347a5e2624220159449b292b0`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d799d17a45ee9b9c740f1c29d16dc8f38cf9896646171a2e11091a0c35f0abe`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a118992089f0da676390ceda6841fa8daa325e605167851d1f622311a1a5`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef5de6df9be951588bee6cc08178c55646c714a695418724c3da142911f10c`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 362.3 KB (362301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094ada08a213f863107606b70e3d03d1fd0c85c6f4041c794671a63ba9e32410`  
		Last Modified: Wed, 08 Jan 2025 23:32:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
