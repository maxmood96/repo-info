## `caddy:alpine`

```console
$ docker pull caddy@sha256:0712e33e0e136f06cb6e47a450dfbd96851f29f3c0af4d67ff70ef088af66006
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
$ docker pull caddy@sha256:bdcc44c8c00d3bb286f0043a4e561ce5c4580cdca4d75e67345f5f7e806e4215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17227099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f4130dbbbf3f0b5415eb82116ca8655605e2cd03f35efaf50678dca6022a8a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
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
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11319ed716749f79cf6a7d8ebb201b03933fb92fa17cab752a87c7fe5e4f3ad7`  
		Last Modified: Thu, 09 Jan 2025 09:57:54 GMT  
		Size: 359.6 KB (359591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c476b59a20a26714482050a2668825280292325695abae05e0ce883363c1931`  
		Last Modified: Thu, 09 Jan 2025 09:57:53 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c0a0285d5654119b4a53b2b45ca4d2d835a3db69970f5bbce2e5dbe5142f9`  
		Last Modified: Thu, 09 Jan 2025 09:57:54 GMT  
		Size: 13.5 MB (13488507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b59c39e4f027cad72915547945bbe62b161eadf3744007251676995f1cc18e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a631fef393b15e195cbb4f326f76316858e8a5ef03c749d8e936e13ccf454330`

```dockerfile
```

-	Layers:
	-	`sha256:8b87f9e244ce27e3fb5867276a809071f53e188a0311bec0a767ade00b5fdee7`  
		Last Modified: Thu, 09 Jan 2025 09:57:53 GMT  
		Size: 18.2 KB (18173 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:dc6fa86716fc6d585db9e0e81fd22989dbd1f85c972e95d6e2444d6891f33116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16917548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2ae1247c99c1b6e15eb8d99588475e0aa0941438f1528b99daa248dfb9ea7c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
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
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107bdf6ce028a76617f1d865cd4cbd786dc2c23ff12c85eabb3bf568ce14d871`  
		Last Modified: Thu, 09 Jan 2025 11:25:15 GMT  
		Size: 356.0 KB (355975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945f48b7a0830e680752926a4fc8d15fb1e8f301a5c20f05b23b5c22a43282e`  
		Last Modified: Thu, 09 Jan 2025 11:25:15 GMT  
		Size: 7.5 KB (7499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1901a7959dffc44338025ff7d2d340f86eb493708842d1a3f6e79caeb3ccdc95`  
		Last Modified: Thu, 09 Jan 2025 11:25:17 GMT  
		Size: 13.5 MB (13458528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9c51e0fc0be697f4a9375e9b7f427b905ad6b6f70188129a7adfbabdb2a20454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 KB (299653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e18342cc2feb20a7b1215537b1a087dc980012c4f8e71dc694951c4e32d09d`

```dockerfile
```

-	Layers:
	-	`sha256:d1d7ffb88e227fc24f6f7d88cc2dcf3768aa1acb1178edca44b656ab1a0b62f2`  
		Last Modified: Thu, 09 Jan 2025 11:25:15 GMT  
		Size: 281.3 KB (281263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d411f0a77aaecd8b2e82ec4d6de1c2316cd92e9fc44ad0373d854d12570cc7`  
		Last Modified: Thu, 09 Jan 2025 11:25:15 GMT  
		Size: 18.4 KB (18390 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:81bde3e1c55e4a0ffaa2f78ef9898ca6e5dcf2b143318ef7f1c5929e8f64e243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17771016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36ab5fd4591551a0fc4d4b997f5760427d4ad959603aba636c49bf8333b5b52`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358b972603cdd603797faa822b772e499332c981a41956d0a1a08802b64b0545`  
		Last Modified: Thu, 09 Jan 2025 08:06:30 GMT  
		Size: 370.9 KB (370921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0904b3217a12a43b4a5d324f258e81582c57df371cb672388377c8b357bef39`  
		Last Modified: Thu, 09 Jan 2025 08:06:30 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28621d44e4b151f361d9eece4c467aff27990519eb77f84513abccdfc01a5bc`  
		Last Modified: Thu, 09 Jan 2025 08:06:30 GMT  
		Size: 13.3 MB (13301798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1ed7ca14502561c438576f6960be0c2351ac03dbb5fb4e8252dba05c8e5cb515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 KB (299738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e493cbe533368f0bfd3d33827398ec4a382d93a815df820420874b333678b1`

```dockerfile
```

-	Layers:
	-	`sha256:a12b67a5524696586ed6886c5dae67e68332bf1a1e500cf230b3baeeec2a415e`  
		Last Modified: Thu, 09 Jan 2025 08:06:30 GMT  
		Size: 281.3 KB (281299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e6c350c712562c3e3aa825daf46d52eedb597b17027856e9a7bab23554d409`  
		Last Modified: Thu, 09 Jan 2025 08:06:30 GMT  
		Size: 18.4 KB (18439 bytes)  
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
$ docker pull caddy@sha256:43c0d8234c895b0c928724630c0506fb519b6dee4894654a4073ca64166f2116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c19225d55f90062ed06dc4e89d435e2a032c7f790ed94622cc504d199dce20a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
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
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133f978d27748ff20909b453bad67ffe6ce2e2db1b364c8236b3866de721c206`  
		Last Modified: Thu, 09 Jan 2025 08:56:33 GMT  
		Size: 366.7 KB (366655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4171661e0459bf431866f66f0a2d5238d4776d3c4fbdd048458b2a8633b7133f`  
		Last Modified: Thu, 09 Jan 2025 08:56:33 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1edc16925e9eea65170007c811539a898c763de36ea998a1f28a70a877b0fd8`  
		Last Modified: Thu, 09 Jan 2025 08:56:33 GMT  
		Size: 13.9 MB (13904055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:be35a07d81ce031fa6897d10685b2599628246a204b1c3aaf24bcdf48c046485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 KB (297499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d33a47991af7cc0e92f4d2f8bce9b34364af046c23f2682df5511670bdba05`

```dockerfile
```

-	Layers:
	-	`sha256:684669fce8e461a4ac64980d4292f747273b98a49eb69d9863f7cdae69010d24`  
		Last Modified: Thu, 09 Jan 2025 08:56:33 GMT  
		Size: 279.2 KB (279244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d42ec76f5b2e45bfbeb2f21d0310b0b6b31fe4747f29e2aa3370b4d18a60b15`  
		Last Modified: Thu, 09 Jan 2025 08:56:33 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
