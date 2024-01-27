## `traefik:latest`

```console
$ docker pull traefik@sha256:b131774f4052c4cc35781dc078b44e93706d3ebf7eddafa0b25be6567fcd06c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:a6b19e415e41b0e48b5c81713f3a60693a38f292059bd7347eef78bc9ae8044a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43233245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee69e8120b64a420b5deca1cf46db0e4188ef76c7807a45c0f26d8a5ac2ab2bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:55:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 03:56:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.7/traefik_v2.10.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 03:56:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 03:56:15 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:56:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:56:16 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 03:56:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987f790ee1434532d04fff8e0ff09f57d177ab515cdad8c0c3797d839f186a98`  
		Last Modified: Sat, 27 Jan 2024 03:56:31 GMT  
		Size: 622.8 KB (622798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d80f829c660d4ca9f0cf5c29678d30cbb7922ae43f9b783d15a2fcbce9f786`  
		Last Modified: Sat, 27 Jan 2024 03:57:16 GMT  
		Size: 39.2 MB (39207537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5300d181735bfc4dbb1dcaefae56d132d04c53b7e951c6d23139c55b6ea5cb25`  
		Last Modified: Sat, 27 Jan 2024 03:57:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:82aec7a0d7f4ee2d6fa39b2ec4e729fcd5fc0b7ab55eb987bc79d66fc3abbb05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40817977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7a4e3d57c06a55f5132dcc35840b0705550dbfa3a6ee98e473877671acd539`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 11:16:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 06 Dec 2023 19:49:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.7/traefik_v2.10.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 06 Dec 2023 19:49:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 06 Dec 2023 19:49:34 GMT
EXPOSE 80
# Wed, 06 Dec 2023 19:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Dec 2023 19:49:35 GMT
CMD ["traefik"]
# Wed, 06 Dec 2023 19:49:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cc333e699b1d6d62e16cf9f495bf1e6ecc7fd649ecb87389920df6793f0739`  
		Last Modified: Fri, 01 Dec 2023 11:16:56 GMT  
		Size: 622.7 KB (622708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4204dbb89422185322324d73ad620b6b37e65708e76befdc7c808a3ff33bdacb`  
		Last Modified: Wed, 06 Dec 2023 19:49:55 GMT  
		Size: 37.0 MB (37048032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1678da4540f9fd5354abf93fec0542e3639d54e99b21750e82108004a134094a`  
		Last Modified: Wed, 06 Dec 2023 19:49:49 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1f03597e0370e10e95c948a490af4ab182e9185068e212ba6e621d43f7f73ca7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40214807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72c2dc074ab16d1bd1a1a657d7c8baeb8265740f81fcbab3a1a0559255e922`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 06 Dec 2023 19:54:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.7/traefik_v2.10.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 06 Dec 2023 19:54:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 06 Dec 2023 19:54:44 GMT
EXPOSE 80
# Wed, 06 Dec 2023 19:54:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Dec 2023 19:54:44 GMT
CMD ["traefik"]
# Wed, 06 Dec 2023 19:54:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024ea96dbe9d8eecf209e531af8ecb6502f18063303473b3d8335b373efb8a00`  
		Last Modified: Fri, 01 Dec 2023 09:31:22 GMT  
		Size: 624.5 KB (624520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ca6f355517b7c96d4dc25ab437ed008b0a935537be122866a708c2805d696d`  
		Last Modified: Wed, 06 Dec 2023 19:55:02 GMT  
		Size: 36.3 MB (36256886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c0b2a752e75ae8c19870e602af930cfc9fae869f307d23ca5d36eb2528247a`  
		Last Modified: Wed, 06 Dec 2023 19:54:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:25c3f790c8f196a595eb4d28cd1c7cda5884e6cbf750064b1f7c694ce60594a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42075226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a489eb79d81b420f7860ed3ee4921aeea0c036afadcfffc3f3d2db68bafa547`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:19:00 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 27 Jan 2024 04:21:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.7/traefik_v2.10.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 27 Jan 2024 04:21:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 27 Jan 2024 04:21:53 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:21:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:21:53 GMT
CMD ["traefik"]
# Sat, 27 Jan 2024 04:21:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8e27c29b7fbf4c31ac7c82b3365eca2436fa8dafa39d1b1e168d59122e8fb`  
		Last Modified: Sat, 27 Jan 2024 04:23:16 GMT  
		Size: 623.3 KB (623315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98a7c6ddf066bafcb3b1737d91ae72f4364a8635af2ec74297c29d7e70dc0b6`  
		Last Modified: Sat, 27 Jan 2024 04:23:54 GMT  
		Size: 38.2 MB (38234013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6bc624331de066b251130dd05437f611cd7065ac98474a52399e353c4dab30`  
		Last Modified: Sat, 27 Jan 2024 04:23:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
