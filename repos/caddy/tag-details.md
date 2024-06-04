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
-	[`caddy:2.8`](#caddy28)
-	[`caddy:2.8-alpine`](#caddy28-alpine)
-	[`caddy:2.8-builder`](#caddy28-builder)
-	[`caddy:2.8-builder-alpine`](#caddy28-builder-alpine)
-	[`caddy:2.8-builder-windowsservercore-1809`](#caddy28-builder-windowsservercore-1809)
-	[`caddy:2.8-builder-windowsservercore-ltsc2022`](#caddy28-builder-windowsservercore-ltsc2022)
-	[`caddy:2.8-windowsservercore`](#caddy28-windowsservercore)
-	[`caddy:2.8-windowsservercore-1809`](#caddy28-windowsservercore-1809)
-	[`caddy:2.8-windowsservercore-ltsc2022`](#caddy28-windowsservercore-ltsc2022)
-	[`caddy:2.8.4`](#caddy284)
-	[`caddy:2.8.4-alpine`](#caddy284-alpine)
-	[`caddy:2.8.4-builder`](#caddy284-builder)
-	[`caddy:2.8.4-builder-alpine`](#caddy284-builder-alpine)
-	[`caddy:2.8.4-builder-windowsservercore-1809`](#caddy284-builder-windowsservercore-1809)
-	[`caddy:2.8.4-builder-windowsservercore-ltsc2022`](#caddy284-builder-windowsservercore-ltsc2022)
-	[`caddy:2.8.4-windowsservercore`](#caddy284-windowsservercore)
-	[`caddy:2.8.4-windowsservercore-1809`](#caddy284-windowsservercore-1809)
-	[`caddy:2.8.4-windowsservercore-ltsc2022`](#caddy284-windowsservercore-ltsc2022)
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
$ docker pull caddy@sha256:f848613a14e81ddf87d67c67f3b011be5849068fd2cc8ab8d1c421b153f74fcc
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
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:c092823e9774ccbc7a761d4fd45d49332cc050a4ed13e209c0752fbe77408cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18625893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379e9d34447ebff04422e00130985b166b7fc9cef98876e70d97e6d83269c215`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ecfa782506bda1924ea74bea4182d74f0557cebbf18a71fd48fe97fc6c59c8`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 357.4 KB (357381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94997ff2e374d1bfa99bd1f1a8e8f43cf6e148f63f8e9fe26265ae3d10ca8c9f`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08df330a016638626ff383f490ecf44b254e9ddbae0b4129c2b18c456201e5e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:56 GMT  
		Size: 14.6 MB (14638937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:041cc73927bb91ca88f8e88d7176aa520def52fca3402b730194a040a57b7a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eadb390bbfcd1f11cb6e7d8a95f43d2c71a613fc1e0f23a122e9bf12f4767b`

```dockerfile
```

-	Layers:
	-	`sha256:2f1d323a5412e4d8283ffbbf553b6c8317cfcd3199cff1626166d1fada238a5e`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 263.8 KB (263814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c05f7c8878252295ae4ac295bcdedbd14f7e95ed4ac7e789ad372763a182494`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:66473e2c9d4a1db0ae9bd459956d42d53e9991c58c900251753d648330f3f42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17496054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731a02bd06ee6a92070bf885f12f1dbbbbb736ec9db845b31b5fd8d0f9ec0c42`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30eae165a31e9dfba433ec2953fd144ad11b8b3b833ef35d2566b9fb75a56a`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 357.7 KB (357701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c943ab66970deade36497f4930fc57c4b3c8f30aba0bc7d118ec65b050da491`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb558a164f07a87610adfe7dab44e2f703cc5fd3e8c72f775b7706e2e2e5d3ea`  
		Last Modified: Mon, 03 Jun 2024 20:14:26 GMT  
		Size: 13.8 MB (13765815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:603f2ccec3669ac6a2749b7353e1bc949f166b4e3af650ce31d52b84be0a695d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c14dd01315a75e80a6d6459314782e218de761094d650564e70127e2639069a`

```dockerfile
```

-	Layers:
	-	`sha256:22cc7a81c0b1dd55893d0bd0bb7529a2d0ba81511a60787234b85f74f2bc367f`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d85c3fe08f25f0ff105839b738bc42d3cd0d4b3d804633ea99274c5aaf8838fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17195439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03a1673034f8209e77bd2c19e591b4feb4ebae6b72397a9f294cc1c84ce8983`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e694f733a431bd3ad4ee991d4dab8f760be8e7af16eacaf4bf3a47768fd799`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 354.1 KB (354065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975bb16f920c19614bb988818a5b0554e151e90bda59fa8681309d8b27c4ec89`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959163643e12b18c2516a3514743986aa91426069415a4bda6d18f8206ee9772`  
		Last Modified: Mon, 03 Jun 2024 21:48:35 GMT  
		Size: 13.7 MB (13739856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:7e9a460f5b40fa9161b5224a405302787d1cd40fd02b57e29ea38adf50273061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c0a5fe9e0133bc16645e387182bcbfbb594cd603582cfad20279c015a84854`

```dockerfile
```

-	Layers:
	-	`sha256:54e0c5426f56d92b29a5e46ccabe21ffe0344d4f8c2a851ed9d1776cf02307eb`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 263.9 KB (263882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0174d523126387bb17ee8b36c86137b0d32d7434536ff5438d297ce4fc56aaf`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bfbce093116fb3f94ffec6951d6cb067a22cda867b73854e4630954bc3548e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18015071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614062123a347849d270f9e29c9cb8647ae01e7b9463875be85bc1b6924e6bc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='866b6186626d4a7f35d5c010f3f532b022a35dd21f3512bd2015d6de39add0ccc0e8f778878a927ea4a5131ed1dfa8f114b1b9831eaa741f8aebc5c2d88747fd' ;; 		armhf)   binArch='armv6'; checksum='7cb786e8f1af7573ece485f2a9348c3ba7c6191346f5917075027f5cf5309fc0b8e3113e48092fc723d01171cd3c8bdfd076af17e69b1a6c1a9a0d5e53fdf1d2' ;; 		armv7)   binArch='armv7'; checksum='e1a7c02a0986d260ead1ffa9023e78bc1903139813ef5233a06d1f7d621f71ce37eb0042a991287256f85dae64924278514d183bcd805ef0329a096e4574dc06' ;; 		aarch64) binArch='arm64'; checksum='1a619b1ad15fc2163fa597a00b2c6174e6d00b8ce5206d18e0691edf9251ac8dcf1ebf059d7bd065a9ce0b3427071943dd2385d27fa78df0678cefea07280154' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c6d9b6a8db14b4a44de453023ae7b9d6f85b646dfb22a7e4bd5859556fb9cc42e1fb16b3ea5312a2b97bce4ab1f87a71daa430dc57cea09c0dea739409d5434f' ;; 		s390x)   binArch='s390x'; checksum='312ff46594f445d643acbc0d2f118c5af9419dd9e2ea1a8398a8a7772d172ec616d79f83eb4e3550efd26188c3fa1ddff1d9255bb3a55fe6b4384b0db818502a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_DATA_HOME=/data
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/udp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /srv
# Thu, 30 May 2024 14:50:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679b063c3cccee55ed2da27af5dca9a85a3447ab5ea8e8223f2399d695b9e9f`  
		Last Modified: Thu, 30 May 2024 14:41:43 GMT  
		Size: 369.2 KB (369156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3036766387a41a19917f6f36c51dc3d94c3c78b15ec4aa0703d5c7a3094789`  
		Last Modified: Thu, 30 May 2024 14:41:42 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553446b932e7710418d71ee0fa94d83a2d0b6d6de2c8033f103a6c4ee8ac8037`  
		Last Modified: Thu, 30 May 2024 22:40:07 GMT  
		Size: 13.6 MB (13551656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:f1ec6ba7f30a7039a101a631a18df1f1a91391309caa49bd0e9e7b95e335523f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 KB (281801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c841bc8bf71a85025aff6456ac07ef330aac19bfae66e33b7973eef4c031019`

```dockerfile
```

-	Layers:
	-	`sha256:58daa084cecd327bebce8ec82a37814b9bc513354002eeaa73370e4fa127cd02`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 263.9 KB (263919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7d58bbbff5474e240bb6c7ac3ee4866a0b9cd4a10541a9b2783a894127c0a8`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:3e6afc21f26a045b9cff8dded3a108350486ae0a14e809309a3b6fcbaf2ab44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17239755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dca62d441c172288e8c02545931a5a24e62efb67f3197ae3f98fce961d4ff89`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc90e19cccec8c93b7fc82b34313edb20031c9beb48eba2301ddeea45c3283c2`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 370.4 KB (370398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495869352c1369757545722b0b5a9bdb38f1e4128851a01a45d6a896324eb208`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6255e5da3daad8d4f46b62aad8f74352472eb69509d4a85ddabb97dd5776032a`  
		Last Modified: Tue, 04 Jun 2024 01:47:46 GMT  
		Size: 13.3 MB (13292030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:c76863ba66130346110cedfd2bd2346b62eccfdaad6b2d977209af4667f6e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022c234dffa5c4adf5045497989c7751c3e9b547b1a551497603480c7274dee0`

```dockerfile
```

-	Layers:
	-	`sha256:5e4ec7316421ca7d7aff7105fd8504943835e4121422cf9529f52ab819de1d56`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 261.9 KB (261918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64ee8324a31e6505d22eddd274754e4cc07367c231b3f4d616f9761409bd6266`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:5d61f08a2244fdd9670175600ad9e49611e5c5224f3b2b4ea2ce07ac56ab3a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17988811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa45066278353d53895c24f1f52b51c98e1463beb562cbbe8d777a691ef0d333`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9dcde94bf3f93b54ed692d25df606aadecebd0f28dd77d53b2c325c79116a9`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 364.9 KB (364869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129cdd4fd7c6eaafbd0d2ee17d753e1dc55f2b053dfe7eee597a638caec99dbf`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be0dc6e23084d8005f5b12d389c12d178b61dd29787c3eedee3a345071254b`  
		Last Modified: Mon, 03 Jun 2024 21:31:39 GMT  
		Size: 14.2 MB (14156119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:a71f8245a1fd40b0a5ede0f920e638a267abfedc83a33ef8f3e1f2b6ef63eb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643cd9393627b6ccbef5905e3848878f075de79071ab70ba90611cc1e8448a2d`

```dockerfile
```

-	Layers:
	-	`sha256:ac2552b9d22cc667e50951ca72233fe141aa9ba5177bfceaf4c6018693a777d0`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 261.9 KB (261860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ae05b2ef2b85ef54cad975979e33c0d69ebc0cb9ff24041f016c7f2ae25182`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:d92bc6499fe7029cf6bf56040d7ffc6584792daa76a39a09dd63228e3561e434
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

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:c092823e9774ccbc7a761d4fd45d49332cc050a4ed13e209c0752fbe77408cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18625893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379e9d34447ebff04422e00130985b166b7fc9cef98876e70d97e6d83269c215`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ecfa782506bda1924ea74bea4182d74f0557cebbf18a71fd48fe97fc6c59c8`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 357.4 KB (357381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94997ff2e374d1bfa99bd1f1a8e8f43cf6e148f63f8e9fe26265ae3d10ca8c9f`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08df330a016638626ff383f490ecf44b254e9ddbae0b4129c2b18c456201e5e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:56 GMT  
		Size: 14.6 MB (14638937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:041cc73927bb91ca88f8e88d7176aa520def52fca3402b730194a040a57b7a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eadb390bbfcd1f11cb6e7d8a95f43d2c71a613fc1e0f23a122e9bf12f4767b`

```dockerfile
```

-	Layers:
	-	`sha256:2f1d323a5412e4d8283ffbbf553b6c8317cfcd3199cff1626166d1fada238a5e`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 263.8 KB (263814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c05f7c8878252295ae4ac295bcdedbd14f7e95ed4ac7e789ad372763a182494`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:66473e2c9d4a1db0ae9bd459956d42d53e9991c58c900251753d648330f3f42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17496054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731a02bd06ee6a92070bf885f12f1dbbbbb736ec9db845b31b5fd8d0f9ec0c42`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30eae165a31e9dfba433ec2953fd144ad11b8b3b833ef35d2566b9fb75a56a`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 357.7 KB (357701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c943ab66970deade36497f4930fc57c4b3c8f30aba0bc7d118ec65b050da491`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb558a164f07a87610adfe7dab44e2f703cc5fd3e8c72f775b7706e2e2e5d3ea`  
		Last Modified: Mon, 03 Jun 2024 20:14:26 GMT  
		Size: 13.8 MB (13765815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:603f2ccec3669ac6a2749b7353e1bc949f166b4e3af650ce31d52b84be0a695d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c14dd01315a75e80a6d6459314782e218de761094d650564e70127e2639069a`

```dockerfile
```

-	Layers:
	-	`sha256:22cc7a81c0b1dd55893d0bd0bb7529a2d0ba81511a60787234b85f74f2bc367f`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d85c3fe08f25f0ff105839b738bc42d3cd0d4b3d804633ea99274c5aaf8838fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17195439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03a1673034f8209e77bd2c19e591b4feb4ebae6b72397a9f294cc1c84ce8983`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e694f733a431bd3ad4ee991d4dab8f760be8e7af16eacaf4bf3a47768fd799`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 354.1 KB (354065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975bb16f920c19614bb988818a5b0554e151e90bda59fa8681309d8b27c4ec89`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959163643e12b18c2516a3514743986aa91426069415a4bda6d18f8206ee9772`  
		Last Modified: Mon, 03 Jun 2024 21:48:35 GMT  
		Size: 13.7 MB (13739856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7e9a460f5b40fa9161b5224a405302787d1cd40fd02b57e29ea38adf50273061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c0a5fe9e0133bc16645e387182bcbfbb594cd603582cfad20279c015a84854`

```dockerfile
```

-	Layers:
	-	`sha256:54e0c5426f56d92b29a5e46ccabe21ffe0344d4f8c2a851ed9d1776cf02307eb`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 263.9 KB (263882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0174d523126387bb17ee8b36c86137b0d32d7434536ff5438d297ce4fc56aaf`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bfbce093116fb3f94ffec6951d6cb067a22cda867b73854e4630954bc3548e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18015071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614062123a347849d270f9e29c9cb8647ae01e7b9463875be85bc1b6924e6bc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='866b6186626d4a7f35d5c010f3f532b022a35dd21f3512bd2015d6de39add0ccc0e8f778878a927ea4a5131ed1dfa8f114b1b9831eaa741f8aebc5c2d88747fd' ;; 		armhf)   binArch='armv6'; checksum='7cb786e8f1af7573ece485f2a9348c3ba7c6191346f5917075027f5cf5309fc0b8e3113e48092fc723d01171cd3c8bdfd076af17e69b1a6c1a9a0d5e53fdf1d2' ;; 		armv7)   binArch='armv7'; checksum='e1a7c02a0986d260ead1ffa9023e78bc1903139813ef5233a06d1f7d621f71ce37eb0042a991287256f85dae64924278514d183bcd805ef0329a096e4574dc06' ;; 		aarch64) binArch='arm64'; checksum='1a619b1ad15fc2163fa597a00b2c6174e6d00b8ce5206d18e0691edf9251ac8dcf1ebf059d7bd065a9ce0b3427071943dd2385d27fa78df0678cefea07280154' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c6d9b6a8db14b4a44de453023ae7b9d6f85b646dfb22a7e4bd5859556fb9cc42e1fb16b3ea5312a2b97bce4ab1f87a71daa430dc57cea09c0dea739409d5434f' ;; 		s390x)   binArch='s390x'; checksum='312ff46594f445d643acbc0d2f118c5af9419dd9e2ea1a8398a8a7772d172ec616d79f83eb4e3550efd26188c3fa1ddff1d9255bb3a55fe6b4384b0db818502a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_DATA_HOME=/data
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/udp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /srv
# Thu, 30 May 2024 14:50:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679b063c3cccee55ed2da27af5dca9a85a3447ab5ea8e8223f2399d695b9e9f`  
		Last Modified: Thu, 30 May 2024 14:41:43 GMT  
		Size: 369.2 KB (369156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3036766387a41a19917f6f36c51dc3d94c3c78b15ec4aa0703d5c7a3094789`  
		Last Modified: Thu, 30 May 2024 14:41:42 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553446b932e7710418d71ee0fa94d83a2d0b6d6de2c8033f103a6c4ee8ac8037`  
		Last Modified: Thu, 30 May 2024 22:40:07 GMT  
		Size: 13.6 MB (13551656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f1ec6ba7f30a7039a101a631a18df1f1a91391309caa49bd0e9e7b95e335523f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 KB (281801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c841bc8bf71a85025aff6456ac07ef330aac19bfae66e33b7973eef4c031019`

```dockerfile
```

-	Layers:
	-	`sha256:58daa084cecd327bebce8ec82a37814b9bc513354002eeaa73370e4fa127cd02`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 263.9 KB (263919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7d58bbbff5474e240bb6c7ac3ee4866a0b9cd4a10541a9b2783a894127c0a8`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3e6afc21f26a045b9cff8dded3a108350486ae0a14e809309a3b6fcbaf2ab44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17239755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dca62d441c172288e8c02545931a5a24e62efb67f3197ae3f98fce961d4ff89`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc90e19cccec8c93b7fc82b34313edb20031c9beb48eba2301ddeea45c3283c2`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 370.4 KB (370398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495869352c1369757545722b0b5a9bdb38f1e4128851a01a45d6a896324eb208`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6255e5da3daad8d4f46b62aad8f74352472eb69509d4a85ddabb97dd5776032a`  
		Last Modified: Tue, 04 Jun 2024 01:47:46 GMT  
		Size: 13.3 MB (13292030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c76863ba66130346110cedfd2bd2346b62eccfdaad6b2d977209af4667f6e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022c234dffa5c4adf5045497989c7751c3e9b547b1a551497603480c7274dee0`

```dockerfile
```

-	Layers:
	-	`sha256:5e4ec7316421ca7d7aff7105fd8504943835e4121422cf9529f52ab819de1d56`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 261.9 KB (261918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64ee8324a31e6505d22eddd274754e4cc07367c231b3f4d616f9761409bd6266`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:5d61f08a2244fdd9670175600ad9e49611e5c5224f3b2b4ea2ce07ac56ab3a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17988811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa45066278353d53895c24f1f52b51c98e1463beb562cbbe8d777a691ef0d333`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9dcde94bf3f93b54ed692d25df606aadecebd0f28dd77d53b2c325c79116a9`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 364.9 KB (364869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129cdd4fd7c6eaafbd0d2ee17d753e1dc55f2b053dfe7eee597a638caec99dbf`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be0dc6e23084d8005f5b12d389c12d178b61dd29787c3eedee3a345071254b`  
		Last Modified: Mon, 03 Jun 2024 21:31:39 GMT  
		Size: 14.2 MB (14156119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a71f8245a1fd40b0a5ede0f920e638a267abfedc83a33ef8f3e1f2b6ef63eb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643cd9393627b6ccbef5905e3848878f075de79071ab70ba90611cc1e8448a2d`

```dockerfile
```

-	Layers:
	-	`sha256:ac2552b9d22cc667e50951ca72233fe141aa9ba5177bfceaf4c6018693a777d0`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 261.9 KB (261860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ae05b2ef2b85ef54cad975979e33c0d69ebc0cb9ff24041f016c7f2ae25182`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:3db37b69486800de84befa0dd692b4023beb435421703bbdb6f84a8055ddf011
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
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:df570c9c66505c887b2e78591181a8898bc1b8e25110e72ebbe1975b3fe89579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32f73a324a2d0e72a305f33619431bbfaba72840c70d6bec3f65f6e1cde8f6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46b7a5114a614bbc3afd1c49e40787c13c7c99cbc9af08e76fd9efa15e25b3f`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 5.9 MB (5914553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f6f6b1947c18c1bac715d995f46ce46727337a1ada0c4e7c2f2984a04aecb`  
		Last Modified: Mon, 03 Jun 2024 19:01:04 GMT  
		Size: 1.5 MB (1500680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806b02ef115ec1e534f2d36220b8eb1378cd4c1c96f410c53777e98f2f53a4cc`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:4da5f7d3f531e501a3ee5d389bc618d16c71bb86651fd68109d1f4981c3521d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986ce2397a27ef8d158052d579cb6a3b7b091330a59c01f105c3613c419d96ec`

```dockerfile
```

-	Layers:
	-	`sha256:3b2971fdad01a0613ef3e83c2cb8aab230ab0e62c4706ed98be8e9996b059dc4`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 275.7 KB (275708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cee59000fd2235e2e4bae2324c59b0c5d0288ad38996227843424658929c6c0`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:775a4428a3050de7079c89cff231c7ca54a01750ef752e8956584f4f8aaf76e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687f926297703c36c0b447b824401e090c54ddea35df95e9ac60b4ec2cfacab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199f8807ec47ac7592520ba82c877d9f6e6de8581f5f275abc56366dde16c1e`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 5.9 MB (5863451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7034939efcb080f679b56509133f9446262a4f442bf0c7394b454b1301f8791`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 1.4 MB (1423814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88cb6dc9c9687d4c1e64363a7e442ceab1456f49fb00aa819559ef0f0db699b`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3631380eaad063eb4441aeeb50616e75119a076efa5ee77af875aee22185549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5d75ee09562d929629215ec9ed12f6d436dcf52ad8986145bfa751437e09cc`

```dockerfile
```

-	Layers:
	-	`sha256:74ab8498bb88c256e9c05c7a0d99618dc4453b94584fb9c2c4dc360f08d6a47a`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:51fb29be03522856b8f507ea4df9ba1500972b756133c5bd35bddbca62d88ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d732f429c533cb427cdc7e7e044a83cfd84ced4da7224ac736da16d2c9dc43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444cd28ed296484ff90ddfb993c5cfce9deb7c7ee33a5fdf232fe5728d76ae7`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 292.5 KB (292462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d908fd62c89b1c0b846c14fa9daab8130baecf2d44514d246f96e1a89b6386d1`  
		Last Modified: Wed, 29 May 2024 01:38:47 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e444f239d275345fbcb28de09591b1ce21727483c1005dce419cc2136850fda`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f65578e4b162e83a0db7ae060959bda593a7d3f1774d5df8a3db0daefb184`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 5.4 MB (5351021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9ddad03f4d41f0e3d32a6b453c421c3c9d40d33ce4e2ac44f5ab0daff9a718`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 1.4 MB (1420766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f597d1755326223ce04f920c0eafbb47bf1630a3bc422c26b40698041417a49`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:63b2efa558ce0c277b21c332f0ac76eb069250f04c2bd6e22d86a6c04ca39e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a8dd5917ba43f4ca990fac2e0ce2eb472d317991a141f663eee67969cb8091`

```dockerfile
```

-	Layers:
	-	`sha256:d0f1adf29c41b7079e6776c969549d8fe63a0d2349f3f262e352780c396389b6`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 278.3 KB (278320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d8f39dc5b6142e254a1cfa5b6d44f9b0ee1b56653d76f5de94cff5466ad44a`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f0e70454943d37a64344820181d8396714d91d40ffd3a04844076a3b41d69a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78085757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb59a6bfcf30a2dfc3705ca6f25183cd395301a7a185380c978cea1117557ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SETCAP=1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 30 May 2024 14:50:16 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fd4d77c1150ba7c64d2b9cb1ad73058c134eea51cdf8a7c969379c3fe358c3`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6930e6242b08ff7992e85b10519d54167d7ffdedf7199e086b7c8be95e4baf6`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d49fbb06d2ec1fb8e7c2633794d12f435fe6098384a1ba28e82e7be07d06a38`  
		Last Modified: Thu, 30 May 2024 14:42:18 GMT  
		Size: 6.0 MB (6033730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31dd998a75477c407a2dee8c594a80ba41fdac4dd42d9d67a7c414c4c8997b9`  
		Last Modified: Thu, 30 May 2024 22:40:31 GMT  
		Size: 1.4 MB (1397169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770803ae5abd93eb1dcbc65ce6b1ccdfd01a538b7c537f05e868e88c81d9d430`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:acae0dfa758b68833a5e19bd4804c3a3916e795ee6dde565fc338a83efe0a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 KB (295844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de6d746bee70c9e18f38b0e19e943d1a7fcdb8b1b73856d337570218ce8c0bb`

```dockerfile
```

-	Layers:
	-	`sha256:1abefdba7275d0ce20e30a7257a2ed4eae90e1997c2acdafc5dae8ae0afccec3`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 275.8 KB (275813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5fee8e57abbb9909e5460f0b9e029723da0ba965f905c8d24ee042cab953b8`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:5bec9aca46cc2b81188b8dafd0415a432fefce0b94a93585e6866c635c05860e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98626dc8793adc0d9d1556e0d3019819e6c04c9ab5adc9ec2050ad07a27631b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7130843bbd3e7aec4f18d777d8486e1a31bc676e485de7fbd9674a170777d8e`  
		Last Modified: Tue, 28 May 2024 23:35:05 GMT  
		Size: 295.9 KB (295891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c97ae223460d35ee30ac67c808649bb863398f7373aeff23f0dd033662e29`  
		Last Modified: Tue, 28 May 2024 23:35:07 GMT  
		Size: 66.4 MB (66430055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8885cb230dbccfd815664d1c1a6f3bfa5328a48b9192145c2a16236fb973f8b3`  
		Last Modified: Tue, 28 May 2024 23:35:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434d6eb71e6463f36189c536f37f5e808afd8a2888e4cf6564148bb8e0d568fb`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 6.2 MB (6240121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152d73d2731afedc609d6f5911728ace83ce1c08e1dbcd5460e4cbd48f006d6`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 1.4 MB (1390031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3288aae2d128567448ca4a8038c23cd41eb09e6cc2046a729c45fbe9f88ff9e1`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e52ddd12fdb8d2940ec7abd3835bf37d4cb84f53dbbe0fbed3cbef7396129e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf175f54a787ed0ace3a3b04deef8d8eb90713125b37f236e50a036adfc185`

```dockerfile
```

-	Layers:
	-	`sha256:0d74303319f715f2000d3da32d63018ae9f0c705fa1499bb9372bb231e0bb45d`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 273.8 KB (273846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e85be5da6c5e14cd99bac3703afc52f78692560e39587f4b95b73ce6a5ea02`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:bbd371f55e5fd21330c24bcfd34a1a8702191867cceb0b340c3b21002c23a3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af99e1c137b5b73332bc84f34766ea766f1369cccc49d900bc35cd805ff0dfc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7fb356c901d4b14e02b6bca1b10852f4a9f85dc695ab3239d771383ee632a5`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 6.2 MB (6179567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62ccaf0be9fd4c408957b5068154bc456143c35dc8c818955199c1cc19412fd`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216b4bc58f3ca32cc60a50bb5a7f1d89bc4c869fcbcc8a3d79cfc455e3a829aa`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a0cd00361f284c2509ee135e57e9ba892603c9babba263a8c9a4019ec816f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea05560489e0436aeabee2b1d096e6ef1883871da7006a5f427be424a1588525`

```dockerfile
```

-	Layers:
	-	`sha256:7a0297889ae2bc64168bf10de6cb03222bf8a8d3915e6eb4e76077607f4f1dca`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 273.8 KB (273754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f562e536bfdd4352eb3a45746b1c36b9bcb4b47e266c037b4ef05073aa9771`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:0e6791b30064fce15067fec856819501eb37e90a3d63c8954f615b1bb9a50cd4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212210875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec756e07bb7339ed40f5aaa265ac85ae87f7cbe499cb07dcb30bae80fca70a5c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:58:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:58:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:58:45 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:58:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:58:58 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:59:04 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:59:05 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:00:17 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:18 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:02:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:48 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:02:49 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90a3c07c43efebd99803cdb9bad2d8149315d6fe71ed67ca3c907554d9e0d9`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d2da37d6aadb3a05b1b91cab3d0735e673ee46930e50eff76541ca6cd703c4`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998290d6ae9e03557ab29c99bdecd95a1646d0b2b6e01375977bc9ca92e7679f`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febc0e57a30d4aaef8d997796e999f07cd8d02fefada73c1d9a8d3b2efb2d0a5`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9634b04a70d192ce4d61fc9cacd9dfe77dc2ce74925adb17ec44604eae27767e`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d148249d3a6d5d5e8a6682e3d3c7577ec3e6c4db642ff5a298431e2aa6015a`  
		Last Modified: Wed, 15 May 2024 22:00:24 GMT  
		Size: 25.4 MB (25444377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abaff09d8cdfae3edceb6c5711ad840eb5f47c5bc4b76b2e6b4da440009de54`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302450cd0c74f7f8c4e0ef1ddc17b877078794558e3bc9ea20be56798e14f0b1`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 345.6 KB (345575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5856fa608f5aaadb2aa345cb0e4e8b4727bc567c776a2ca50b9b9b2ae049ca71`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b86ddf0d69a3769b0f5587cfee9e1dee2b6c0de79f2c6b192fc06caac1639`  
		Last Modified: Wed, 15 May 2024 22:00:32 GMT  
		Size: 71.8 MB (71755992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f91b25b9e6cb7c3077ad2c0725b9b9f62ce4feb0a96fd7c1a075d356fe1b1`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5f7203aa8356980751a8d0d837f026ab70683bb5d98c69c30ec9dfbdd96909`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a29c49e69b7ad65d25803b5ede17ea3a9a1de029f8ed9efba96ae8d8a6ee647`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980757db2f634cea769d2bbf611fabaefc8ef068bf3449adfb4aab3dfc8d82d`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b729eaf00df1c3145830dc1c7b99c931760b57c4ac1cb3c7e089c2daec1b5f40`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b29deaba4982d0ebc1399cdd05eb16d24ab4aeb0b856a15f355845ceb3a2d07`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 2.0 MB (1976480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2eb9ded10797df67ff42377be07f21c463ee93afda3ef414f90864dde3bf2`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:7ec8bed26a5de8b4d209ef792271790786a9034467431218920c382cfbbb6fab
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a48743c09fc4e5f8c297ca67457a44f3de2a7521f27fe42b0bab9e46883c203`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 22:51:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:51:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:51:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:54:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:54:20 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:54:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:54:45 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:58:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:58:59 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:03:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:03:12 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:03:13 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:04:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:04:42 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b721870b6ca4ac86a4dd17a9efa72d3bbbc3e2f4db24604ab3e5529ac9483`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231059aab43e3c4c95c41ffa0eaaf0a505c5a3e17b120dfc894682b1930a3968`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83508e294490f2fa915d9cd65227cc8e8661207b15aa2cfdaf074ff8ae7bb4d4`  
		Last Modified: Wed, 15 May 2024 22:59:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d676bfa2282c568dda9fa4af2f2e6d235ebca82a6c367717bf083bad7dd8b3a`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3161f170f396d7c78bb77ee80c5b634beca05d901f05396abeab4e06be7f5`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c76d7a1b3a9e63480abdc848b1fd30a006301a1e471568b571a209702755daa`  
		Last Modified: Wed, 15 May 2024 22:59:07 GMT  
		Size: 25.6 MB (25574881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dcf82dafd8633a79265dca42870493640409651674a91b43f2adf04c165a`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dac5092add95bf42e98f932737023e0c6ef6ca428f58802291c2cc4c9559b7`  
		Last Modified: Wed, 15 May 2024 22:59:03 GMT  
		Size: 345.9 KB (345903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7992418d5500de5ceeac2fa4f57b54353f18a13b476f19add206e269ef1e6fc`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad77f522384c92c66907f62599064a34ebdd67556de4d2570970de37d46d8`  
		Last Modified: Wed, 15 May 2024 22:59:13 GMT  
		Size: 71.7 MB (71743817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716ef2ea189a02632506ad12bdad7990790c5792d611ac5831fdfa2896ac298`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0238b1a68b5dc8e13a99e71e8c0013bd2b7dfaf127ce1af2e7b6f0b8d52f3`  
		Last Modified: Mon, 03 Jun 2024 19:04:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5109dfca4e11a4fc1d216988f7afe6fa800a6dcef66617d88c19636ab6e50cb7`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081c9df7b06e5088479a8f522501c4643b3179a9b34e5a83fc27ed9d4e5fe539`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b6cca533939895b90c344b768eaf02c53ac76b0a4c97a456d440aba3a8b571`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b805480f52756d99d47ee659a1b21cd0f116bb7fbc8a883a407689bd131635b`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 2.0 MB (1951462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be79ded6647b5f2dfe026d26fc2a855941e795f364266d2bf246cc5c8dc56a`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:1bb8f3d134ec8113c17d4ea0e073e94944f4bce8c7429055f2fa6168e36ab96b
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

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:df570c9c66505c887b2e78591181a8898bc1b8e25110e72ebbe1975b3fe89579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32f73a324a2d0e72a305f33619431bbfaba72840c70d6bec3f65f6e1cde8f6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46b7a5114a614bbc3afd1c49e40787c13c7c99cbc9af08e76fd9efa15e25b3f`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 5.9 MB (5914553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f6f6b1947c18c1bac715d995f46ce46727337a1ada0c4e7c2f2984a04aecb`  
		Last Modified: Mon, 03 Jun 2024 19:01:04 GMT  
		Size: 1.5 MB (1500680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806b02ef115ec1e534f2d36220b8eb1378cd4c1c96f410c53777e98f2f53a4cc`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4da5f7d3f531e501a3ee5d389bc618d16c71bb86651fd68109d1f4981c3521d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986ce2397a27ef8d158052d579cb6a3b7b091330a59c01f105c3613c419d96ec`

```dockerfile
```

-	Layers:
	-	`sha256:3b2971fdad01a0613ef3e83c2cb8aab230ab0e62c4706ed98be8e9996b059dc4`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 275.7 KB (275708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cee59000fd2235e2e4bae2324c59b0c5d0288ad38996227843424658929c6c0`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:775a4428a3050de7079c89cff231c7ca54a01750ef752e8956584f4f8aaf76e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687f926297703c36c0b447b824401e090c54ddea35df95e9ac60b4ec2cfacab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199f8807ec47ac7592520ba82c877d9f6e6de8581f5f275abc56366dde16c1e`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 5.9 MB (5863451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7034939efcb080f679b56509133f9446262a4f442bf0c7394b454b1301f8791`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 1.4 MB (1423814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88cb6dc9c9687d4c1e64363a7e442ceab1456f49fb00aa819559ef0f0db699b`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3631380eaad063eb4441aeeb50616e75119a076efa5ee77af875aee22185549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5d75ee09562d929629215ec9ed12f6d436dcf52ad8986145bfa751437e09cc`

```dockerfile
```

-	Layers:
	-	`sha256:74ab8498bb88c256e9c05c7a0d99618dc4453b94584fb9c2c4dc360f08d6a47a`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:51fb29be03522856b8f507ea4df9ba1500972b756133c5bd35bddbca62d88ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d732f429c533cb427cdc7e7e044a83cfd84ced4da7224ac736da16d2c9dc43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444cd28ed296484ff90ddfb993c5cfce9deb7c7ee33a5fdf232fe5728d76ae7`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 292.5 KB (292462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d908fd62c89b1c0b846c14fa9daab8130baecf2d44514d246f96e1a89b6386d1`  
		Last Modified: Wed, 29 May 2024 01:38:47 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e444f239d275345fbcb28de09591b1ce21727483c1005dce419cc2136850fda`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f65578e4b162e83a0db7ae060959bda593a7d3f1774d5df8a3db0daefb184`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 5.4 MB (5351021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9ddad03f4d41f0e3d32a6b453c421c3c9d40d33ce4e2ac44f5ab0daff9a718`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 1.4 MB (1420766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f597d1755326223ce04f920c0eafbb47bf1630a3bc422c26b40698041417a49`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:63b2efa558ce0c277b21c332f0ac76eb069250f04c2bd6e22d86a6c04ca39e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a8dd5917ba43f4ca990fac2e0ce2eb472d317991a141f663eee67969cb8091`

```dockerfile
```

-	Layers:
	-	`sha256:d0f1adf29c41b7079e6776c969549d8fe63a0d2349f3f262e352780c396389b6`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 278.3 KB (278320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d8f39dc5b6142e254a1cfa5b6d44f9b0ee1b56653d76f5de94cff5466ad44a`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f0e70454943d37a64344820181d8396714d91d40ffd3a04844076a3b41d69a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78085757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb59a6bfcf30a2dfc3705ca6f25183cd395301a7a185380c978cea1117557ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SETCAP=1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 30 May 2024 14:50:16 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fd4d77c1150ba7c64d2b9cb1ad73058c134eea51cdf8a7c969379c3fe358c3`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6930e6242b08ff7992e85b10519d54167d7ffdedf7199e086b7c8be95e4baf6`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d49fbb06d2ec1fb8e7c2633794d12f435fe6098384a1ba28e82e7be07d06a38`  
		Last Modified: Thu, 30 May 2024 14:42:18 GMT  
		Size: 6.0 MB (6033730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31dd998a75477c407a2dee8c594a80ba41fdac4dd42d9d67a7c414c4c8997b9`  
		Last Modified: Thu, 30 May 2024 22:40:31 GMT  
		Size: 1.4 MB (1397169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770803ae5abd93eb1dcbc65ce6b1ccdfd01a538b7c537f05e868e88c81d9d430`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:acae0dfa758b68833a5e19bd4804c3a3916e795ee6dde565fc338a83efe0a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 KB (295844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de6d746bee70c9e18f38b0e19e943d1a7fcdb8b1b73856d337570218ce8c0bb`

```dockerfile
```

-	Layers:
	-	`sha256:1abefdba7275d0ce20e30a7257a2ed4eae90e1997c2acdafc5dae8ae0afccec3`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 275.8 KB (275813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5fee8e57abbb9909e5460f0b9e029723da0ba965f905c8d24ee042cab953b8`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:5bec9aca46cc2b81188b8dafd0415a432fefce0b94a93585e6866c635c05860e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98626dc8793adc0d9d1556e0d3019819e6c04c9ab5adc9ec2050ad07a27631b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7130843bbd3e7aec4f18d777d8486e1a31bc676e485de7fbd9674a170777d8e`  
		Last Modified: Tue, 28 May 2024 23:35:05 GMT  
		Size: 295.9 KB (295891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c97ae223460d35ee30ac67c808649bb863398f7373aeff23f0dd033662e29`  
		Last Modified: Tue, 28 May 2024 23:35:07 GMT  
		Size: 66.4 MB (66430055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8885cb230dbccfd815664d1c1a6f3bfa5328a48b9192145c2a16236fb973f8b3`  
		Last Modified: Tue, 28 May 2024 23:35:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434d6eb71e6463f36189c536f37f5e808afd8a2888e4cf6564148bb8e0d568fb`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 6.2 MB (6240121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152d73d2731afedc609d6f5911728ace83ce1c08e1dbcd5460e4cbd48f006d6`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 1.4 MB (1390031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3288aae2d128567448ca4a8038c23cd41eb09e6cc2046a729c45fbe9f88ff9e1`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e52ddd12fdb8d2940ec7abd3835bf37d4cb84f53dbbe0fbed3cbef7396129e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf175f54a787ed0ace3a3b04deef8d8eb90713125b37f236e50a036adfc185`

```dockerfile
```

-	Layers:
	-	`sha256:0d74303319f715f2000d3da32d63018ae9f0c705fa1499bb9372bb231e0bb45d`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 273.8 KB (273846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e85be5da6c5e14cd99bac3703afc52f78692560e39587f4b95b73ce6a5ea02`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bbd371f55e5fd21330c24bcfd34a1a8702191867cceb0b340c3b21002c23a3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af99e1c137b5b73332bc84f34766ea766f1369cccc49d900bc35cd805ff0dfc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7fb356c901d4b14e02b6bca1b10852f4a9f85dc695ab3239d771383ee632a5`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 6.2 MB (6179567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62ccaf0be9fd4c408957b5068154bc456143c35dc8c818955199c1cc19412fd`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216b4bc58f3ca32cc60a50bb5a7f1d89bc4c869fcbcc8a3d79cfc455e3a829aa`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a0cd00361f284c2509ee135e57e9ba892603c9babba263a8c9a4019ec816f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea05560489e0436aeabee2b1d096e6ef1883871da7006a5f427be424a1588525`

```dockerfile
```

-	Layers:
	-	`sha256:7a0297889ae2bc64168bf10de6cb03222bf8a8d3915e6eb4e76077607f4f1dca`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 273.8 KB (273754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f562e536bfdd4352eb3a45746b1c36b9bcb4b47e266c037b4ef05073aa9771`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:dcee0b1539d2763646c0ab649486962e588b05ca78d46bf87c7bc0a2d2f39d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:7ec8bed26a5de8b4d209ef792271790786a9034467431218920c382cfbbb6fab
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a48743c09fc4e5f8c297ca67457a44f3de2a7521f27fe42b0bab9e46883c203`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 22:51:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:51:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:51:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:54:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:54:20 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:54:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:54:45 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:58:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:58:59 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:03:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:03:12 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:03:13 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:04:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:04:42 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b721870b6ca4ac86a4dd17a9efa72d3bbbc3e2f4db24604ab3e5529ac9483`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231059aab43e3c4c95c41ffa0eaaf0a505c5a3e17b120dfc894682b1930a3968`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83508e294490f2fa915d9cd65227cc8e8661207b15aa2cfdaf074ff8ae7bb4d4`  
		Last Modified: Wed, 15 May 2024 22:59:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d676bfa2282c568dda9fa4af2f2e6d235ebca82a6c367717bf083bad7dd8b3a`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3161f170f396d7c78bb77ee80c5b634beca05d901f05396abeab4e06be7f5`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c76d7a1b3a9e63480abdc848b1fd30a006301a1e471568b571a209702755daa`  
		Last Modified: Wed, 15 May 2024 22:59:07 GMT  
		Size: 25.6 MB (25574881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dcf82dafd8633a79265dca42870493640409651674a91b43f2adf04c165a`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dac5092add95bf42e98f932737023e0c6ef6ca428f58802291c2cc4c9559b7`  
		Last Modified: Wed, 15 May 2024 22:59:03 GMT  
		Size: 345.9 KB (345903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7992418d5500de5ceeac2fa4f57b54353f18a13b476f19add206e269ef1e6fc`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad77f522384c92c66907f62599064a34ebdd67556de4d2570970de37d46d8`  
		Last Modified: Wed, 15 May 2024 22:59:13 GMT  
		Size: 71.7 MB (71743817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716ef2ea189a02632506ad12bdad7990790c5792d611ac5831fdfa2896ac298`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0238b1a68b5dc8e13a99e71e8c0013bd2b7dfaf127ce1af2e7b6f0b8d52f3`  
		Last Modified: Mon, 03 Jun 2024 19:04:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5109dfca4e11a4fc1d216988f7afe6fa800a6dcef66617d88c19636ab6e50cb7`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081c9df7b06e5088479a8f522501c4643b3179a9b34e5a83fc27ed9d4e5fe539`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b6cca533939895b90c344b768eaf02c53ac76b0a4c97a456d440aba3a8b571`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b805480f52756d99d47ee659a1b21cd0f116bb7fbc8a883a407689bd131635b`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 2.0 MB (1951462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be79ded6647b5f2dfe026d26fc2a855941e795f364266d2bf246cc5c8dc56a`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:59f3fab8e735fb586ed740691880ee298cf3caae458593effaf99bdacceaa0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:0e6791b30064fce15067fec856819501eb37e90a3d63c8954f615b1bb9a50cd4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212210875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec756e07bb7339ed40f5aaa265ac85ae87f7cbe499cb07dcb30bae80fca70a5c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:58:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:58:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:58:45 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:58:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:58:58 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:59:04 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:59:05 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:00:17 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:18 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:02:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:48 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:02:49 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90a3c07c43efebd99803cdb9bad2d8149315d6fe71ed67ca3c907554d9e0d9`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d2da37d6aadb3a05b1b91cab3d0735e673ee46930e50eff76541ca6cd703c4`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998290d6ae9e03557ab29c99bdecd95a1646d0b2b6e01375977bc9ca92e7679f`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febc0e57a30d4aaef8d997796e999f07cd8d02fefada73c1d9a8d3b2efb2d0a5`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9634b04a70d192ce4d61fc9cacd9dfe77dc2ce74925adb17ec44604eae27767e`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d148249d3a6d5d5e8a6682e3d3c7577ec3e6c4db642ff5a298431e2aa6015a`  
		Last Modified: Wed, 15 May 2024 22:00:24 GMT  
		Size: 25.4 MB (25444377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abaff09d8cdfae3edceb6c5711ad840eb5f47c5bc4b76b2e6b4da440009de54`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302450cd0c74f7f8c4e0ef1ddc17b877078794558e3bc9ea20be56798e14f0b1`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 345.6 KB (345575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5856fa608f5aaadb2aa345cb0e4e8b4727bc567c776a2ca50b9b9b2ae049ca71`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b86ddf0d69a3769b0f5587cfee9e1dee2b6c0de79f2c6b192fc06caac1639`  
		Last Modified: Wed, 15 May 2024 22:00:32 GMT  
		Size: 71.8 MB (71755992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f91b25b9e6cb7c3077ad2c0725b9b9f62ce4feb0a96fd7c1a075d356fe1b1`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5f7203aa8356980751a8d0d837f026ab70683bb5d98c69c30ec9dfbdd96909`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a29c49e69b7ad65d25803b5ede17ea3a9a1de029f8ed9efba96ae8d8a6ee647`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980757db2f634cea769d2bbf611fabaefc8ef068bf3449adfb4aab3dfc8d82d`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b729eaf00df1c3145830dc1c7b99c931760b57c4ac1cb3c7e089c2daec1b5f40`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b29deaba4982d0ebc1399cdd05eb16d24ab4aeb0b856a15f355845ceb3a2d07`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 2.0 MB (1976480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2eb9ded10797df67ff42377be07f21c463ee93afda3ef414f90864dde3bf2`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:a0b338adc338b131f1b4811bd7f95964e764e483c22ab46c1ba97947e90beced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:dbab4057e60d72545d940471196dda51a1c0cbb62ec6fec4bd62a6c6110be70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:298ce474adcb68acbbf7d561e3182062bc7c263ef39cfac2632da7d9841bf435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8`

```console
$ docker pull caddy@sha256:f848613a14e81ddf87d67c67f3b011be5849068fd2cc8ab8d1c421b153f74fcc
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
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8` - linux; amd64

```console
$ docker pull caddy@sha256:c092823e9774ccbc7a761d4fd45d49332cc050a4ed13e209c0752fbe77408cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18625893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379e9d34447ebff04422e00130985b166b7fc9cef98876e70d97e6d83269c215`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ecfa782506bda1924ea74bea4182d74f0557cebbf18a71fd48fe97fc6c59c8`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 357.4 KB (357381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94997ff2e374d1bfa99bd1f1a8e8f43cf6e148f63f8e9fe26265ae3d10ca8c9f`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08df330a016638626ff383f490ecf44b254e9ddbae0b4129c2b18c456201e5e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:56 GMT  
		Size: 14.6 MB (14638937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:041cc73927bb91ca88f8e88d7176aa520def52fca3402b730194a040a57b7a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eadb390bbfcd1f11cb6e7d8a95f43d2c71a613fc1e0f23a122e9bf12f4767b`

```dockerfile
```

-	Layers:
	-	`sha256:2f1d323a5412e4d8283ffbbf553b6c8317cfcd3199cff1626166d1fada238a5e`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 263.8 KB (263814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c05f7c8878252295ae4ac295bcdedbd14f7e95ed4ac7e789ad372763a182494`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; arm variant v6

```console
$ docker pull caddy@sha256:66473e2c9d4a1db0ae9bd459956d42d53e9991c58c900251753d648330f3f42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17496054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731a02bd06ee6a92070bf885f12f1dbbbbb736ec9db845b31b5fd8d0f9ec0c42`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30eae165a31e9dfba433ec2953fd144ad11b8b3b833ef35d2566b9fb75a56a`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 357.7 KB (357701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c943ab66970deade36497f4930fc57c4b3c8f30aba0bc7d118ec65b050da491`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb558a164f07a87610adfe7dab44e2f703cc5fd3e8c72f775b7706e2e2e5d3ea`  
		Last Modified: Mon, 03 Jun 2024 20:14:26 GMT  
		Size: 13.8 MB (13765815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:603f2ccec3669ac6a2749b7353e1bc949f166b4e3af650ce31d52b84be0a695d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c14dd01315a75e80a6d6459314782e218de761094d650564e70127e2639069a`

```dockerfile
```

-	Layers:
	-	`sha256:22cc7a81c0b1dd55893d0bd0bb7529a2d0ba81511a60787234b85f74f2bc367f`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d85c3fe08f25f0ff105839b738bc42d3cd0d4b3d804633ea99274c5aaf8838fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17195439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03a1673034f8209e77bd2c19e591b4feb4ebae6b72397a9f294cc1c84ce8983`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e694f733a431bd3ad4ee991d4dab8f760be8e7af16eacaf4bf3a47768fd799`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 354.1 KB (354065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975bb16f920c19614bb988818a5b0554e151e90bda59fa8681309d8b27c4ec89`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959163643e12b18c2516a3514743986aa91426069415a4bda6d18f8206ee9772`  
		Last Modified: Mon, 03 Jun 2024 21:48:35 GMT  
		Size: 13.7 MB (13739856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:7e9a460f5b40fa9161b5224a405302787d1cd40fd02b57e29ea38adf50273061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c0a5fe9e0133bc16645e387182bcbfbb594cd603582cfad20279c015a84854`

```dockerfile
```

-	Layers:
	-	`sha256:54e0c5426f56d92b29a5e46ccabe21ffe0344d4f8c2a851ed9d1776cf02307eb`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 263.9 KB (263882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0174d523126387bb17ee8b36c86137b0d32d7434536ff5438d297ce4fc56aaf`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bfbce093116fb3f94ffec6951d6cb067a22cda867b73854e4630954bc3548e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18015071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614062123a347849d270f9e29c9cb8647ae01e7b9463875be85bc1b6924e6bc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='866b6186626d4a7f35d5c010f3f532b022a35dd21f3512bd2015d6de39add0ccc0e8f778878a927ea4a5131ed1dfa8f114b1b9831eaa741f8aebc5c2d88747fd' ;; 		armhf)   binArch='armv6'; checksum='7cb786e8f1af7573ece485f2a9348c3ba7c6191346f5917075027f5cf5309fc0b8e3113e48092fc723d01171cd3c8bdfd076af17e69b1a6c1a9a0d5e53fdf1d2' ;; 		armv7)   binArch='armv7'; checksum='e1a7c02a0986d260ead1ffa9023e78bc1903139813ef5233a06d1f7d621f71ce37eb0042a991287256f85dae64924278514d183bcd805ef0329a096e4574dc06' ;; 		aarch64) binArch='arm64'; checksum='1a619b1ad15fc2163fa597a00b2c6174e6d00b8ce5206d18e0691edf9251ac8dcf1ebf059d7bd065a9ce0b3427071943dd2385d27fa78df0678cefea07280154' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c6d9b6a8db14b4a44de453023ae7b9d6f85b646dfb22a7e4bd5859556fb9cc42e1fb16b3ea5312a2b97bce4ab1f87a71daa430dc57cea09c0dea739409d5434f' ;; 		s390x)   binArch='s390x'; checksum='312ff46594f445d643acbc0d2f118c5af9419dd9e2ea1a8398a8a7772d172ec616d79f83eb4e3550efd26188c3fa1ddff1d9255bb3a55fe6b4384b0db818502a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_DATA_HOME=/data
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/udp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /srv
# Thu, 30 May 2024 14:50:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679b063c3cccee55ed2da27af5dca9a85a3447ab5ea8e8223f2399d695b9e9f`  
		Last Modified: Thu, 30 May 2024 14:41:43 GMT  
		Size: 369.2 KB (369156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3036766387a41a19917f6f36c51dc3d94c3c78b15ec4aa0703d5c7a3094789`  
		Last Modified: Thu, 30 May 2024 14:41:42 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553446b932e7710418d71ee0fa94d83a2d0b6d6de2c8033f103a6c4ee8ac8037`  
		Last Modified: Thu, 30 May 2024 22:40:07 GMT  
		Size: 13.6 MB (13551656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:f1ec6ba7f30a7039a101a631a18df1f1a91391309caa49bd0e9e7b95e335523f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 KB (281801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c841bc8bf71a85025aff6456ac07ef330aac19bfae66e33b7973eef4c031019`

```dockerfile
```

-	Layers:
	-	`sha256:58daa084cecd327bebce8ec82a37814b9bc513354002eeaa73370e4fa127cd02`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 263.9 KB (263919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7d58bbbff5474e240bb6c7ac3ee4866a0b9cd4a10541a9b2783a894127c0a8`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; ppc64le

```console
$ docker pull caddy@sha256:3e6afc21f26a045b9cff8dded3a108350486ae0a14e809309a3b6fcbaf2ab44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17239755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dca62d441c172288e8c02545931a5a24e62efb67f3197ae3f98fce961d4ff89`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc90e19cccec8c93b7fc82b34313edb20031c9beb48eba2301ddeea45c3283c2`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 370.4 KB (370398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495869352c1369757545722b0b5a9bdb38f1e4128851a01a45d6a896324eb208`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6255e5da3daad8d4f46b62aad8f74352472eb69509d4a85ddabb97dd5776032a`  
		Last Modified: Tue, 04 Jun 2024 01:47:46 GMT  
		Size: 13.3 MB (13292030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:c76863ba66130346110cedfd2bd2346b62eccfdaad6b2d977209af4667f6e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022c234dffa5c4adf5045497989c7751c3e9b547b1a551497603480c7274dee0`

```dockerfile
```

-	Layers:
	-	`sha256:5e4ec7316421ca7d7aff7105fd8504943835e4121422cf9529f52ab819de1d56`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 261.9 KB (261918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64ee8324a31e6505d22eddd274754e4cc07367c231b3f4d616f9761409bd6266`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; s390x

```console
$ docker pull caddy@sha256:5d61f08a2244fdd9670175600ad9e49611e5c5224f3b2b4ea2ce07ac56ab3a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17988811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa45066278353d53895c24f1f52b51c98e1463beb562cbbe8d777a691ef0d333`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9dcde94bf3f93b54ed692d25df606aadecebd0f28dd77d53b2c325c79116a9`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 364.9 KB (364869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129cdd4fd7c6eaafbd0d2ee17d753e1dc55f2b053dfe7eee597a638caec99dbf`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be0dc6e23084d8005f5b12d389c12d178b61dd29787c3eedee3a345071254b`  
		Last Modified: Mon, 03 Jun 2024 21:31:39 GMT  
		Size: 14.2 MB (14156119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:a71f8245a1fd40b0a5ede0f920e638a267abfedc83a33ef8f3e1f2b6ef63eb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643cd9393627b6ccbef5905e3848878f075de79071ab70ba90611cc1e8448a2d`

```dockerfile
```

-	Layers:
	-	`sha256:ac2552b9d22cc667e50951ca72233fe141aa9ba5177bfceaf4c6018693a777d0`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 261.9 KB (261860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ae05b2ef2b85ef54cad975979e33c0d69ebc0cb9ff24041f016c7f2ae25182`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-alpine`

```console
$ docker pull caddy@sha256:d92bc6499fe7029cf6bf56040d7ffc6584792daa76a39a09dd63228e3561e434
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

### `caddy:2.8-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:c092823e9774ccbc7a761d4fd45d49332cc050a4ed13e209c0752fbe77408cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18625893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379e9d34447ebff04422e00130985b166b7fc9cef98876e70d97e6d83269c215`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ecfa782506bda1924ea74bea4182d74f0557cebbf18a71fd48fe97fc6c59c8`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 357.4 KB (357381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94997ff2e374d1bfa99bd1f1a8e8f43cf6e148f63f8e9fe26265ae3d10ca8c9f`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08df330a016638626ff383f490ecf44b254e9ddbae0b4129c2b18c456201e5e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:56 GMT  
		Size: 14.6 MB (14638937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:041cc73927bb91ca88f8e88d7176aa520def52fca3402b730194a040a57b7a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eadb390bbfcd1f11cb6e7d8a95f43d2c71a613fc1e0f23a122e9bf12f4767b`

```dockerfile
```

-	Layers:
	-	`sha256:2f1d323a5412e4d8283ffbbf553b6c8317cfcd3199cff1626166d1fada238a5e`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 263.8 KB (263814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c05f7c8878252295ae4ac295bcdedbd14f7e95ed4ac7e789ad372763a182494`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:66473e2c9d4a1db0ae9bd459956d42d53e9991c58c900251753d648330f3f42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17496054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731a02bd06ee6a92070bf885f12f1dbbbbb736ec9db845b31b5fd8d0f9ec0c42`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30eae165a31e9dfba433ec2953fd144ad11b8b3b833ef35d2566b9fb75a56a`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 357.7 KB (357701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c943ab66970deade36497f4930fc57c4b3c8f30aba0bc7d118ec65b050da491`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb558a164f07a87610adfe7dab44e2f703cc5fd3e8c72f775b7706e2e2e5d3ea`  
		Last Modified: Mon, 03 Jun 2024 20:14:26 GMT  
		Size: 13.8 MB (13765815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:603f2ccec3669ac6a2749b7353e1bc949f166b4e3af650ce31d52b84be0a695d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c14dd01315a75e80a6d6459314782e218de761094d650564e70127e2639069a`

```dockerfile
```

-	Layers:
	-	`sha256:22cc7a81c0b1dd55893d0bd0bb7529a2d0ba81511a60787234b85f74f2bc367f`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d85c3fe08f25f0ff105839b738bc42d3cd0d4b3d804633ea99274c5aaf8838fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17195439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03a1673034f8209e77bd2c19e591b4feb4ebae6b72397a9f294cc1c84ce8983`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e694f733a431bd3ad4ee991d4dab8f760be8e7af16eacaf4bf3a47768fd799`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 354.1 KB (354065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975bb16f920c19614bb988818a5b0554e151e90bda59fa8681309d8b27c4ec89`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959163643e12b18c2516a3514743986aa91426069415a4bda6d18f8206ee9772`  
		Last Modified: Mon, 03 Jun 2024 21:48:35 GMT  
		Size: 13.7 MB (13739856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7e9a460f5b40fa9161b5224a405302787d1cd40fd02b57e29ea38adf50273061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c0a5fe9e0133bc16645e387182bcbfbb594cd603582cfad20279c015a84854`

```dockerfile
```

-	Layers:
	-	`sha256:54e0c5426f56d92b29a5e46ccabe21ffe0344d4f8c2a851ed9d1776cf02307eb`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 263.9 KB (263882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0174d523126387bb17ee8b36c86137b0d32d7434536ff5438d297ce4fc56aaf`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bfbce093116fb3f94ffec6951d6cb067a22cda867b73854e4630954bc3548e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18015071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614062123a347849d270f9e29c9cb8647ae01e7b9463875be85bc1b6924e6bc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='866b6186626d4a7f35d5c010f3f532b022a35dd21f3512bd2015d6de39add0ccc0e8f778878a927ea4a5131ed1dfa8f114b1b9831eaa741f8aebc5c2d88747fd' ;; 		armhf)   binArch='armv6'; checksum='7cb786e8f1af7573ece485f2a9348c3ba7c6191346f5917075027f5cf5309fc0b8e3113e48092fc723d01171cd3c8bdfd076af17e69b1a6c1a9a0d5e53fdf1d2' ;; 		armv7)   binArch='armv7'; checksum='e1a7c02a0986d260ead1ffa9023e78bc1903139813ef5233a06d1f7d621f71ce37eb0042a991287256f85dae64924278514d183bcd805ef0329a096e4574dc06' ;; 		aarch64) binArch='arm64'; checksum='1a619b1ad15fc2163fa597a00b2c6174e6d00b8ce5206d18e0691edf9251ac8dcf1ebf059d7bd065a9ce0b3427071943dd2385d27fa78df0678cefea07280154' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c6d9b6a8db14b4a44de453023ae7b9d6f85b646dfb22a7e4bd5859556fb9cc42e1fb16b3ea5312a2b97bce4ab1f87a71daa430dc57cea09c0dea739409d5434f' ;; 		s390x)   binArch='s390x'; checksum='312ff46594f445d643acbc0d2f118c5af9419dd9e2ea1a8398a8a7772d172ec616d79f83eb4e3550efd26188c3fa1ddff1d9255bb3a55fe6b4384b0db818502a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_DATA_HOME=/data
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/udp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /srv
# Thu, 30 May 2024 14:50:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679b063c3cccee55ed2da27af5dca9a85a3447ab5ea8e8223f2399d695b9e9f`  
		Last Modified: Thu, 30 May 2024 14:41:43 GMT  
		Size: 369.2 KB (369156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3036766387a41a19917f6f36c51dc3d94c3c78b15ec4aa0703d5c7a3094789`  
		Last Modified: Thu, 30 May 2024 14:41:42 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553446b932e7710418d71ee0fa94d83a2d0b6d6de2c8033f103a6c4ee8ac8037`  
		Last Modified: Thu, 30 May 2024 22:40:07 GMT  
		Size: 13.6 MB (13551656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f1ec6ba7f30a7039a101a631a18df1f1a91391309caa49bd0e9e7b95e335523f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 KB (281801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c841bc8bf71a85025aff6456ac07ef330aac19bfae66e33b7973eef4c031019`

```dockerfile
```

-	Layers:
	-	`sha256:58daa084cecd327bebce8ec82a37814b9bc513354002eeaa73370e4fa127cd02`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 263.9 KB (263919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7d58bbbff5474e240bb6c7ac3ee4866a0b9cd4a10541a9b2783a894127c0a8`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3e6afc21f26a045b9cff8dded3a108350486ae0a14e809309a3b6fcbaf2ab44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17239755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dca62d441c172288e8c02545931a5a24e62efb67f3197ae3f98fce961d4ff89`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc90e19cccec8c93b7fc82b34313edb20031c9beb48eba2301ddeea45c3283c2`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 370.4 KB (370398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495869352c1369757545722b0b5a9bdb38f1e4128851a01a45d6a896324eb208`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6255e5da3daad8d4f46b62aad8f74352472eb69509d4a85ddabb97dd5776032a`  
		Last Modified: Tue, 04 Jun 2024 01:47:46 GMT  
		Size: 13.3 MB (13292030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c76863ba66130346110cedfd2bd2346b62eccfdaad6b2d977209af4667f6e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022c234dffa5c4adf5045497989c7751c3e9b547b1a551497603480c7274dee0`

```dockerfile
```

-	Layers:
	-	`sha256:5e4ec7316421ca7d7aff7105fd8504943835e4121422cf9529f52ab819de1d56`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 261.9 KB (261918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64ee8324a31e6505d22eddd274754e4cc07367c231b3f4d616f9761409bd6266`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:5d61f08a2244fdd9670175600ad9e49611e5c5224f3b2b4ea2ce07ac56ab3a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17988811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa45066278353d53895c24f1f52b51c98e1463beb562cbbe8d777a691ef0d333`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9dcde94bf3f93b54ed692d25df606aadecebd0f28dd77d53b2c325c79116a9`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 364.9 KB (364869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129cdd4fd7c6eaafbd0d2ee17d753e1dc55f2b053dfe7eee597a638caec99dbf`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be0dc6e23084d8005f5b12d389c12d178b61dd29787c3eedee3a345071254b`  
		Last Modified: Mon, 03 Jun 2024 21:31:39 GMT  
		Size: 14.2 MB (14156119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a71f8245a1fd40b0a5ede0f920e638a267abfedc83a33ef8f3e1f2b6ef63eb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643cd9393627b6ccbef5905e3848878f075de79071ab70ba90611cc1e8448a2d`

```dockerfile
```

-	Layers:
	-	`sha256:ac2552b9d22cc667e50951ca72233fe141aa9ba5177bfceaf4c6018693a777d0`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 261.9 KB (261860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ae05b2ef2b85ef54cad975979e33c0d69ebc0cb9ff24041f016c7f2ae25182`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8-builder`

```console
$ docker pull caddy@sha256:3db37b69486800de84befa0dd692b4023beb435421703bbdb6f84a8055ddf011
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
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-builder` - linux; amd64

```console
$ docker pull caddy@sha256:df570c9c66505c887b2e78591181a8898bc1b8e25110e72ebbe1975b3fe89579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32f73a324a2d0e72a305f33619431bbfaba72840c70d6bec3f65f6e1cde8f6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46b7a5114a614bbc3afd1c49e40787c13c7c99cbc9af08e76fd9efa15e25b3f`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 5.9 MB (5914553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f6f6b1947c18c1bac715d995f46ce46727337a1ada0c4e7c2f2984a04aecb`  
		Last Modified: Mon, 03 Jun 2024 19:01:04 GMT  
		Size: 1.5 MB (1500680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806b02ef115ec1e534f2d36220b8eb1378cd4c1c96f410c53777e98f2f53a4cc`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:4da5f7d3f531e501a3ee5d389bc618d16c71bb86651fd68109d1f4981c3521d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986ce2397a27ef8d158052d579cb6a3b7b091330a59c01f105c3613c419d96ec`

```dockerfile
```

-	Layers:
	-	`sha256:3b2971fdad01a0613ef3e83c2cb8aab230ab0e62c4706ed98be8e9996b059dc4`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 275.7 KB (275708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cee59000fd2235e2e4bae2324c59b0c5d0288ad38996227843424658929c6c0`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:775a4428a3050de7079c89cff231c7ca54a01750ef752e8956584f4f8aaf76e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687f926297703c36c0b447b824401e090c54ddea35df95e9ac60b4ec2cfacab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199f8807ec47ac7592520ba82c877d9f6e6de8581f5f275abc56366dde16c1e`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 5.9 MB (5863451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7034939efcb080f679b56509133f9446262a4f442bf0c7394b454b1301f8791`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 1.4 MB (1423814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88cb6dc9c9687d4c1e64363a7e442ceab1456f49fb00aa819559ef0f0db699b`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3631380eaad063eb4441aeeb50616e75119a076efa5ee77af875aee22185549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5d75ee09562d929629215ec9ed12f6d436dcf52ad8986145bfa751437e09cc`

```dockerfile
```

-	Layers:
	-	`sha256:74ab8498bb88c256e9c05c7a0d99618dc4453b94584fb9c2c4dc360f08d6a47a`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:51fb29be03522856b8f507ea4df9ba1500972b756133c5bd35bddbca62d88ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d732f429c533cb427cdc7e7e044a83cfd84ced4da7224ac736da16d2c9dc43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444cd28ed296484ff90ddfb993c5cfce9deb7c7ee33a5fdf232fe5728d76ae7`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 292.5 KB (292462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d908fd62c89b1c0b846c14fa9daab8130baecf2d44514d246f96e1a89b6386d1`  
		Last Modified: Wed, 29 May 2024 01:38:47 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e444f239d275345fbcb28de09591b1ce21727483c1005dce419cc2136850fda`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f65578e4b162e83a0db7ae060959bda593a7d3f1774d5df8a3db0daefb184`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 5.4 MB (5351021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9ddad03f4d41f0e3d32a6b453c421c3c9d40d33ce4e2ac44f5ab0daff9a718`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 1.4 MB (1420766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f597d1755326223ce04f920c0eafbb47bf1630a3bc422c26b40698041417a49`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:63b2efa558ce0c277b21c332f0ac76eb069250f04c2bd6e22d86a6c04ca39e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a8dd5917ba43f4ca990fac2e0ce2eb472d317991a141f663eee67969cb8091`

```dockerfile
```

-	Layers:
	-	`sha256:d0f1adf29c41b7079e6776c969549d8fe63a0d2349f3f262e352780c396389b6`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 278.3 KB (278320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d8f39dc5b6142e254a1cfa5b6d44f9b0ee1b56653d76f5de94cff5466ad44a`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f0e70454943d37a64344820181d8396714d91d40ffd3a04844076a3b41d69a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78085757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb59a6bfcf30a2dfc3705ca6f25183cd395301a7a185380c978cea1117557ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SETCAP=1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 30 May 2024 14:50:16 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fd4d77c1150ba7c64d2b9cb1ad73058c134eea51cdf8a7c969379c3fe358c3`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6930e6242b08ff7992e85b10519d54167d7ffdedf7199e086b7c8be95e4baf6`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d49fbb06d2ec1fb8e7c2633794d12f435fe6098384a1ba28e82e7be07d06a38`  
		Last Modified: Thu, 30 May 2024 14:42:18 GMT  
		Size: 6.0 MB (6033730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31dd998a75477c407a2dee8c594a80ba41fdac4dd42d9d67a7c414c4c8997b9`  
		Last Modified: Thu, 30 May 2024 22:40:31 GMT  
		Size: 1.4 MB (1397169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770803ae5abd93eb1dcbc65ce6b1ccdfd01a538b7c537f05e868e88c81d9d430`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:acae0dfa758b68833a5e19bd4804c3a3916e795ee6dde565fc338a83efe0a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 KB (295844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de6d746bee70c9e18f38b0e19e943d1a7fcdb8b1b73856d337570218ce8c0bb`

```dockerfile
```

-	Layers:
	-	`sha256:1abefdba7275d0ce20e30a7257a2ed4eae90e1997c2acdafc5dae8ae0afccec3`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 275.8 KB (275813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5fee8e57abbb9909e5460f0b9e029723da0ba965f905c8d24ee042cab953b8`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:5bec9aca46cc2b81188b8dafd0415a432fefce0b94a93585e6866c635c05860e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98626dc8793adc0d9d1556e0d3019819e6c04c9ab5adc9ec2050ad07a27631b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7130843bbd3e7aec4f18d777d8486e1a31bc676e485de7fbd9674a170777d8e`  
		Last Modified: Tue, 28 May 2024 23:35:05 GMT  
		Size: 295.9 KB (295891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c97ae223460d35ee30ac67c808649bb863398f7373aeff23f0dd033662e29`  
		Last Modified: Tue, 28 May 2024 23:35:07 GMT  
		Size: 66.4 MB (66430055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8885cb230dbccfd815664d1c1a6f3bfa5328a48b9192145c2a16236fb973f8b3`  
		Last Modified: Tue, 28 May 2024 23:35:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434d6eb71e6463f36189c536f37f5e808afd8a2888e4cf6564148bb8e0d568fb`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 6.2 MB (6240121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152d73d2731afedc609d6f5911728ace83ce1c08e1dbcd5460e4cbd48f006d6`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 1.4 MB (1390031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3288aae2d128567448ca4a8038c23cd41eb09e6cc2046a729c45fbe9f88ff9e1`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e52ddd12fdb8d2940ec7abd3835bf37d4cb84f53dbbe0fbed3cbef7396129e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf175f54a787ed0ace3a3b04deef8d8eb90713125b37f236e50a036adfc185`

```dockerfile
```

-	Layers:
	-	`sha256:0d74303319f715f2000d3da32d63018ae9f0c705fa1499bb9372bb231e0bb45d`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 273.8 KB (273846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e85be5da6c5e14cd99bac3703afc52f78692560e39587f4b95b73ce6a5ea02`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; s390x

```console
$ docker pull caddy@sha256:bbd371f55e5fd21330c24bcfd34a1a8702191867cceb0b340c3b21002c23a3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af99e1c137b5b73332bc84f34766ea766f1369cccc49d900bc35cd805ff0dfc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7fb356c901d4b14e02b6bca1b10852f4a9f85dc695ab3239d771383ee632a5`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 6.2 MB (6179567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62ccaf0be9fd4c408957b5068154bc456143c35dc8c818955199c1cc19412fd`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216b4bc58f3ca32cc60a50bb5a7f1d89bc4c869fcbcc8a3d79cfc455e3a829aa`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a0cd00361f284c2509ee135e57e9ba892603c9babba263a8c9a4019ec816f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea05560489e0436aeabee2b1d096e6ef1883871da7006a5f427be424a1588525`

```dockerfile
```

-	Layers:
	-	`sha256:7a0297889ae2bc64168bf10de6cb03222bf8a8d3915e6eb4e76077607f4f1dca`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 273.8 KB (273754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f562e536bfdd4352eb3a45746b1c36b9bcb4b47e266c037b4ef05073aa9771`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:0e6791b30064fce15067fec856819501eb37e90a3d63c8954f615b1bb9a50cd4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212210875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec756e07bb7339ed40f5aaa265ac85ae87f7cbe499cb07dcb30bae80fca70a5c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:58:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:58:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:58:45 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:58:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:58:58 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:59:04 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:59:05 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:00:17 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:18 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:02:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:48 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:02:49 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90a3c07c43efebd99803cdb9bad2d8149315d6fe71ed67ca3c907554d9e0d9`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d2da37d6aadb3a05b1b91cab3d0735e673ee46930e50eff76541ca6cd703c4`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998290d6ae9e03557ab29c99bdecd95a1646d0b2b6e01375977bc9ca92e7679f`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febc0e57a30d4aaef8d997796e999f07cd8d02fefada73c1d9a8d3b2efb2d0a5`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9634b04a70d192ce4d61fc9cacd9dfe77dc2ce74925adb17ec44604eae27767e`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d148249d3a6d5d5e8a6682e3d3c7577ec3e6c4db642ff5a298431e2aa6015a`  
		Last Modified: Wed, 15 May 2024 22:00:24 GMT  
		Size: 25.4 MB (25444377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abaff09d8cdfae3edceb6c5711ad840eb5f47c5bc4b76b2e6b4da440009de54`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302450cd0c74f7f8c4e0ef1ddc17b877078794558e3bc9ea20be56798e14f0b1`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 345.6 KB (345575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5856fa608f5aaadb2aa345cb0e4e8b4727bc567c776a2ca50b9b9b2ae049ca71`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b86ddf0d69a3769b0f5587cfee9e1dee2b6c0de79f2c6b192fc06caac1639`  
		Last Modified: Wed, 15 May 2024 22:00:32 GMT  
		Size: 71.8 MB (71755992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f91b25b9e6cb7c3077ad2c0725b9b9f62ce4feb0a96fd7c1a075d356fe1b1`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5f7203aa8356980751a8d0d837f026ab70683bb5d98c69c30ec9dfbdd96909`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a29c49e69b7ad65d25803b5ede17ea3a9a1de029f8ed9efba96ae8d8a6ee647`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980757db2f634cea769d2bbf611fabaefc8ef068bf3449adfb4aab3dfc8d82d`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b729eaf00df1c3145830dc1c7b99c931760b57c4ac1cb3c7e089c2daec1b5f40`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b29deaba4982d0ebc1399cdd05eb16d24ab4aeb0b856a15f355845ceb3a2d07`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 2.0 MB (1976480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2eb9ded10797df67ff42377be07f21c463ee93afda3ef414f90864dde3bf2`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8-builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:7ec8bed26a5de8b4d209ef792271790786a9034467431218920c382cfbbb6fab
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a48743c09fc4e5f8c297ca67457a44f3de2a7521f27fe42b0bab9e46883c203`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 22:51:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:51:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:51:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:54:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:54:20 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:54:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:54:45 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:58:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:58:59 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:03:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:03:12 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:03:13 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:04:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:04:42 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b721870b6ca4ac86a4dd17a9efa72d3bbbc3e2f4db24604ab3e5529ac9483`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231059aab43e3c4c95c41ffa0eaaf0a505c5a3e17b120dfc894682b1930a3968`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83508e294490f2fa915d9cd65227cc8e8661207b15aa2cfdaf074ff8ae7bb4d4`  
		Last Modified: Wed, 15 May 2024 22:59:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d676bfa2282c568dda9fa4af2f2e6d235ebca82a6c367717bf083bad7dd8b3a`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3161f170f396d7c78bb77ee80c5b634beca05d901f05396abeab4e06be7f5`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c76d7a1b3a9e63480abdc848b1fd30a006301a1e471568b571a209702755daa`  
		Last Modified: Wed, 15 May 2024 22:59:07 GMT  
		Size: 25.6 MB (25574881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dcf82dafd8633a79265dca42870493640409651674a91b43f2adf04c165a`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dac5092add95bf42e98f932737023e0c6ef6ca428f58802291c2cc4c9559b7`  
		Last Modified: Wed, 15 May 2024 22:59:03 GMT  
		Size: 345.9 KB (345903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7992418d5500de5ceeac2fa4f57b54353f18a13b476f19add206e269ef1e6fc`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad77f522384c92c66907f62599064a34ebdd67556de4d2570970de37d46d8`  
		Last Modified: Wed, 15 May 2024 22:59:13 GMT  
		Size: 71.7 MB (71743817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716ef2ea189a02632506ad12bdad7990790c5792d611ac5831fdfa2896ac298`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0238b1a68b5dc8e13a99e71e8c0013bd2b7dfaf127ce1af2e7b6f0b8d52f3`  
		Last Modified: Mon, 03 Jun 2024 19:04:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5109dfca4e11a4fc1d216988f7afe6fa800a6dcef66617d88c19636ab6e50cb7`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081c9df7b06e5088479a8f522501c4643b3179a9b34e5a83fc27ed9d4e5fe539`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b6cca533939895b90c344b768eaf02c53ac76b0a4c97a456d440aba3a8b571`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b805480f52756d99d47ee659a1b21cd0f116bb7fbc8a883a407689bd131635b`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 2.0 MB (1951462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be79ded6647b5f2dfe026d26fc2a855941e795f364266d2bf246cc5c8dc56a`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-builder-alpine`

```console
$ docker pull caddy@sha256:1bb8f3d134ec8113c17d4ea0e073e94944f4bce8c7429055f2fa6168e36ab96b
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

### `caddy:2.8-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:df570c9c66505c887b2e78591181a8898bc1b8e25110e72ebbe1975b3fe89579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32f73a324a2d0e72a305f33619431bbfaba72840c70d6bec3f65f6e1cde8f6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46b7a5114a614bbc3afd1c49e40787c13c7c99cbc9af08e76fd9efa15e25b3f`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 5.9 MB (5914553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f6f6b1947c18c1bac715d995f46ce46727337a1ada0c4e7c2f2984a04aecb`  
		Last Modified: Mon, 03 Jun 2024 19:01:04 GMT  
		Size: 1.5 MB (1500680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806b02ef115ec1e534f2d36220b8eb1378cd4c1c96f410c53777e98f2f53a4cc`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4da5f7d3f531e501a3ee5d389bc618d16c71bb86651fd68109d1f4981c3521d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986ce2397a27ef8d158052d579cb6a3b7b091330a59c01f105c3613c419d96ec`

```dockerfile
```

-	Layers:
	-	`sha256:3b2971fdad01a0613ef3e83c2cb8aab230ab0e62c4706ed98be8e9996b059dc4`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 275.7 KB (275708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cee59000fd2235e2e4bae2324c59b0c5d0288ad38996227843424658929c6c0`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:775a4428a3050de7079c89cff231c7ca54a01750ef752e8956584f4f8aaf76e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687f926297703c36c0b447b824401e090c54ddea35df95e9ac60b4ec2cfacab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199f8807ec47ac7592520ba82c877d9f6e6de8581f5f275abc56366dde16c1e`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 5.9 MB (5863451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7034939efcb080f679b56509133f9446262a4f442bf0c7394b454b1301f8791`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 1.4 MB (1423814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88cb6dc9c9687d4c1e64363a7e442ceab1456f49fb00aa819559ef0f0db699b`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3631380eaad063eb4441aeeb50616e75119a076efa5ee77af875aee22185549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5d75ee09562d929629215ec9ed12f6d436dcf52ad8986145bfa751437e09cc`

```dockerfile
```

-	Layers:
	-	`sha256:74ab8498bb88c256e9c05c7a0d99618dc4453b94584fb9c2c4dc360f08d6a47a`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:51fb29be03522856b8f507ea4df9ba1500972b756133c5bd35bddbca62d88ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d732f429c533cb427cdc7e7e044a83cfd84ced4da7224ac736da16d2c9dc43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444cd28ed296484ff90ddfb993c5cfce9deb7c7ee33a5fdf232fe5728d76ae7`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 292.5 KB (292462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d908fd62c89b1c0b846c14fa9daab8130baecf2d44514d246f96e1a89b6386d1`  
		Last Modified: Wed, 29 May 2024 01:38:47 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e444f239d275345fbcb28de09591b1ce21727483c1005dce419cc2136850fda`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f65578e4b162e83a0db7ae060959bda593a7d3f1774d5df8a3db0daefb184`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 5.4 MB (5351021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9ddad03f4d41f0e3d32a6b453c421c3c9d40d33ce4e2ac44f5ab0daff9a718`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 1.4 MB (1420766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f597d1755326223ce04f920c0eafbb47bf1630a3bc422c26b40698041417a49`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:63b2efa558ce0c277b21c332f0ac76eb069250f04c2bd6e22d86a6c04ca39e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a8dd5917ba43f4ca990fac2e0ce2eb472d317991a141f663eee67969cb8091`

```dockerfile
```

-	Layers:
	-	`sha256:d0f1adf29c41b7079e6776c969549d8fe63a0d2349f3f262e352780c396389b6`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 278.3 KB (278320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d8f39dc5b6142e254a1cfa5b6d44f9b0ee1b56653d76f5de94cff5466ad44a`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f0e70454943d37a64344820181d8396714d91d40ffd3a04844076a3b41d69a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78085757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb59a6bfcf30a2dfc3705ca6f25183cd395301a7a185380c978cea1117557ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SETCAP=1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 30 May 2024 14:50:16 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fd4d77c1150ba7c64d2b9cb1ad73058c134eea51cdf8a7c969379c3fe358c3`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6930e6242b08ff7992e85b10519d54167d7ffdedf7199e086b7c8be95e4baf6`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d49fbb06d2ec1fb8e7c2633794d12f435fe6098384a1ba28e82e7be07d06a38`  
		Last Modified: Thu, 30 May 2024 14:42:18 GMT  
		Size: 6.0 MB (6033730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31dd998a75477c407a2dee8c594a80ba41fdac4dd42d9d67a7c414c4c8997b9`  
		Last Modified: Thu, 30 May 2024 22:40:31 GMT  
		Size: 1.4 MB (1397169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770803ae5abd93eb1dcbc65ce6b1ccdfd01a538b7c537f05e868e88c81d9d430`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:acae0dfa758b68833a5e19bd4804c3a3916e795ee6dde565fc338a83efe0a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 KB (295844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de6d746bee70c9e18f38b0e19e943d1a7fcdb8b1b73856d337570218ce8c0bb`

```dockerfile
```

-	Layers:
	-	`sha256:1abefdba7275d0ce20e30a7257a2ed4eae90e1997c2acdafc5dae8ae0afccec3`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 275.8 KB (275813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5fee8e57abbb9909e5460f0b9e029723da0ba965f905c8d24ee042cab953b8`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:5bec9aca46cc2b81188b8dafd0415a432fefce0b94a93585e6866c635c05860e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98626dc8793adc0d9d1556e0d3019819e6c04c9ab5adc9ec2050ad07a27631b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7130843bbd3e7aec4f18d777d8486e1a31bc676e485de7fbd9674a170777d8e`  
		Last Modified: Tue, 28 May 2024 23:35:05 GMT  
		Size: 295.9 KB (295891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c97ae223460d35ee30ac67c808649bb863398f7373aeff23f0dd033662e29`  
		Last Modified: Tue, 28 May 2024 23:35:07 GMT  
		Size: 66.4 MB (66430055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8885cb230dbccfd815664d1c1a6f3bfa5328a48b9192145c2a16236fb973f8b3`  
		Last Modified: Tue, 28 May 2024 23:35:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434d6eb71e6463f36189c536f37f5e808afd8a2888e4cf6564148bb8e0d568fb`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 6.2 MB (6240121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152d73d2731afedc609d6f5911728ace83ce1c08e1dbcd5460e4cbd48f006d6`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 1.4 MB (1390031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3288aae2d128567448ca4a8038c23cd41eb09e6cc2046a729c45fbe9f88ff9e1`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e52ddd12fdb8d2940ec7abd3835bf37d4cb84f53dbbe0fbed3cbef7396129e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf175f54a787ed0ace3a3b04deef8d8eb90713125b37f236e50a036adfc185`

```dockerfile
```

-	Layers:
	-	`sha256:0d74303319f715f2000d3da32d63018ae9f0c705fa1499bb9372bb231e0bb45d`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 273.8 KB (273846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e85be5da6c5e14cd99bac3703afc52f78692560e39587f4b95b73ce6a5ea02`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bbd371f55e5fd21330c24bcfd34a1a8702191867cceb0b340c3b21002c23a3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af99e1c137b5b73332bc84f34766ea766f1369cccc49d900bc35cd805ff0dfc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7fb356c901d4b14e02b6bca1b10852f4a9f85dc695ab3239d771383ee632a5`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 6.2 MB (6179567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62ccaf0be9fd4c408957b5068154bc456143c35dc8c818955199c1cc19412fd`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216b4bc58f3ca32cc60a50bb5a7f1d89bc4c869fcbcc8a3d79cfc455e3a829aa`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a0cd00361f284c2509ee135e57e9ba892603c9babba263a8c9a4019ec816f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea05560489e0436aeabee2b1d096e6ef1883871da7006a5f427be424a1588525`

```dockerfile
```

-	Layers:
	-	`sha256:7a0297889ae2bc64168bf10de6cb03222bf8a8d3915e6eb4e76077607f4f1dca`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 273.8 KB (273754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f562e536bfdd4352eb3a45746b1c36b9bcb4b47e266c037b4ef05073aa9771`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:dcee0b1539d2763646c0ab649486962e588b05ca78d46bf87c7bc0a2d2f39d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:7ec8bed26a5de8b4d209ef792271790786a9034467431218920c382cfbbb6fab
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a48743c09fc4e5f8c297ca67457a44f3de2a7521f27fe42b0bab9e46883c203`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 22:51:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:51:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:51:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:54:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:54:20 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:54:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:54:45 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:58:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:58:59 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:03:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:03:12 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:03:13 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:04:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:04:42 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b721870b6ca4ac86a4dd17a9efa72d3bbbc3e2f4db24604ab3e5529ac9483`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231059aab43e3c4c95c41ffa0eaaf0a505c5a3e17b120dfc894682b1930a3968`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83508e294490f2fa915d9cd65227cc8e8661207b15aa2cfdaf074ff8ae7bb4d4`  
		Last Modified: Wed, 15 May 2024 22:59:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d676bfa2282c568dda9fa4af2f2e6d235ebca82a6c367717bf083bad7dd8b3a`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3161f170f396d7c78bb77ee80c5b634beca05d901f05396abeab4e06be7f5`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c76d7a1b3a9e63480abdc848b1fd30a006301a1e471568b571a209702755daa`  
		Last Modified: Wed, 15 May 2024 22:59:07 GMT  
		Size: 25.6 MB (25574881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dcf82dafd8633a79265dca42870493640409651674a91b43f2adf04c165a`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dac5092add95bf42e98f932737023e0c6ef6ca428f58802291c2cc4c9559b7`  
		Last Modified: Wed, 15 May 2024 22:59:03 GMT  
		Size: 345.9 KB (345903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7992418d5500de5ceeac2fa4f57b54353f18a13b476f19add206e269ef1e6fc`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad77f522384c92c66907f62599064a34ebdd67556de4d2570970de37d46d8`  
		Last Modified: Wed, 15 May 2024 22:59:13 GMT  
		Size: 71.7 MB (71743817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716ef2ea189a02632506ad12bdad7990790c5792d611ac5831fdfa2896ac298`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0238b1a68b5dc8e13a99e71e8c0013bd2b7dfaf127ce1af2e7b6f0b8d52f3`  
		Last Modified: Mon, 03 Jun 2024 19:04:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5109dfca4e11a4fc1d216988f7afe6fa800a6dcef66617d88c19636ab6e50cb7`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081c9df7b06e5088479a8f522501c4643b3179a9b34e5a83fc27ed9d4e5fe539`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b6cca533939895b90c344b768eaf02c53ac76b0a4c97a456d440aba3a8b571`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b805480f52756d99d47ee659a1b21cd0f116bb7fbc8a883a407689bd131635b`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 2.0 MB (1951462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be79ded6647b5f2dfe026d26fc2a855941e795f364266d2bf246cc5c8dc56a`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:59f3fab8e735fb586ed740691880ee298cf3caae458593effaf99bdacceaa0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:0e6791b30064fce15067fec856819501eb37e90a3d63c8954f615b1bb9a50cd4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212210875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec756e07bb7339ed40f5aaa265ac85ae87f7cbe499cb07dcb30bae80fca70a5c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:58:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:58:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:58:45 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:58:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:58:58 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:59:04 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:59:05 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:00:17 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:18 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:02:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:48 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:02:49 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90a3c07c43efebd99803cdb9bad2d8149315d6fe71ed67ca3c907554d9e0d9`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d2da37d6aadb3a05b1b91cab3d0735e673ee46930e50eff76541ca6cd703c4`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998290d6ae9e03557ab29c99bdecd95a1646d0b2b6e01375977bc9ca92e7679f`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febc0e57a30d4aaef8d997796e999f07cd8d02fefada73c1d9a8d3b2efb2d0a5`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9634b04a70d192ce4d61fc9cacd9dfe77dc2ce74925adb17ec44604eae27767e`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d148249d3a6d5d5e8a6682e3d3c7577ec3e6c4db642ff5a298431e2aa6015a`  
		Last Modified: Wed, 15 May 2024 22:00:24 GMT  
		Size: 25.4 MB (25444377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abaff09d8cdfae3edceb6c5711ad840eb5f47c5bc4b76b2e6b4da440009de54`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302450cd0c74f7f8c4e0ef1ddc17b877078794558e3bc9ea20be56798e14f0b1`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 345.6 KB (345575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5856fa608f5aaadb2aa345cb0e4e8b4727bc567c776a2ca50b9b9b2ae049ca71`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b86ddf0d69a3769b0f5587cfee9e1dee2b6c0de79f2c6b192fc06caac1639`  
		Last Modified: Wed, 15 May 2024 22:00:32 GMT  
		Size: 71.8 MB (71755992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f91b25b9e6cb7c3077ad2c0725b9b9f62ce4feb0a96fd7c1a075d356fe1b1`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5f7203aa8356980751a8d0d837f026ab70683bb5d98c69c30ec9dfbdd96909`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a29c49e69b7ad65d25803b5ede17ea3a9a1de029f8ed9efba96ae8d8a6ee647`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980757db2f634cea769d2bbf611fabaefc8ef068bf3449adfb4aab3dfc8d82d`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b729eaf00df1c3145830dc1c7b99c931760b57c4ac1cb3c7e089c2daec1b5f40`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b29deaba4982d0ebc1399cdd05eb16d24ab4aeb0b856a15f355845ceb3a2d07`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 2.0 MB (1976480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2eb9ded10797df67ff42377be07f21c463ee93afda3ef414f90864dde3bf2`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore`

```console
$ docker pull caddy@sha256:a0b338adc338b131f1b4811bd7f95964e764e483c22ab46c1ba97947e90beced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore-1809`

```console
$ docker pull caddy@sha256:dbab4057e60d72545d940471196dda51a1c0cbb62ec6fec4bd62a6c6110be70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:298ce474adcb68acbbf7d561e3182062bc7c263ef39cfac2632da7d9841bf435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.4`

```console
$ docker pull caddy@sha256:f5af55ebb433cb652b27f5b5fc5732853bcb00afeddedb9579be6a10c9a42b1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.4` - linux; amd64

```console
$ docker pull caddy@sha256:c092823e9774ccbc7a761d4fd45d49332cc050a4ed13e209c0752fbe77408cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18625893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379e9d34447ebff04422e00130985b166b7fc9cef98876e70d97e6d83269c215`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ecfa782506bda1924ea74bea4182d74f0557cebbf18a71fd48fe97fc6c59c8`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 357.4 KB (357381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94997ff2e374d1bfa99bd1f1a8e8f43cf6e148f63f8e9fe26265ae3d10ca8c9f`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08df330a016638626ff383f490ecf44b254e9ddbae0b4129c2b18c456201e5e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:56 GMT  
		Size: 14.6 MB (14638937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4` - unknown; unknown

```console
$ docker pull caddy@sha256:041cc73927bb91ca88f8e88d7176aa520def52fca3402b730194a040a57b7a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eadb390bbfcd1f11cb6e7d8a95f43d2c71a613fc1e0f23a122e9bf12f4767b`

```dockerfile
```

-	Layers:
	-	`sha256:2f1d323a5412e4d8283ffbbf553b6c8317cfcd3199cff1626166d1fada238a5e`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 263.8 KB (263814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c05f7c8878252295ae4ac295bcdedbd14f7e95ed4ac7e789ad372763a182494`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4` - linux; arm variant v6

```console
$ docker pull caddy@sha256:66473e2c9d4a1db0ae9bd459956d42d53e9991c58c900251753d648330f3f42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17496054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731a02bd06ee6a92070bf885f12f1dbbbbb736ec9db845b31b5fd8d0f9ec0c42`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30eae165a31e9dfba433ec2953fd144ad11b8b3b833ef35d2566b9fb75a56a`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 357.7 KB (357701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c943ab66970deade36497f4930fc57c4b3c8f30aba0bc7d118ec65b050da491`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb558a164f07a87610adfe7dab44e2f703cc5fd3e8c72f775b7706e2e2e5d3ea`  
		Last Modified: Mon, 03 Jun 2024 20:14:26 GMT  
		Size: 13.8 MB (13765815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4` - unknown; unknown

```console
$ docker pull caddy@sha256:603f2ccec3669ac6a2749b7353e1bc949f166b4e3af650ce31d52b84be0a695d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c14dd01315a75e80a6d6459314782e218de761094d650564e70127e2639069a`

```dockerfile
```

-	Layers:
	-	`sha256:22cc7a81c0b1dd55893d0bd0bb7529a2d0ba81511a60787234b85f74f2bc367f`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d85c3fe08f25f0ff105839b738bc42d3cd0d4b3d804633ea99274c5aaf8838fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17195439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03a1673034f8209e77bd2c19e591b4feb4ebae6b72397a9f294cc1c84ce8983`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e694f733a431bd3ad4ee991d4dab8f760be8e7af16eacaf4bf3a47768fd799`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 354.1 KB (354065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975bb16f920c19614bb988818a5b0554e151e90bda59fa8681309d8b27c4ec89`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959163643e12b18c2516a3514743986aa91426069415a4bda6d18f8206ee9772`  
		Last Modified: Mon, 03 Jun 2024 21:48:35 GMT  
		Size: 13.7 MB (13739856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4` - unknown; unknown

```console
$ docker pull caddy@sha256:7e9a460f5b40fa9161b5224a405302787d1cd40fd02b57e29ea38adf50273061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c0a5fe9e0133bc16645e387182bcbfbb594cd603582cfad20279c015a84854`

```dockerfile
```

-	Layers:
	-	`sha256:54e0c5426f56d92b29a5e46ccabe21ffe0344d4f8c2a851ed9d1776cf02307eb`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 263.9 KB (263882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0174d523126387bb17ee8b36c86137b0d32d7434536ff5438d297ce4fc56aaf`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4` - linux; ppc64le

```console
$ docker pull caddy@sha256:3e6afc21f26a045b9cff8dded3a108350486ae0a14e809309a3b6fcbaf2ab44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17239755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dca62d441c172288e8c02545931a5a24e62efb67f3197ae3f98fce961d4ff89`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc90e19cccec8c93b7fc82b34313edb20031c9beb48eba2301ddeea45c3283c2`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 370.4 KB (370398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495869352c1369757545722b0b5a9bdb38f1e4128851a01a45d6a896324eb208`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6255e5da3daad8d4f46b62aad8f74352472eb69509d4a85ddabb97dd5776032a`  
		Last Modified: Tue, 04 Jun 2024 01:47:46 GMT  
		Size: 13.3 MB (13292030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4` - unknown; unknown

```console
$ docker pull caddy@sha256:c76863ba66130346110cedfd2bd2346b62eccfdaad6b2d977209af4667f6e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022c234dffa5c4adf5045497989c7751c3e9b547b1a551497603480c7274dee0`

```dockerfile
```

-	Layers:
	-	`sha256:5e4ec7316421ca7d7aff7105fd8504943835e4121422cf9529f52ab819de1d56`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 261.9 KB (261918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64ee8324a31e6505d22eddd274754e4cc07367c231b3f4d616f9761409bd6266`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4` - linux; s390x

```console
$ docker pull caddy@sha256:5d61f08a2244fdd9670175600ad9e49611e5c5224f3b2b4ea2ce07ac56ab3a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17988811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa45066278353d53895c24f1f52b51c98e1463beb562cbbe8d777a691ef0d333`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9dcde94bf3f93b54ed692d25df606aadecebd0f28dd77d53b2c325c79116a9`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 364.9 KB (364869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129cdd4fd7c6eaafbd0d2ee17d753e1dc55f2b053dfe7eee597a638caec99dbf`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be0dc6e23084d8005f5b12d389c12d178b61dd29787c3eedee3a345071254b`  
		Last Modified: Mon, 03 Jun 2024 21:31:39 GMT  
		Size: 14.2 MB (14156119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4` - unknown; unknown

```console
$ docker pull caddy@sha256:a71f8245a1fd40b0a5ede0f920e638a267abfedc83a33ef8f3e1f2b6ef63eb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643cd9393627b6ccbef5905e3848878f075de79071ab70ba90611cc1e8448a2d`

```dockerfile
```

-	Layers:
	-	`sha256:ac2552b9d22cc667e50951ca72233fe141aa9ba5177bfceaf4c6018693a777d0`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 261.9 KB (261860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ae05b2ef2b85ef54cad975979e33c0d69ebc0cb9ff24041f016c7f2ae25182`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8.4` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.4-alpine`

```console
$ docker pull caddy@sha256:2597ffaba95118cc8f444144052544bcbbd9018c26dde150ace3aa38f79bc125
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2.8.4-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:c092823e9774ccbc7a761d4fd45d49332cc050a4ed13e209c0752fbe77408cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18625893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379e9d34447ebff04422e00130985b166b7fc9cef98876e70d97e6d83269c215`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ecfa782506bda1924ea74bea4182d74f0557cebbf18a71fd48fe97fc6c59c8`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 357.4 KB (357381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94997ff2e374d1bfa99bd1f1a8e8f43cf6e148f63f8e9fe26265ae3d10ca8c9f`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08df330a016638626ff383f490ecf44b254e9ddbae0b4129c2b18c456201e5e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:56 GMT  
		Size: 14.6 MB (14638937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:041cc73927bb91ca88f8e88d7176aa520def52fca3402b730194a040a57b7a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eadb390bbfcd1f11cb6e7d8a95f43d2c71a613fc1e0f23a122e9bf12f4767b`

```dockerfile
```

-	Layers:
	-	`sha256:2f1d323a5412e4d8283ffbbf553b6c8317cfcd3199cff1626166d1fada238a5e`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 263.8 KB (263814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c05f7c8878252295ae4ac295bcdedbd14f7e95ed4ac7e789ad372763a182494`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:66473e2c9d4a1db0ae9bd459956d42d53e9991c58c900251753d648330f3f42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17496054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731a02bd06ee6a92070bf885f12f1dbbbbb736ec9db845b31b5fd8d0f9ec0c42`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30eae165a31e9dfba433ec2953fd144ad11b8b3b833ef35d2566b9fb75a56a`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 357.7 KB (357701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c943ab66970deade36497f4930fc57c4b3c8f30aba0bc7d118ec65b050da491`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb558a164f07a87610adfe7dab44e2f703cc5fd3e8c72f775b7706e2e2e5d3ea`  
		Last Modified: Mon, 03 Jun 2024 20:14:26 GMT  
		Size: 13.8 MB (13765815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:603f2ccec3669ac6a2749b7353e1bc949f166b4e3af650ce31d52b84be0a695d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c14dd01315a75e80a6d6459314782e218de761094d650564e70127e2639069a`

```dockerfile
```

-	Layers:
	-	`sha256:22cc7a81c0b1dd55893d0bd0bb7529a2d0ba81511a60787234b85f74f2bc367f`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d85c3fe08f25f0ff105839b738bc42d3cd0d4b3d804633ea99274c5aaf8838fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17195439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03a1673034f8209e77bd2c19e591b4feb4ebae6b72397a9f294cc1c84ce8983`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e694f733a431bd3ad4ee991d4dab8f760be8e7af16eacaf4bf3a47768fd799`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 354.1 KB (354065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975bb16f920c19614bb988818a5b0554e151e90bda59fa8681309d8b27c4ec89`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959163643e12b18c2516a3514743986aa91426069415a4bda6d18f8206ee9772`  
		Last Modified: Mon, 03 Jun 2024 21:48:35 GMT  
		Size: 13.7 MB (13739856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7e9a460f5b40fa9161b5224a405302787d1cd40fd02b57e29ea38adf50273061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c0a5fe9e0133bc16645e387182bcbfbb594cd603582cfad20279c015a84854`

```dockerfile
```

-	Layers:
	-	`sha256:54e0c5426f56d92b29a5e46ccabe21ffe0344d4f8c2a851ed9d1776cf02307eb`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 263.9 KB (263882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0174d523126387bb17ee8b36c86137b0d32d7434536ff5438d297ce4fc56aaf`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3e6afc21f26a045b9cff8dded3a108350486ae0a14e809309a3b6fcbaf2ab44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17239755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dca62d441c172288e8c02545931a5a24e62efb67f3197ae3f98fce961d4ff89`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc90e19cccec8c93b7fc82b34313edb20031c9beb48eba2301ddeea45c3283c2`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 370.4 KB (370398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495869352c1369757545722b0b5a9bdb38f1e4128851a01a45d6a896324eb208`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6255e5da3daad8d4f46b62aad8f74352472eb69509d4a85ddabb97dd5776032a`  
		Last Modified: Tue, 04 Jun 2024 01:47:46 GMT  
		Size: 13.3 MB (13292030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c76863ba66130346110cedfd2bd2346b62eccfdaad6b2d977209af4667f6e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022c234dffa5c4adf5045497989c7751c3e9b547b1a551497603480c7274dee0`

```dockerfile
```

-	Layers:
	-	`sha256:5e4ec7316421ca7d7aff7105fd8504943835e4121422cf9529f52ab819de1d56`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 261.9 KB (261918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64ee8324a31e6505d22eddd274754e4cc07367c231b3f4d616f9761409bd6266`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:5d61f08a2244fdd9670175600ad9e49611e5c5224f3b2b4ea2ce07ac56ab3a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17988811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa45066278353d53895c24f1f52b51c98e1463beb562cbbe8d777a691ef0d333`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9dcde94bf3f93b54ed692d25df606aadecebd0f28dd77d53b2c325c79116a9`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 364.9 KB (364869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129cdd4fd7c6eaafbd0d2ee17d753e1dc55f2b053dfe7eee597a638caec99dbf`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be0dc6e23084d8005f5b12d389c12d178b61dd29787c3eedee3a345071254b`  
		Last Modified: Mon, 03 Jun 2024 21:31:39 GMT  
		Size: 14.2 MB (14156119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a71f8245a1fd40b0a5ede0f920e638a267abfedc83a33ef8f3e1f2b6ef63eb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643cd9393627b6ccbef5905e3848878f075de79071ab70ba90611cc1e8448a2d`

```dockerfile
```

-	Layers:
	-	`sha256:ac2552b9d22cc667e50951ca72233fe141aa9ba5177bfceaf4c6018693a777d0`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 261.9 KB (261860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ae05b2ef2b85ef54cad975979e33c0d69ebc0cb9ff24041f016c7f2ae25182`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8.4-builder`

```console
$ docker pull caddy@sha256:55508f3d559b518d77d8ad453453c02ef616d7697c2a1503feb091123e9751c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.4-builder` - linux; amd64

```console
$ docker pull caddy@sha256:df570c9c66505c887b2e78591181a8898bc1b8e25110e72ebbe1975b3fe89579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32f73a324a2d0e72a305f33619431bbfaba72840c70d6bec3f65f6e1cde8f6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46b7a5114a614bbc3afd1c49e40787c13c7c99cbc9af08e76fd9efa15e25b3f`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 5.9 MB (5914553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f6f6b1947c18c1bac715d995f46ce46727337a1ada0c4e7c2f2984a04aecb`  
		Last Modified: Mon, 03 Jun 2024 19:01:04 GMT  
		Size: 1.5 MB (1500680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806b02ef115ec1e534f2d36220b8eb1378cd4c1c96f410c53777e98f2f53a4cc`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:4da5f7d3f531e501a3ee5d389bc618d16c71bb86651fd68109d1f4981c3521d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986ce2397a27ef8d158052d579cb6a3b7b091330a59c01f105c3613c419d96ec`

```dockerfile
```

-	Layers:
	-	`sha256:3b2971fdad01a0613ef3e83c2cb8aab230ab0e62c4706ed98be8e9996b059dc4`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 275.7 KB (275708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cee59000fd2235e2e4bae2324c59b0c5d0288ad38996227843424658929c6c0`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:775a4428a3050de7079c89cff231c7ca54a01750ef752e8956584f4f8aaf76e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687f926297703c36c0b447b824401e090c54ddea35df95e9ac60b4ec2cfacab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199f8807ec47ac7592520ba82c877d9f6e6de8581f5f275abc56366dde16c1e`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 5.9 MB (5863451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7034939efcb080f679b56509133f9446262a4f442bf0c7394b454b1301f8791`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 1.4 MB (1423814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88cb6dc9c9687d4c1e64363a7e442ceab1456f49fb00aa819559ef0f0db699b`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3631380eaad063eb4441aeeb50616e75119a076efa5ee77af875aee22185549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5d75ee09562d929629215ec9ed12f6d436dcf52ad8986145bfa751437e09cc`

```dockerfile
```

-	Layers:
	-	`sha256:74ab8498bb88c256e9c05c7a0d99618dc4453b94584fb9c2c4dc360f08d6a47a`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:51fb29be03522856b8f507ea4df9ba1500972b756133c5bd35bddbca62d88ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d732f429c533cb427cdc7e7e044a83cfd84ced4da7224ac736da16d2c9dc43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444cd28ed296484ff90ddfb993c5cfce9deb7c7ee33a5fdf232fe5728d76ae7`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 292.5 KB (292462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d908fd62c89b1c0b846c14fa9daab8130baecf2d44514d246f96e1a89b6386d1`  
		Last Modified: Wed, 29 May 2024 01:38:47 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e444f239d275345fbcb28de09591b1ce21727483c1005dce419cc2136850fda`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f65578e4b162e83a0db7ae060959bda593a7d3f1774d5df8a3db0daefb184`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 5.4 MB (5351021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9ddad03f4d41f0e3d32a6b453c421c3c9d40d33ce4e2ac44f5ab0daff9a718`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 1.4 MB (1420766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f597d1755326223ce04f920c0eafbb47bf1630a3bc422c26b40698041417a49`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:63b2efa558ce0c277b21c332f0ac76eb069250f04c2bd6e22d86a6c04ca39e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a8dd5917ba43f4ca990fac2e0ce2eb472d317991a141f663eee67969cb8091`

```dockerfile
```

-	Layers:
	-	`sha256:d0f1adf29c41b7079e6776c969549d8fe63a0d2349f3f262e352780c396389b6`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 278.3 KB (278320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d8f39dc5b6142e254a1cfa5b6d44f9b0ee1b56653d76f5de94cff5466ad44a`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:5bec9aca46cc2b81188b8dafd0415a432fefce0b94a93585e6866c635c05860e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98626dc8793adc0d9d1556e0d3019819e6c04c9ab5adc9ec2050ad07a27631b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7130843bbd3e7aec4f18d777d8486e1a31bc676e485de7fbd9674a170777d8e`  
		Last Modified: Tue, 28 May 2024 23:35:05 GMT  
		Size: 295.9 KB (295891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c97ae223460d35ee30ac67c808649bb863398f7373aeff23f0dd033662e29`  
		Last Modified: Tue, 28 May 2024 23:35:07 GMT  
		Size: 66.4 MB (66430055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8885cb230dbccfd815664d1c1a6f3bfa5328a48b9192145c2a16236fb973f8b3`  
		Last Modified: Tue, 28 May 2024 23:35:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434d6eb71e6463f36189c536f37f5e808afd8a2888e4cf6564148bb8e0d568fb`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 6.2 MB (6240121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152d73d2731afedc609d6f5911728ace83ce1c08e1dbcd5460e4cbd48f006d6`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 1.4 MB (1390031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3288aae2d128567448ca4a8038c23cd41eb09e6cc2046a729c45fbe9f88ff9e1`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e52ddd12fdb8d2940ec7abd3835bf37d4cb84f53dbbe0fbed3cbef7396129e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf175f54a787ed0ace3a3b04deef8d8eb90713125b37f236e50a036adfc185`

```dockerfile
```

-	Layers:
	-	`sha256:0d74303319f715f2000d3da32d63018ae9f0c705fa1499bb9372bb231e0bb45d`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 273.8 KB (273846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e85be5da6c5e14cd99bac3703afc52f78692560e39587f4b95b73ce6a5ea02`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-builder` - linux; s390x

```console
$ docker pull caddy@sha256:bbd371f55e5fd21330c24bcfd34a1a8702191867cceb0b340c3b21002c23a3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af99e1c137b5b73332bc84f34766ea766f1369cccc49d900bc35cd805ff0dfc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7fb356c901d4b14e02b6bca1b10852f4a9f85dc695ab3239d771383ee632a5`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 6.2 MB (6179567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62ccaf0be9fd4c408957b5068154bc456143c35dc8c818955199c1cc19412fd`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216b4bc58f3ca32cc60a50bb5a7f1d89bc4c869fcbcc8a3d79cfc455e3a829aa`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a0cd00361f284c2509ee135e57e9ba892603c9babba263a8c9a4019ec816f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea05560489e0436aeabee2b1d096e6ef1883871da7006a5f427be424a1588525`

```dockerfile
```

-	Layers:
	-	`sha256:7a0297889ae2bc64168bf10de6cb03222bf8a8d3915e6eb4e76077607f4f1dca`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 273.8 KB (273754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f562e536bfdd4352eb3a45746b1c36b9bcb4b47e266c037b4ef05073aa9771`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:0e6791b30064fce15067fec856819501eb37e90a3d63c8954f615b1bb9a50cd4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212210875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec756e07bb7339ed40f5aaa265ac85ae87f7cbe499cb07dcb30bae80fca70a5c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:58:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:58:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:58:45 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:58:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:58:58 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:59:04 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:59:05 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:00:17 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:18 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:02:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:48 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:02:49 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90a3c07c43efebd99803cdb9bad2d8149315d6fe71ed67ca3c907554d9e0d9`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d2da37d6aadb3a05b1b91cab3d0735e673ee46930e50eff76541ca6cd703c4`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998290d6ae9e03557ab29c99bdecd95a1646d0b2b6e01375977bc9ca92e7679f`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febc0e57a30d4aaef8d997796e999f07cd8d02fefada73c1d9a8d3b2efb2d0a5`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9634b04a70d192ce4d61fc9cacd9dfe77dc2ce74925adb17ec44604eae27767e`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d148249d3a6d5d5e8a6682e3d3c7577ec3e6c4db642ff5a298431e2aa6015a`  
		Last Modified: Wed, 15 May 2024 22:00:24 GMT  
		Size: 25.4 MB (25444377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abaff09d8cdfae3edceb6c5711ad840eb5f47c5bc4b76b2e6b4da440009de54`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302450cd0c74f7f8c4e0ef1ddc17b877078794558e3bc9ea20be56798e14f0b1`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 345.6 KB (345575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5856fa608f5aaadb2aa345cb0e4e8b4727bc567c776a2ca50b9b9b2ae049ca71`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b86ddf0d69a3769b0f5587cfee9e1dee2b6c0de79f2c6b192fc06caac1639`  
		Last Modified: Wed, 15 May 2024 22:00:32 GMT  
		Size: 71.8 MB (71755992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f91b25b9e6cb7c3077ad2c0725b9b9f62ce4feb0a96fd7c1a075d356fe1b1`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5f7203aa8356980751a8d0d837f026ab70683bb5d98c69c30ec9dfbdd96909`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a29c49e69b7ad65d25803b5ede17ea3a9a1de029f8ed9efba96ae8d8a6ee647`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980757db2f634cea769d2bbf611fabaefc8ef068bf3449adfb4aab3dfc8d82d`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b729eaf00df1c3145830dc1c7b99c931760b57c4ac1cb3c7e089c2daec1b5f40`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b29deaba4982d0ebc1399cdd05eb16d24ab4aeb0b856a15f355845ceb3a2d07`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 2.0 MB (1976480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2eb9ded10797df67ff42377be07f21c463ee93afda3ef414f90864dde3bf2`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8.4-builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:7ec8bed26a5de8b4d209ef792271790786a9034467431218920c382cfbbb6fab
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a48743c09fc4e5f8c297ca67457a44f3de2a7521f27fe42b0bab9e46883c203`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 22:51:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:51:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:51:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:54:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:54:20 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:54:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:54:45 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:58:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:58:59 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:03:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:03:12 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:03:13 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:04:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:04:42 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b721870b6ca4ac86a4dd17a9efa72d3bbbc3e2f4db24604ab3e5529ac9483`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231059aab43e3c4c95c41ffa0eaaf0a505c5a3e17b120dfc894682b1930a3968`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83508e294490f2fa915d9cd65227cc8e8661207b15aa2cfdaf074ff8ae7bb4d4`  
		Last Modified: Wed, 15 May 2024 22:59:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d676bfa2282c568dda9fa4af2f2e6d235ebca82a6c367717bf083bad7dd8b3a`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3161f170f396d7c78bb77ee80c5b634beca05d901f05396abeab4e06be7f5`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c76d7a1b3a9e63480abdc848b1fd30a006301a1e471568b571a209702755daa`  
		Last Modified: Wed, 15 May 2024 22:59:07 GMT  
		Size: 25.6 MB (25574881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dcf82dafd8633a79265dca42870493640409651674a91b43f2adf04c165a`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dac5092add95bf42e98f932737023e0c6ef6ca428f58802291c2cc4c9559b7`  
		Last Modified: Wed, 15 May 2024 22:59:03 GMT  
		Size: 345.9 KB (345903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7992418d5500de5ceeac2fa4f57b54353f18a13b476f19add206e269ef1e6fc`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad77f522384c92c66907f62599064a34ebdd67556de4d2570970de37d46d8`  
		Last Modified: Wed, 15 May 2024 22:59:13 GMT  
		Size: 71.7 MB (71743817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716ef2ea189a02632506ad12bdad7990790c5792d611ac5831fdfa2896ac298`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0238b1a68b5dc8e13a99e71e8c0013bd2b7dfaf127ce1af2e7b6f0b8d52f3`  
		Last Modified: Mon, 03 Jun 2024 19:04:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5109dfca4e11a4fc1d216988f7afe6fa800a6dcef66617d88c19636ab6e50cb7`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081c9df7b06e5088479a8f522501c4643b3179a9b34e5a83fc27ed9d4e5fe539`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b6cca533939895b90c344b768eaf02c53ac76b0a4c97a456d440aba3a8b571`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b805480f52756d99d47ee659a1b21cd0f116bb7fbc8a883a407689bd131635b`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 2.0 MB (1951462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be79ded6647b5f2dfe026d26fc2a855941e795f364266d2bf246cc5c8dc56a`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.4-builder-alpine`

```console
$ docker pull caddy@sha256:9f4c8965330d05617a8228c958c7c67098353fcc75d1703d1a60b269065dde5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2.8.4-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:df570c9c66505c887b2e78591181a8898bc1b8e25110e72ebbe1975b3fe89579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32f73a324a2d0e72a305f33619431bbfaba72840c70d6bec3f65f6e1cde8f6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46b7a5114a614bbc3afd1c49e40787c13c7c99cbc9af08e76fd9efa15e25b3f`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 5.9 MB (5914553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f6f6b1947c18c1bac715d995f46ce46727337a1ada0c4e7c2f2984a04aecb`  
		Last Modified: Mon, 03 Jun 2024 19:01:04 GMT  
		Size: 1.5 MB (1500680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806b02ef115ec1e534f2d36220b8eb1378cd4c1c96f410c53777e98f2f53a4cc`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4da5f7d3f531e501a3ee5d389bc618d16c71bb86651fd68109d1f4981c3521d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986ce2397a27ef8d158052d579cb6a3b7b091330a59c01f105c3613c419d96ec`

```dockerfile
```

-	Layers:
	-	`sha256:3b2971fdad01a0613ef3e83c2cb8aab230ab0e62c4706ed98be8e9996b059dc4`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 275.7 KB (275708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cee59000fd2235e2e4bae2324c59b0c5d0288ad38996227843424658929c6c0`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:775a4428a3050de7079c89cff231c7ca54a01750ef752e8956584f4f8aaf76e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687f926297703c36c0b447b824401e090c54ddea35df95e9ac60b4ec2cfacab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199f8807ec47ac7592520ba82c877d9f6e6de8581f5f275abc56366dde16c1e`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 5.9 MB (5863451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7034939efcb080f679b56509133f9446262a4f442bf0c7394b454b1301f8791`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 1.4 MB (1423814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88cb6dc9c9687d4c1e64363a7e442ceab1456f49fb00aa819559ef0f0db699b`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3631380eaad063eb4441aeeb50616e75119a076efa5ee77af875aee22185549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5d75ee09562d929629215ec9ed12f6d436dcf52ad8986145bfa751437e09cc`

```dockerfile
```

-	Layers:
	-	`sha256:74ab8498bb88c256e9c05c7a0d99618dc4453b94584fb9c2c4dc360f08d6a47a`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:51fb29be03522856b8f507ea4df9ba1500972b756133c5bd35bddbca62d88ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d732f429c533cb427cdc7e7e044a83cfd84ced4da7224ac736da16d2c9dc43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444cd28ed296484ff90ddfb993c5cfce9deb7c7ee33a5fdf232fe5728d76ae7`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 292.5 KB (292462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d908fd62c89b1c0b846c14fa9daab8130baecf2d44514d246f96e1a89b6386d1`  
		Last Modified: Wed, 29 May 2024 01:38:47 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e444f239d275345fbcb28de09591b1ce21727483c1005dce419cc2136850fda`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f65578e4b162e83a0db7ae060959bda593a7d3f1774d5df8a3db0daefb184`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 5.4 MB (5351021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9ddad03f4d41f0e3d32a6b453c421c3c9d40d33ce4e2ac44f5ab0daff9a718`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 1.4 MB (1420766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f597d1755326223ce04f920c0eafbb47bf1630a3bc422c26b40698041417a49`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:63b2efa558ce0c277b21c332f0ac76eb069250f04c2bd6e22d86a6c04ca39e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a8dd5917ba43f4ca990fac2e0ce2eb472d317991a141f663eee67969cb8091`

```dockerfile
```

-	Layers:
	-	`sha256:d0f1adf29c41b7079e6776c969549d8fe63a0d2349f3f262e352780c396389b6`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 278.3 KB (278320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d8f39dc5b6142e254a1cfa5b6d44f9b0ee1b56653d76f5de94cff5466ad44a`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:5bec9aca46cc2b81188b8dafd0415a432fefce0b94a93585e6866c635c05860e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98626dc8793adc0d9d1556e0d3019819e6c04c9ab5adc9ec2050ad07a27631b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7130843bbd3e7aec4f18d777d8486e1a31bc676e485de7fbd9674a170777d8e`  
		Last Modified: Tue, 28 May 2024 23:35:05 GMT  
		Size: 295.9 KB (295891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c97ae223460d35ee30ac67c808649bb863398f7373aeff23f0dd033662e29`  
		Last Modified: Tue, 28 May 2024 23:35:07 GMT  
		Size: 66.4 MB (66430055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8885cb230dbccfd815664d1c1a6f3bfa5328a48b9192145c2a16236fb973f8b3`  
		Last Modified: Tue, 28 May 2024 23:35:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434d6eb71e6463f36189c536f37f5e808afd8a2888e4cf6564148bb8e0d568fb`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 6.2 MB (6240121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152d73d2731afedc609d6f5911728ace83ce1c08e1dbcd5460e4cbd48f006d6`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 1.4 MB (1390031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3288aae2d128567448ca4a8038c23cd41eb09e6cc2046a729c45fbe9f88ff9e1`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e52ddd12fdb8d2940ec7abd3835bf37d4cb84f53dbbe0fbed3cbef7396129e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf175f54a787ed0ace3a3b04deef8d8eb90713125b37f236e50a036adfc185`

```dockerfile
```

-	Layers:
	-	`sha256:0d74303319f715f2000d3da32d63018ae9f0c705fa1499bb9372bb231e0bb45d`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 273.8 KB (273846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e85be5da6c5e14cd99bac3703afc52f78692560e39587f4b95b73ce6a5ea02`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.4-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bbd371f55e5fd21330c24bcfd34a1a8702191867cceb0b340c3b21002c23a3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af99e1c137b5b73332bc84f34766ea766f1369cccc49d900bc35cd805ff0dfc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7fb356c901d4b14e02b6bca1b10852f4a9f85dc695ab3239d771383ee632a5`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 6.2 MB (6179567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62ccaf0be9fd4c408957b5068154bc456143c35dc8c818955199c1cc19412fd`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216b4bc58f3ca32cc60a50bb5a7f1d89bc4c869fcbcc8a3d79cfc455e3a829aa`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.4-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a0cd00361f284c2509ee135e57e9ba892603c9babba263a8c9a4019ec816f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea05560489e0436aeabee2b1d096e6ef1883871da7006a5f427be424a1588525`

```dockerfile
```

-	Layers:
	-	`sha256:7a0297889ae2bc64168bf10de6cb03222bf8a8d3915e6eb4e76077607f4f1dca`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 273.8 KB (273754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f562e536bfdd4352eb3a45746b1c36b9bcb4b47e266c037b4ef05073aa9771`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8.4-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:dcee0b1539d2763646c0ab649486962e588b05ca78d46bf87c7bc0a2d2f39d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.4-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:7ec8bed26a5de8b4d209ef792271790786a9034467431218920c382cfbbb6fab
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a48743c09fc4e5f8c297ca67457a44f3de2a7521f27fe42b0bab9e46883c203`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 22:51:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:51:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:51:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:54:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:54:20 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:54:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:54:45 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:58:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:58:59 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:03:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:03:12 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:03:13 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:04:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:04:42 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b721870b6ca4ac86a4dd17a9efa72d3bbbc3e2f4db24604ab3e5529ac9483`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231059aab43e3c4c95c41ffa0eaaf0a505c5a3e17b120dfc894682b1930a3968`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83508e294490f2fa915d9cd65227cc8e8661207b15aa2cfdaf074ff8ae7bb4d4`  
		Last Modified: Wed, 15 May 2024 22:59:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d676bfa2282c568dda9fa4af2f2e6d235ebca82a6c367717bf083bad7dd8b3a`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3161f170f396d7c78bb77ee80c5b634beca05d901f05396abeab4e06be7f5`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c76d7a1b3a9e63480abdc848b1fd30a006301a1e471568b571a209702755daa`  
		Last Modified: Wed, 15 May 2024 22:59:07 GMT  
		Size: 25.6 MB (25574881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dcf82dafd8633a79265dca42870493640409651674a91b43f2adf04c165a`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dac5092add95bf42e98f932737023e0c6ef6ca428f58802291c2cc4c9559b7`  
		Last Modified: Wed, 15 May 2024 22:59:03 GMT  
		Size: 345.9 KB (345903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7992418d5500de5ceeac2fa4f57b54353f18a13b476f19add206e269ef1e6fc`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad77f522384c92c66907f62599064a34ebdd67556de4d2570970de37d46d8`  
		Last Modified: Wed, 15 May 2024 22:59:13 GMT  
		Size: 71.7 MB (71743817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716ef2ea189a02632506ad12bdad7990790c5792d611ac5831fdfa2896ac298`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0238b1a68b5dc8e13a99e71e8c0013bd2b7dfaf127ce1af2e7b6f0b8d52f3`  
		Last Modified: Mon, 03 Jun 2024 19:04:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5109dfca4e11a4fc1d216988f7afe6fa800a6dcef66617d88c19636ab6e50cb7`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081c9df7b06e5088479a8f522501c4643b3179a9b34e5a83fc27ed9d4e5fe539`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b6cca533939895b90c344b768eaf02c53ac76b0a4c97a456d440aba3a8b571`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b805480f52756d99d47ee659a1b21cd0f116bb7fbc8a883a407689bd131635b`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 2.0 MB (1951462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be79ded6647b5f2dfe026d26fc2a855941e795f364266d2bf246cc5c8dc56a`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.4-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:59f3fab8e735fb586ed740691880ee298cf3caae458593effaf99bdacceaa0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8.4-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:0e6791b30064fce15067fec856819501eb37e90a3d63c8954f615b1bb9a50cd4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212210875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec756e07bb7339ed40f5aaa265ac85ae87f7cbe499cb07dcb30bae80fca70a5c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:58:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:58:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:58:45 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:58:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:58:58 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:59:04 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:59:05 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:00:17 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:18 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:02:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:48 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:02:49 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90a3c07c43efebd99803cdb9bad2d8149315d6fe71ed67ca3c907554d9e0d9`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d2da37d6aadb3a05b1b91cab3d0735e673ee46930e50eff76541ca6cd703c4`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998290d6ae9e03557ab29c99bdecd95a1646d0b2b6e01375977bc9ca92e7679f`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febc0e57a30d4aaef8d997796e999f07cd8d02fefada73c1d9a8d3b2efb2d0a5`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9634b04a70d192ce4d61fc9cacd9dfe77dc2ce74925adb17ec44604eae27767e`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d148249d3a6d5d5e8a6682e3d3c7577ec3e6c4db642ff5a298431e2aa6015a`  
		Last Modified: Wed, 15 May 2024 22:00:24 GMT  
		Size: 25.4 MB (25444377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abaff09d8cdfae3edceb6c5711ad840eb5f47c5bc4b76b2e6b4da440009de54`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302450cd0c74f7f8c4e0ef1ddc17b877078794558e3bc9ea20be56798e14f0b1`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 345.6 KB (345575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5856fa608f5aaadb2aa345cb0e4e8b4727bc567c776a2ca50b9b9b2ae049ca71`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b86ddf0d69a3769b0f5587cfee9e1dee2b6c0de79f2c6b192fc06caac1639`  
		Last Modified: Wed, 15 May 2024 22:00:32 GMT  
		Size: 71.8 MB (71755992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f91b25b9e6cb7c3077ad2c0725b9b9f62ce4feb0a96fd7c1a075d356fe1b1`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5f7203aa8356980751a8d0d837f026ab70683bb5d98c69c30ec9dfbdd96909`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a29c49e69b7ad65d25803b5ede17ea3a9a1de029f8ed9efba96ae8d8a6ee647`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980757db2f634cea769d2bbf611fabaefc8ef068bf3449adfb4aab3dfc8d82d`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b729eaf00df1c3145830dc1c7b99c931760b57c4ac1cb3c7e089c2daec1b5f40`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b29deaba4982d0ebc1399cdd05eb16d24ab4aeb0b856a15f355845ceb3a2d07`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 2.0 MB (1976480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2eb9ded10797df67ff42377be07f21c463ee93afda3ef414f90864dde3bf2`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.4-windowsservercore`

```console
$ docker pull caddy@sha256:a0b338adc338b131f1b4811bd7f95964e764e483c22ab46c1ba97947e90beced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.4-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8.4-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.4-windowsservercore-1809`

```console
$ docker pull caddy@sha256:dbab4057e60d72545d940471196dda51a1c0cbb62ec6fec4bd62a6c6110be70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.4-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.4-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:298ce474adcb68acbbf7d561e3182062bc7c263ef39cfac2632da7d9841bf435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8.4-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:d92bc6499fe7029cf6bf56040d7ffc6584792daa76a39a09dd63228e3561e434
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

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:c092823e9774ccbc7a761d4fd45d49332cc050a4ed13e209c0752fbe77408cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18625893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379e9d34447ebff04422e00130985b166b7fc9cef98876e70d97e6d83269c215`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ecfa782506bda1924ea74bea4182d74f0557cebbf18a71fd48fe97fc6c59c8`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 357.4 KB (357381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94997ff2e374d1bfa99bd1f1a8e8f43cf6e148f63f8e9fe26265ae3d10ca8c9f`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08df330a016638626ff383f490ecf44b254e9ddbae0b4129c2b18c456201e5e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:56 GMT  
		Size: 14.6 MB (14638937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:041cc73927bb91ca88f8e88d7176aa520def52fca3402b730194a040a57b7a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eadb390bbfcd1f11cb6e7d8a95f43d2c71a613fc1e0f23a122e9bf12f4767b`

```dockerfile
```

-	Layers:
	-	`sha256:2f1d323a5412e4d8283ffbbf553b6c8317cfcd3199cff1626166d1fada238a5e`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 263.8 KB (263814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c05f7c8878252295ae4ac295bcdedbd14f7e95ed4ac7e789ad372763a182494`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:66473e2c9d4a1db0ae9bd459956d42d53e9991c58c900251753d648330f3f42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17496054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731a02bd06ee6a92070bf885f12f1dbbbbb736ec9db845b31b5fd8d0f9ec0c42`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30eae165a31e9dfba433ec2953fd144ad11b8b3b833ef35d2566b9fb75a56a`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 357.7 KB (357701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c943ab66970deade36497f4930fc57c4b3c8f30aba0bc7d118ec65b050da491`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb558a164f07a87610adfe7dab44e2f703cc5fd3e8c72f775b7706e2e2e5d3ea`  
		Last Modified: Mon, 03 Jun 2024 20:14:26 GMT  
		Size: 13.8 MB (13765815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:603f2ccec3669ac6a2749b7353e1bc949f166b4e3af650ce31d52b84be0a695d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c14dd01315a75e80a6d6459314782e218de761094d650564e70127e2639069a`

```dockerfile
```

-	Layers:
	-	`sha256:22cc7a81c0b1dd55893d0bd0bb7529a2d0ba81511a60787234b85f74f2bc367f`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d85c3fe08f25f0ff105839b738bc42d3cd0d4b3d804633ea99274c5aaf8838fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17195439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03a1673034f8209e77bd2c19e591b4feb4ebae6b72397a9f294cc1c84ce8983`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e694f733a431bd3ad4ee991d4dab8f760be8e7af16eacaf4bf3a47768fd799`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 354.1 KB (354065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975bb16f920c19614bb988818a5b0554e151e90bda59fa8681309d8b27c4ec89`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959163643e12b18c2516a3514743986aa91426069415a4bda6d18f8206ee9772`  
		Last Modified: Mon, 03 Jun 2024 21:48:35 GMT  
		Size: 13.7 MB (13739856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7e9a460f5b40fa9161b5224a405302787d1cd40fd02b57e29ea38adf50273061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c0a5fe9e0133bc16645e387182bcbfbb594cd603582cfad20279c015a84854`

```dockerfile
```

-	Layers:
	-	`sha256:54e0c5426f56d92b29a5e46ccabe21ffe0344d4f8c2a851ed9d1776cf02307eb`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 263.9 KB (263882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0174d523126387bb17ee8b36c86137b0d32d7434536ff5438d297ce4fc56aaf`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bfbce093116fb3f94ffec6951d6cb067a22cda867b73854e4630954bc3548e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18015071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614062123a347849d270f9e29c9cb8647ae01e7b9463875be85bc1b6924e6bc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='866b6186626d4a7f35d5c010f3f532b022a35dd21f3512bd2015d6de39add0ccc0e8f778878a927ea4a5131ed1dfa8f114b1b9831eaa741f8aebc5c2d88747fd' ;; 		armhf)   binArch='armv6'; checksum='7cb786e8f1af7573ece485f2a9348c3ba7c6191346f5917075027f5cf5309fc0b8e3113e48092fc723d01171cd3c8bdfd076af17e69b1a6c1a9a0d5e53fdf1d2' ;; 		armv7)   binArch='armv7'; checksum='e1a7c02a0986d260ead1ffa9023e78bc1903139813ef5233a06d1f7d621f71ce37eb0042a991287256f85dae64924278514d183bcd805ef0329a096e4574dc06' ;; 		aarch64) binArch='arm64'; checksum='1a619b1ad15fc2163fa597a00b2c6174e6d00b8ce5206d18e0691edf9251ac8dcf1ebf059d7bd065a9ce0b3427071943dd2385d27fa78df0678cefea07280154' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c6d9b6a8db14b4a44de453023ae7b9d6f85b646dfb22a7e4bd5859556fb9cc42e1fb16b3ea5312a2b97bce4ab1f87a71daa430dc57cea09c0dea739409d5434f' ;; 		s390x)   binArch='s390x'; checksum='312ff46594f445d643acbc0d2f118c5af9419dd9e2ea1a8398a8a7772d172ec616d79f83eb4e3550efd26188c3fa1ddff1d9255bb3a55fe6b4384b0db818502a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_DATA_HOME=/data
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/udp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /srv
# Thu, 30 May 2024 14:50:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679b063c3cccee55ed2da27af5dca9a85a3447ab5ea8e8223f2399d695b9e9f`  
		Last Modified: Thu, 30 May 2024 14:41:43 GMT  
		Size: 369.2 KB (369156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3036766387a41a19917f6f36c51dc3d94c3c78b15ec4aa0703d5c7a3094789`  
		Last Modified: Thu, 30 May 2024 14:41:42 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553446b932e7710418d71ee0fa94d83a2d0b6d6de2c8033f103a6c4ee8ac8037`  
		Last Modified: Thu, 30 May 2024 22:40:07 GMT  
		Size: 13.6 MB (13551656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f1ec6ba7f30a7039a101a631a18df1f1a91391309caa49bd0e9e7b95e335523f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 KB (281801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c841bc8bf71a85025aff6456ac07ef330aac19bfae66e33b7973eef4c031019`

```dockerfile
```

-	Layers:
	-	`sha256:58daa084cecd327bebce8ec82a37814b9bc513354002eeaa73370e4fa127cd02`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 263.9 KB (263919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7d58bbbff5474e240bb6c7ac3ee4866a0b9cd4a10541a9b2783a894127c0a8`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3e6afc21f26a045b9cff8dded3a108350486ae0a14e809309a3b6fcbaf2ab44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17239755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dca62d441c172288e8c02545931a5a24e62efb67f3197ae3f98fce961d4ff89`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc90e19cccec8c93b7fc82b34313edb20031c9beb48eba2301ddeea45c3283c2`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 370.4 KB (370398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495869352c1369757545722b0b5a9bdb38f1e4128851a01a45d6a896324eb208`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6255e5da3daad8d4f46b62aad8f74352472eb69509d4a85ddabb97dd5776032a`  
		Last Modified: Tue, 04 Jun 2024 01:47:46 GMT  
		Size: 13.3 MB (13292030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c76863ba66130346110cedfd2bd2346b62eccfdaad6b2d977209af4667f6e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022c234dffa5c4adf5045497989c7751c3e9b547b1a551497603480c7274dee0`

```dockerfile
```

-	Layers:
	-	`sha256:5e4ec7316421ca7d7aff7105fd8504943835e4121422cf9529f52ab819de1d56`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 261.9 KB (261918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64ee8324a31e6505d22eddd274754e4cc07367c231b3f4d616f9761409bd6266`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:5d61f08a2244fdd9670175600ad9e49611e5c5224f3b2b4ea2ce07ac56ab3a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17988811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa45066278353d53895c24f1f52b51c98e1463beb562cbbe8d777a691ef0d333`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9dcde94bf3f93b54ed692d25df606aadecebd0f28dd77d53b2c325c79116a9`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 364.9 KB (364869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129cdd4fd7c6eaafbd0d2ee17d753e1dc55f2b053dfe7eee597a638caec99dbf`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be0dc6e23084d8005f5b12d389c12d178b61dd29787c3eedee3a345071254b`  
		Last Modified: Mon, 03 Jun 2024 21:31:39 GMT  
		Size: 14.2 MB (14156119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a71f8245a1fd40b0a5ede0f920e638a267abfedc83a33ef8f3e1f2b6ef63eb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643cd9393627b6ccbef5905e3848878f075de79071ab70ba90611cc1e8448a2d`

```dockerfile
```

-	Layers:
	-	`sha256:ac2552b9d22cc667e50951ca72233fe141aa9ba5177bfceaf4c6018693a777d0`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 261.9 KB (261860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ae05b2ef2b85ef54cad975979e33c0d69ebc0cb9ff24041f016c7f2ae25182`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder`

```console
$ docker pull caddy@sha256:3db37b69486800de84befa0dd692b4023beb435421703bbdb6f84a8055ddf011
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
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:df570c9c66505c887b2e78591181a8898bc1b8e25110e72ebbe1975b3fe89579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32f73a324a2d0e72a305f33619431bbfaba72840c70d6bec3f65f6e1cde8f6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46b7a5114a614bbc3afd1c49e40787c13c7c99cbc9af08e76fd9efa15e25b3f`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 5.9 MB (5914553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f6f6b1947c18c1bac715d995f46ce46727337a1ada0c4e7c2f2984a04aecb`  
		Last Modified: Mon, 03 Jun 2024 19:01:04 GMT  
		Size: 1.5 MB (1500680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806b02ef115ec1e534f2d36220b8eb1378cd4c1c96f410c53777e98f2f53a4cc`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:4da5f7d3f531e501a3ee5d389bc618d16c71bb86651fd68109d1f4981c3521d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986ce2397a27ef8d158052d579cb6a3b7b091330a59c01f105c3613c419d96ec`

```dockerfile
```

-	Layers:
	-	`sha256:3b2971fdad01a0613ef3e83c2cb8aab230ab0e62c4706ed98be8e9996b059dc4`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 275.7 KB (275708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cee59000fd2235e2e4bae2324c59b0c5d0288ad38996227843424658929c6c0`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:775a4428a3050de7079c89cff231c7ca54a01750ef752e8956584f4f8aaf76e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687f926297703c36c0b447b824401e090c54ddea35df95e9ac60b4ec2cfacab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199f8807ec47ac7592520ba82c877d9f6e6de8581f5f275abc56366dde16c1e`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 5.9 MB (5863451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7034939efcb080f679b56509133f9446262a4f442bf0c7394b454b1301f8791`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 1.4 MB (1423814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88cb6dc9c9687d4c1e64363a7e442ceab1456f49fb00aa819559ef0f0db699b`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3631380eaad063eb4441aeeb50616e75119a076efa5ee77af875aee22185549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5d75ee09562d929629215ec9ed12f6d436dcf52ad8986145bfa751437e09cc`

```dockerfile
```

-	Layers:
	-	`sha256:74ab8498bb88c256e9c05c7a0d99618dc4453b94584fb9c2c4dc360f08d6a47a`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:51fb29be03522856b8f507ea4df9ba1500972b756133c5bd35bddbca62d88ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d732f429c533cb427cdc7e7e044a83cfd84ced4da7224ac736da16d2c9dc43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444cd28ed296484ff90ddfb993c5cfce9deb7c7ee33a5fdf232fe5728d76ae7`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 292.5 KB (292462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d908fd62c89b1c0b846c14fa9daab8130baecf2d44514d246f96e1a89b6386d1`  
		Last Modified: Wed, 29 May 2024 01:38:47 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e444f239d275345fbcb28de09591b1ce21727483c1005dce419cc2136850fda`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f65578e4b162e83a0db7ae060959bda593a7d3f1774d5df8a3db0daefb184`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 5.4 MB (5351021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9ddad03f4d41f0e3d32a6b453c421c3c9d40d33ce4e2ac44f5ab0daff9a718`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 1.4 MB (1420766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f597d1755326223ce04f920c0eafbb47bf1630a3bc422c26b40698041417a49`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:63b2efa558ce0c277b21c332f0ac76eb069250f04c2bd6e22d86a6c04ca39e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a8dd5917ba43f4ca990fac2e0ce2eb472d317991a141f663eee67969cb8091`

```dockerfile
```

-	Layers:
	-	`sha256:d0f1adf29c41b7079e6776c969549d8fe63a0d2349f3f262e352780c396389b6`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 278.3 KB (278320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d8f39dc5b6142e254a1cfa5b6d44f9b0ee1b56653d76f5de94cff5466ad44a`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f0e70454943d37a64344820181d8396714d91d40ffd3a04844076a3b41d69a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78085757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb59a6bfcf30a2dfc3705ca6f25183cd395301a7a185380c978cea1117557ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SETCAP=1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 30 May 2024 14:50:16 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fd4d77c1150ba7c64d2b9cb1ad73058c134eea51cdf8a7c969379c3fe358c3`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6930e6242b08ff7992e85b10519d54167d7ffdedf7199e086b7c8be95e4baf6`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d49fbb06d2ec1fb8e7c2633794d12f435fe6098384a1ba28e82e7be07d06a38`  
		Last Modified: Thu, 30 May 2024 14:42:18 GMT  
		Size: 6.0 MB (6033730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31dd998a75477c407a2dee8c594a80ba41fdac4dd42d9d67a7c414c4c8997b9`  
		Last Modified: Thu, 30 May 2024 22:40:31 GMT  
		Size: 1.4 MB (1397169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770803ae5abd93eb1dcbc65ce6b1ccdfd01a538b7c537f05e868e88c81d9d430`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:acae0dfa758b68833a5e19bd4804c3a3916e795ee6dde565fc338a83efe0a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 KB (295844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de6d746bee70c9e18f38b0e19e943d1a7fcdb8b1b73856d337570218ce8c0bb`

```dockerfile
```

-	Layers:
	-	`sha256:1abefdba7275d0ce20e30a7257a2ed4eae90e1997c2acdafc5dae8ae0afccec3`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 275.8 KB (275813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5fee8e57abbb9909e5460f0b9e029723da0ba965f905c8d24ee042cab953b8`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:5bec9aca46cc2b81188b8dafd0415a432fefce0b94a93585e6866c635c05860e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98626dc8793adc0d9d1556e0d3019819e6c04c9ab5adc9ec2050ad07a27631b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7130843bbd3e7aec4f18d777d8486e1a31bc676e485de7fbd9674a170777d8e`  
		Last Modified: Tue, 28 May 2024 23:35:05 GMT  
		Size: 295.9 KB (295891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c97ae223460d35ee30ac67c808649bb863398f7373aeff23f0dd033662e29`  
		Last Modified: Tue, 28 May 2024 23:35:07 GMT  
		Size: 66.4 MB (66430055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8885cb230dbccfd815664d1c1a6f3bfa5328a48b9192145c2a16236fb973f8b3`  
		Last Modified: Tue, 28 May 2024 23:35:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434d6eb71e6463f36189c536f37f5e808afd8a2888e4cf6564148bb8e0d568fb`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 6.2 MB (6240121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152d73d2731afedc609d6f5911728ace83ce1c08e1dbcd5460e4cbd48f006d6`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 1.4 MB (1390031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3288aae2d128567448ca4a8038c23cd41eb09e6cc2046a729c45fbe9f88ff9e1`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:e52ddd12fdb8d2940ec7abd3835bf37d4cb84f53dbbe0fbed3cbef7396129e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf175f54a787ed0ace3a3b04deef8d8eb90713125b37f236e50a036adfc185`

```dockerfile
```

-	Layers:
	-	`sha256:0d74303319f715f2000d3da32d63018ae9f0c705fa1499bb9372bb231e0bb45d`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 273.8 KB (273846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e85be5da6c5e14cd99bac3703afc52f78692560e39587f4b95b73ce6a5ea02`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:bbd371f55e5fd21330c24bcfd34a1a8702191867cceb0b340c3b21002c23a3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af99e1c137b5b73332bc84f34766ea766f1369cccc49d900bc35cd805ff0dfc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7fb356c901d4b14e02b6bca1b10852f4a9f85dc695ab3239d771383ee632a5`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 6.2 MB (6179567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62ccaf0be9fd4c408957b5068154bc456143c35dc8c818955199c1cc19412fd`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216b4bc58f3ca32cc60a50bb5a7f1d89bc4c869fcbcc8a3d79cfc455e3a829aa`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a0cd00361f284c2509ee135e57e9ba892603c9babba263a8c9a4019ec816f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea05560489e0436aeabee2b1d096e6ef1883871da7006a5f427be424a1588525`

```dockerfile
```

-	Layers:
	-	`sha256:7a0297889ae2bc64168bf10de6cb03222bf8a8d3915e6eb4e76077607f4f1dca`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 273.8 KB (273754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f562e536bfdd4352eb3a45746b1c36b9bcb4b47e266c037b4ef05073aa9771`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:0e6791b30064fce15067fec856819501eb37e90a3d63c8954f615b1bb9a50cd4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212210875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec756e07bb7339ed40f5aaa265ac85ae87f7cbe499cb07dcb30bae80fca70a5c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:58:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:58:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:58:45 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:58:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:58:58 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:59:04 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:59:05 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:00:17 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:18 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:02:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:48 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:02:49 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90a3c07c43efebd99803cdb9bad2d8149315d6fe71ed67ca3c907554d9e0d9`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d2da37d6aadb3a05b1b91cab3d0735e673ee46930e50eff76541ca6cd703c4`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998290d6ae9e03557ab29c99bdecd95a1646d0b2b6e01375977bc9ca92e7679f`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febc0e57a30d4aaef8d997796e999f07cd8d02fefada73c1d9a8d3b2efb2d0a5`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9634b04a70d192ce4d61fc9cacd9dfe77dc2ce74925adb17ec44604eae27767e`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d148249d3a6d5d5e8a6682e3d3c7577ec3e6c4db642ff5a298431e2aa6015a`  
		Last Modified: Wed, 15 May 2024 22:00:24 GMT  
		Size: 25.4 MB (25444377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abaff09d8cdfae3edceb6c5711ad840eb5f47c5bc4b76b2e6b4da440009de54`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302450cd0c74f7f8c4e0ef1ddc17b877078794558e3bc9ea20be56798e14f0b1`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 345.6 KB (345575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5856fa608f5aaadb2aa345cb0e4e8b4727bc567c776a2ca50b9b9b2ae049ca71`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b86ddf0d69a3769b0f5587cfee9e1dee2b6c0de79f2c6b192fc06caac1639`  
		Last Modified: Wed, 15 May 2024 22:00:32 GMT  
		Size: 71.8 MB (71755992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f91b25b9e6cb7c3077ad2c0725b9b9f62ce4feb0a96fd7c1a075d356fe1b1`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5f7203aa8356980751a8d0d837f026ab70683bb5d98c69c30ec9dfbdd96909`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a29c49e69b7ad65d25803b5ede17ea3a9a1de029f8ed9efba96ae8d8a6ee647`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980757db2f634cea769d2bbf611fabaefc8ef068bf3449adfb4aab3dfc8d82d`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b729eaf00df1c3145830dc1c7b99c931760b57c4ac1cb3c7e089c2daec1b5f40`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b29deaba4982d0ebc1399cdd05eb16d24ab4aeb0b856a15f355845ceb3a2d07`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 2.0 MB (1976480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2eb9ded10797df67ff42377be07f21c463ee93afda3ef414f90864dde3bf2`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:7ec8bed26a5de8b4d209ef792271790786a9034467431218920c382cfbbb6fab
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a48743c09fc4e5f8c297ca67457a44f3de2a7521f27fe42b0bab9e46883c203`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 22:51:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:51:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:51:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:54:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:54:20 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:54:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:54:45 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:58:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:58:59 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:03:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:03:12 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:03:13 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:04:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:04:42 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b721870b6ca4ac86a4dd17a9efa72d3bbbc3e2f4db24604ab3e5529ac9483`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231059aab43e3c4c95c41ffa0eaaf0a505c5a3e17b120dfc894682b1930a3968`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83508e294490f2fa915d9cd65227cc8e8661207b15aa2cfdaf074ff8ae7bb4d4`  
		Last Modified: Wed, 15 May 2024 22:59:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d676bfa2282c568dda9fa4af2f2e6d235ebca82a6c367717bf083bad7dd8b3a`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3161f170f396d7c78bb77ee80c5b634beca05d901f05396abeab4e06be7f5`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c76d7a1b3a9e63480abdc848b1fd30a006301a1e471568b571a209702755daa`  
		Last Modified: Wed, 15 May 2024 22:59:07 GMT  
		Size: 25.6 MB (25574881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dcf82dafd8633a79265dca42870493640409651674a91b43f2adf04c165a`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dac5092add95bf42e98f932737023e0c6ef6ca428f58802291c2cc4c9559b7`  
		Last Modified: Wed, 15 May 2024 22:59:03 GMT  
		Size: 345.9 KB (345903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7992418d5500de5ceeac2fa4f57b54353f18a13b476f19add206e269ef1e6fc`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad77f522384c92c66907f62599064a34ebdd67556de4d2570970de37d46d8`  
		Last Modified: Wed, 15 May 2024 22:59:13 GMT  
		Size: 71.7 MB (71743817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716ef2ea189a02632506ad12bdad7990790c5792d611ac5831fdfa2896ac298`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0238b1a68b5dc8e13a99e71e8c0013bd2b7dfaf127ce1af2e7b6f0b8d52f3`  
		Last Modified: Mon, 03 Jun 2024 19:04:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5109dfca4e11a4fc1d216988f7afe6fa800a6dcef66617d88c19636ab6e50cb7`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081c9df7b06e5088479a8f522501c4643b3179a9b34e5a83fc27ed9d4e5fe539`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b6cca533939895b90c344b768eaf02c53ac76b0a4c97a456d440aba3a8b571`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b805480f52756d99d47ee659a1b21cd0f116bb7fbc8a883a407689bd131635b`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 2.0 MB (1951462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be79ded6647b5f2dfe026d26fc2a855941e795f364266d2bf246cc5c8dc56a`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:1bb8f3d134ec8113c17d4ea0e073e94944f4bce8c7429055f2fa6168e36ab96b
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

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:df570c9c66505c887b2e78591181a8898bc1b8e25110e72ebbe1975b3fe89579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32f73a324a2d0e72a305f33619431bbfaba72840c70d6bec3f65f6e1cde8f6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46b7a5114a614bbc3afd1c49e40787c13c7c99cbc9af08e76fd9efa15e25b3f`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 5.9 MB (5914553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f6f6b1947c18c1bac715d995f46ce46727337a1ada0c4e7c2f2984a04aecb`  
		Last Modified: Mon, 03 Jun 2024 19:01:04 GMT  
		Size: 1.5 MB (1500680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806b02ef115ec1e534f2d36220b8eb1378cd4c1c96f410c53777e98f2f53a4cc`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4da5f7d3f531e501a3ee5d389bc618d16c71bb86651fd68109d1f4981c3521d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986ce2397a27ef8d158052d579cb6a3b7b091330a59c01f105c3613c419d96ec`

```dockerfile
```

-	Layers:
	-	`sha256:3b2971fdad01a0613ef3e83c2cb8aab230ab0e62c4706ed98be8e9996b059dc4`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 275.7 KB (275708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cee59000fd2235e2e4bae2324c59b0c5d0288ad38996227843424658929c6c0`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:775a4428a3050de7079c89cff231c7ca54a01750ef752e8956584f4f8aaf76e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687f926297703c36c0b447b824401e090c54ddea35df95e9ac60b4ec2cfacab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b926c4213f62dccc19847129b4de9c528cedb231ca46aa95c9bc8603cc739f`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 293.6 KB (293627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55093d222540f79eba4e3ad81fd00f65a988f24d5900796c91eb04223727a4`  
		Last Modified: Wed, 29 May 2024 00:35:26 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3af59e8dedc847da2d87ea38022fe188427a7a19f10ccd50c70802491db23`  
		Last Modified: Wed, 29 May 2024 00:35:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199f8807ec47ac7592520ba82c877d9f6e6de8581f5f275abc56366dde16c1e`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 5.9 MB (5863451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7034939efcb080f679b56509133f9446262a4f442bf0c7394b454b1301f8791`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 1.4 MB (1423814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88cb6dc9c9687d4c1e64363a7e442ceab1456f49fb00aa819559ef0f0db699b`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3631380eaad063eb4441aeeb50616e75119a076efa5ee77af875aee22185549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5d75ee09562d929629215ec9ed12f6d436dcf52ad8986145bfa751437e09cc`

```dockerfile
```

-	Layers:
	-	`sha256:74ab8498bb88c256e9c05c7a0d99618dc4453b94584fb9c2c4dc360f08d6a47a`  
		Last Modified: Mon, 03 Jun 2024 20:14:54 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:51fb29be03522856b8f507ea4df9ba1500972b756133c5bd35bddbca62d88ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d732f429c533cb427cdc7e7e044a83cfd84ced4da7224ac736da16d2c9dc43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444cd28ed296484ff90ddfb993c5cfce9deb7c7ee33a5fdf232fe5728d76ae7`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 292.5 KB (292462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d908fd62c89b1c0b846c14fa9daab8130baecf2d44514d246f96e1a89b6386d1`  
		Last Modified: Wed, 29 May 2024 01:38:47 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e444f239d275345fbcb28de09591b1ce21727483c1005dce419cc2136850fda`  
		Last Modified: Wed, 29 May 2024 01:38:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f65578e4b162e83a0db7ae060959bda593a7d3f1774d5df8a3db0daefb184`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 5.4 MB (5351021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9ddad03f4d41f0e3d32a6b453c421c3c9d40d33ce4e2ac44f5ab0daff9a718`  
		Last Modified: Mon, 03 Jun 2024 21:49:10 GMT  
		Size: 1.4 MB (1420766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f597d1755326223ce04f920c0eafbb47bf1630a3bc422c26b40698041417a49`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:63b2efa558ce0c277b21c332f0ac76eb069250f04c2bd6e22d86a6c04ca39e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a8dd5917ba43f4ca990fac2e0ce2eb472d317991a141f663eee67969cb8091`

```dockerfile
```

-	Layers:
	-	`sha256:d0f1adf29c41b7079e6776c969549d8fe63a0d2349f3f262e352780c396389b6`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 278.3 KB (278320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d8f39dc5b6142e254a1cfa5b6d44f9b0ee1b56653d76f5de94cff5466ad44a`  
		Last Modified: Mon, 03 Jun 2024 21:49:09 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f0e70454943d37a64344820181d8396714d91d40ffd3a04844076a3b41d69a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78085757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb59a6bfcf30a2dfc3705ca6f25183cd395301a7a185380c978cea1117557ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SETCAP=1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 30 May 2024 14:50:16 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fd4d77c1150ba7c64d2b9cb1ad73058c134eea51cdf8a7c969379c3fe358c3`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6930e6242b08ff7992e85b10519d54167d7ffdedf7199e086b7c8be95e4baf6`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d49fbb06d2ec1fb8e7c2633794d12f435fe6098384a1ba28e82e7be07d06a38`  
		Last Modified: Thu, 30 May 2024 14:42:18 GMT  
		Size: 6.0 MB (6033730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31dd998a75477c407a2dee8c594a80ba41fdac4dd42d9d67a7c414c4c8997b9`  
		Last Modified: Thu, 30 May 2024 22:40:31 GMT  
		Size: 1.4 MB (1397169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770803ae5abd93eb1dcbc65ce6b1ccdfd01a538b7c537f05e868e88c81d9d430`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:acae0dfa758b68833a5e19bd4804c3a3916e795ee6dde565fc338a83efe0a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 KB (295844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de6d746bee70c9e18f38b0e19e943d1a7fcdb8b1b73856d337570218ce8c0bb`

```dockerfile
```

-	Layers:
	-	`sha256:1abefdba7275d0ce20e30a7257a2ed4eae90e1997c2acdafc5dae8ae0afccec3`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 275.8 KB (275813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5fee8e57abbb9909e5460f0b9e029723da0ba965f905c8d24ee042cab953b8`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:5bec9aca46cc2b81188b8dafd0415a432fefce0b94a93585e6866c635c05860e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98626dc8793adc0d9d1556e0d3019819e6c04c9ab5adc9ec2050ad07a27631b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7130843bbd3e7aec4f18d777d8486e1a31bc676e485de7fbd9674a170777d8e`  
		Last Modified: Tue, 28 May 2024 23:35:05 GMT  
		Size: 295.9 KB (295891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c97ae223460d35ee30ac67c808649bb863398f7373aeff23f0dd033662e29`  
		Last Modified: Tue, 28 May 2024 23:35:07 GMT  
		Size: 66.4 MB (66430055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8885cb230dbccfd815664d1c1a6f3bfa5328a48b9192145c2a16236fb973f8b3`  
		Last Modified: Tue, 28 May 2024 23:35:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434d6eb71e6463f36189c536f37f5e808afd8a2888e4cf6564148bb8e0d568fb`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 6.2 MB (6240121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152d73d2731afedc609d6f5911728ace83ce1c08e1dbcd5460e4cbd48f006d6`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 1.4 MB (1390031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3288aae2d128567448ca4a8038c23cd41eb09e6cc2046a729c45fbe9f88ff9e1`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e52ddd12fdb8d2940ec7abd3835bf37d4cb84f53dbbe0fbed3cbef7396129e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf175f54a787ed0ace3a3b04deef8d8eb90713125b37f236e50a036adfc185`

```dockerfile
```

-	Layers:
	-	`sha256:0d74303319f715f2000d3da32d63018ae9f0c705fa1499bb9372bb231e0bb45d`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 273.8 KB (273846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e85be5da6c5e14cd99bac3703afc52f78692560e39587f4b95b73ce6a5ea02`  
		Last Modified: Tue, 04 Jun 2024 01:48:32 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bbd371f55e5fd21330c24bcfd34a1a8702191867cceb0b340c3b21002c23a3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af99e1c137b5b73332bc84f34766ea766f1369cccc49d900bc35cd805ff0dfc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7fb356c901d4b14e02b6bca1b10852f4a9f85dc695ab3239d771383ee632a5`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 6.2 MB (6179567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62ccaf0be9fd4c408957b5068154bc456143c35dc8c818955199c1cc19412fd`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216b4bc58f3ca32cc60a50bb5a7f1d89bc4c869fcbcc8a3d79cfc455e3a829aa`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a0cd00361f284c2509ee135e57e9ba892603c9babba263a8c9a4019ec816f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea05560489e0436aeabee2b1d096e6ef1883871da7006a5f427be424a1588525`

```dockerfile
```

-	Layers:
	-	`sha256:7a0297889ae2bc64168bf10de6cb03222bf8a8d3915e6eb4e76077607f4f1dca`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 273.8 KB (273754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f562e536bfdd4352eb3a45746b1c36b9bcb4b47e266c037b4ef05073aa9771`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:dcee0b1539d2763646c0ab649486962e588b05ca78d46bf87c7bc0a2d2f39d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:7ec8bed26a5de8b4d209ef792271790786a9034467431218920c382cfbbb6fab
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a48743c09fc4e5f8c297ca67457a44f3de2a7521f27fe42b0bab9e46883c203`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 22:51:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:51:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:51:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:54:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:54:20 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:54:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:54:45 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:58:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:58:59 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:03:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:03:12 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:03:13 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:04:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:04:42 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b721870b6ca4ac86a4dd17a9efa72d3bbbc3e2f4db24604ab3e5529ac9483`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231059aab43e3c4c95c41ffa0eaaf0a505c5a3e17b120dfc894682b1930a3968`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83508e294490f2fa915d9cd65227cc8e8661207b15aa2cfdaf074ff8ae7bb4d4`  
		Last Modified: Wed, 15 May 2024 22:59:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d676bfa2282c568dda9fa4af2f2e6d235ebca82a6c367717bf083bad7dd8b3a`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3161f170f396d7c78bb77ee80c5b634beca05d901f05396abeab4e06be7f5`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c76d7a1b3a9e63480abdc848b1fd30a006301a1e471568b571a209702755daa`  
		Last Modified: Wed, 15 May 2024 22:59:07 GMT  
		Size: 25.6 MB (25574881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dcf82dafd8633a79265dca42870493640409651674a91b43f2adf04c165a`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dac5092add95bf42e98f932737023e0c6ef6ca428f58802291c2cc4c9559b7`  
		Last Modified: Wed, 15 May 2024 22:59:03 GMT  
		Size: 345.9 KB (345903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7992418d5500de5ceeac2fa4f57b54353f18a13b476f19add206e269ef1e6fc`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad77f522384c92c66907f62599064a34ebdd67556de4d2570970de37d46d8`  
		Last Modified: Wed, 15 May 2024 22:59:13 GMT  
		Size: 71.7 MB (71743817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716ef2ea189a02632506ad12bdad7990790c5792d611ac5831fdfa2896ac298`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb0238b1a68b5dc8e13a99e71e8c0013bd2b7dfaf127ce1af2e7b6f0b8d52f3`  
		Last Modified: Mon, 03 Jun 2024 19:04:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5109dfca4e11a4fc1d216988f7afe6fa800a6dcef66617d88c19636ab6e50cb7`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081c9df7b06e5088479a8f522501c4643b3179a9b34e5a83fc27ed9d4e5fe539`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b6cca533939895b90c344b768eaf02c53ac76b0a4c97a456d440aba3a8b571`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b805480f52756d99d47ee659a1b21cd0f116bb7fbc8a883a407689bd131635b`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 2.0 MB (1951462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99be79ded6647b5f2dfe026d26fc2a855941e795f364266d2bf246cc5c8dc56a`  
		Last Modified: Mon, 03 Jun 2024 19:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:59f3fab8e735fb586ed740691880ee298cf3caae458593effaf99bdacceaa0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:0e6791b30064fce15067fec856819501eb37e90a3d63c8954f615b1bb9a50cd4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212210875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec756e07bb7339ed40f5aaa265ac85ae87f7cbe499cb07dcb30bae80fca70a5c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:58:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:58:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:58:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:58:45 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:58:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:58:58 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:59:04 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:59:05 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:00:17 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:00:18 GMT
WORKDIR C:\go
# Mon, 03 Jun 2024 19:02:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:48 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 19:02:49 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90a3c07c43efebd99803cdb9bad2d8149315d6fe71ed67ca3c907554d9e0d9`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d2da37d6aadb3a05b1b91cab3d0735e673ee46930e50eff76541ca6cd703c4`  
		Last Modified: Wed, 15 May 2024 22:00:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998290d6ae9e03557ab29c99bdecd95a1646d0b2b6e01375977bc9ca92e7679f`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febc0e57a30d4aaef8d997796e999f07cd8d02fefada73c1d9a8d3b2efb2d0a5`  
		Last Modified: Wed, 15 May 2024 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9634b04a70d192ce4d61fc9cacd9dfe77dc2ce74925adb17ec44604eae27767e`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d148249d3a6d5d5e8a6682e3d3c7577ec3e6c4db642ff5a298431e2aa6015a`  
		Last Modified: Wed, 15 May 2024 22:00:24 GMT  
		Size: 25.4 MB (25444377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abaff09d8cdfae3edceb6c5711ad840eb5f47c5bc4b76b2e6b4da440009de54`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302450cd0c74f7f8c4e0ef1ddc17b877078794558e3bc9ea20be56798e14f0b1`  
		Last Modified: Wed, 15 May 2024 22:00:21 GMT  
		Size: 345.6 KB (345575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5856fa608f5aaadb2aa345cb0e4e8b4727bc567c776a2ca50b9b9b2ae049ca71`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b86ddf0d69a3769b0f5587cfee9e1dee2b6c0de79f2c6b192fc06caac1639`  
		Last Modified: Wed, 15 May 2024 22:00:32 GMT  
		Size: 71.8 MB (71755992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f91b25b9e6cb7c3077ad2c0725b9b9f62ce4feb0a96fd7c1a075d356fe1b1`  
		Last Modified: Wed, 15 May 2024 22:00:20 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5f7203aa8356980751a8d0d837f026ab70683bb5d98c69c30ec9dfbdd96909`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a29c49e69b7ad65d25803b5ede17ea3a9a1de029f8ed9efba96ae8d8a6ee647`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980757db2f634cea769d2bbf611fabaefc8ef068bf3449adfb4aab3dfc8d82d`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b729eaf00df1c3145830dc1c7b99c931760b57c4ac1cb3c7e089c2daec1b5f40`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b29deaba4982d0ebc1399cdd05eb16d24ab4aeb0b856a15f355845ceb3a2d07`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 2.0 MB (1976480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2eb9ded10797df67ff42377be07f21c463ee93afda3ef414f90864dde3bf2`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:f848613a14e81ddf87d67c67f3b011be5849068fd2cc8ab8d1c421b153f74fcc
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
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:c092823e9774ccbc7a761d4fd45d49332cc050a4ed13e209c0752fbe77408cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18625893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379e9d34447ebff04422e00130985b166b7fc9cef98876e70d97e6d83269c215`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ecfa782506bda1924ea74bea4182d74f0557cebbf18a71fd48fe97fc6c59c8`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 357.4 KB (357381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94997ff2e374d1bfa99bd1f1a8e8f43cf6e148f63f8e9fe26265ae3d10ca8c9f`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08df330a016638626ff383f490ecf44b254e9ddbae0b4129c2b18c456201e5e3`  
		Last Modified: Mon, 03 Jun 2024 19:00:56 GMT  
		Size: 14.6 MB (14638937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:041cc73927bb91ca88f8e88d7176aa520def52fca3402b730194a040a57b7a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64eadb390bbfcd1f11cb6e7d8a95f43d2c71a613fc1e0f23a122e9bf12f4767b`

```dockerfile
```

-	Layers:
	-	`sha256:2f1d323a5412e4d8283ffbbf553b6c8317cfcd3199cff1626166d1fada238a5e`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 263.8 KB (263814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c05f7c8878252295ae4ac295bcdedbd14f7e95ed4ac7e789ad372763a182494`  
		Last Modified: Mon, 03 Jun 2024 19:00:55 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:66473e2c9d4a1db0ae9bd459956d42d53e9991c58c900251753d648330f3f42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17496054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731a02bd06ee6a92070bf885f12f1dbbbbb736ec9db845b31b5fd8d0f9ec0c42`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc30eae165a31e9dfba433ec2953fd144ad11b8b3b833ef35d2566b9fb75a56a`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 357.7 KB (357701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c943ab66970deade36497f4930fc57c4b3c8f30aba0bc7d118ec65b050da491`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb558a164f07a87610adfe7dab44e2f703cc5fd3e8c72f775b7706e2e2e5d3ea`  
		Last Modified: Mon, 03 Jun 2024 20:14:26 GMT  
		Size: 13.8 MB (13765815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:603f2ccec3669ac6a2749b7353e1bc949f166b4e3af650ce31d52b84be0a695d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c14dd01315a75e80a6d6459314782e218de761094d650564e70127e2639069a`

```dockerfile
```

-	Layers:
	-	`sha256:22cc7a81c0b1dd55893d0bd0bb7529a2d0ba81511a60787234b85f74f2bc367f`  
		Last Modified: Mon, 03 Jun 2024 20:14:25 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d85c3fe08f25f0ff105839b738bc42d3cd0d4b3d804633ea99274c5aaf8838fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17195439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03a1673034f8209e77bd2c19e591b4feb4ebae6b72397a9f294cc1c84ce8983`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e694f733a431bd3ad4ee991d4dab8f760be8e7af16eacaf4bf3a47768fd799`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 354.1 KB (354065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975bb16f920c19614bb988818a5b0554e151e90bda59fa8681309d8b27c4ec89`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959163643e12b18c2516a3514743986aa91426069415a4bda6d18f8206ee9772`  
		Last Modified: Mon, 03 Jun 2024 21:48:35 GMT  
		Size: 13.7 MB (13739856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:7e9a460f5b40fa9161b5224a405302787d1cd40fd02b57e29ea38adf50273061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c0a5fe9e0133bc16645e387182bcbfbb594cd603582cfad20279c015a84854`

```dockerfile
```

-	Layers:
	-	`sha256:54e0c5426f56d92b29a5e46ccabe21ffe0344d4f8c2a851ed9d1776cf02307eb`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 263.9 KB (263882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0174d523126387bb17ee8b36c86137b0d32d7434536ff5438d297ce4fc56aaf`  
		Last Modified: Mon, 03 Jun 2024 21:48:34 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bfbce093116fb3f94ffec6951d6cb067a22cda867b73854e4630954bc3548e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18015071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614062123a347849d270f9e29c9cb8647ae01e7b9463875be85bc1b6924e6bc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='866b6186626d4a7f35d5c010f3f532b022a35dd21f3512bd2015d6de39add0ccc0e8f778878a927ea4a5131ed1dfa8f114b1b9831eaa741f8aebc5c2d88747fd' ;; 		armhf)   binArch='armv6'; checksum='7cb786e8f1af7573ece485f2a9348c3ba7c6191346f5917075027f5cf5309fc0b8e3113e48092fc723d01171cd3c8bdfd076af17e69b1a6c1a9a0d5e53fdf1d2' ;; 		armv7)   binArch='armv7'; checksum='e1a7c02a0986d260ead1ffa9023e78bc1903139813ef5233a06d1f7d621f71ce37eb0042a991287256f85dae64924278514d183bcd805ef0329a096e4574dc06' ;; 		aarch64) binArch='arm64'; checksum='1a619b1ad15fc2163fa597a00b2c6174e6d00b8ce5206d18e0691edf9251ac8dcf1ebf059d7bd065a9ce0b3427071943dd2385d27fa78df0678cefea07280154' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c6d9b6a8db14b4a44de453023ae7b9d6f85b646dfb22a7e4bd5859556fb9cc42e1fb16b3ea5312a2b97bce4ab1f87a71daa430dc57cea09c0dea739409d5434f' ;; 		s390x)   binArch='s390x'; checksum='312ff46594f445d643acbc0d2f118c5af9419dd9e2ea1a8398a8a7772d172ec616d79f83eb4e3550efd26188c3fa1ddff1d9255bb3a55fe6b4384b0db818502a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 30 May 2024 14:50:16 GMT
ENV XDG_DATA_HOME=/data
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 14:50:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[443/udp:{}]
# Thu, 30 May 2024 14:50:16 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /srv
# Thu, 30 May 2024 14:50:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679b063c3cccee55ed2da27af5dca9a85a3447ab5ea8e8223f2399d695b9e9f`  
		Last Modified: Thu, 30 May 2024 14:41:43 GMT  
		Size: 369.2 KB (369156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3036766387a41a19917f6f36c51dc3d94c3c78b15ec4aa0703d5c7a3094789`  
		Last Modified: Thu, 30 May 2024 14:41:42 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553446b932e7710418d71ee0fa94d83a2d0b6d6de2c8033f103a6c4ee8ac8037`  
		Last Modified: Thu, 30 May 2024 22:40:07 GMT  
		Size: 13.6 MB (13551656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:f1ec6ba7f30a7039a101a631a18df1f1a91391309caa49bd0e9e7b95e335523f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 KB (281801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c841bc8bf71a85025aff6456ac07ef330aac19bfae66e33b7973eef4c031019`

```dockerfile
```

-	Layers:
	-	`sha256:58daa084cecd327bebce8ec82a37814b9bc513354002eeaa73370e4fa127cd02`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 263.9 KB (263919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7d58bbbff5474e240bb6c7ac3ee4866a0b9cd4a10541a9b2783a894127c0a8`  
		Last Modified: Thu, 30 May 2024 22:40:06 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:3e6afc21f26a045b9cff8dded3a108350486ae0a14e809309a3b6fcbaf2ab44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17239755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dca62d441c172288e8c02545931a5a24e62efb67f3197ae3f98fce961d4ff89`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc90e19cccec8c93b7fc82b34313edb20031c9beb48eba2301ddeea45c3283c2`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 370.4 KB (370398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495869352c1369757545722b0b5a9bdb38f1e4128851a01a45d6a896324eb208`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6255e5da3daad8d4f46b62aad8f74352472eb69509d4a85ddabb97dd5776032a`  
		Last Modified: Tue, 04 Jun 2024 01:47:46 GMT  
		Size: 13.3 MB (13292030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:c76863ba66130346110cedfd2bd2346b62eccfdaad6b2d977209af4667f6e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022c234dffa5c4adf5045497989c7751c3e9b547b1a551497603480c7274dee0`

```dockerfile
```

-	Layers:
	-	`sha256:5e4ec7316421ca7d7aff7105fd8504943835e4121422cf9529f52ab819de1d56`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 261.9 KB (261918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64ee8324a31e6505d22eddd274754e4cc07367c231b3f4d616f9761409bd6266`  
		Last Modified: Tue, 04 Jun 2024 01:47:45 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:5d61f08a2244fdd9670175600ad9e49611e5c5224f3b2b4ea2ce07ac56ab3a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17988811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa45066278353d53895c24f1f52b51c98e1463beb562cbbe8d777a691ef0d333`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 03:28:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[443/udp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /srv
# Mon, 03 Jun 2024 03:28:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9dcde94bf3f93b54ed692d25df606aadecebd0f28dd77d53b2c325c79116a9`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 364.9 KB (364869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129cdd4fd7c6eaafbd0d2ee17d753e1dc55f2b053dfe7eee597a638caec99dbf`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be0dc6e23084d8005f5b12d389c12d178b61dd29787c3eedee3a345071254b`  
		Last Modified: Mon, 03 Jun 2024 21:31:39 GMT  
		Size: 14.2 MB (14156119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:a71f8245a1fd40b0a5ede0f920e638a267abfedc83a33ef8f3e1f2b6ef63eb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643cd9393627b6ccbef5905e3848878f075de79071ab70ba90611cc1e8448a2d`

```dockerfile
```

-	Layers:
	-	`sha256:ac2552b9d22cc667e50951ca72233fe141aa9ba5177bfceaf4c6018693a777d0`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 261.9 KB (261860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ae05b2ef2b85ef54cad975979e33c0d69ebc0cb9ff24041f016c7f2ae25182`  
		Last Modified: Mon, 03 Jun 2024 21:31:38 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:a0b338adc338b131f1b4811bd7f95964e764e483c22ab46c1ba97947e90beced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:dbab4057e60d72545d940471196dda51a1c0cbb62ec6fec4bd62a6c6110be70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:03475dfcb6d5e587ed271d5554b5a8821896ecd4d3a171d83c919af73b1bc837
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195908263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a1566fc687726dd4e38dc61725fc5369588fbef4068ad9a193ef55859930d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:01:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:43 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:03:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:03:08 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:03:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:03:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:03:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:03:13 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:03:14 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:03:33 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:03:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a677f3de1150ebba6a18022f22b556ec0d464e0924b3ac647e484b4e9cb8a4`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0ef72246bcb821bd21b542fafefb448f254b42b5ea68e3b94b626abfe3779b`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18a603459c5ceccbec879b5a1870afa9f948e255264c85373265a16189a2b1`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd19a3eb05716373aed2b17ef5313025c5c4f56a6197ab697dcff06d9d4fd76b`  
		Last Modified: Mon, 03 Jun 2024 19:03:45 GMT  
		Size: 15.3 MB (15282972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4a38c04ae4acea262371e3e7a678a669e48544b959354e6eaff44935156b02`  
		Last Modified: Mon, 03 Jun 2024 19:03:43 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e764547189475ad7817dfc8c6327d0a752478241118c17fe87c84a1cea22dbf`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d4ac70f658e6e2463809a535b9bb2c71343c88e9594ac415c2c18934348ea`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c2e68bce0632c593ead5b0916f563c507656d06a0af54848385cf5cb457ed`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a90bec08b6f800dc2aed61db450112ce7ce22fa556d202379c97dcd3372c8`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465186eed583ca46dedc9c1d0774831b8dfa0bc126eb1c220c879c310483a0d3`  
		Last Modified: Mon, 03 Jun 2024 19:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172a17780e079b5d2e5ccf6d55decbb02c326d01ff8a867926edffee09d3699`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7d1a244aaf1710b94b5531e61ec04faf429fd94b65c7b0cf43d030d7c54252`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b7e91f780d1d5fef68930c2f162b07ae79991e4629369b9cc51b708d8695d`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574cbe874b866d2d57e873b61c273358ceba1b021c6af54fc9cef3a38fcc25d0`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3febfe7aaa179425203f0276245c514e67004e63b24f193d2ed320875561d7b`  
		Last Modified: Mon, 03 Jun 2024 19:03:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c3a9908a6a76fd6422cec7aa801080193dd106041c3f6194e19bca35cab6a`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0b247e8b1402b2de944a1c5cc40ee9bd99fa88d32fc83c304cdcec7c57857`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68152255ac3f4af23ef6a85e738daf4f30fea1fd23a2c4fd2472244b26191058`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd15ba4e2d75254724538cc0e4d45d8b6470671af8fbba72a5b64612f7fcddf`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 369.7 KB (369717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3b8d720c0b2449807d77100d57526e780cd663a382904cabf12e41e980e7c`  
		Last Modified: Mon, 03 Jun 2024 19:03:37 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:298ce474adcb68acbbf7d561e3182062bc7c263ef39cfac2632da7d9841bf435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
