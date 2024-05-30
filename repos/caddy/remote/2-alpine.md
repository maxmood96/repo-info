## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:7750cb6f08350f2c39207ea87232f7b278f586410232e912542f1d128995636c
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

### `caddy:2-alpine` - unknown; unknown

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

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:690174bca4a22f78fd061b913fb9af04c35053cf591739e4274f1e5758136779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17493419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a1618df6b54bfa5f963ddc58cc727860e3264267ceba5a03a89dd90f4a5cd6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6242b091285cd3a94637051278e15e4e5fac103eba7cc862f4c049dbd89e5d8`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 357.7 KB (357710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8165fbffda6934ae4fa48e7fb8912c4a52fffdf33dddb24e1fa2823af18b77`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b840d124a7e1135a2bccb8f1921209ee443c13f74e6b5270dbf3d9b5905d87`  
		Last Modified: Thu, 30 May 2024 00:33:31 GMT  
		Size: 13.8 MB (13763171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:18ca096172a9af5d32f39e949ca51c2f3a04b0c3fdd3d3c19c61dc3edacddf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db94e6c76f858c4cb979b37ea5de4a12782484dd46cfca89e9dd213837ad5b74`

```dockerfile
```

-	Layers:
	-	`sha256:a26aa7bb711b04c54e7691a704b1edf426a27937b3bda1721d70aaeddb786cc5`  
		Last Modified: Thu, 30 May 2024 00:33:30 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:3d1e889eda417007d88637f9adca7509e5bb547492e555d4a758ce2df850a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17156262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3523597ee5af2fd110570a00e504f5e22dd8704d65c7c8778bc0c9ef96ae269`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b527911aa0f8852117f57452d522fb961c184d105b0818cb4a87109b08272643`  
		Last Modified: Wed, 01 May 2024 22:05:53 GMT  
		Size: 353.7 KB (353705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ab12f0e1a27e1224e11b4fc25b25dc760337a04bb0883175300b1a8842aff2`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fa49870fc1f8bcbe7983ca022544c47da797299179b3287255e96b1254a28d`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 13.9 MB (13893683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1f74bd28526188e78a3ee7ac25ba3de34683b3251d1e0b495cc33270910d6d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060e4e44fb56999c235e64a72bcb39cc3db4a016d5e7307bb82c1a31106afb75`

```dockerfile
```

-	Layers:
	-	`sha256:eeda73bc8fa144234fa52e9915e531709e0b3d01b8aa6ed8dabfbeaa03d8ec52`  
		Last Modified: Thu, 02 May 2024 01:08:18 GMT  
		Size: 269.0 KB (268967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039dd7674e2f60b9d2f360db16a7759fb38a2b8153fda85eff01c915c1da050e`  
		Last Modified: Thu, 02 May 2024 01:08:17 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:578dcc962eb6776e3e6ed964d11a13d40983f294e590f0040fc9febce144fa3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17278610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220a025aa536c6d9e845318ec54c7969a55f365311b36886f0eed8b3a218012`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f50788699932589070b139144f3b1440a2948fa84be4ca81ecdc1d1a54e4e69`  
		Last Modified: Wed, 01 May 2024 22:12:04 GMT  
		Size: 368.8 KB (368765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b07f03c61a8e689485aedd78191737c91a5f2f23e95122ca9de2af436c14c`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef67f47d4ab395e9c3fa86967774f6a1f31b10e560ad19c1a48b64db88bb6ee0`  
		Last Modified: Thu, 02 May 2024 04:53:38 GMT  
		Size: 13.6 MB (13569000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:38001a08c78526af0f51525a1f82a25923b94559287782c232932bff2c9a6682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b174326e15ad188a5fc078e50318dbccac12850ef07b98ac27e0ccdf2b05e9`

```dockerfile
```

-	Layers:
	-	`sha256:93cfedcf72234e144ba3ae74894f78ff082dc5b8330cbd00229c9377c80c9d93`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 268.9 KB (268918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a58d69a87e8d3b310715fe89231c5f8d7a4d5d6ee5add7d9a97ea9273937afa`  
		Last Modified: Thu, 02 May 2024 04:53:37 GMT  
		Size: 17.6 KB (17552 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:2c0050449fe45c8df3fa0b90fa1621dd8fb2de864d8154aa379c73b71d1ee769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17060083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913f3ac3d369a2d5a24e332dec6da8cbca6f9d6c570768127927ee62e7aa7770`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 01 May 2024 14:17:43 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 May 2024 14:17:43 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 14:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[443/udp:{}]
# Wed, 01 May 2024 14:17:43 GMT
EXPOSE map[2019/tcp:{}]
# Wed, 01 May 2024 14:17:43 GMT
WORKDIR /srv
# Wed, 01 May 2024 14:17:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0550c488b324bf74512534b8af77dc0690e94dd12f1286c76669cb03c733692`  
		Last Modified: Wed, 01 May 2024 22:06:02 GMT  
		Size: 370.3 KB (370278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f53ff24ab7a11bdbef2dbc4774bd8c9241c60f282247607ac7401ec586a681`  
		Last Modified: Thu, 02 May 2024 01:07:51 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30849c5c1ec8a58215a8ad6e5f79db3be0b1d9c9f843dcd81c42748732a39917`  
		Last Modified: Thu, 02 May 2024 01:07:52 GMT  
		Size: 13.3 MB (13333836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:09f14bafcec41acaf23fa3fbfcb3542d754279ff9bcd6994883dd551a91d9118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 KB (284603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e3abe481d46e34ec2db9e2960600548a2a65472765919c636e793baecc365e`

```dockerfile
```

-	Layers:
	-	`sha256:d8a5956a258ed188944c638c13de5928c93ec3795de1dbc3881214c0ddb98063`  
		Last Modified: Thu, 02 May 2024 01:07:52 GMT  
		Size: 267.0 KB (267003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24c13f8f699644b031a10dbed52d9ed326c7dde29529b70a82bb603d2677989`  
		Last Modified: Thu, 02 May 2024 01:07:51 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:a901a1a96c982a13a5b375f9854ac2881ada2dad6e0b51a280e4e0409b3be7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17987293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaa0aacb2cad6d7dedd2ae0e0a01b4240ab829d2054697264b7f35a3c8c727`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
	-	`sha256:80dffc4dc5008bcfd45facfcd56c34ac3e08dcd41d6dcf4dbf7b1304998e48f7`  
		Last Modified: Thu, 30 May 2024 01:51:03 GMT  
		Size: 14.2 MB (14154597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f8f994f364719dfc87e3eec9d3d9370870f7dd53fc55a85894cd74b295a064e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 KB (279390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279088462e9f352f79f89f32ee4c95eb980369084a4efdd389b4d8de75cdaba`

```dockerfile
```

-	Layers:
	-	`sha256:ad7f9ab13108a2a745e3bc6420a3bc827b9c09669eede8eaabf3013581262027`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 261.9 KB (261857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79640b0ba457ce4da05d0515c66bb0761b3ba7246808b89cff28c88c7d94f23`  
		Last Modified: Thu, 30 May 2024 01:51:02 GMT  
		Size: 17.5 KB (17533 bytes)  
		MIME: application/vnd.in-toto+json
