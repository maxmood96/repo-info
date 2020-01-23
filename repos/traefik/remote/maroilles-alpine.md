## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:5c83e759dd0242f06079871204c4a70c0a38e9cb926374a7589608376430f8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:f9f7bc3071415790c015ad52995e2997d9d1cfd5cffdde58cb403e15d71fbe4e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27028274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439e73a064c8f244ce1fe21cb3abcc9b314309275e3b26fd6ac0276946f669c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:31:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:31:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:31:02 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:31:02 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:31:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198d6da64444dd0f60f3c566038d6c9157c290fb6152ec296204e862073f365f`  
		Last Modified: Tue, 10 Dec 2019 22:32:13 GMT  
		Size: 23.5 MB (23546279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd7a10facf04db24667668cb9792494b0e49f33e439cccf618f435ef237bfa3`  
		Last Modified: Tue, 10 Dec 2019 22:32:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:59849962d6b994b67dc7fbc511912c5a1b87944e9b1fda436acb6502c53506a8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25301946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5307869ccfa13af9d37cbe35f32b4bfa91f47eb7cb00bad6cfdfbac45293e452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:39 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:42 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:43 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d03b0a042ba73cfa9ff088a916bb4dd22cec09c6862278e94c8f4445863f12`  
		Last Modified: Thu, 23 Jan 2020 20:54:01 GMT  
		Size: 22.0 MB (22032328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c7026f34a4d522e997bb9203822966f0365b1d11745be187098906406a66e3`  
		Last Modified: Thu, 23 Jan 2020 20:53:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:69880c97f253a7dab9e3fb1e477bc209a297ceb369f259841a14ec194ac5fbe3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25175702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630da378646ff9d16799a8f19fc83d02d28fe478003b44b8f37a8b0a4b715079`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:39:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:39:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:39:27 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:39:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:39:28 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:39:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ad2d17ee7cb6da8499ef5415cad503d05873da472bcfc6d2ac07e9bdbad2c`  
		Last Modified: Tue, 10 Dec 2019 22:40:19 GMT  
		Size: 21.8 MB (21759668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ac7ce9940a937d298cf00954af64fd399df1a840cad75914caeb0b5cf224`  
		Last Modified: Tue, 10 Dec 2019 22:40:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
