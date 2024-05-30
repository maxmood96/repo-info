## `caddy:alpine`

```console
$ docker pull caddy@sha256:45dd173e0e60e86065ca2f157b32c3375399d2e41daa0c51444f8a2c013de6a9
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
$ docker pull caddy@sha256:f6bdaeaa2da17edf5a8c33cd6f3cde4e96b37152c2791d4308c1b6695e2a79f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18626191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2528051e99d3f23b9fddb25e751078881b1a4237ff2e4bdd77c4c503b66563bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb615d7326964b43a9e5dd3dd14734c53a02dc2cef9fa9ffc00314a64e79a3fe`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 357.4 KB (357368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb87b8526d1948b1e9d896525df20cef23bed00873f22a774db258b070e92a`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333cc5c2a4bdfc22594bac44d124a78fd574d27c4da57ec41e156269d656a58`  
		Last Modified: Wed, 29 May 2024 23:01:06 GMT  
		Size: 14.6 MB (14639245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9cdbbc45a19237aea8ac5d7ebb37954541082503b26be511135699351c58b4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574268ca9e9da984347d108b60adfdee7bb5792198f3904485d2570a0d3c5e06`

```dockerfile
```

-	Layers:
	-	`sha256:5a044e0dbe68da74ba6be9d21c1fd4ffcc1d42e0061d9f810df5a7b5bf3804ab`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa7cd9091a42e6e0007de5a9ef9c7b132d08ecd23fcb96aadf925cbef4ccef6`  
		Last Modified: Wed, 29 May 2024 23:01:05 GMT  
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
$ docker pull caddy@sha256:33587c0c74c28133fda233fae25100c1cbd9daa4d91a0613abe792da607a267d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18014817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e753e0e37929b336c8bdb1c1788195b1c4ff73374cc0f601ffcd25badf6805d9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:22:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV CADDY_VERSION=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='90d7f2325f9f6feec22c2c84fb1bdad2e94ae08b227d3c44eaa6b82ce1ff5a31fedc047d95e4a0ec2df4c1cebf3426cf6003c9f1d665ba3e67093bc12b89606a' ;; 		armhf)   binArch='armv6'; checksum='93a0467fe0945dfc12e86a22b161a8d230b9bd728db39293fae32175b438e04726d6a4f8d432b42db4fb48bae10227e0b1a714667f636f669c707e7996671724' ;; 		armv7)   binArch='armv7'; checksum='98a7a06cf1202c6bc484907d255c1afd5302a38a6ed15a0fccebb1be861bceab2f496ffacc796a144e637dbac4f0de4494eb53952e5a8e37532e19aa58c6679a' ;; 		aarch64) binArch='arm64'; checksum='37e6b62ebf76cac029204cd906dba72fd68ed302079dd4828efc2ade7aed746d8fc4aa301ceb8d1fbe277973247df563c8fa51d815c4c2e8f18f88cfefc1c40a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='6156c44046e4e0b892c6ff79af387d86f96c0f1a2306f4496ba2b00f03d195e40f805c8f2c95a4f05293cbf283de23285ed94cea7eaeae1c4f910295a6c78c07' ;; 		s390x)   binArch='s390x'; checksum='e9199812aba23ed037d2d2cc75f01a9a9c583a31bcc2b7ef336b646548e3e460a78a606397ed61c570b8ba5e352bf44affafd3eb9d66656f31d2263ac8275ca1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.0/caddy_2.8.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 29 May 2024 21:22:21 GMT
ENV XDG_DATA_HOME=/data
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.version=v2.8.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 21:22:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[443/udp:{}]
# Wed, 29 May 2024 21:22:21 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 29 May 2024 21:22:21 GMT
WORKDIR /srv
# Wed, 29 May 2024 21:22:21 GMT
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
	-	`sha256:7407665a6cf5b70587119826edf95030e1b1bf3964cdd1b1a9313b5c893e0dc0`  
		Last Modified: Thu, 30 May 2024 14:41:44 GMT  
		Size: 13.6 MB (13551402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:dc92486b9ee4a0071a4a49bbb8d8cb8d91769cc903ea22b31a18b8b41fabb2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 KB (281801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973d279c782195694d3b7b2eda3426355bdcca0e322caea05a4c182f114cce82`

```dockerfile
```

-	Layers:
	-	`sha256:44646b1851f909ae3c78626d5e787b1493c59b402cdd33c2f0b2ed7d04207d70`  
		Last Modified: Thu, 30 May 2024 14:41:43 GMT  
		Size: 263.9 KB (263919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c569ce55b55f3f9f576d9432be5e5a243b727dbdf2b4aa79a73e6611c2b047cd`  
		Last Modified: Thu, 30 May 2024 14:41:42 GMT  
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
