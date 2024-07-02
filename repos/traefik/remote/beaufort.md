## `traefik:beaufort`

```console
$ docker pull traefik@sha256:2e18efe9b193527928fc96855042c9afe55eea2d6e7fce1b3be44837f47aba5f
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
$ docker pull traefik@sha256:9214fcecc5833b4df2bfe6bf92714f35220d79a4c5c626931701dbbdb555f86b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47470718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4ed730cae1fd3aea7db703c77c5f27cc5550748e492cd963a386f409562568`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:35:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 02 Jul 2024 22:20:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.4/traefik_v3.0.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 02 Jul 2024 22:20:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 02 Jul 2024 22:20:25 GMT
EXPOSE 80
# Tue, 02 Jul 2024 22:20:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 22:20:26 GMT
CMD ["traefik"]
# Tue, 02 Jul 2024 22:20:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:4c4266770910efb770c6a364e5c3df8dce8f41084200d0e626a649d4355f5ad5`  
		Last Modified: Tue, 02 Jul 2024 22:21:17 GMT  
		Size: 43.4 MB (43383361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e108beaf7ab999124e5a818a055627c77fc914d4219428894ee145e04d44ac`  
		Last Modified: Tue, 02 Jul 2024 22:21:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9a8b6b163ff9e16ee1904d985ac71bdf7bba0121a714b4721c9636bb917ef112
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44537465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cccf9fc98e4dd2bd091cb98a3deb573567da9cc4b244ad5fe5fb0c10437fa99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:59:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 02 Jul 2024 22:18:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.4/traefik_v3.0.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 02 Jul 2024 22:18:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 02 Jul 2024 22:18:37 GMT
EXPOSE 80
# Tue, 02 Jul 2024 22:18:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 22:18:37 GMT
CMD ["traefik"]
# Tue, 02 Jul 2024 22:18:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:3b0858dceb8f450988be90e79b46ccee19f667d5514d693baace82caa211792e`  
		Last Modified: Tue, 02 Jul 2024 22:19:29 GMT  
		Size: 40.7 MB (40706129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45c4424794f1284e97838fadf2adc8b23c8bde3e2785d4309f6f95d83174c6d`  
		Last Modified: Tue, 02 Jul 2024 22:19:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a72b31d2f6c4153ea52642f603d453d750220436ea32468ac91b477a6f9f2f91
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44757703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026b28c1a47d6bf1af02bf2908dbf65e72d14ca16db00dfbf1ef3d303e032d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:25:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 02 Jul 2024 21:51:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.4/traefik_v3.0.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 02 Jul 2024 21:51:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 02 Jul 2024 21:51:36 GMT
EXPOSE 80
# Tue, 02 Jul 2024 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 21:51:36 GMT
CMD ["traefik"]
# Tue, 02 Jul 2024 21:51:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:4c8304620d0a7a95b8f70fd903fe8b4ad2c43de69e88af1ff551fa7378a51333`  
		Last Modified: Tue, 02 Jul 2024 21:52:18 GMT  
		Size: 40.2 MB (40203052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceaf6f568c6bc23c11fa39ad3bc83240c4d27103163cc26221a91a74e0d4c870`  
		Last Modified: Tue, 02 Jul 2024 21:52:14 GMT  
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
$ docker pull traefik@sha256:162264350e65fbecd8017a4481583e60bba3a02e6d6d12c63dab7ac7a5fb8812
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46041760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291fbcd612b84130437fe389b6ae5e404faaed1029d9c5a7a9cebea65341ca69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 22:21:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jun 2024 22:21:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.3/traefik_v3.0.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jun 2024 22:21:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jun 2024 22:21:17 GMT
EXPOSE 80
# Thu, 20 Jun 2024 22:21:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jun 2024 22:21:18 GMT
CMD ["traefik"]
# Thu, 20 Jun 2024 22:21:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552ab5febcd528c558dcc899a972d320b269b0634f72fbc02b23d8d2a09493cb`  
		Last Modified: Thu, 20 Jun 2024 22:24:37 GMT  
		Size: 464.1 KB (464074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423708b6928dc80984cdf35cbfecccbc95a58c8625b65d68e6cacc57027976a1`  
		Last Modified: Thu, 20 Jun 2024 22:24:24 GMT  
		Size: 42.1 MB (42115461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ca97581c4ab515a4d695746887989ab6e09c29c780a04eab217d4904f019e7`  
		Last Modified: Thu, 20 Jun 2024 22:24:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
