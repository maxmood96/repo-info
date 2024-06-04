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
