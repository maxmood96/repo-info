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
-	[`caddy:2.8.1`](#caddy281)
-	[`caddy:2.8.1-alpine`](#caddy281-alpine)
-	[`caddy:2.8.1-builder`](#caddy281-builder)
-	[`caddy:2.8.1-builder-alpine`](#caddy281-builder-alpine)
-	[`caddy:2.8.1-builder-windowsservercore-1809`](#caddy281-builder-windowsservercore-1809)
-	[`caddy:2.8.1-builder-windowsservercore-ltsc2022`](#caddy281-builder-windowsservercore-ltsc2022)
-	[`caddy:2.8.1-windowsservercore`](#caddy281-windowsservercore)
-	[`caddy:2.8.1-windowsservercore-1809`](#caddy281-windowsservercore-1809)
-	[`caddy:2.8.1-windowsservercore-ltsc2022`](#caddy281-windowsservercore-ltsc2022)
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
$ docker pull caddy@sha256:7414db60780a20966cd9621d1dcffcdcef060607ff32ddbfde2a3737405846c4
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
$ docker pull caddy@sha256:21b4e37fefdfbc0b38227b3b6fcb805cfeab34715f39d218e4786cdf1a40c55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4829de267201b0e17026cc10e9f5c6aaf0cb9ecf4c47af6cca07c724e01ecef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65acfd58ee0383df10e747701a535d8eb3dac0dd8ad8947a9489b09700ad9d34`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 357.4 KB (357362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e249d258482cb8cd5b424e1644ad35cca37f57a78ae82f68da40abb4058219`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad68dac2ba05429229b54df92b7d1c8ecf608e981628a2ccd42f75bc9e35585`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 14.6 MB (14639266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:0488da5140275dd85cabcbc6b4bd17ff4bc2a6b00173e98925c9559401389b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fbf645e9ac813c3bebf57f4eb989db435692e28e27b909e33a2ab0fb485a34`

```dockerfile
```

-	Layers:
	-	`sha256:399151dcea96073c9d5de979846a5a1b681fc579ac0be2d6b8f46a712067ad74`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ac1b53e222fa9515008993e54b82ed153489351621785b922ad6c38b02e16b`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:27cb90616a8c910028f265c9a35e37b0a53ec818bcf78dca8935cb78685966f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51165ded103a1f093954ce84fe7980b1e20850c4c3565fcaf815aed24b4aa55c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5ade106a2b14c91e811b5be595c661aca72225039cc90670aeb4e92acc8fb`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 357.7 KB (357706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1311d826171a92f66f193a8b4b680699154cc050cf64890527f23bce7e030465`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5914ee1e526c5be906731c807280905bb260186dfcc9ded13553155ef1d07f`  
		Last Modified: Thu, 30 May 2024 19:57:55 GMT  
		Size: 13.8 MB (13763012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:175d31b3aaf4bc9dc28938abb562c3639d2055acaaaa3b8b9a39ba9fbc3c31a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d117aac14a02f2556053c54ab993841ba82072e99f3ac61b5b263bcf783489e3`

```dockerfile
```

-	Layers:
	-	`sha256:b0bfc7c1bc28a001a221f1019947525245d903ddd68cdb36cecdebaf8be32643`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8bb480061ddd6a6c02b0133c5961abc6436f59ddd73c75040346b05d836fc8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17192991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8909144dcba13d585205edef980f7651a16da9574485be2862dec9ddacbc26c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5084781186f063a0bb6c3944407d818125eff602e2318b2b477ab01942afd5ef`  
		Last Modified: Thu, 30 May 2024 04:24:05 GMT  
		Size: 354.1 KB (354057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18302bdcf86d42d09129aeacce97eb83894389c4281eb661bb74d24898b3954d`  
		Last Modified: Thu, 30 May 2024 04:24:04 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4ba1984187ea68f8b4e33c5da9fd0cd0b837eb49cceaf672bc040a8a9b5b2`  
		Last Modified: Thu, 30 May 2024 20:10:44 GMT  
		Size: 13.7 MB (13737415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:f3e04cfab426b603f0d3f9b04f93e53e5e96a896700417a416fc37f1ee8b9e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f470fb5d78b3b8b2143c88cf1d1cb11e6a759e7dd600d33067744eb3969d7064`

```dockerfile
```

-	Layers:
	-	`sha256:f90edc2b668319b5941bbfe7959e6d360942247c4efee398915d63f654d5a3c7`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
		Size: 263.9 KB (263883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70d2cebd4de6bf0de572d0e63bacef20ac991ca8f27f020a435f0a261fe1d6c`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
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
$ docker pull caddy@sha256:c324482f435aa50ae30f531d417545d7cc5586d76847279cba2077ea33e735a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17241541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0655e1dc6ab3c3e5f2b29fe680646c4dbd6a51427f027e8131c98c462244aa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ad67972e40ad224d572ec1975dcf39e560dcbe6b551c3ba4f39919a337f3b`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 370.4 KB (370393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa024c4e0f280d11973c0eda3b12f09a76e0381d137bc1b3f32a5aec6b814c79`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 7.4 KB (7447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b777476a3ae956d01f8bd0551800403bdb2da307a3fd8920e2e479f14378d7d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 13.3 MB (13293823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:9e12f88ecde4df21cdd45a0ffb3cdf4fd8bbfb9a96063d66950f31a36c43ad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca7c5ceea57fcbe9468b1e28d188e8c92d894fe93efad5a85c8b9218fa8bbd7`

```dockerfile
```

-	Layers:
	-	`sha256:57c8adf6ec56a24a31792e239bf6547209e7c64f44343f4c7086558bd2ab4f4a`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 261.9 KB (261919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816f1138bf9ebcc1df2835942273446b6aedfefd4561b7fa37c561975d172b4d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:9e74b95e547eb1588c353d45473bb032367622a294199a26e72f8b352d023713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86dfcd59aa0a6fd0d01bfd9a897f6975a68f6680daf026ecc2ec85b35e29304`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240f4b8c6e2d5ad7a70cc783c821c10a0a0ecb4279a36796296b53241fc0105f`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 14.2 MB (14154632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:aa3915fa8f7c9eaa46531086b6bf775173944010b62e751853379935819e2273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915a3930126fcee6c8cb4e8dcd4de24dcd0583072e33f2deaf7229e5385856f`

```dockerfile
```

-	Layers:
	-	`sha256:f4fce58be66b513afeb7b2fb194ae632e3c8457df54b0f13f72d1fbe09a43bf1`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01188c3d77dabde06f83507c443768248401b1b69ef1d5c709e82a4691cc4f9`  
		Last Modified: Thu, 30 May 2024 20:10:41 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:54b067d60ae306670ab09f10b6f309f19e4e0f43927ae514d3740fbe7964872f
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
$ docker pull caddy@sha256:21b4e37fefdfbc0b38227b3b6fcb805cfeab34715f39d218e4786cdf1a40c55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4829de267201b0e17026cc10e9f5c6aaf0cb9ecf4c47af6cca07c724e01ecef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65acfd58ee0383df10e747701a535d8eb3dac0dd8ad8947a9489b09700ad9d34`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 357.4 KB (357362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e249d258482cb8cd5b424e1644ad35cca37f57a78ae82f68da40abb4058219`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad68dac2ba05429229b54df92b7d1c8ecf608e981628a2ccd42f75bc9e35585`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 14.6 MB (14639266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0488da5140275dd85cabcbc6b4bd17ff4bc2a6b00173e98925c9559401389b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fbf645e9ac813c3bebf57f4eb989db435692e28e27b909e33a2ab0fb485a34`

```dockerfile
```

-	Layers:
	-	`sha256:399151dcea96073c9d5de979846a5a1b681fc579ac0be2d6b8f46a712067ad74`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ac1b53e222fa9515008993e54b82ed153489351621785b922ad6c38b02e16b`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:27cb90616a8c910028f265c9a35e37b0a53ec818bcf78dca8935cb78685966f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51165ded103a1f093954ce84fe7980b1e20850c4c3565fcaf815aed24b4aa55c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5ade106a2b14c91e811b5be595c661aca72225039cc90670aeb4e92acc8fb`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 357.7 KB (357706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1311d826171a92f66f193a8b4b680699154cc050cf64890527f23bce7e030465`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5914ee1e526c5be906731c807280905bb260186dfcc9ded13553155ef1d07f`  
		Last Modified: Thu, 30 May 2024 19:57:55 GMT  
		Size: 13.8 MB (13763012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:175d31b3aaf4bc9dc28938abb562c3639d2055acaaaa3b8b9a39ba9fbc3c31a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d117aac14a02f2556053c54ab993841ba82072e99f3ac61b5b263bcf783489e3`

```dockerfile
```

-	Layers:
	-	`sha256:b0bfc7c1bc28a001a221f1019947525245d903ddd68cdb36cecdebaf8be32643`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8bb480061ddd6a6c02b0133c5961abc6436f59ddd73c75040346b05d836fc8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17192991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8909144dcba13d585205edef980f7651a16da9574485be2862dec9ddacbc26c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5084781186f063a0bb6c3944407d818125eff602e2318b2b477ab01942afd5ef`  
		Last Modified: Thu, 30 May 2024 04:24:05 GMT  
		Size: 354.1 KB (354057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18302bdcf86d42d09129aeacce97eb83894389c4281eb661bb74d24898b3954d`  
		Last Modified: Thu, 30 May 2024 04:24:04 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4ba1984187ea68f8b4e33c5da9fd0cd0b837eb49cceaf672bc040a8a9b5b2`  
		Last Modified: Thu, 30 May 2024 20:10:44 GMT  
		Size: 13.7 MB (13737415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f3e04cfab426b603f0d3f9b04f93e53e5e96a896700417a416fc37f1ee8b9e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f470fb5d78b3b8b2143c88cf1d1cb11e6a759e7dd600d33067744eb3969d7064`

```dockerfile
```

-	Layers:
	-	`sha256:f90edc2b668319b5941bbfe7959e6d360942247c4efee398915d63f654d5a3c7`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
		Size: 263.9 KB (263883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70d2cebd4de6bf0de572d0e63bacef20ac991ca8f27f020a435f0a261fe1d6c`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
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
$ docker pull caddy@sha256:c324482f435aa50ae30f531d417545d7cc5586d76847279cba2077ea33e735a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17241541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0655e1dc6ab3c3e5f2b29fe680646c4dbd6a51427f027e8131c98c462244aa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ad67972e40ad224d572ec1975dcf39e560dcbe6b551c3ba4f39919a337f3b`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 370.4 KB (370393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa024c4e0f280d11973c0eda3b12f09a76e0381d137bc1b3f32a5aec6b814c79`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 7.4 KB (7447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b777476a3ae956d01f8bd0551800403bdb2da307a3fd8920e2e479f14378d7d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 13.3 MB (13293823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9e12f88ecde4df21cdd45a0ffb3cdf4fd8bbfb9a96063d66950f31a36c43ad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca7c5ceea57fcbe9468b1e28d188e8c92d894fe93efad5a85c8b9218fa8bbd7`

```dockerfile
```

-	Layers:
	-	`sha256:57c8adf6ec56a24a31792e239bf6547209e7c64f44343f4c7086558bd2ab4f4a`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 261.9 KB (261919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816f1138bf9ebcc1df2835942273446b6aedfefd4561b7fa37c561975d172b4d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9e74b95e547eb1588c353d45473bb032367622a294199a26e72f8b352d023713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86dfcd59aa0a6fd0d01bfd9a897f6975a68f6680daf026ecc2ec85b35e29304`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240f4b8c6e2d5ad7a70cc783c821c10a0a0ecb4279a36796296b53241fc0105f`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 14.2 MB (14154632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:aa3915fa8f7c9eaa46531086b6bf775173944010b62e751853379935819e2273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915a3930126fcee6c8cb4e8dcd4de24dcd0583072e33f2deaf7229e5385856f`

```dockerfile
```

-	Layers:
	-	`sha256:f4fce58be66b513afeb7b2fb194ae632e3c8457df54b0f13f72d1fbe09a43bf1`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01188c3d77dabde06f83507c443768248401b1b69ef1d5c709e82a4691cc4f9`  
		Last Modified: Thu, 30 May 2024 20:10:41 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:37acf9e88ea74ef051bc1ec68ea9abd535320ea4eea1a0162aaf378ee5200a3c
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
$ docker pull caddy@sha256:9726224af4eeb16d52a30ae22fe0e0b06695c0e024f9efb295cf4bee09f57197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776279b710312f522ae60c2863326cc1b272d10acbb7f565d772d98cd7b45109`
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
	-	`sha256:b934fec1d0841de3fdf41cc33cdbc48551b5a2f0a7e6cdab65f224087005518c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 5.9 MB (5914558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3972621d02a746fb40b7f7396e9691786ac8736303b398c6036603239d4d71d6`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 1.5 MB (1500667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d524b2ee4c08318c294fb228d9d12bab4fdd1be5680e9c48d6c95a639cbaab`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:97b225e025145914c962df9facde72df887ac62754d89d0cbb531457bab05426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad49ab463e282ed01ac585005909bd73c83fadaeec1f96c8eddfbfd71db4e495`

```dockerfile
```

-	Layers:
	-	`sha256:7d8246f33a79fee33df45c06b03b4587ae80b11e9e8b4d884bc9ea55c5f85d9c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65fa569730f7d004dc9753ba63162b78b1fb241a2220365c79acf93bf64ec978`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:1fec3f7cab4729a430b8900be91337b7128699996c4fe0e1f3276789bd73025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b9fd44380823bd1943c0c1323b5d18b8d9cb6e5c054a20fd34d47e4a32d76c`
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
	-	`sha256:37d29efacbef5349371d8c2b88d68d880f345b5761f3223195407d2f95ed5b78`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 5.9 MB (5863446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e246b302345acefe6f5fe19701bee3f3c7e41a579ac1f76719acfad40786c2`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9137f20e52fd92773254f39e98b2c7b450128319173ca7acc759d95a5f325f0`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0bae879cdc66bcf071ce11018dfa7a07f602174d15582f2686fab10d6eb92d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9cfa298cd1818c69cf4b7c8b3df281a4a0e7928bf74488818b845639cc3c78`

```dockerfile
```

-	Layers:
	-	`sha256:69fe8062c086bf0def17c0407ea8856c140fdcb4d91cbd072987f1ab485c8439`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a1cb5e5de00be496dfe69ae4b4b55230c24327646c520e703a1b46dbd995296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04f376c2097ec4f9c5be43112ed5755c8e9f8b429f273a156dbcf4100dac79c`
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
	-	`sha256:8de42c46a5fc5e9bac21fd33a111406ceb9878dc1ff409dc9d7e62fca23b4fcb`  
		Last Modified: Thu, 30 May 2024 04:24:48 GMT  
		Size: 5.4 MB (5351041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d2d11b544756b6d8e93d89deb6119d65357b73278523bf5c2a4d35b3f58b1b`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 1.4 MB (1420765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cf89bcfa50143b74197a95c225b86c05af80d1319563716b6899bd75b746a3`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a6fe6195f181c5e90ee9a4c1d38d366c455b473f8f4fc109dc1db70c5536aa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d02df18f656835cd563756dfb06fc058e7157558482de610c8115675323a174`

```dockerfile
```

-	Layers:
	-	`sha256:689cb17aa17b78a3cb1fa0f18c25a34897b2276d84a65e29248992fdef29bcf6`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 278.3 KB (278321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f873bbf7f705ed6d30295cdc42ae04010f2a5f0dfe91acde3bf6fe05adfcca1`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
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
$ docker pull caddy@sha256:ca03efc1964e5a73d468e9543c9333e83b1d1c0a6077535c3bee9c732bbc407a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c94ee31a8787237f2a3fe0960078a830918ff0e25b743630569c2f95a3fb3ca`
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
	-	`sha256:61014b2ea6ecad7540420fd97ff35c204099831314d8af4b6bcefabfd60768c6`  
		Last Modified: Thu, 30 May 2024 03:50:11 GMT  
		Size: 6.2 MB (6240110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cddf047e6287c6194328f1cf1610743e450a59fffc7cdada00665f3e1a69de`  
		Last Modified: Thu, 30 May 2024 20:12:56 GMT  
		Size: 1.4 MB (1390030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d2892632bead1789583b0e83a9a7b547a7edbbd4cabe2723a57aa3da576895`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:c1735d271d08cab1c8e1dfe80f3d307bc4a569503cd3ac559de060137ad1e9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181edb797ade073642b1fa5a3acd2419f770ddce2b8b6dd0cf38dd37239cafd8`

```dockerfile
```

-	Layers:
	-	`sha256:cf87e4d2788d6a74320378065b9c88194584b780484699e00b81db822aef09a1`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde88d90ec100ec769b0531716096a71efafe182ff6ca6e5beafb579172743a`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:ddf41b94ba50096d4c83958a2f93d05e972a29f78e3cdbf5cc7297201d87d403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fe4747836e96d532a84ce7c51866f14573dd2a7184a1c98e09a3ecbb753511`
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
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dcf8f9ebef9601e1beaad8b4cc3d76b0eb4ff186a55cbca98c315ee818a4df`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fca2fb511f3ca4f6c95cda9f18b178cad865110e6249189b3d42a59533f87a`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:1a4cccca18bb45637c2fe9de18eb24b88ef5f1e5bee1f1aa4404906aa207c47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1676179af361cea13064135f85238a0c19b852b0b327478717c9c00c8db37f4`

```dockerfile
```

-	Layers:
	-	`sha256:339a9ba6f90463c144e1ee97eda33e02e6a462b01c2084c0c6c670f9b485074b`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90037cfca85f081f1a829fa848b68182197ddc46f70884e3e05924221d35e02d`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:10597519ab8ae6e2997ab33ed37ec084b7fa48197540fd8a5e9d6232e3eeefe7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212211421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c8c5c0c49c5e91e4db193bb2ceb6f49da6bb49f53d1f9273feefb5c4c4e8d`
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
# Thu, 30 May 2024 19:55:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:55:15 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:55:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:55:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 19:56:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 19:56:09 GMT
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
	-	`sha256:781a5790a63eb24d3d7b709f3885381842614c685aacc0e9f064de800ae074a5`  
		Last Modified: Thu, 30 May 2024 19:56:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adfb41eec4d294c5d5a6989921400c3ce8eac86190ca0e2729a220714fed0b7`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f50fb992e0f2417cc3d5dbd89e9bae09e2871bfb3da8442273c4393ccfeaea`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fe5c664cb62db2aa80c45ca5f51cc3c7a49fd4db915c14c9d3f3697b6e6a8`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dd35d7efa642909c8543d67ac3db36e703c2e00eba4cb7eb057a17a7c65632`  
		Last Modified: Thu, 30 May 2024 19:56:13 GMT  
		Size: 2.0 MB (1977015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcfc24e4cea1030166263d016513ca0181219e291b60093398c292a71217196`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:31ea6cb75b5ad08fb08500916a0a249d3cd3fac67e2062428129f1255fd747a6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d816cca71514d888c55882cedda59c9e63b2873912ab19d832e8f0c192cfa6`
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
# Thu, 30 May 2024 19:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:58:09 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:58:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:58:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 20:00:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 20:00:16 GMT
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
	-	`sha256:0fbedff9109d9c95af2643ac63a5cacb1b2bc7f05ffacb6f738c7bd71a8eccec`  
		Last Modified: Thu, 30 May 2024 20:00:20 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca153f0633c0d2c02ede7da833835063735438dffc496ac2f6e096fd2ffba56`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8add55d5a48aeb589d70b12c70950ab9d36ea1844e46a0c3243431fc5d023`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c23241851e0ece31bec24fbcc64f6a45ad49e757b6d83fd867de1db46ef1750`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1af3c5163dc4db242d8d318f53106e3edab0cbfcdee3719d51d1eb44031b1f`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 2.0 MB (1951704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fab58945a98d4f4ef5a6f69ce2d9c53b14cdfdb6bbf677de534c9df7f2a5d11`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:9b0e5fefc8876b84dc74dd15b7413da6ad26b0642a4fb11d8f37399ad47fa572
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
$ docker pull caddy@sha256:9726224af4eeb16d52a30ae22fe0e0b06695c0e024f9efb295cf4bee09f57197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776279b710312f522ae60c2863326cc1b272d10acbb7f565d772d98cd7b45109`
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
	-	`sha256:b934fec1d0841de3fdf41cc33cdbc48551b5a2f0a7e6cdab65f224087005518c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 5.9 MB (5914558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3972621d02a746fb40b7f7396e9691786ac8736303b398c6036603239d4d71d6`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 1.5 MB (1500667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d524b2ee4c08318c294fb228d9d12bab4fdd1be5680e9c48d6c95a639cbaab`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:97b225e025145914c962df9facde72df887ac62754d89d0cbb531457bab05426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad49ab463e282ed01ac585005909bd73c83fadaeec1f96c8eddfbfd71db4e495`

```dockerfile
```

-	Layers:
	-	`sha256:7d8246f33a79fee33df45c06b03b4587ae80b11e9e8b4d884bc9ea55c5f85d9c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65fa569730f7d004dc9753ba63162b78b1fb241a2220365c79acf93bf64ec978`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:1fec3f7cab4729a430b8900be91337b7128699996c4fe0e1f3276789bd73025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b9fd44380823bd1943c0c1323b5d18b8d9cb6e5c054a20fd34d47e4a32d76c`
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
	-	`sha256:37d29efacbef5349371d8c2b88d68d880f345b5761f3223195407d2f95ed5b78`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 5.9 MB (5863446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e246b302345acefe6f5fe19701bee3f3c7e41a579ac1f76719acfad40786c2`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9137f20e52fd92773254f39e98b2c7b450128319173ca7acc759d95a5f325f0`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0bae879cdc66bcf071ce11018dfa7a07f602174d15582f2686fab10d6eb92d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9cfa298cd1818c69cf4b7c8b3df281a4a0e7928bf74488818b845639cc3c78`

```dockerfile
```

-	Layers:
	-	`sha256:69fe8062c086bf0def17c0407ea8856c140fdcb4d91cbd072987f1ab485c8439`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a1cb5e5de00be496dfe69ae4b4b55230c24327646c520e703a1b46dbd995296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04f376c2097ec4f9c5be43112ed5755c8e9f8b429f273a156dbcf4100dac79c`
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
	-	`sha256:8de42c46a5fc5e9bac21fd33a111406ceb9878dc1ff409dc9d7e62fca23b4fcb`  
		Last Modified: Thu, 30 May 2024 04:24:48 GMT  
		Size: 5.4 MB (5351041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d2d11b544756b6d8e93d89deb6119d65357b73278523bf5c2a4d35b3f58b1b`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 1.4 MB (1420765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cf89bcfa50143b74197a95c225b86c05af80d1319563716b6899bd75b746a3`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a6fe6195f181c5e90ee9a4c1d38d366c455b473f8f4fc109dc1db70c5536aa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d02df18f656835cd563756dfb06fc058e7157558482de610c8115675323a174`

```dockerfile
```

-	Layers:
	-	`sha256:689cb17aa17b78a3cb1fa0f18c25a34897b2276d84a65e29248992fdef29bcf6`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 278.3 KB (278321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f873bbf7f705ed6d30295cdc42ae04010f2a5f0dfe91acde3bf6fe05adfcca1`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
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
$ docker pull caddy@sha256:ca03efc1964e5a73d468e9543c9333e83b1d1c0a6077535c3bee9c732bbc407a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c94ee31a8787237f2a3fe0960078a830918ff0e25b743630569c2f95a3fb3ca`
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
	-	`sha256:61014b2ea6ecad7540420fd97ff35c204099831314d8af4b6bcefabfd60768c6`  
		Last Modified: Thu, 30 May 2024 03:50:11 GMT  
		Size: 6.2 MB (6240110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cddf047e6287c6194328f1cf1610743e450a59fffc7cdada00665f3e1a69de`  
		Last Modified: Thu, 30 May 2024 20:12:56 GMT  
		Size: 1.4 MB (1390030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d2892632bead1789583b0e83a9a7b547a7edbbd4cabe2723a57aa3da576895`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c1735d271d08cab1c8e1dfe80f3d307bc4a569503cd3ac559de060137ad1e9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181edb797ade073642b1fa5a3acd2419f770ddce2b8b6dd0cf38dd37239cafd8`

```dockerfile
```

-	Layers:
	-	`sha256:cf87e4d2788d6a74320378065b9c88194584b780484699e00b81db822aef09a1`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde88d90ec100ec769b0531716096a71efafe182ff6ca6e5beafb579172743a`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:ddf41b94ba50096d4c83958a2f93d05e972a29f78e3cdbf5cc7297201d87d403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fe4747836e96d532a84ce7c51866f14573dd2a7184a1c98e09a3ecbb753511`
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
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dcf8f9ebef9601e1beaad8b4cc3d76b0eb4ff186a55cbca98c315ee818a4df`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fca2fb511f3ca4f6c95cda9f18b178cad865110e6249189b3d42a59533f87a`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1a4cccca18bb45637c2fe9de18eb24b88ef5f1e5bee1f1aa4404906aa207c47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1676179af361cea13064135f85238a0c19b852b0b327478717c9c00c8db37f4`

```dockerfile
```

-	Layers:
	-	`sha256:339a9ba6f90463c144e1ee97eda33e02e6a462b01c2084c0c6c670f9b485074b`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90037cfca85f081f1a829fa848b68182197ddc46f70884e3e05924221d35e02d`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:4c00208a7869c08a9cb6ef821d15eafeac675e507194f54957fc91cbaf787e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:31ea6cb75b5ad08fb08500916a0a249d3cd3fac67e2062428129f1255fd747a6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d816cca71514d888c55882cedda59c9e63b2873912ab19d832e8f0c192cfa6`
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
# Thu, 30 May 2024 19:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:58:09 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:58:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:58:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 20:00:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 20:00:16 GMT
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
	-	`sha256:0fbedff9109d9c95af2643ac63a5cacb1b2bc7f05ffacb6f738c7bd71a8eccec`  
		Last Modified: Thu, 30 May 2024 20:00:20 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca153f0633c0d2c02ede7da833835063735438dffc496ac2f6e096fd2ffba56`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8add55d5a48aeb589d70b12c70950ab9d36ea1844e46a0c3243431fc5d023`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c23241851e0ece31bec24fbcc64f6a45ad49e757b6d83fd867de1db46ef1750`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1af3c5163dc4db242d8d318f53106e3edab0cbfcdee3719d51d1eb44031b1f`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 2.0 MB (1951704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fab58945a98d4f4ef5a6f69ce2d9c53b14cdfdb6bbf677de534c9df7f2a5d11`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:026063496c4412e2f6ad3d7eff0b72334f52eb6a26a76ad7d55413f1f2215b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:10597519ab8ae6e2997ab33ed37ec084b7fa48197540fd8a5e9d6232e3eeefe7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212211421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c8c5c0c49c5e91e4db193bb2ceb6f49da6bb49f53d1f9273feefb5c4c4e8d`
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
# Thu, 30 May 2024 19:55:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:55:15 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:55:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:55:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 19:56:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 19:56:09 GMT
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
	-	`sha256:781a5790a63eb24d3d7b709f3885381842614c685aacc0e9f064de800ae074a5`  
		Last Modified: Thu, 30 May 2024 19:56:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adfb41eec4d294c5d5a6989921400c3ce8eac86190ca0e2729a220714fed0b7`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f50fb992e0f2417cc3d5dbd89e9bae09e2871bfb3da8442273c4393ccfeaea`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fe5c664cb62db2aa80c45ca5f51cc3c7a49fd4db915c14c9d3f3697b6e6a8`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dd35d7efa642909c8543d67ac3db36e703c2e00eba4cb7eb057a17a7c65632`  
		Last Modified: Thu, 30 May 2024 19:56:13 GMT  
		Size: 2.0 MB (1977015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcfc24e4cea1030166263d016513ca0181219e291b60093398c292a71217196`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:968fc01b86c3c4fd80a64a2e2bdbad91006c31b5dea58261ba4c678ee97341a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:d48df926bf363a40ecdc79c34c0a1fd25177d1ad25f3588dcc722924acd201a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7a8c826b69b921eba34d21e8f1432aa2173c0ef6595ac138f64856a830ee1204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8`

```console
$ docker pull caddy@sha256:7414db60780a20966cd9621d1dcffcdcef060607ff32ddbfde2a3737405846c4
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
$ docker pull caddy@sha256:21b4e37fefdfbc0b38227b3b6fcb805cfeab34715f39d218e4786cdf1a40c55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4829de267201b0e17026cc10e9f5c6aaf0cb9ecf4c47af6cca07c724e01ecef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65acfd58ee0383df10e747701a535d8eb3dac0dd8ad8947a9489b09700ad9d34`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 357.4 KB (357362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e249d258482cb8cd5b424e1644ad35cca37f57a78ae82f68da40abb4058219`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad68dac2ba05429229b54df92b7d1c8ecf608e981628a2ccd42f75bc9e35585`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 14.6 MB (14639266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:0488da5140275dd85cabcbc6b4bd17ff4bc2a6b00173e98925c9559401389b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fbf645e9ac813c3bebf57f4eb989db435692e28e27b909e33a2ab0fb485a34`

```dockerfile
```

-	Layers:
	-	`sha256:399151dcea96073c9d5de979846a5a1b681fc579ac0be2d6b8f46a712067ad74`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ac1b53e222fa9515008993e54b82ed153489351621785b922ad6c38b02e16b`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; arm variant v6

```console
$ docker pull caddy@sha256:27cb90616a8c910028f265c9a35e37b0a53ec818bcf78dca8935cb78685966f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51165ded103a1f093954ce84fe7980b1e20850c4c3565fcaf815aed24b4aa55c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5ade106a2b14c91e811b5be595c661aca72225039cc90670aeb4e92acc8fb`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 357.7 KB (357706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1311d826171a92f66f193a8b4b680699154cc050cf64890527f23bce7e030465`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5914ee1e526c5be906731c807280905bb260186dfcc9ded13553155ef1d07f`  
		Last Modified: Thu, 30 May 2024 19:57:55 GMT  
		Size: 13.8 MB (13763012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:175d31b3aaf4bc9dc28938abb562c3639d2055acaaaa3b8b9a39ba9fbc3c31a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d117aac14a02f2556053c54ab993841ba82072e99f3ac61b5b263bcf783489e3`

```dockerfile
```

-	Layers:
	-	`sha256:b0bfc7c1bc28a001a221f1019947525245d903ddd68cdb36cecdebaf8be32643`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8bb480061ddd6a6c02b0133c5961abc6436f59ddd73c75040346b05d836fc8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17192991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8909144dcba13d585205edef980f7651a16da9574485be2862dec9ddacbc26c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5084781186f063a0bb6c3944407d818125eff602e2318b2b477ab01942afd5ef`  
		Last Modified: Thu, 30 May 2024 04:24:05 GMT  
		Size: 354.1 KB (354057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18302bdcf86d42d09129aeacce97eb83894389c4281eb661bb74d24898b3954d`  
		Last Modified: Thu, 30 May 2024 04:24:04 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4ba1984187ea68f8b4e33c5da9fd0cd0b837eb49cceaf672bc040a8a9b5b2`  
		Last Modified: Thu, 30 May 2024 20:10:44 GMT  
		Size: 13.7 MB (13737415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:f3e04cfab426b603f0d3f9b04f93e53e5e96a896700417a416fc37f1ee8b9e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f470fb5d78b3b8b2143c88cf1d1cb11e6a759e7dd600d33067744eb3969d7064`

```dockerfile
```

-	Layers:
	-	`sha256:f90edc2b668319b5941bbfe7959e6d360942247c4efee398915d63f654d5a3c7`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
		Size: 263.9 KB (263883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70d2cebd4de6bf0de572d0e63bacef20ac991ca8f27f020a435f0a261fe1d6c`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
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
$ docker pull caddy@sha256:c324482f435aa50ae30f531d417545d7cc5586d76847279cba2077ea33e735a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17241541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0655e1dc6ab3c3e5f2b29fe680646c4dbd6a51427f027e8131c98c462244aa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ad67972e40ad224d572ec1975dcf39e560dcbe6b551c3ba4f39919a337f3b`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 370.4 KB (370393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa024c4e0f280d11973c0eda3b12f09a76e0381d137bc1b3f32a5aec6b814c79`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 7.4 KB (7447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b777476a3ae956d01f8bd0551800403bdb2da307a3fd8920e2e479f14378d7d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 13.3 MB (13293823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:9e12f88ecde4df21cdd45a0ffb3cdf4fd8bbfb9a96063d66950f31a36c43ad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca7c5ceea57fcbe9468b1e28d188e8c92d894fe93efad5a85c8b9218fa8bbd7`

```dockerfile
```

-	Layers:
	-	`sha256:57c8adf6ec56a24a31792e239bf6547209e7c64f44343f4c7086558bd2ab4f4a`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 261.9 KB (261919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816f1138bf9ebcc1df2835942273446b6aedfefd4561b7fa37c561975d172b4d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - linux; s390x

```console
$ docker pull caddy@sha256:9e74b95e547eb1588c353d45473bb032367622a294199a26e72f8b352d023713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86dfcd59aa0a6fd0d01bfd9a897f6975a68f6680daf026ecc2ec85b35e29304`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240f4b8c6e2d5ad7a70cc783c821c10a0a0ecb4279a36796296b53241fc0105f`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 14.2 MB (14154632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8` - unknown; unknown

```console
$ docker pull caddy@sha256:aa3915fa8f7c9eaa46531086b6bf775173944010b62e751853379935819e2273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915a3930126fcee6c8cb4e8dcd4de24dcd0583072e33f2deaf7229e5385856f`

```dockerfile
```

-	Layers:
	-	`sha256:f4fce58be66b513afeb7b2fb194ae632e3c8457df54b0f13f72d1fbe09a43bf1`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01188c3d77dabde06f83507c443768248401b1b69ef1d5c709e82a4691cc4f9`  
		Last Modified: Thu, 30 May 2024 20:10:41 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-alpine`

```console
$ docker pull caddy@sha256:54b067d60ae306670ab09f10b6f309f19e4e0f43927ae514d3740fbe7964872f
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
$ docker pull caddy@sha256:21b4e37fefdfbc0b38227b3b6fcb805cfeab34715f39d218e4786cdf1a40c55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4829de267201b0e17026cc10e9f5c6aaf0cb9ecf4c47af6cca07c724e01ecef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65acfd58ee0383df10e747701a535d8eb3dac0dd8ad8947a9489b09700ad9d34`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 357.4 KB (357362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e249d258482cb8cd5b424e1644ad35cca37f57a78ae82f68da40abb4058219`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad68dac2ba05429229b54df92b7d1c8ecf608e981628a2ccd42f75bc9e35585`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 14.6 MB (14639266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0488da5140275dd85cabcbc6b4bd17ff4bc2a6b00173e98925c9559401389b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fbf645e9ac813c3bebf57f4eb989db435692e28e27b909e33a2ab0fb485a34`

```dockerfile
```

-	Layers:
	-	`sha256:399151dcea96073c9d5de979846a5a1b681fc579ac0be2d6b8f46a712067ad74`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ac1b53e222fa9515008993e54b82ed153489351621785b922ad6c38b02e16b`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:27cb90616a8c910028f265c9a35e37b0a53ec818bcf78dca8935cb78685966f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51165ded103a1f093954ce84fe7980b1e20850c4c3565fcaf815aed24b4aa55c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5ade106a2b14c91e811b5be595c661aca72225039cc90670aeb4e92acc8fb`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 357.7 KB (357706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1311d826171a92f66f193a8b4b680699154cc050cf64890527f23bce7e030465`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5914ee1e526c5be906731c807280905bb260186dfcc9ded13553155ef1d07f`  
		Last Modified: Thu, 30 May 2024 19:57:55 GMT  
		Size: 13.8 MB (13763012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:175d31b3aaf4bc9dc28938abb562c3639d2055acaaaa3b8b9a39ba9fbc3c31a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d117aac14a02f2556053c54ab993841ba82072e99f3ac61b5b263bcf783489e3`

```dockerfile
```

-	Layers:
	-	`sha256:b0bfc7c1bc28a001a221f1019947525245d903ddd68cdb36cecdebaf8be32643`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8bb480061ddd6a6c02b0133c5961abc6436f59ddd73c75040346b05d836fc8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17192991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8909144dcba13d585205edef980f7651a16da9574485be2862dec9ddacbc26c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5084781186f063a0bb6c3944407d818125eff602e2318b2b477ab01942afd5ef`  
		Last Modified: Thu, 30 May 2024 04:24:05 GMT  
		Size: 354.1 KB (354057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18302bdcf86d42d09129aeacce97eb83894389c4281eb661bb74d24898b3954d`  
		Last Modified: Thu, 30 May 2024 04:24:04 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4ba1984187ea68f8b4e33c5da9fd0cd0b837eb49cceaf672bc040a8a9b5b2`  
		Last Modified: Thu, 30 May 2024 20:10:44 GMT  
		Size: 13.7 MB (13737415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f3e04cfab426b603f0d3f9b04f93e53e5e96a896700417a416fc37f1ee8b9e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f470fb5d78b3b8b2143c88cf1d1cb11e6a759e7dd600d33067744eb3969d7064`

```dockerfile
```

-	Layers:
	-	`sha256:f90edc2b668319b5941bbfe7959e6d360942247c4efee398915d63f654d5a3c7`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
		Size: 263.9 KB (263883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70d2cebd4de6bf0de572d0e63bacef20ac991ca8f27f020a435f0a261fe1d6c`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
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
$ docker pull caddy@sha256:c324482f435aa50ae30f531d417545d7cc5586d76847279cba2077ea33e735a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17241541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0655e1dc6ab3c3e5f2b29fe680646c4dbd6a51427f027e8131c98c462244aa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ad67972e40ad224d572ec1975dcf39e560dcbe6b551c3ba4f39919a337f3b`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 370.4 KB (370393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa024c4e0f280d11973c0eda3b12f09a76e0381d137bc1b3f32a5aec6b814c79`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 7.4 KB (7447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b777476a3ae956d01f8bd0551800403bdb2da307a3fd8920e2e479f14378d7d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 13.3 MB (13293823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9e12f88ecde4df21cdd45a0ffb3cdf4fd8bbfb9a96063d66950f31a36c43ad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca7c5ceea57fcbe9468b1e28d188e8c92d894fe93efad5a85c8b9218fa8bbd7`

```dockerfile
```

-	Layers:
	-	`sha256:57c8adf6ec56a24a31792e239bf6547209e7c64f44343f4c7086558bd2ab4f4a`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 261.9 KB (261919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816f1138bf9ebcc1df2835942273446b6aedfefd4561b7fa37c561975d172b4d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9e74b95e547eb1588c353d45473bb032367622a294199a26e72f8b352d023713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86dfcd59aa0a6fd0d01bfd9a897f6975a68f6680daf026ecc2ec85b35e29304`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240f4b8c6e2d5ad7a70cc783c821c10a0a0ecb4279a36796296b53241fc0105f`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 14.2 MB (14154632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:aa3915fa8f7c9eaa46531086b6bf775173944010b62e751853379935819e2273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915a3930126fcee6c8cb4e8dcd4de24dcd0583072e33f2deaf7229e5385856f`

```dockerfile
```

-	Layers:
	-	`sha256:f4fce58be66b513afeb7b2fb194ae632e3c8457df54b0f13f72d1fbe09a43bf1`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01188c3d77dabde06f83507c443768248401b1b69ef1d5c709e82a4691cc4f9`  
		Last Modified: Thu, 30 May 2024 20:10:41 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8-builder`

```console
$ docker pull caddy@sha256:37acf9e88ea74ef051bc1ec68ea9abd535320ea4eea1a0162aaf378ee5200a3c
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
$ docker pull caddy@sha256:9726224af4eeb16d52a30ae22fe0e0b06695c0e024f9efb295cf4bee09f57197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776279b710312f522ae60c2863326cc1b272d10acbb7f565d772d98cd7b45109`
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
	-	`sha256:b934fec1d0841de3fdf41cc33cdbc48551b5a2f0a7e6cdab65f224087005518c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 5.9 MB (5914558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3972621d02a746fb40b7f7396e9691786ac8736303b398c6036603239d4d71d6`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 1.5 MB (1500667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d524b2ee4c08318c294fb228d9d12bab4fdd1be5680e9c48d6c95a639cbaab`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:97b225e025145914c962df9facde72df887ac62754d89d0cbb531457bab05426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad49ab463e282ed01ac585005909bd73c83fadaeec1f96c8eddfbfd71db4e495`

```dockerfile
```

-	Layers:
	-	`sha256:7d8246f33a79fee33df45c06b03b4587ae80b11e9e8b4d884bc9ea55c5f85d9c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65fa569730f7d004dc9753ba63162b78b1fb241a2220365c79acf93bf64ec978`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:1fec3f7cab4729a430b8900be91337b7128699996c4fe0e1f3276789bd73025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b9fd44380823bd1943c0c1323b5d18b8d9cb6e5c054a20fd34d47e4a32d76c`
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
	-	`sha256:37d29efacbef5349371d8c2b88d68d880f345b5761f3223195407d2f95ed5b78`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 5.9 MB (5863446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e246b302345acefe6f5fe19701bee3f3c7e41a579ac1f76719acfad40786c2`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9137f20e52fd92773254f39e98b2c7b450128319173ca7acc759d95a5f325f0`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0bae879cdc66bcf071ce11018dfa7a07f602174d15582f2686fab10d6eb92d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9cfa298cd1818c69cf4b7c8b3df281a4a0e7928bf74488818b845639cc3c78`

```dockerfile
```

-	Layers:
	-	`sha256:69fe8062c086bf0def17c0407ea8856c140fdcb4d91cbd072987f1ab485c8439`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a1cb5e5de00be496dfe69ae4b4b55230c24327646c520e703a1b46dbd995296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04f376c2097ec4f9c5be43112ed5755c8e9f8b429f273a156dbcf4100dac79c`
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
	-	`sha256:8de42c46a5fc5e9bac21fd33a111406ceb9878dc1ff409dc9d7e62fca23b4fcb`  
		Last Modified: Thu, 30 May 2024 04:24:48 GMT  
		Size: 5.4 MB (5351041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d2d11b544756b6d8e93d89deb6119d65357b73278523bf5c2a4d35b3f58b1b`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 1.4 MB (1420765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cf89bcfa50143b74197a95c225b86c05af80d1319563716b6899bd75b746a3`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a6fe6195f181c5e90ee9a4c1d38d366c455b473f8f4fc109dc1db70c5536aa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d02df18f656835cd563756dfb06fc058e7157558482de610c8115675323a174`

```dockerfile
```

-	Layers:
	-	`sha256:689cb17aa17b78a3cb1fa0f18c25a34897b2276d84a65e29248992fdef29bcf6`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 278.3 KB (278321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f873bbf7f705ed6d30295cdc42ae04010f2a5f0dfe91acde3bf6fe05adfcca1`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
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
$ docker pull caddy@sha256:ca03efc1964e5a73d468e9543c9333e83b1d1c0a6077535c3bee9c732bbc407a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c94ee31a8787237f2a3fe0960078a830918ff0e25b743630569c2f95a3fb3ca`
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
	-	`sha256:61014b2ea6ecad7540420fd97ff35c204099831314d8af4b6bcefabfd60768c6`  
		Last Modified: Thu, 30 May 2024 03:50:11 GMT  
		Size: 6.2 MB (6240110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cddf047e6287c6194328f1cf1610743e450a59fffc7cdada00665f3e1a69de`  
		Last Modified: Thu, 30 May 2024 20:12:56 GMT  
		Size: 1.4 MB (1390030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d2892632bead1789583b0e83a9a7b547a7edbbd4cabe2723a57aa3da576895`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:c1735d271d08cab1c8e1dfe80f3d307bc4a569503cd3ac559de060137ad1e9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181edb797ade073642b1fa5a3acd2419f770ddce2b8b6dd0cf38dd37239cafd8`

```dockerfile
```

-	Layers:
	-	`sha256:cf87e4d2788d6a74320378065b9c88194584b780484699e00b81db822aef09a1`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde88d90ec100ec769b0531716096a71efafe182ff6ca6e5beafb579172743a`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - linux; s390x

```console
$ docker pull caddy@sha256:ddf41b94ba50096d4c83958a2f93d05e972a29f78e3cdbf5cc7297201d87d403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fe4747836e96d532a84ce7c51866f14573dd2a7184a1c98e09a3ecbb753511`
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
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dcf8f9ebef9601e1beaad8b4cc3d76b0eb4ff186a55cbca98c315ee818a4df`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fca2fb511f3ca4f6c95cda9f18b178cad865110e6249189b3d42a59533f87a`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:1a4cccca18bb45637c2fe9de18eb24b88ef5f1e5bee1f1aa4404906aa207c47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1676179af361cea13064135f85238a0c19b852b0b327478717c9c00c8db37f4`

```dockerfile
```

-	Layers:
	-	`sha256:339a9ba6f90463c144e1ee97eda33e02e6a462b01c2084c0c6c670f9b485074b`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90037cfca85f081f1a829fa848b68182197ddc46f70884e3e05924221d35e02d`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:10597519ab8ae6e2997ab33ed37ec084b7fa48197540fd8a5e9d6232e3eeefe7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212211421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c8c5c0c49c5e91e4db193bb2ceb6f49da6bb49f53d1f9273feefb5c4c4e8d`
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
# Thu, 30 May 2024 19:55:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:55:15 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:55:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:55:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 19:56:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 19:56:09 GMT
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
	-	`sha256:781a5790a63eb24d3d7b709f3885381842614c685aacc0e9f064de800ae074a5`  
		Last Modified: Thu, 30 May 2024 19:56:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adfb41eec4d294c5d5a6989921400c3ce8eac86190ca0e2729a220714fed0b7`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f50fb992e0f2417cc3d5dbd89e9bae09e2871bfb3da8442273c4393ccfeaea`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fe5c664cb62db2aa80c45ca5f51cc3c7a49fd4db915c14c9d3f3697b6e6a8`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dd35d7efa642909c8543d67ac3db36e703c2e00eba4cb7eb057a17a7c65632`  
		Last Modified: Thu, 30 May 2024 19:56:13 GMT  
		Size: 2.0 MB (1977015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcfc24e4cea1030166263d016513ca0181219e291b60093398c292a71217196`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8-builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:31ea6cb75b5ad08fb08500916a0a249d3cd3fac67e2062428129f1255fd747a6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d816cca71514d888c55882cedda59c9e63b2873912ab19d832e8f0c192cfa6`
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
# Thu, 30 May 2024 19:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:58:09 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:58:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:58:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 20:00:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 20:00:16 GMT
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
	-	`sha256:0fbedff9109d9c95af2643ac63a5cacb1b2bc7f05ffacb6f738c7bd71a8eccec`  
		Last Modified: Thu, 30 May 2024 20:00:20 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca153f0633c0d2c02ede7da833835063735438dffc496ac2f6e096fd2ffba56`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8add55d5a48aeb589d70b12c70950ab9d36ea1844e46a0c3243431fc5d023`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c23241851e0ece31bec24fbcc64f6a45ad49e757b6d83fd867de1db46ef1750`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1af3c5163dc4db242d8d318f53106e3edab0cbfcdee3719d51d1eb44031b1f`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 2.0 MB (1951704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fab58945a98d4f4ef5a6f69ce2d9c53b14cdfdb6bbf677de534c9df7f2a5d11`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-builder-alpine`

```console
$ docker pull caddy@sha256:9b0e5fefc8876b84dc74dd15b7413da6ad26b0642a4fb11d8f37399ad47fa572
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
$ docker pull caddy@sha256:9726224af4eeb16d52a30ae22fe0e0b06695c0e024f9efb295cf4bee09f57197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776279b710312f522ae60c2863326cc1b272d10acbb7f565d772d98cd7b45109`
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
	-	`sha256:b934fec1d0841de3fdf41cc33cdbc48551b5a2f0a7e6cdab65f224087005518c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 5.9 MB (5914558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3972621d02a746fb40b7f7396e9691786ac8736303b398c6036603239d4d71d6`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 1.5 MB (1500667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d524b2ee4c08318c294fb228d9d12bab4fdd1be5680e9c48d6c95a639cbaab`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:97b225e025145914c962df9facde72df887ac62754d89d0cbb531457bab05426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad49ab463e282ed01ac585005909bd73c83fadaeec1f96c8eddfbfd71db4e495`

```dockerfile
```

-	Layers:
	-	`sha256:7d8246f33a79fee33df45c06b03b4587ae80b11e9e8b4d884bc9ea55c5f85d9c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65fa569730f7d004dc9753ba63162b78b1fb241a2220365c79acf93bf64ec978`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:1fec3f7cab4729a430b8900be91337b7128699996c4fe0e1f3276789bd73025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b9fd44380823bd1943c0c1323b5d18b8d9cb6e5c054a20fd34d47e4a32d76c`
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
	-	`sha256:37d29efacbef5349371d8c2b88d68d880f345b5761f3223195407d2f95ed5b78`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 5.9 MB (5863446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e246b302345acefe6f5fe19701bee3f3c7e41a579ac1f76719acfad40786c2`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9137f20e52fd92773254f39e98b2c7b450128319173ca7acc759d95a5f325f0`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0bae879cdc66bcf071ce11018dfa7a07f602174d15582f2686fab10d6eb92d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9cfa298cd1818c69cf4b7c8b3df281a4a0e7928bf74488818b845639cc3c78`

```dockerfile
```

-	Layers:
	-	`sha256:69fe8062c086bf0def17c0407ea8856c140fdcb4d91cbd072987f1ab485c8439`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a1cb5e5de00be496dfe69ae4b4b55230c24327646c520e703a1b46dbd995296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04f376c2097ec4f9c5be43112ed5755c8e9f8b429f273a156dbcf4100dac79c`
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
	-	`sha256:8de42c46a5fc5e9bac21fd33a111406ceb9878dc1ff409dc9d7e62fca23b4fcb`  
		Last Modified: Thu, 30 May 2024 04:24:48 GMT  
		Size: 5.4 MB (5351041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d2d11b544756b6d8e93d89deb6119d65357b73278523bf5c2a4d35b3f58b1b`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 1.4 MB (1420765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cf89bcfa50143b74197a95c225b86c05af80d1319563716b6899bd75b746a3`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a6fe6195f181c5e90ee9a4c1d38d366c455b473f8f4fc109dc1db70c5536aa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d02df18f656835cd563756dfb06fc058e7157558482de610c8115675323a174`

```dockerfile
```

-	Layers:
	-	`sha256:689cb17aa17b78a3cb1fa0f18c25a34897b2276d84a65e29248992fdef29bcf6`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 278.3 KB (278321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f873bbf7f705ed6d30295cdc42ae04010f2a5f0dfe91acde3bf6fe05adfcca1`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
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
$ docker pull caddy@sha256:ca03efc1964e5a73d468e9543c9333e83b1d1c0a6077535c3bee9c732bbc407a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c94ee31a8787237f2a3fe0960078a830918ff0e25b743630569c2f95a3fb3ca`
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
	-	`sha256:61014b2ea6ecad7540420fd97ff35c204099831314d8af4b6bcefabfd60768c6`  
		Last Modified: Thu, 30 May 2024 03:50:11 GMT  
		Size: 6.2 MB (6240110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cddf047e6287c6194328f1cf1610743e450a59fffc7cdada00665f3e1a69de`  
		Last Modified: Thu, 30 May 2024 20:12:56 GMT  
		Size: 1.4 MB (1390030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d2892632bead1789583b0e83a9a7b547a7edbbd4cabe2723a57aa3da576895`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c1735d271d08cab1c8e1dfe80f3d307bc4a569503cd3ac559de060137ad1e9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181edb797ade073642b1fa5a3acd2419f770ddce2b8b6dd0cf38dd37239cafd8`

```dockerfile
```

-	Layers:
	-	`sha256:cf87e4d2788d6a74320378065b9c88194584b780484699e00b81db822aef09a1`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde88d90ec100ec769b0531716096a71efafe182ff6ca6e5beafb579172743a`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:ddf41b94ba50096d4c83958a2f93d05e972a29f78e3cdbf5cc7297201d87d403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fe4747836e96d532a84ce7c51866f14573dd2a7184a1c98e09a3ecbb753511`
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
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dcf8f9ebef9601e1beaad8b4cc3d76b0eb4ff186a55cbca98c315ee818a4df`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fca2fb511f3ca4f6c95cda9f18b178cad865110e6249189b3d42a59533f87a`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1a4cccca18bb45637c2fe9de18eb24b88ef5f1e5bee1f1aa4404906aa207c47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1676179af361cea13064135f85238a0c19b852b0b327478717c9c00c8db37f4`

```dockerfile
```

-	Layers:
	-	`sha256:339a9ba6f90463c144e1ee97eda33e02e6a462b01c2084c0c6c670f9b485074b`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90037cfca85f081f1a829fa848b68182197ddc46f70884e3e05924221d35e02d`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:4c00208a7869c08a9cb6ef821d15eafeac675e507194f54957fc91cbaf787e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:31ea6cb75b5ad08fb08500916a0a249d3cd3fac67e2062428129f1255fd747a6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d816cca71514d888c55882cedda59c9e63b2873912ab19d832e8f0c192cfa6`
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
# Thu, 30 May 2024 19:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:58:09 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:58:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:58:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 20:00:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 20:00:16 GMT
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
	-	`sha256:0fbedff9109d9c95af2643ac63a5cacb1b2bc7f05ffacb6f738c7bd71a8eccec`  
		Last Modified: Thu, 30 May 2024 20:00:20 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca153f0633c0d2c02ede7da833835063735438dffc496ac2f6e096fd2ffba56`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8add55d5a48aeb589d70b12c70950ab9d36ea1844e46a0c3243431fc5d023`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c23241851e0ece31bec24fbcc64f6a45ad49e757b6d83fd867de1db46ef1750`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1af3c5163dc4db242d8d318f53106e3edab0cbfcdee3719d51d1eb44031b1f`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 2.0 MB (1951704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fab58945a98d4f4ef5a6f69ce2d9c53b14cdfdb6bbf677de534c9df7f2a5d11`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:026063496c4412e2f6ad3d7eff0b72334f52eb6a26a76ad7d55413f1f2215b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:10597519ab8ae6e2997ab33ed37ec084b7fa48197540fd8a5e9d6232e3eeefe7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212211421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c8c5c0c49c5e91e4db193bb2ceb6f49da6bb49f53d1f9273feefb5c4c4e8d`
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
# Thu, 30 May 2024 19:55:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:55:15 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:55:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:55:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 19:56:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 19:56:09 GMT
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
	-	`sha256:781a5790a63eb24d3d7b709f3885381842614c685aacc0e9f064de800ae074a5`  
		Last Modified: Thu, 30 May 2024 19:56:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adfb41eec4d294c5d5a6989921400c3ce8eac86190ca0e2729a220714fed0b7`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f50fb992e0f2417cc3d5dbd89e9bae09e2871bfb3da8442273c4393ccfeaea`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fe5c664cb62db2aa80c45ca5f51cc3c7a49fd4db915c14c9d3f3697b6e6a8`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dd35d7efa642909c8543d67ac3db36e703c2e00eba4cb7eb057a17a7c65632`  
		Last Modified: Thu, 30 May 2024 19:56:13 GMT  
		Size: 2.0 MB (1977015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcfc24e4cea1030166263d016513ca0181219e291b60093398c292a71217196`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore`

```console
$ docker pull caddy@sha256:968fc01b86c3c4fd80a64a2e2bdbad91006c31b5dea58261ba4c678ee97341a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore-1809`

```console
$ docker pull caddy@sha256:d48df926bf363a40ecdc79c34c0a1fd25177d1ad25f3588dcc722924acd201a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7a8c826b69b921eba34d21e8f1432aa2173c0ef6595ac138f64856a830ee1204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.1`

```console
$ docker pull caddy@sha256:7414db60780a20966cd9621d1dcffcdcef060607ff32ddbfde2a3737405846c4
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

### `caddy:2.8.1` - linux; amd64

```console
$ docker pull caddy@sha256:21b4e37fefdfbc0b38227b3b6fcb805cfeab34715f39d218e4786cdf1a40c55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4829de267201b0e17026cc10e9f5c6aaf0cb9ecf4c47af6cca07c724e01ecef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65acfd58ee0383df10e747701a535d8eb3dac0dd8ad8947a9489b09700ad9d34`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 357.4 KB (357362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e249d258482cb8cd5b424e1644ad35cca37f57a78ae82f68da40abb4058219`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad68dac2ba05429229b54df92b7d1c8ecf608e981628a2ccd42f75bc9e35585`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 14.6 MB (14639266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1` - unknown; unknown

```console
$ docker pull caddy@sha256:0488da5140275dd85cabcbc6b4bd17ff4bc2a6b00173e98925c9559401389b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fbf645e9ac813c3bebf57f4eb989db435692e28e27b909e33a2ab0fb485a34`

```dockerfile
```

-	Layers:
	-	`sha256:399151dcea96073c9d5de979846a5a1b681fc579ac0be2d6b8f46a712067ad74`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ac1b53e222fa9515008993e54b82ed153489351621785b922ad6c38b02e16b`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1` - linux; arm variant v6

```console
$ docker pull caddy@sha256:27cb90616a8c910028f265c9a35e37b0a53ec818bcf78dca8935cb78685966f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51165ded103a1f093954ce84fe7980b1e20850c4c3565fcaf815aed24b4aa55c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5ade106a2b14c91e811b5be595c661aca72225039cc90670aeb4e92acc8fb`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 357.7 KB (357706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1311d826171a92f66f193a8b4b680699154cc050cf64890527f23bce7e030465`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5914ee1e526c5be906731c807280905bb260186dfcc9ded13553155ef1d07f`  
		Last Modified: Thu, 30 May 2024 19:57:55 GMT  
		Size: 13.8 MB (13763012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1` - unknown; unknown

```console
$ docker pull caddy@sha256:175d31b3aaf4bc9dc28938abb562c3639d2055acaaaa3b8b9a39ba9fbc3c31a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d117aac14a02f2556053c54ab993841ba82072e99f3ac61b5b263bcf783489e3`

```dockerfile
```

-	Layers:
	-	`sha256:b0bfc7c1bc28a001a221f1019947525245d903ddd68cdb36cecdebaf8be32643`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8bb480061ddd6a6c02b0133c5961abc6436f59ddd73c75040346b05d836fc8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17192991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8909144dcba13d585205edef980f7651a16da9574485be2862dec9ddacbc26c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5084781186f063a0bb6c3944407d818125eff602e2318b2b477ab01942afd5ef`  
		Last Modified: Thu, 30 May 2024 04:24:05 GMT  
		Size: 354.1 KB (354057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18302bdcf86d42d09129aeacce97eb83894389c4281eb661bb74d24898b3954d`  
		Last Modified: Thu, 30 May 2024 04:24:04 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4ba1984187ea68f8b4e33c5da9fd0cd0b837eb49cceaf672bc040a8a9b5b2`  
		Last Modified: Thu, 30 May 2024 20:10:44 GMT  
		Size: 13.7 MB (13737415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1` - unknown; unknown

```console
$ docker pull caddy@sha256:f3e04cfab426b603f0d3f9b04f93e53e5e96a896700417a416fc37f1ee8b9e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f470fb5d78b3b8b2143c88cf1d1cb11e6a759e7dd600d33067744eb3969d7064`

```dockerfile
```

-	Layers:
	-	`sha256:f90edc2b668319b5941bbfe7959e6d360942247c4efee398915d63f654d5a3c7`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
		Size: 263.9 KB (263883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70d2cebd4de6bf0de572d0e63bacef20ac991ca8f27f020a435f0a261fe1d6c`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1` - linux; arm64 variant v8

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

### `caddy:2.8.1` - unknown; unknown

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

### `caddy:2.8.1` - linux; ppc64le

```console
$ docker pull caddy@sha256:c324482f435aa50ae30f531d417545d7cc5586d76847279cba2077ea33e735a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17241541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0655e1dc6ab3c3e5f2b29fe680646c4dbd6a51427f027e8131c98c462244aa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ad67972e40ad224d572ec1975dcf39e560dcbe6b551c3ba4f39919a337f3b`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 370.4 KB (370393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa024c4e0f280d11973c0eda3b12f09a76e0381d137bc1b3f32a5aec6b814c79`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 7.4 KB (7447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b777476a3ae956d01f8bd0551800403bdb2da307a3fd8920e2e479f14378d7d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 13.3 MB (13293823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1` - unknown; unknown

```console
$ docker pull caddy@sha256:9e12f88ecde4df21cdd45a0ffb3cdf4fd8bbfb9a96063d66950f31a36c43ad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca7c5ceea57fcbe9468b1e28d188e8c92d894fe93efad5a85c8b9218fa8bbd7`

```dockerfile
```

-	Layers:
	-	`sha256:57c8adf6ec56a24a31792e239bf6547209e7c64f44343f4c7086558bd2ab4f4a`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 261.9 KB (261919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816f1138bf9ebcc1df2835942273446b6aedfefd4561b7fa37c561975d172b4d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1` - linux; s390x

```console
$ docker pull caddy@sha256:9e74b95e547eb1588c353d45473bb032367622a294199a26e72f8b352d023713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86dfcd59aa0a6fd0d01bfd9a897f6975a68f6680daf026ecc2ec85b35e29304`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240f4b8c6e2d5ad7a70cc783c821c10a0a0ecb4279a36796296b53241fc0105f`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 14.2 MB (14154632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1` - unknown; unknown

```console
$ docker pull caddy@sha256:aa3915fa8f7c9eaa46531086b6bf775173944010b62e751853379935819e2273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915a3930126fcee6c8cb4e8dcd4de24dcd0583072e33f2deaf7229e5385856f`

```dockerfile
```

-	Layers:
	-	`sha256:f4fce58be66b513afeb7b2fb194ae632e3c8457df54b0f13f72d1fbe09a43bf1`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01188c3d77dabde06f83507c443768248401b1b69ef1d5c709e82a4691cc4f9`  
		Last Modified: Thu, 30 May 2024 20:10:41 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8.1` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.1-alpine`

```console
$ docker pull caddy@sha256:54b067d60ae306670ab09f10b6f309f19e4e0f43927ae514d3740fbe7964872f
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

### `caddy:2.8.1-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:21b4e37fefdfbc0b38227b3b6fcb805cfeab34715f39d218e4786cdf1a40c55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4829de267201b0e17026cc10e9f5c6aaf0cb9ecf4c47af6cca07c724e01ecef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65acfd58ee0383df10e747701a535d8eb3dac0dd8ad8947a9489b09700ad9d34`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 357.4 KB (357362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e249d258482cb8cd5b424e1644ad35cca37f57a78ae82f68da40abb4058219`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad68dac2ba05429229b54df92b7d1c8ecf608e981628a2ccd42f75bc9e35585`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 14.6 MB (14639266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0488da5140275dd85cabcbc6b4bd17ff4bc2a6b00173e98925c9559401389b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fbf645e9ac813c3bebf57f4eb989db435692e28e27b909e33a2ab0fb485a34`

```dockerfile
```

-	Layers:
	-	`sha256:399151dcea96073c9d5de979846a5a1b681fc579ac0be2d6b8f46a712067ad74`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ac1b53e222fa9515008993e54b82ed153489351621785b922ad6c38b02e16b`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:27cb90616a8c910028f265c9a35e37b0a53ec818bcf78dca8935cb78685966f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51165ded103a1f093954ce84fe7980b1e20850c4c3565fcaf815aed24b4aa55c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5ade106a2b14c91e811b5be595c661aca72225039cc90670aeb4e92acc8fb`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 357.7 KB (357706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1311d826171a92f66f193a8b4b680699154cc050cf64890527f23bce7e030465`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5914ee1e526c5be906731c807280905bb260186dfcc9ded13553155ef1d07f`  
		Last Modified: Thu, 30 May 2024 19:57:55 GMT  
		Size: 13.8 MB (13763012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:175d31b3aaf4bc9dc28938abb562c3639d2055acaaaa3b8b9a39ba9fbc3c31a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d117aac14a02f2556053c54ab993841ba82072e99f3ac61b5b263bcf783489e3`

```dockerfile
```

-	Layers:
	-	`sha256:b0bfc7c1bc28a001a221f1019947525245d903ddd68cdb36cecdebaf8be32643`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8bb480061ddd6a6c02b0133c5961abc6436f59ddd73c75040346b05d836fc8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17192991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8909144dcba13d585205edef980f7651a16da9574485be2862dec9ddacbc26c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5084781186f063a0bb6c3944407d818125eff602e2318b2b477ab01942afd5ef`  
		Last Modified: Thu, 30 May 2024 04:24:05 GMT  
		Size: 354.1 KB (354057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18302bdcf86d42d09129aeacce97eb83894389c4281eb661bb74d24898b3954d`  
		Last Modified: Thu, 30 May 2024 04:24:04 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4ba1984187ea68f8b4e33c5da9fd0cd0b837eb49cceaf672bc040a8a9b5b2`  
		Last Modified: Thu, 30 May 2024 20:10:44 GMT  
		Size: 13.7 MB (13737415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f3e04cfab426b603f0d3f9b04f93e53e5e96a896700417a416fc37f1ee8b9e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f470fb5d78b3b8b2143c88cf1d1cb11e6a759e7dd600d33067744eb3969d7064`

```dockerfile
```

-	Layers:
	-	`sha256:f90edc2b668319b5941bbfe7959e6d360942247c4efee398915d63f654d5a3c7`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
		Size: 263.9 KB (263883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70d2cebd4de6bf0de572d0e63bacef20ac991ca8f27f020a435f0a261fe1d6c`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-alpine` - linux; arm64 variant v8

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

### `caddy:2.8.1-alpine` - unknown; unknown

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

### `caddy:2.8.1-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:c324482f435aa50ae30f531d417545d7cc5586d76847279cba2077ea33e735a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17241541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0655e1dc6ab3c3e5f2b29fe680646c4dbd6a51427f027e8131c98c462244aa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ad67972e40ad224d572ec1975dcf39e560dcbe6b551c3ba4f39919a337f3b`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 370.4 KB (370393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa024c4e0f280d11973c0eda3b12f09a76e0381d137bc1b3f32a5aec6b814c79`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 7.4 KB (7447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b777476a3ae956d01f8bd0551800403bdb2da307a3fd8920e2e479f14378d7d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 13.3 MB (13293823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9e12f88ecde4df21cdd45a0ffb3cdf4fd8bbfb9a96063d66950f31a36c43ad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca7c5ceea57fcbe9468b1e28d188e8c92d894fe93efad5a85c8b9218fa8bbd7`

```dockerfile
```

-	Layers:
	-	`sha256:57c8adf6ec56a24a31792e239bf6547209e7c64f44343f4c7086558bd2ab4f4a`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 261.9 KB (261919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816f1138bf9ebcc1df2835942273446b6aedfefd4561b7fa37c561975d172b4d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9e74b95e547eb1588c353d45473bb032367622a294199a26e72f8b352d023713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86dfcd59aa0a6fd0d01bfd9a897f6975a68f6680daf026ecc2ec85b35e29304`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240f4b8c6e2d5ad7a70cc783c821c10a0a0ecb4279a36796296b53241fc0105f`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 14.2 MB (14154632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:aa3915fa8f7c9eaa46531086b6bf775173944010b62e751853379935819e2273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915a3930126fcee6c8cb4e8dcd4de24dcd0583072e33f2deaf7229e5385856f`

```dockerfile
```

-	Layers:
	-	`sha256:f4fce58be66b513afeb7b2fb194ae632e3c8457df54b0f13f72d1fbe09a43bf1`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01188c3d77dabde06f83507c443768248401b1b69ef1d5c709e82a4691cc4f9`  
		Last Modified: Thu, 30 May 2024 20:10:41 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8.1-builder`

```console
$ docker pull caddy@sha256:37acf9e88ea74ef051bc1ec68ea9abd535320ea4eea1a0162aaf378ee5200a3c
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

### `caddy:2.8.1-builder` - linux; amd64

```console
$ docker pull caddy@sha256:9726224af4eeb16d52a30ae22fe0e0b06695c0e024f9efb295cf4bee09f57197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776279b710312f522ae60c2863326cc1b272d10acbb7f565d772d98cd7b45109`
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
	-	`sha256:b934fec1d0841de3fdf41cc33cdbc48551b5a2f0a7e6cdab65f224087005518c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 5.9 MB (5914558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3972621d02a746fb40b7f7396e9691786ac8736303b398c6036603239d4d71d6`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 1.5 MB (1500667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d524b2ee4c08318c294fb228d9d12bab4fdd1be5680e9c48d6c95a639cbaab`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:97b225e025145914c962df9facde72df887ac62754d89d0cbb531457bab05426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad49ab463e282ed01ac585005909bd73c83fadaeec1f96c8eddfbfd71db4e495`

```dockerfile
```

-	Layers:
	-	`sha256:7d8246f33a79fee33df45c06b03b4587ae80b11e9e8b4d884bc9ea55c5f85d9c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65fa569730f7d004dc9753ba63162b78b1fb241a2220365c79acf93bf64ec978`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:1fec3f7cab4729a430b8900be91337b7128699996c4fe0e1f3276789bd73025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b9fd44380823bd1943c0c1323b5d18b8d9cb6e5c054a20fd34d47e4a32d76c`
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
	-	`sha256:37d29efacbef5349371d8c2b88d68d880f345b5761f3223195407d2f95ed5b78`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 5.9 MB (5863446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e246b302345acefe6f5fe19701bee3f3c7e41a579ac1f76719acfad40786c2`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9137f20e52fd92773254f39e98b2c7b450128319173ca7acc759d95a5f325f0`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0bae879cdc66bcf071ce11018dfa7a07f602174d15582f2686fab10d6eb92d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9cfa298cd1818c69cf4b7c8b3df281a4a0e7928bf74488818b845639cc3c78`

```dockerfile
```

-	Layers:
	-	`sha256:69fe8062c086bf0def17c0407ea8856c140fdcb4d91cbd072987f1ab485c8439`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a1cb5e5de00be496dfe69ae4b4b55230c24327646c520e703a1b46dbd995296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04f376c2097ec4f9c5be43112ed5755c8e9f8b429f273a156dbcf4100dac79c`
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
	-	`sha256:8de42c46a5fc5e9bac21fd33a111406ceb9878dc1ff409dc9d7e62fca23b4fcb`  
		Last Modified: Thu, 30 May 2024 04:24:48 GMT  
		Size: 5.4 MB (5351041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d2d11b544756b6d8e93d89deb6119d65357b73278523bf5c2a4d35b3f58b1b`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 1.4 MB (1420765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cf89bcfa50143b74197a95c225b86c05af80d1319563716b6899bd75b746a3`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a6fe6195f181c5e90ee9a4c1d38d366c455b473f8f4fc109dc1db70c5536aa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d02df18f656835cd563756dfb06fc058e7157558482de610c8115675323a174`

```dockerfile
```

-	Layers:
	-	`sha256:689cb17aa17b78a3cb1fa0f18c25a34897b2276d84a65e29248992fdef29bcf6`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 278.3 KB (278321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f873bbf7f705ed6d30295cdc42ae04010f2a5f0dfe91acde3bf6fe05adfcca1`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-builder` - linux; arm64 variant v8

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

### `caddy:2.8.1-builder` - unknown; unknown

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

### `caddy:2.8.1-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ca03efc1964e5a73d468e9543c9333e83b1d1c0a6077535c3bee9c732bbc407a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c94ee31a8787237f2a3fe0960078a830918ff0e25b743630569c2f95a3fb3ca`
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
	-	`sha256:61014b2ea6ecad7540420fd97ff35c204099831314d8af4b6bcefabfd60768c6`  
		Last Modified: Thu, 30 May 2024 03:50:11 GMT  
		Size: 6.2 MB (6240110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cddf047e6287c6194328f1cf1610743e450a59fffc7cdada00665f3e1a69de`  
		Last Modified: Thu, 30 May 2024 20:12:56 GMT  
		Size: 1.4 MB (1390030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d2892632bead1789583b0e83a9a7b547a7edbbd4cabe2723a57aa3da576895`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:c1735d271d08cab1c8e1dfe80f3d307bc4a569503cd3ac559de060137ad1e9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181edb797ade073642b1fa5a3acd2419f770ddce2b8b6dd0cf38dd37239cafd8`

```dockerfile
```

-	Layers:
	-	`sha256:cf87e4d2788d6a74320378065b9c88194584b780484699e00b81db822aef09a1`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde88d90ec100ec769b0531716096a71efafe182ff6ca6e5beafb579172743a`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-builder` - linux; s390x

```console
$ docker pull caddy@sha256:ddf41b94ba50096d4c83958a2f93d05e972a29f78e3cdbf5cc7297201d87d403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fe4747836e96d532a84ce7c51866f14573dd2a7184a1c98e09a3ecbb753511`
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
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dcf8f9ebef9601e1beaad8b4cc3d76b0eb4ff186a55cbca98c315ee818a4df`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fca2fb511f3ca4f6c95cda9f18b178cad865110e6249189b3d42a59533f87a`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:1a4cccca18bb45637c2fe9de18eb24b88ef5f1e5bee1f1aa4404906aa207c47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1676179af361cea13064135f85238a0c19b852b0b327478717c9c00c8db37f4`

```dockerfile
```

-	Layers:
	-	`sha256:339a9ba6f90463c144e1ee97eda33e02e6a462b01c2084c0c6c670f9b485074b`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90037cfca85f081f1a829fa848b68182197ddc46f70884e3e05924221d35e02d`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:10597519ab8ae6e2997ab33ed37ec084b7fa48197540fd8a5e9d6232e3eeefe7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212211421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c8c5c0c49c5e91e4db193bb2ceb6f49da6bb49f53d1f9273feefb5c4c4e8d`
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
# Thu, 30 May 2024 19:55:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:55:15 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:55:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:55:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 19:56:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 19:56:09 GMT
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
	-	`sha256:781a5790a63eb24d3d7b709f3885381842614c685aacc0e9f064de800ae074a5`  
		Last Modified: Thu, 30 May 2024 19:56:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adfb41eec4d294c5d5a6989921400c3ce8eac86190ca0e2729a220714fed0b7`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f50fb992e0f2417cc3d5dbd89e9bae09e2871bfb3da8442273c4393ccfeaea`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fe5c664cb62db2aa80c45ca5f51cc3c7a49fd4db915c14c9d3f3697b6e6a8`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dd35d7efa642909c8543d67ac3db36e703c2e00eba4cb7eb057a17a7c65632`  
		Last Modified: Thu, 30 May 2024 19:56:13 GMT  
		Size: 2.0 MB (1977015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcfc24e4cea1030166263d016513ca0181219e291b60093398c292a71217196`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8.1-builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:31ea6cb75b5ad08fb08500916a0a249d3cd3fac67e2062428129f1255fd747a6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d816cca71514d888c55882cedda59c9e63b2873912ab19d832e8f0c192cfa6`
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
# Thu, 30 May 2024 19:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:58:09 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:58:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:58:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 20:00:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 20:00:16 GMT
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
	-	`sha256:0fbedff9109d9c95af2643ac63a5cacb1b2bc7f05ffacb6f738c7bd71a8eccec`  
		Last Modified: Thu, 30 May 2024 20:00:20 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca153f0633c0d2c02ede7da833835063735438dffc496ac2f6e096fd2ffba56`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8add55d5a48aeb589d70b12c70950ab9d36ea1844e46a0c3243431fc5d023`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c23241851e0ece31bec24fbcc64f6a45ad49e757b6d83fd867de1db46ef1750`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1af3c5163dc4db242d8d318f53106e3edab0cbfcdee3719d51d1eb44031b1f`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 2.0 MB (1951704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fab58945a98d4f4ef5a6f69ce2d9c53b14cdfdb6bbf677de534c9df7f2a5d11`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.1-builder-alpine`

```console
$ docker pull caddy@sha256:9b0e5fefc8876b84dc74dd15b7413da6ad26b0642a4fb11d8f37399ad47fa572
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

### `caddy:2.8.1-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:9726224af4eeb16d52a30ae22fe0e0b06695c0e024f9efb295cf4bee09f57197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776279b710312f522ae60c2863326cc1b272d10acbb7f565d772d98cd7b45109`
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
	-	`sha256:b934fec1d0841de3fdf41cc33cdbc48551b5a2f0a7e6cdab65f224087005518c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 5.9 MB (5914558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3972621d02a746fb40b7f7396e9691786ac8736303b398c6036603239d4d71d6`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 1.5 MB (1500667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d524b2ee4c08318c294fb228d9d12bab4fdd1be5680e9c48d6c95a639cbaab`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:97b225e025145914c962df9facde72df887ac62754d89d0cbb531457bab05426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad49ab463e282ed01ac585005909bd73c83fadaeec1f96c8eddfbfd71db4e495`

```dockerfile
```

-	Layers:
	-	`sha256:7d8246f33a79fee33df45c06b03b4587ae80b11e9e8b4d884bc9ea55c5f85d9c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65fa569730f7d004dc9753ba63162b78b1fb241a2220365c79acf93bf64ec978`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:1fec3f7cab4729a430b8900be91337b7128699996c4fe0e1f3276789bd73025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b9fd44380823bd1943c0c1323b5d18b8d9cb6e5c054a20fd34d47e4a32d76c`
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
	-	`sha256:37d29efacbef5349371d8c2b88d68d880f345b5761f3223195407d2f95ed5b78`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 5.9 MB (5863446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e246b302345acefe6f5fe19701bee3f3c7e41a579ac1f76719acfad40786c2`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9137f20e52fd92773254f39e98b2c7b450128319173ca7acc759d95a5f325f0`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0bae879cdc66bcf071ce11018dfa7a07f602174d15582f2686fab10d6eb92d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9cfa298cd1818c69cf4b7c8b3df281a4a0e7928bf74488818b845639cc3c78`

```dockerfile
```

-	Layers:
	-	`sha256:69fe8062c086bf0def17c0407ea8856c140fdcb4d91cbd072987f1ab485c8439`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a1cb5e5de00be496dfe69ae4b4b55230c24327646c520e703a1b46dbd995296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04f376c2097ec4f9c5be43112ed5755c8e9f8b429f273a156dbcf4100dac79c`
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
	-	`sha256:8de42c46a5fc5e9bac21fd33a111406ceb9878dc1ff409dc9d7e62fca23b4fcb`  
		Last Modified: Thu, 30 May 2024 04:24:48 GMT  
		Size: 5.4 MB (5351041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d2d11b544756b6d8e93d89deb6119d65357b73278523bf5c2a4d35b3f58b1b`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 1.4 MB (1420765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cf89bcfa50143b74197a95c225b86c05af80d1319563716b6899bd75b746a3`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a6fe6195f181c5e90ee9a4c1d38d366c455b473f8f4fc109dc1db70c5536aa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d02df18f656835cd563756dfb06fc058e7157558482de610c8115675323a174`

```dockerfile
```

-	Layers:
	-	`sha256:689cb17aa17b78a3cb1fa0f18c25a34897b2276d84a65e29248992fdef29bcf6`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 278.3 KB (278321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f873bbf7f705ed6d30295cdc42ae04010f2a5f0dfe91acde3bf6fe05adfcca1`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-builder-alpine` - linux; arm64 variant v8

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

### `caddy:2.8.1-builder-alpine` - unknown; unknown

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

### `caddy:2.8.1-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ca03efc1964e5a73d468e9543c9333e83b1d1c0a6077535c3bee9c732bbc407a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c94ee31a8787237f2a3fe0960078a830918ff0e25b743630569c2f95a3fb3ca`
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
	-	`sha256:61014b2ea6ecad7540420fd97ff35c204099831314d8af4b6bcefabfd60768c6`  
		Last Modified: Thu, 30 May 2024 03:50:11 GMT  
		Size: 6.2 MB (6240110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cddf047e6287c6194328f1cf1610743e450a59fffc7cdada00665f3e1a69de`  
		Last Modified: Thu, 30 May 2024 20:12:56 GMT  
		Size: 1.4 MB (1390030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d2892632bead1789583b0e83a9a7b547a7edbbd4cabe2723a57aa3da576895`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c1735d271d08cab1c8e1dfe80f3d307bc4a569503cd3ac559de060137ad1e9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181edb797ade073642b1fa5a3acd2419f770ddce2b8b6dd0cf38dd37239cafd8`

```dockerfile
```

-	Layers:
	-	`sha256:cf87e4d2788d6a74320378065b9c88194584b780484699e00b81db822aef09a1`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde88d90ec100ec769b0531716096a71efafe182ff6ca6e5beafb579172743a`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.8.1-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:ddf41b94ba50096d4c83958a2f93d05e972a29f78e3cdbf5cc7297201d87d403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fe4747836e96d532a84ce7c51866f14573dd2a7184a1c98e09a3ecbb753511`
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
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dcf8f9ebef9601e1beaad8b4cc3d76b0eb4ff186a55cbca98c315ee818a4df`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fca2fb511f3ca4f6c95cda9f18b178cad865110e6249189b3d42a59533f87a`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.8.1-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1a4cccca18bb45637c2fe9de18eb24b88ef5f1e5bee1f1aa4404906aa207c47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1676179af361cea13064135f85238a0c19b852b0b327478717c9c00c8db37f4`

```dockerfile
```

-	Layers:
	-	`sha256:339a9ba6f90463c144e1ee97eda33e02e6a462b01c2084c0c6c670f9b485074b`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90037cfca85f081f1a829fa848b68182197ddc46f70884e3e05924221d35e02d`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.8.1-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:4c00208a7869c08a9cb6ef821d15eafeac675e507194f54957fc91cbaf787e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.1-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:31ea6cb75b5ad08fb08500916a0a249d3cd3fac67e2062428129f1255fd747a6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d816cca71514d888c55882cedda59c9e63b2873912ab19d832e8f0c192cfa6`
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
# Thu, 30 May 2024 19:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:58:09 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:58:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:58:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 20:00:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 20:00:16 GMT
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
	-	`sha256:0fbedff9109d9c95af2643ac63a5cacb1b2bc7f05ffacb6f738c7bd71a8eccec`  
		Last Modified: Thu, 30 May 2024 20:00:20 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca153f0633c0d2c02ede7da833835063735438dffc496ac2f6e096fd2ffba56`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8add55d5a48aeb589d70b12c70950ab9d36ea1844e46a0c3243431fc5d023`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c23241851e0ece31bec24fbcc64f6a45ad49e757b6d83fd867de1db46ef1750`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1af3c5163dc4db242d8d318f53106e3edab0cbfcdee3719d51d1eb44031b1f`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 2.0 MB (1951704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fab58945a98d4f4ef5a6f69ce2d9c53b14cdfdb6bbf677de534c9df7f2a5d11`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.1-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:026063496c4412e2f6ad3d7eff0b72334f52eb6a26a76ad7d55413f1f2215b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8.1-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:10597519ab8ae6e2997ab33ed37ec084b7fa48197540fd8a5e9d6232e3eeefe7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212211421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c8c5c0c49c5e91e4db193bb2ceb6f49da6bb49f53d1f9273feefb5c4c4e8d`
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
# Thu, 30 May 2024 19:55:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:55:15 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:55:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:55:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 19:56:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 19:56:09 GMT
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
	-	`sha256:781a5790a63eb24d3d7b709f3885381842614c685aacc0e9f064de800ae074a5`  
		Last Modified: Thu, 30 May 2024 19:56:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adfb41eec4d294c5d5a6989921400c3ce8eac86190ca0e2729a220714fed0b7`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f50fb992e0f2417cc3d5dbd89e9bae09e2871bfb3da8442273c4393ccfeaea`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fe5c664cb62db2aa80c45ca5f51cc3c7a49fd4db915c14c9d3f3697b6e6a8`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dd35d7efa642909c8543d67ac3db36e703c2e00eba4cb7eb057a17a7c65632`  
		Last Modified: Thu, 30 May 2024 19:56:13 GMT  
		Size: 2.0 MB (1977015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcfc24e4cea1030166263d016513ca0181219e291b60093398c292a71217196`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.1-windowsservercore`

```console
$ docker pull caddy@sha256:968fc01b86c3c4fd80a64a2e2bdbad91006c31b5dea58261ba4c678ee97341a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.1-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.8.1-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.1-windowsservercore-1809`

```console
$ docker pull caddy@sha256:d48df926bf363a40ecdc79c34c0a1fd25177d1ad25f3588dcc722924acd201a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2.8.1-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.8.1-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7a8c826b69b921eba34d21e8f1432aa2173c0ef6595ac138f64856a830ee1204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2.8.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:54b067d60ae306670ab09f10b6f309f19e4e0f43927ae514d3740fbe7964872f
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
$ docker pull caddy@sha256:21b4e37fefdfbc0b38227b3b6fcb805cfeab34715f39d218e4786cdf1a40c55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4829de267201b0e17026cc10e9f5c6aaf0cb9ecf4c47af6cca07c724e01ecef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65acfd58ee0383df10e747701a535d8eb3dac0dd8ad8947a9489b09700ad9d34`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 357.4 KB (357362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e249d258482cb8cd5b424e1644ad35cca37f57a78ae82f68da40abb4058219`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad68dac2ba05429229b54df92b7d1c8ecf608e981628a2ccd42f75bc9e35585`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 14.6 MB (14639266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0488da5140275dd85cabcbc6b4bd17ff4bc2a6b00173e98925c9559401389b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fbf645e9ac813c3bebf57f4eb989db435692e28e27b909e33a2ab0fb485a34`

```dockerfile
```

-	Layers:
	-	`sha256:399151dcea96073c9d5de979846a5a1b681fc579ac0be2d6b8f46a712067ad74`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ac1b53e222fa9515008993e54b82ed153489351621785b922ad6c38b02e16b`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:27cb90616a8c910028f265c9a35e37b0a53ec818bcf78dca8935cb78685966f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51165ded103a1f093954ce84fe7980b1e20850c4c3565fcaf815aed24b4aa55c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5ade106a2b14c91e811b5be595c661aca72225039cc90670aeb4e92acc8fb`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 357.7 KB (357706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1311d826171a92f66f193a8b4b680699154cc050cf64890527f23bce7e030465`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5914ee1e526c5be906731c807280905bb260186dfcc9ded13553155ef1d07f`  
		Last Modified: Thu, 30 May 2024 19:57:55 GMT  
		Size: 13.8 MB (13763012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:175d31b3aaf4bc9dc28938abb562c3639d2055acaaaa3b8b9a39ba9fbc3c31a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d117aac14a02f2556053c54ab993841ba82072e99f3ac61b5b263bcf783489e3`

```dockerfile
```

-	Layers:
	-	`sha256:b0bfc7c1bc28a001a221f1019947525245d903ddd68cdb36cecdebaf8be32643`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8bb480061ddd6a6c02b0133c5961abc6436f59ddd73c75040346b05d836fc8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17192991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8909144dcba13d585205edef980f7651a16da9574485be2862dec9ddacbc26c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5084781186f063a0bb6c3944407d818125eff602e2318b2b477ab01942afd5ef`  
		Last Modified: Thu, 30 May 2024 04:24:05 GMT  
		Size: 354.1 KB (354057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18302bdcf86d42d09129aeacce97eb83894389c4281eb661bb74d24898b3954d`  
		Last Modified: Thu, 30 May 2024 04:24:04 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4ba1984187ea68f8b4e33c5da9fd0cd0b837eb49cceaf672bc040a8a9b5b2`  
		Last Modified: Thu, 30 May 2024 20:10:44 GMT  
		Size: 13.7 MB (13737415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f3e04cfab426b603f0d3f9b04f93e53e5e96a896700417a416fc37f1ee8b9e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f470fb5d78b3b8b2143c88cf1d1cb11e6a759e7dd600d33067744eb3969d7064`

```dockerfile
```

-	Layers:
	-	`sha256:f90edc2b668319b5941bbfe7959e6d360942247c4efee398915d63f654d5a3c7`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
		Size: 263.9 KB (263883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70d2cebd4de6bf0de572d0e63bacef20ac991ca8f27f020a435f0a261fe1d6c`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
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
$ docker pull caddy@sha256:c324482f435aa50ae30f531d417545d7cc5586d76847279cba2077ea33e735a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17241541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0655e1dc6ab3c3e5f2b29fe680646c4dbd6a51427f027e8131c98c462244aa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ad67972e40ad224d572ec1975dcf39e560dcbe6b551c3ba4f39919a337f3b`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 370.4 KB (370393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa024c4e0f280d11973c0eda3b12f09a76e0381d137bc1b3f32a5aec6b814c79`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 7.4 KB (7447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b777476a3ae956d01f8bd0551800403bdb2da307a3fd8920e2e479f14378d7d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 13.3 MB (13293823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9e12f88ecde4df21cdd45a0ffb3cdf4fd8bbfb9a96063d66950f31a36c43ad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca7c5ceea57fcbe9468b1e28d188e8c92d894fe93efad5a85c8b9218fa8bbd7`

```dockerfile
```

-	Layers:
	-	`sha256:57c8adf6ec56a24a31792e239bf6547209e7c64f44343f4c7086558bd2ab4f4a`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 261.9 KB (261919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816f1138bf9ebcc1df2835942273446b6aedfefd4561b7fa37c561975d172b4d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9e74b95e547eb1588c353d45473bb032367622a294199a26e72f8b352d023713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86dfcd59aa0a6fd0d01bfd9a897f6975a68f6680daf026ecc2ec85b35e29304`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240f4b8c6e2d5ad7a70cc783c821c10a0a0ecb4279a36796296b53241fc0105f`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 14.2 MB (14154632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:aa3915fa8f7c9eaa46531086b6bf775173944010b62e751853379935819e2273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915a3930126fcee6c8cb4e8dcd4de24dcd0583072e33f2deaf7229e5385856f`

```dockerfile
```

-	Layers:
	-	`sha256:f4fce58be66b513afeb7b2fb194ae632e3c8457df54b0f13f72d1fbe09a43bf1`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01188c3d77dabde06f83507c443768248401b1b69ef1d5c709e82a4691cc4f9`  
		Last Modified: Thu, 30 May 2024 20:10:41 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder`

```console
$ docker pull caddy@sha256:37acf9e88ea74ef051bc1ec68ea9abd535320ea4eea1a0162aaf378ee5200a3c
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
$ docker pull caddy@sha256:9726224af4eeb16d52a30ae22fe0e0b06695c0e024f9efb295cf4bee09f57197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776279b710312f522ae60c2863326cc1b272d10acbb7f565d772d98cd7b45109`
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
	-	`sha256:b934fec1d0841de3fdf41cc33cdbc48551b5a2f0a7e6cdab65f224087005518c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 5.9 MB (5914558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3972621d02a746fb40b7f7396e9691786ac8736303b398c6036603239d4d71d6`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 1.5 MB (1500667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d524b2ee4c08318c294fb228d9d12bab4fdd1be5680e9c48d6c95a639cbaab`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:97b225e025145914c962df9facde72df887ac62754d89d0cbb531457bab05426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad49ab463e282ed01ac585005909bd73c83fadaeec1f96c8eddfbfd71db4e495`

```dockerfile
```

-	Layers:
	-	`sha256:7d8246f33a79fee33df45c06b03b4587ae80b11e9e8b4d884bc9ea55c5f85d9c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65fa569730f7d004dc9753ba63162b78b1fb241a2220365c79acf93bf64ec978`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:1fec3f7cab4729a430b8900be91337b7128699996c4fe0e1f3276789bd73025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b9fd44380823bd1943c0c1323b5d18b8d9cb6e5c054a20fd34d47e4a32d76c`
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
	-	`sha256:37d29efacbef5349371d8c2b88d68d880f345b5761f3223195407d2f95ed5b78`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 5.9 MB (5863446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e246b302345acefe6f5fe19701bee3f3c7e41a579ac1f76719acfad40786c2`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9137f20e52fd92773254f39e98b2c7b450128319173ca7acc759d95a5f325f0`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0bae879cdc66bcf071ce11018dfa7a07f602174d15582f2686fab10d6eb92d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9cfa298cd1818c69cf4b7c8b3df281a4a0e7928bf74488818b845639cc3c78`

```dockerfile
```

-	Layers:
	-	`sha256:69fe8062c086bf0def17c0407ea8856c140fdcb4d91cbd072987f1ab485c8439`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a1cb5e5de00be496dfe69ae4b4b55230c24327646c520e703a1b46dbd995296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04f376c2097ec4f9c5be43112ed5755c8e9f8b429f273a156dbcf4100dac79c`
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
	-	`sha256:8de42c46a5fc5e9bac21fd33a111406ceb9878dc1ff409dc9d7e62fca23b4fcb`  
		Last Modified: Thu, 30 May 2024 04:24:48 GMT  
		Size: 5.4 MB (5351041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d2d11b544756b6d8e93d89deb6119d65357b73278523bf5c2a4d35b3f58b1b`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 1.4 MB (1420765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cf89bcfa50143b74197a95c225b86c05af80d1319563716b6899bd75b746a3`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a6fe6195f181c5e90ee9a4c1d38d366c455b473f8f4fc109dc1db70c5536aa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d02df18f656835cd563756dfb06fc058e7157558482de610c8115675323a174`

```dockerfile
```

-	Layers:
	-	`sha256:689cb17aa17b78a3cb1fa0f18c25a34897b2276d84a65e29248992fdef29bcf6`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 278.3 KB (278321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f873bbf7f705ed6d30295cdc42ae04010f2a5f0dfe91acde3bf6fe05adfcca1`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
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
$ docker pull caddy@sha256:ca03efc1964e5a73d468e9543c9333e83b1d1c0a6077535c3bee9c732bbc407a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c94ee31a8787237f2a3fe0960078a830918ff0e25b743630569c2f95a3fb3ca`
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
	-	`sha256:61014b2ea6ecad7540420fd97ff35c204099831314d8af4b6bcefabfd60768c6`  
		Last Modified: Thu, 30 May 2024 03:50:11 GMT  
		Size: 6.2 MB (6240110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cddf047e6287c6194328f1cf1610743e450a59fffc7cdada00665f3e1a69de`  
		Last Modified: Thu, 30 May 2024 20:12:56 GMT  
		Size: 1.4 MB (1390030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d2892632bead1789583b0e83a9a7b547a7edbbd4cabe2723a57aa3da576895`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:c1735d271d08cab1c8e1dfe80f3d307bc4a569503cd3ac559de060137ad1e9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181edb797ade073642b1fa5a3acd2419f770ddce2b8b6dd0cf38dd37239cafd8`

```dockerfile
```

-	Layers:
	-	`sha256:cf87e4d2788d6a74320378065b9c88194584b780484699e00b81db822aef09a1`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde88d90ec100ec769b0531716096a71efafe182ff6ca6e5beafb579172743a`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:ddf41b94ba50096d4c83958a2f93d05e972a29f78e3cdbf5cc7297201d87d403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fe4747836e96d532a84ce7c51866f14573dd2a7184a1c98e09a3ecbb753511`
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
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dcf8f9ebef9601e1beaad8b4cc3d76b0eb4ff186a55cbca98c315ee818a4df`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fca2fb511f3ca4f6c95cda9f18b178cad865110e6249189b3d42a59533f87a`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:1a4cccca18bb45637c2fe9de18eb24b88ef5f1e5bee1f1aa4404906aa207c47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1676179af361cea13064135f85238a0c19b852b0b327478717c9c00c8db37f4`

```dockerfile
```

-	Layers:
	-	`sha256:339a9ba6f90463c144e1ee97eda33e02e6a462b01c2084c0c6c670f9b485074b`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90037cfca85f081f1a829fa848b68182197ddc46f70884e3e05924221d35e02d`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:10597519ab8ae6e2997ab33ed37ec084b7fa48197540fd8a5e9d6232e3eeefe7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212211421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c8c5c0c49c5e91e4db193bb2ceb6f49da6bb49f53d1f9273feefb5c4c4e8d`
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
# Thu, 30 May 2024 19:55:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:55:15 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:55:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:55:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 19:56:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 19:56:09 GMT
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
	-	`sha256:781a5790a63eb24d3d7b709f3885381842614c685aacc0e9f064de800ae074a5`  
		Last Modified: Thu, 30 May 2024 19:56:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adfb41eec4d294c5d5a6989921400c3ce8eac86190ca0e2729a220714fed0b7`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f50fb992e0f2417cc3d5dbd89e9bae09e2871bfb3da8442273c4393ccfeaea`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fe5c664cb62db2aa80c45ca5f51cc3c7a49fd4db915c14c9d3f3697b6e6a8`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dd35d7efa642909c8543d67ac3db36e703c2e00eba4cb7eb057a17a7c65632`  
		Last Modified: Thu, 30 May 2024 19:56:13 GMT  
		Size: 2.0 MB (1977015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcfc24e4cea1030166263d016513ca0181219e291b60093398c292a71217196`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:31ea6cb75b5ad08fb08500916a0a249d3cd3fac67e2062428129f1255fd747a6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d816cca71514d888c55882cedda59c9e63b2873912ab19d832e8f0c192cfa6`
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
# Thu, 30 May 2024 19:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:58:09 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:58:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:58:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 20:00:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 20:00:16 GMT
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
	-	`sha256:0fbedff9109d9c95af2643ac63a5cacb1b2bc7f05ffacb6f738c7bd71a8eccec`  
		Last Modified: Thu, 30 May 2024 20:00:20 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca153f0633c0d2c02ede7da833835063735438dffc496ac2f6e096fd2ffba56`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8add55d5a48aeb589d70b12c70950ab9d36ea1844e46a0c3243431fc5d023`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c23241851e0ece31bec24fbcc64f6a45ad49e757b6d83fd867de1db46ef1750`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1af3c5163dc4db242d8d318f53106e3edab0cbfcdee3719d51d1eb44031b1f`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 2.0 MB (1951704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fab58945a98d4f4ef5a6f69ce2d9c53b14cdfdb6bbf677de534c9df7f2a5d11`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:9b0e5fefc8876b84dc74dd15b7413da6ad26b0642a4fb11d8f37399ad47fa572
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
$ docker pull caddy@sha256:9726224af4eeb16d52a30ae22fe0e0b06695c0e024f9efb295cf4bee09f57197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80673029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776279b710312f522ae60c2863326cc1b272d10acbb7f565d772d98cd7b45109`
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
	-	`sha256:b934fec1d0841de3fdf41cc33cdbc48551b5a2f0a7e6cdab65f224087005518c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 5.9 MB (5914558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3972621d02a746fb40b7f7396e9691786ac8736303b398c6036603239d4d71d6`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 1.5 MB (1500667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d524b2ee4c08318c294fb228d9d12bab4fdd1be5680e9c48d6c95a639cbaab`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:97b225e025145914c962df9facde72df887ac62754d89d0cbb531457bab05426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 KB (295278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad49ab463e282ed01ac585005909bd73c83fadaeec1f96c8eddfbfd71db4e495`

```dockerfile
```

-	Layers:
	-	`sha256:7d8246f33a79fee33df45c06b03b4587ae80b11e9e8b4d884bc9ea55c5f85d9c`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 275.7 KB (275709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65fa569730f7d004dc9753ba63162b78b1fb241a2220365c79acf93bf64ec978`  
		Last Modified: Thu, 30 May 2024 19:53:37 GMT  
		Size: 19.6 KB (19569 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:1fec3f7cab4729a430b8900be91337b7128699996c4fe0e1f3276789bd73025b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78661750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b9fd44380823bd1943c0c1323b5d18b8d9cb6e5c054a20fd34d47e4a32d76c`
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
	-	`sha256:37d29efacbef5349371d8c2b88d68d880f345b5761f3223195407d2f95ed5b78`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 5.9 MB (5863446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e246b302345acefe6f5fe19701bee3f3c7e41a579ac1f76719acfad40786c2`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9137f20e52fd92773254f39e98b2c7b450128319173ca7acc759d95a5f325f0`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0bae879cdc66bcf071ce11018dfa7a07f602174d15582f2686fab10d6eb92d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9cfa298cd1818c69cf4b7c8b3df281a4a0e7928bf74488818b845639cc3c78`

```dockerfile
```

-	Layers:
	-	`sha256:69fe8062c086bf0def17c0407ea8856c140fdcb4d91cbd072987f1ab485c8439`  
		Last Modified: Thu, 30 May 2024 19:58:21 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a1cb5e5de00be496dfe69ae4b4b55230c24327646c520e703a1b46dbd995296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04f376c2097ec4f9c5be43112ed5755c8e9f8b429f273a156dbcf4100dac79c`
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
	-	`sha256:8de42c46a5fc5e9bac21fd33a111406ceb9878dc1ff409dc9d7e62fca23b4fcb`  
		Last Modified: Thu, 30 May 2024 04:24:48 GMT  
		Size: 5.4 MB (5351041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d2d11b544756b6d8e93d89deb6119d65357b73278523bf5c2a4d35b3f58b1b`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 1.4 MB (1420765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cf89bcfa50143b74197a95c225b86c05af80d1319563716b6899bd75b746a3`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a6fe6195f181c5e90ee9a4c1d38d366c455b473f8f4fc109dc1db70c5536aa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (298041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d02df18f656835cd563756dfb06fc058e7157558482de610c8115675323a174`

```dockerfile
```

-	Layers:
	-	`sha256:689cb17aa17b78a3cb1fa0f18c25a34897b2276d84a65e29248992fdef29bcf6`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
		Size: 278.3 KB (278321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f873bbf7f705ed6d30295cdc42ae04010f2a5f0dfe91acde3bf6fe05adfcca1`  
		Last Modified: Thu, 30 May 2024 20:11:21 GMT  
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
$ docker pull caddy@sha256:ca03efc1964e5a73d468e9543c9333e83b1d1c0a6077535c3bee9c732bbc407a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77926532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c94ee31a8787237f2a3fe0960078a830918ff0e25b743630569c2f95a3fb3ca`
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
	-	`sha256:61014b2ea6ecad7540420fd97ff35c204099831314d8af4b6bcefabfd60768c6`  
		Last Modified: Thu, 30 May 2024 03:50:11 GMT  
		Size: 6.2 MB (6240110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cddf047e6287c6194328f1cf1610743e450a59fffc7cdada00665f3e1a69de`  
		Last Modified: Thu, 30 May 2024 20:12:56 GMT  
		Size: 1.4 MB (1390030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d2892632bead1789583b0e83a9a7b547a7edbbd4cabe2723a57aa3da576895`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c1735d271d08cab1c8e1dfe80f3d307bc4a569503cd3ac559de060137ad1e9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 KB (293516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181edb797ade073642b1fa5a3acd2419f770ddce2b8b6dd0cf38dd37239cafd8`

```dockerfile
```

-	Layers:
	-	`sha256:cf87e4d2788d6a74320378065b9c88194584b780484699e00b81db822aef09a1`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 273.8 KB (273847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde88d90ec100ec769b0531716096a71efafe182ff6ca6e5beafb579172743a`  
		Last Modified: Thu, 30 May 2024 20:12:55 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:ddf41b94ba50096d4c83958a2f93d05e972a29f78e3cdbf5cc7297201d87d403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fe4747836e96d532a84ce7c51866f14573dd2a7184a1c98e09a3ecbb753511`
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
	-	`sha256:7c9b3f8045285256de876fba6310821fabc1409d0182248ac0dcc358b34bf200`  
		Last Modified: Thu, 30 May 2024 01:51:53 GMT  
		Size: 6.2 MB (6179563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dcf8f9ebef9601e1beaad8b4cc3d76b0eb4ff186a55cbca98c315ee818a4df`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fca2fb511f3ca4f6c95cda9f18b178cad865110e6249189b3d42a59533f87a`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1a4cccca18bb45637c2fe9de18eb24b88ef5f1e5bee1f1aa4404906aa207c47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1676179af361cea13064135f85238a0c19b852b0b327478717c9c00c8db37f4`

```dockerfile
```

-	Layers:
	-	`sha256:339a9ba6f90463c144e1ee97eda33e02e6a462b01c2084c0c6c670f9b485074b`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 273.8 KB (273753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90037cfca85f081f1a829fa848b68182197ddc46f70884e3e05924221d35e02d`  
		Last Modified: Thu, 30 May 2024 20:11:23 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:4c00208a7869c08a9cb6ef821d15eafeac675e507194f54957fc91cbaf787e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:31ea6cb75b5ad08fb08500916a0a249d3cd3fac67e2062428129f1255fd747a6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d816cca71514d888c55882cedda59c9e63b2873912ab19d832e8f0c192cfa6`
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
# Thu, 30 May 2024 19:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:58:09 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:58:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:58:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 20:00:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 20:00:16 GMT
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
	-	`sha256:0fbedff9109d9c95af2643ac63a5cacb1b2bc7f05ffacb6f738c7bd71a8eccec`  
		Last Modified: Thu, 30 May 2024 20:00:20 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca153f0633c0d2c02ede7da833835063735438dffc496ac2f6e096fd2ffba56`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8add55d5a48aeb589d70b12c70950ab9d36ea1844e46a0c3243431fc5d023`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c23241851e0ece31bec24fbcc64f6a45ad49e757b6d83fd867de1db46ef1750`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1af3c5163dc4db242d8d318f53106e3edab0cbfcdee3719d51d1eb44031b1f`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 2.0 MB (1951704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fab58945a98d4f4ef5a6f69ce2d9c53b14cdfdb6bbf677de534c9df7f2a5d11`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:026063496c4412e2f6ad3d7eff0b72334f52eb6a26a76ad7d55413f1f2215b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:10597519ab8ae6e2997ab33ed37ec084b7fa48197540fd8a5e9d6232e3eeefe7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2212211421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41c8c5c0c49c5e91e4db193bb2ceb6f49da6bb49f53d1f9273feefb5c4c4e8d`
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
# Thu, 30 May 2024 19:55:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:55:15 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:55:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:55:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 19:56:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 19:56:09 GMT
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
	-	`sha256:781a5790a63eb24d3d7b709f3885381842614c685aacc0e9f064de800ae074a5`  
		Last Modified: Thu, 30 May 2024 19:56:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adfb41eec4d294c5d5a6989921400c3ce8eac86190ca0e2729a220714fed0b7`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f50fb992e0f2417cc3d5dbd89e9bae09e2871bfb3da8442273c4393ccfeaea`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fe5c664cb62db2aa80c45ca5f51cc3c7a49fd4db915c14c9d3f3697b6e6a8`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dd35d7efa642909c8543d67ac3db36e703c2e00eba4cb7eb057a17a7c65632`  
		Last Modified: Thu, 30 May 2024 19:56:13 GMT  
		Size: 2.0 MB (1977015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcfc24e4cea1030166263d016513ca0181219e291b60093398c292a71217196`  
		Last Modified: Thu, 30 May 2024 19:56:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:7414db60780a20966cd9621d1dcffcdcef060607ff32ddbfde2a3737405846c4
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
$ docker pull caddy@sha256:21b4e37fefdfbc0b38227b3b6fcb805cfeab34715f39d218e4786cdf1a40c55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4829de267201b0e17026cc10e9f5c6aaf0cb9ecf4c47af6cca07c724e01ecef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65acfd58ee0383df10e747701a535d8eb3dac0dd8ad8947a9489b09700ad9d34`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 357.4 KB (357362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e249d258482cb8cd5b424e1644ad35cca37f57a78ae82f68da40abb4058219`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad68dac2ba05429229b54df92b7d1c8ecf608e981628a2ccd42f75bc9e35585`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 14.6 MB (14639266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:0488da5140275dd85cabcbc6b4bd17ff4bc2a6b00173e98925c9559401389b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fbf645e9ac813c3bebf57f4eb989db435692e28e27b909e33a2ab0fb485a34`

```dockerfile
```

-	Layers:
	-	`sha256:399151dcea96073c9d5de979846a5a1b681fc579ac0be2d6b8f46a712067ad74`  
		Last Modified: Thu, 30 May 2024 19:53:29 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ac1b53e222fa9515008993e54b82ed153489351621785b922ad6c38b02e16b`  
		Last Modified: Thu, 30 May 2024 19:53:28 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:27cb90616a8c910028f265c9a35e37b0a53ec818bcf78dca8935cb78685966f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51165ded103a1f093954ce84fe7980b1e20850c4c3565fcaf815aed24b4aa55c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5ade106a2b14c91e811b5be595c661aca72225039cc90670aeb4e92acc8fb`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 357.7 KB (357706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1311d826171a92f66f193a8b4b680699154cc050cf64890527f23bce7e030465`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5914ee1e526c5be906731c807280905bb260186dfcc9ded13553155ef1d07f`  
		Last Modified: Thu, 30 May 2024 19:57:55 GMT  
		Size: 13.8 MB (13763012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:175d31b3aaf4bc9dc28938abb562c3639d2055acaaaa3b8b9a39ba9fbc3c31a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d117aac14a02f2556053c54ab993841ba82072e99f3ac61b5b263bcf783489e3`

```dockerfile
```

-	Layers:
	-	`sha256:b0bfc7c1bc28a001a221f1019947525245d903ddd68cdb36cecdebaf8be32643`  
		Last Modified: Thu, 30 May 2024 19:57:54 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8bb480061ddd6a6c02b0133c5961abc6436f59ddd73c75040346b05d836fc8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17192991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8909144dcba13d585205edef980f7651a16da9574485be2862dec9ddacbc26c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5084781186f063a0bb6c3944407d818125eff602e2318b2b477ab01942afd5ef`  
		Last Modified: Thu, 30 May 2024 04:24:05 GMT  
		Size: 354.1 KB (354057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18302bdcf86d42d09129aeacce97eb83894389c4281eb661bb74d24898b3954d`  
		Last Modified: Thu, 30 May 2024 04:24:04 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4ba1984187ea68f8b4e33c5da9fd0cd0b837eb49cceaf672bc040a8a9b5b2`  
		Last Modified: Thu, 30 May 2024 20:10:44 GMT  
		Size: 13.7 MB (13737415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:f3e04cfab426b603f0d3f9b04f93e53e5e96a896700417a416fc37f1ee8b9e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f470fb5d78b3b8b2143c88cf1d1cb11e6a759e7dd600d33067744eb3969d7064`

```dockerfile
```

-	Layers:
	-	`sha256:f90edc2b668319b5941bbfe7959e6d360942247c4efee398915d63f654d5a3c7`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
		Size: 263.9 KB (263883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70d2cebd4de6bf0de572d0e63bacef20ac991ca8f27f020a435f0a261fe1d6c`  
		Last Modified: Thu, 30 May 2024 20:10:43 GMT  
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
$ docker pull caddy@sha256:c324482f435aa50ae30f531d417545d7cc5586d76847279cba2077ea33e735a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17241541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0655e1dc6ab3c3e5f2b29fe680646c4dbd6a51427f027e8131c98c462244aa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ad67972e40ad224d572ec1975dcf39e560dcbe6b551c3ba4f39919a337f3b`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 370.4 KB (370393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa024c4e0f280d11973c0eda3b12f09a76e0381d137bc1b3f32a5aec6b814c79`  
		Last Modified: Thu, 30 May 2024 03:49:17 GMT  
		Size: 7.4 KB (7447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b777476a3ae956d01f8bd0551800403bdb2da307a3fd8920e2e479f14378d7d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 13.3 MB (13293823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:9e12f88ecde4df21cdd45a0ffb3cdf4fd8bbfb9a96063d66950f31a36c43ad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca7c5ceea57fcbe9468b1e28d188e8c92d894fe93efad5a85c8b9218fa8bbd7`

```dockerfile
```

-	Layers:
	-	`sha256:57c8adf6ec56a24a31792e239bf6547209e7c64f44343f4c7086558bd2ab4f4a`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 261.9 KB (261919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816f1138bf9ebcc1df2835942273446b6aedfefd4561b7fa37c561975d172b4d`  
		Last Modified: Thu, 30 May 2024 20:11:05 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:9e74b95e547eb1588c353d45473bb032367622a294199a26e72f8b352d023713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86dfcd59aa0a6fd0d01bfd9a897f6975a68f6680daf026ecc2ec85b35e29304`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4edb0370be647e880768619b7ae4376984b945fb921a0a2c9abeb7f4c3ec6`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 364.9 KB (364873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7debc9132561db2de4da993fd2232d0be7f688f799445fa78f9af3656ba8c4`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240f4b8c6e2d5ad7a70cc783c821c10a0a0ecb4279a36796296b53241fc0105f`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 14.2 MB (14154632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:aa3915fa8f7c9eaa46531086b6bf775173944010b62e751853379935819e2273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915a3930126fcee6c8cb4e8dcd4de24dcd0583072e33f2deaf7229e5385856f`

```dockerfile
```

-	Layers:
	-	`sha256:f4fce58be66b513afeb7b2fb194ae632e3c8457df54b0f13f72d1fbe09a43bf1`  
		Last Modified: Thu, 30 May 2024 20:10:42 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01188c3d77dabde06f83507c443768248401b1b69ef1d5c709e82a4691cc4f9`  
		Last Modified: Thu, 30 May 2024 20:10:41 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:968fc01b86c3c4fd80a64a2e2bdbad91006c31b5dea58261ba4c678ee97341a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:d48df926bf363a40ecdc79c34c0a1fd25177d1ad25f3588dcc722924acd201a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
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
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7a8c826b69b921eba34d21e8f1432aa2173c0ef6595ac138f64856a830ee1204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:8a859e5b235e64538fa481dfb9bed042aa4775426494d913536d7a417dc36863
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128658583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d212ddc0b7d46916ade47bdfdc02a354cfd896230f4871965d8f54acdaf535d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:08 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:22 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:28 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:29 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:54:34 GMT
RUN caddy version
# Thu, 30 May 2024 19:54:35 GMT
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
	-	`sha256:bd28d89657c62bc0a9414370e4d20949cf6d90a3754cc9cc83bbd947d68385d8`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dffce42b3a93c6dcb89c8119b8de9d2cc7e8e0e8317feaf7cd9196443e84d`  
		Last Modified: Thu, 30 May 2024 19:54:46 GMT  
		Size: 359.9 KB (359860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5699211ec97142ff5ee8b36eecba7d7b8b8a48b752b256c9bb79be28454478`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e326c3d4cca13916661f8d251ca1ba355ef43aac90cb123a1aae87dd3ff886`  
		Last Modified: Thu, 30 May 2024 19:54:48 GMT  
		Size: 15.3 MB (15255909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14adcda1fdb75ee4a38fda124f290dbde1dc66826431129731382871525f05fe`  
		Last Modified: Thu, 30 May 2024 19:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525aef206a761d1b5995be7beb217aa838ec7d1e05805608f1e3c88ea496b624`  
		Last Modified: Thu, 30 May 2024 19:54:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83f0cb1b15632d5728a0fc228889c8328a889816e9e5893bfbfda486e423a`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a35dc8c6b268cac88bea9d7cdbb7a01fe744813bed2b0cd707533e7b8e46fd`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6545c772b737a8fed2a69db09c17cad0a7e111fb1b5b25fc2d25dc67ab06e89`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e122125faf27258b9637497e55eba99d5953cbb2e5d37e885da446b8a6d2db`  
		Last Modified: Thu, 30 May 2024 19:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5a85d9349913ad621ac0e58b44c8cfaf909e69519c9db45b0bddeeb899281`  
		Last Modified: Thu, 30 May 2024 19:54:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7935d97cc7a666b6ed78c3464de92792ef20694f77ea5eb43c223af434255`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32befc8e35ad3e7d8a49b3ec8496d8135ba9a673c3395cac25733bee2cf60`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee7d7f23b87127d7a565da580d9427ec3e8ad2e0f5557fde35d249ee4dba46`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fac278d2e30b07f351c267ed6c470101ead2945b6da2001291809755adcdc9b`  
		Last Modified: Thu, 30 May 2024 19:54:41 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4f0c9b0a843a5437c6c2c859685879c5cc515ccfd0cad0a64fdf09219d4bb`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96febe2e0b0fcb00860b3c6071b9a974a4e5decffc5f7e3ccae60b70b6474cc3`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe0cecb35714e1d0bd2ba02f4fd4464ede77a9b14a65b57d6e38279b7217a9`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bcc027ca9fc0ea5d69d71480a08928c9279dcb826dc4d50d8d65605f8f6ede`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 349.5 KB (349497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c987e28c39468930d912b006e33d2a7b3b4d5e1c421f748f3907ecd0391489`  
		Last Modified: Thu, 30 May 2024 19:54:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
