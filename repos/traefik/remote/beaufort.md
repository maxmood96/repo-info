## `traefik:beaufort`

```console
$ docker pull traefik@sha256:ce3ae40b05fd3407b6fe1713e24916a04e81489cf37b9ebb22b7ae98b12064a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:3212a585ed12db136baaa944f1c2adca228f4722afaac8daed984fda07487b65
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47439745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccea929840f139e13932402d2daa825177ec67872498abac4bd9b8a5634fc07d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:35:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 21 Jun 2024 02:35:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.3/traefik_v3.0.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 21 Jun 2024 02:35:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 21 Jun 2024 02:35:19 GMT
EXPOSE 80
# Fri, 21 Jun 2024 02:35:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Jun 2024 02:35:19 GMT
CMD ["traefik"]
# Fri, 21 Jun 2024 02:35:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8168e2be9d205d7f8b76990ad5a6d495782753c0a87dd78d23354d85a5429be1`  
		Last Modified: Fri, 21 Jun 2024 02:35:40 GMT  
		Size: 463.1 KB (463144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0aaa05be18c1fc350f19b625c1d50f41ca17f8ec2e5da461731b371fdbe3a03`  
		Last Modified: Fri, 21 Jun 2024 02:35:46 GMT  
		Size: 43.4 MB (43352388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eee330854e11ef2f0bf9764e0080f43ec638620b3dd5de013124a124269516`  
		Last Modified: Fri, 21 Jun 2024 02:35:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:158c0c11dc6ccc852912e6257f651dd99bd725542fc3ce53d2d842ad8f780f7c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44511368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddaa38d872cdafe8dea6c990268a63c6149f48bc34810668e143ca96a9ec759`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:59:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 21 Jun 2024 01:59:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.3/traefik_v3.0.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 21 Jun 2024 01:59:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 21 Jun 2024 01:59:53 GMT
EXPOSE 80
# Fri, 21 Jun 2024 01:59:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Jun 2024 01:59:53 GMT
CMD ["traefik"]
# Fri, 21 Jun 2024 01:59:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7337ede81ecb77d813170ec03ead72fa35339996186fe1b56b262ea09626d7e`  
		Last Modified: Fri, 21 Jun 2024 02:00:14 GMT  
		Size: 463.8 KB (463814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310643b7b1181a90ac319402711920a165863b774c95daa78b851231fbd1798a`  
		Last Modified: Fri, 21 Jun 2024 02:00:21 GMT  
		Size: 40.7 MB (40680031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db2efbe36a3b84b87017d82e7cc142ad28835479e9c0598765aa36350a3d36b`  
		Last Modified: Fri, 21 Jun 2024 02:00:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5a7c92575fb90544e7e3be9a4bd7768e15b8a047aaff54566dc1f588bc9a62bb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44738340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b686b657cb9ee2f21e475b202fd667faee76052a0380add3f30f01eae32468`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:25:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 21 Jun 2024 00:25:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.3/traefik_v3.0.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 21 Jun 2024 00:25:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 21 Jun 2024 00:25:07 GMT
EXPOSE 80
# Fri, 21 Jun 2024 00:25:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Jun 2024 00:25:08 GMT
CMD ["traefik"]
# Fri, 21 Jun 2024 00:25:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d410afbd1686b6d27360ccf8005cca1dbc8f1997cc7afb3b70cb39f98673c893`  
		Last Modified: Fri, 21 Jun 2024 00:29:33 GMT  
		Size: 465.5 KB (465483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4a79e389378f4398ac7aa70674dab1162133ec070c73aa2f8cb6507ff42b9d`  
		Last Modified: Fri, 21 Jun 2024 00:29:38 GMT  
		Size: 40.2 MB (40183689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3298374848a97d88ed6229b3cca07f092163e370cf62e66ad08eab7d3b067ecb`  
		Last Modified: Fri, 21 Jun 2024 00:29:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; ppc64le

```console
$ docker pull traefik@sha256:43a10374fbf0dbff1758213cada3bc883e7b7679f9bd00806b4c0a78ff206493
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42993620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cefb6d6d28ba3f4bb19eabc086500d47cb7081f5357d43c9553dcc53fa73c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 23:22:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jun 2024 23:22:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.3/traefik_v3.0.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jun 2024 23:22:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jun 2024 23:22:10 GMT
EXPOSE 80
# Thu, 20 Jun 2024 23:22:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jun 2024 23:22:11 GMT
CMD ["traefik"]
# Thu, 20 Jun 2024 23:22:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f94ae9cb53cbdf673994943d4cf3d69547cd5a988af9cf0a69be06478449e8c`  
		Last Modified: Thu, 20 Jun 2024 23:22:36 GMT  
		Size: 465.9 KB (465853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e9b0aafda8008edd8cc04a6553515e77fce1683b780a82418d5a7192f00583`  
		Last Modified: Thu, 20 Jun 2024 23:22:42 GMT  
		Size: 39.0 MB (38955699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021f8896539203e83ee5ffe045a9e25527689d3a1e138d5c7118fe1f2f8e63d8`  
		Last Modified: Thu, 20 Jun 2024 23:22:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; riscv64

```console
$ docker pull traefik@sha256:28dd9898ad5564a22826141610d2a6c1c9c0a0d6ca0af7f7c4a01606ee21cd58
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45758056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d9bbc39b1588377cd5ebe78b05545b34f5a6d8b4789f60bd5e8d4831fb73bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:34:03 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jun 2024 18:34:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.3/traefik_v3.0.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jun 2024 18:34:32 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jun 2024 18:34:32 GMT
EXPOSE 80
# Thu, 20 Jun 2024 18:34:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jun 2024 18:34:33 GMT
CMD ["traefik"]
# Thu, 20 Jun 2024 18:34:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62714b493fc18e5f8e744f21b9ad7dbe157ba9436e68493c14acfa61c7ad2ff3`  
		Last Modified: Thu, 20 Jun 2024 18:35:35 GMT  
		Size: 463.8 KB (463837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4b21f43ef090213feab67b5f1fc6fe684ae13e7e03f52c0291e75aa36a843e`  
		Last Modified: Thu, 20 Jun 2024 18:36:12 GMT  
		Size: 41.9 MB (41922813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016100715173afa2c4282f73d329bf83751a235ef83983f2e840ad4114ce444a`  
		Last Modified: Thu, 20 Jun 2024 18:35:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:25d2adb5410c3759b52d8837459b5378a1d8a62355fbc67355150a6d9b48545a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46040331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942b94c82c6b5678e972e699a1d9853ab08270ef28c1741c60ed2732fad9cf4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 19:44:18 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 18 Jun 2024 18:43:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.3/traefik_v3.0.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 18 Jun 2024 18:43:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 18 Jun 2024 18:43:27 GMT
EXPOSE 80
# Tue, 18 Jun 2024 18:43:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 18:43:28 GMT
CMD ["traefik"]
# Tue, 18 Jun 2024 18:43:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfdae686589931bbb09e116bfbb8ee205184c76b0a1158eedaa6d28ca76f73f`  
		Last Modified: Thu, 30 May 2024 19:44:53 GMT  
		Size: 464.2 KB (464183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d776cfc63470c9c824525e074b46a386f4788a8d5ee64d979fa1f5d1f74c929`  
		Last Modified: Tue, 18 Jun 2024 18:44:17 GMT  
		Size: 42.1 MB (42115440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a909886d4318ac028660814dbcb6bc4877da3e780ecb9643a8a23966ab14ab6`  
		Last Modified: Tue, 18 Jun 2024 18:44:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
