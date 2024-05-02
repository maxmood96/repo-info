## `caddy:alpine`

```console
$ docker pull caddy@sha256:2e1d4592f1718bb47645da5a83a846fe19094f18e6c921fdf56d174f05c63213
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
$ docker pull caddy@sha256:7b51768d110708c44179dc299884e9ee73d243a37abccce2dc796abc36371a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18476986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e21ce508b7f91169630895a0fe9a9f58288e5eb6e899c3462f168229c84193`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88463a31d6d2c104349aaaaae3b5a60c2a63ba0ac2712ba190211e9cd15d4cc`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 360.6 KB (360570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de93e10dd6701c976a78596c69babad750fc3957060c758b8859daab7fd2dd27`  
		Last Modified: Thu, 02 May 2024 00:51:57 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ae96b49a2d955ff25ddc1858d84596c16d525d531d2342bd372945ccf5e410`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 14.7 MB (14706390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:666c65a5f3beaff567eaca64d4f307c64b81695485a64ad5d33ac192c1b299e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfba4fe57beaf0920d15623535056bcc81e42e1ac5eacec9827a7932a15bc94b`

```dockerfile
```

-	Layers:
	-	`sha256:0f942a2c6c2e9440173dadc3211a6cecf73e846edcdcb423bffad328d9c8727e`  
		Last Modified: Thu, 02 May 2024 00:51:58 GMT  
		Size: 268.9 KB (268899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f88d335506cc1ae671b94135d1dff65cbb966f39e5145fe171d82377ea601c1`  
		Last Modified: Thu, 02 May 2024 00:51:57 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a37e44b94565539d082d85ceab947792effbecc9d7db223ea6abca196ee05a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17432782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b5570c733ff428231e40e91550787c9f5ddc4bb728f09cb7effb937964fa7d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
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
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320944b9d89ce73b5dbd09f5e7a6041004d85f4bef04eb1417a27e8a24f13f5b`  
		Last Modified: Wed, 01 May 2024 21:56:04 GMT  
		Size: 357.3 KB (357340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe068432b49975aecbf4e69d7736019056ee4d62a52931a724ff06f70e86c25`  
		Last Modified: Thu, 02 May 2024 00:56:31 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb925eb8f3d094c61b238fe90aca158009b859c95c7e87ff0cad1f810e65aa9`  
		Last Modified: Thu, 02 May 2024 00:56:32 GMT  
		Size: 13.9 MB (13920901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:29db70769c20c963daa30568350c31fc72970c036d8e8a0d7a7a8a47d275300e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58dc3b1df0157f859652c398af09ae3a777bb2fb92015e0f62436f9e993a7e54`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb7c30b377cc96f8036dbe70e0f8d249776fdbc6cac9bf32c4ba0e42eaa843`  
		Last Modified: Thu, 02 May 2024 00:56:31 GMT  
		Size: 17.4 KB (17443 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v7

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

### `caddy:alpine` - unknown; unknown

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

### `caddy:alpine` - linux; arm64 variant v8

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

### `caddy:alpine` - unknown; unknown

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

### `caddy:alpine` - linux; ppc64le

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

### `caddy:alpine` - unknown; unknown

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

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:faab60dc3a1acc475e2d0f12c86d9f31290b49896611d5cd61feb631ea7b0b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17828011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6446726caf9ff49671c1b47b04ff608cc10c783fd3dbf2a2d79d816140cb2ea`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
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
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7649425a6a944a0c8c4f452b8bc1e2874e0e99c7e097d2aec191fb8ac784fd6d`  
		Last Modified: Wed, 01 May 2024 22:05:37 GMT  
		Size: 364.7 KB (364696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df358d50a949fe6c09ee403e747cafa7b4bcdac928dbb75cee120ea25330f4`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc640f077739a0d0aa11a1722064f9f3d5dfc31ffc720787fe16c78e49d827`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 14.2 MB (14238300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a941d2a34e67bad02c9ee6d9cb55c09fccf5ae73670d0c5cf653ba2457ae8cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 KB (284475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76679ae3672baef460ec34615d3960669d3d95e73990aeddf0e2d5bd8573af8`

```dockerfile
```

-	Layers:
	-	`sha256:144c0dfb68c151b0a1b0c92da22a910fb7b8e8cc63389ab9b7e180d746bbf9c2`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 266.9 KB (266941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958b331e0cf47b7621d5c63aafb1753bf1abd52d632a23dd19e986657b53c310`  
		Last Modified: Thu, 02 May 2024 02:27:01 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json
