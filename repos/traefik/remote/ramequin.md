## `traefik:ramequin`

```console
$ docker pull traefik@sha256:c5bd185c41ba3dbb42cf8a1b9fbdc368bdc96f90c8e598134879935f64e7a7f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:ramequin` - linux; amd64

```console
$ docker pull traefik@sha256:10d11eab6d1254a3dc1a9015a33bd7deb3e779c852e89bbbf2cb69194f82ee90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51766444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5c90e0c7d1b1c8afe3e797fa43bd0f92b8fe25611ebeaf2e238ef84b58d3b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 19:01:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 05 Dec 2025 19:01:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.4/traefik_v3.6.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 05 Dec 2025 19:01:42 GMT
COPY entrypoint.sh / # buildkit
# Fri, 05 Dec 2025 19:01:42 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Dec 2025 19:01:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Dec 2025 19:01:42 GMT
CMD ["traefik"]
# Fri, 05 Dec 2025 19:01:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aeb4cefcd95d34323e377eb57826b068fc5642aec93df786e91a966c5d806ef`  
		Last Modified: Fri, 05 Dec 2025 19:02:20 GMT  
		Size: 456.9 KB (456927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb5f46fa1833f2f5bc608c0d80318882fb52b237fc73e4e42aa7697baa46bf`  
		Last Modified: Fri, 05 Dec 2025 19:02:29 GMT  
		Size: 47.5 MB (47506697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a90fc484f698ba2ec2dd17c556d57edbb7f38bf81dc18bca747b903c210a2a`  
		Last Modified: Fri, 05 Dec 2025 19:02:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:0f88e541ddc02194a21def6a6898a40b6b835d38479b00f3cad5d41fc2c6f6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168e46af62243a2035505abd510bef12a921512798fdd1fbf0854822a273b31c`

```dockerfile
```

-	Layers:
	-	`sha256:21603114a5185a0a19ef9c728adda9b9eeac5d28b828e7094e5c213fb2c69bc3`  
		Last Modified: Fri, 05 Dec 2025 19:10:05 GMT  
		Size: 843.1 KB (843145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a3df5126a8bcab6dc7e03689161390979465649be139bd0eb07265f6fcc15ed`  
		Last Modified: Fri, 05 Dec 2025 19:10:05 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c0085b0d0206eeb231510c295495423c25b99138e063247736e7faf1ff56d7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47052442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1280ec490de409215a82dad09e4844bf4ba0ca365266de395ab9cb0ea96948a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 19:00:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 05 Dec 2025 19:00:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.4/traefik_v3.6.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 05 Dec 2025 19:00:26 GMT
COPY entrypoint.sh / # buildkit
# Fri, 05 Dec 2025 19:00:26 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Dec 2025 19:00:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Dec 2025 19:00:26 GMT
CMD ["traefik"]
# Fri, 05 Dec 2025 19:00:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be50edfa72b2ca4a74106ddc1cdcfcfb79815b358f90b889c666a72834471d8d`  
		Last Modified: Fri, 05 Dec 2025 19:00:48 GMT  
		Size: 457.7 KB (457749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b1bd6f2415c1e9f31e285c2a0f7c49f379a75e3287aa059d289479f5235019`  
		Last Modified: Fri, 05 Dec 2025 19:00:50 GMT  
		Size: 43.1 MB (43090243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083d9534e26c23d3d44a69eca92887df27fe20e04ff0e7d3f5b7850ed33214e`  
		Last Modified: Fri, 05 Dec 2025 19:00:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:de36067b3a8496e79cbc265d8b190ed01bfd5ee5ecfa3a14852f902cbbedc282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d08f9271925e005d94e044155e85c0fea06605396ef545043d169786458f721`

```dockerfile
```

-	Layers:
	-	`sha256:e8795d9e57287a79020ca30ba54d7d8ee0484013c984fc07c932e9415a2149e3`  
		Last Modified: Fri, 05 Dec 2025 19:10:09 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:84e437f372be875258e130616c7531abe1d95f7ee9a84b273c2887d2b35423d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47832753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92decb13dfcedf311dc07e9678ff5a3869ebc258d17c95f5a1621d4d6f32af2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 19:01:41 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 05 Dec 2025 19:01:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.4/traefik_v3.6.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 05 Dec 2025 19:01:43 GMT
COPY entrypoint.sh / # buildkit
# Fri, 05 Dec 2025 19:01:43 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Dec 2025 19:01:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Dec 2025 19:01:43 GMT
CMD ["traefik"]
# Fri, 05 Dec 2025 19:01:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3943e49514e29accc3583632e100569aafd8c21d283fdb3a543df0656627ce`  
		Last Modified: Fri, 05 Dec 2025 19:02:24 GMT  
		Size: 459.0 KB (459019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e264e62030f3b108d29db75f4c03211be382dccc244fa6487e3e327255fdc0ef`  
		Last Modified: Fri, 05 Dec 2025 19:02:36 GMT  
		Size: 43.2 MB (43235296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445170f88d6589b48f52bcc45073bb1b1b5f9443cfdb03f349e62bc5e11edcc2`  
		Last Modified: Fri, 05 Dec 2025 19:02:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:043b28c73c9dd59f310c510868b4d0d0bf0b26f9aecc8e07c9f078d9420e6ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.2 KB (856181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1ba175bbab1e2d9bf864357db900e95076f4c8c2ce8e15387d82cedfd882b3`

```dockerfile
```

-	Layers:
	-	`sha256:09b7d85da698156000daae072b1ed6176183d918cc072497b7e66a6d02abe84b`  
		Last Modified: Fri, 05 Dec 2025 19:10:13 GMT  
		Size: 843.2 KB (843249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6baa74613095a13c98f1dec23d061d75b0212b1042cb3987e9911b3f3b4b53b2`  
		Last Modified: Fri, 05 Dec 2025 19:10:13 GMT  
		Size: 12.9 KB (12932 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:45f4ae2450d8fe1a37bdf765bfc16b7d4039b7be0764ade272d8162129294f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45445861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228218a1632adbd7ab9e6c871ba44b335b2501a60353cdbf0affb054d74e5fe9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 19:01:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 05 Dec 2025 19:01:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.4/traefik_v3.6.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 05 Dec 2025 19:01:12 GMT
COPY entrypoint.sh / # buildkit
# Fri, 05 Dec 2025 19:01:12 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Dec 2025 19:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Dec 2025 19:01:12 GMT
CMD ["traefik"]
# Fri, 05 Dec 2025 19:01:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697210db1e0d0e204cd5688797c1fdf774e33e05629031835e65f0238aea6321`  
		Last Modified: Fri, 05 Dec 2025 19:02:15 GMT  
		Size: 459.4 KB (459447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38f8632c1c23c29083c983f87e310eba03e8d159f265c2156221725491c95a6`  
		Last Modified: Fri, 05 Dec 2025 19:02:23 GMT  
		Size: 41.3 MB (41253803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6adc9afe0cc8e097f91b88309cb5d87a898304bbfac22fb9b1a14efa9e8b94`  
		Last Modified: Fri, 05 Dec 2025 19:02:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:14df2184b5a03c9b1cff9104b7512372073d94fdf620d9fc303ff80c8355baf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.1 KB (854088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffde7597632d2a7bcf5f1566a4ba5332116111256e00bf6819e349d19ac6f6e6`

```dockerfile
```

-	Layers:
	-	`sha256:394f237035e9aa98a76fdf592622f1072e4279817d0360f3c2e445d0a53f1859`  
		Last Modified: Fri, 05 Dec 2025 19:10:17 GMT  
		Size: 841.3 KB (841252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74ec0de704c758884e2cbfc690be198985616e447f264bb557e654a6e01b1b3c`  
		Last Modified: Fri, 05 Dec 2025 19:10:18 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:8da14505b89bd3a8555ae14c92eb2063d8e956cc2f62821181d550221ac2e7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49762908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bbbaf832342dab577217b7dfbfdc8f19a8bdd41860080f3b91ae32e95d90a43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 07 Dec 2025 06:26:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.4/traefik_v3.6.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 07 Dec 2025 06:26:43 GMT
COPY entrypoint.sh / # buildkit
# Sun, 07 Dec 2025 06:26:43 GMT
EXPOSE map[80/tcp:{}]
# Sun, 07 Dec 2025 06:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 07 Dec 2025 06:26:43 GMT
CMD ["traefik"]
# Sun, 07 Dec 2025 06:26:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af791cbe18cccde54cc961a13cf4c5891ced4cdef67b44389ccf9e891855e8d5`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 457.3 KB (457276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7567b2cb5aba81cbc038345051656a65b23312e1e1fc5ec15fcd85b793aef1`  
		Last Modified: Sun, 07 Dec 2025 06:31:38 GMT  
		Size: 45.8 MB (45790024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc48bb47bcc6f3fe2a5a0d2e60a476aae116546e0c312340ef2db605159cfae`  
		Last Modified: Sun, 07 Dec 2025 06:31:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:007767f2a57352873a698e9992a4b8015f80f5aae3551a48288038c1833074fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.1 KB (854084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff407f50f8f1dd3631fbd3986c92a5a478b5f834c9e340fadc7336b76e0fd08`

```dockerfile
```

-	Layers:
	-	`sha256:884365a1a7cd1f4274dab4d0457d7c325c2a662f7435d85581330dd6b814fee9`  
		Last Modified: Sun, 07 Dec 2025 07:09:43 GMT  
		Size: 841.2 KB (841248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29526ee34c4dbb2be15b655a455f0ed442d497ccbe066f3ebeb11b837dd1aee9`  
		Last Modified: Sun, 07 Dec 2025 07:09:44 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:f4420d7cb9212d62c5e42a57aca7c2abefa2c1d8f79d83d2491242b194228b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49760417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a4b5a28d5319ebb0676386d92420e0980d5cd68216ae4fc87ee946a335ba6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 19:01:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 05 Dec 2025 19:01:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.4/traefik_v3.6.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 05 Dec 2025 19:01:12 GMT
COPY entrypoint.sh / # buildkit
# Fri, 05 Dec 2025 19:01:12 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Dec 2025 19:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Dec 2025 19:01:12 GMT
CMD ["traefik"]
# Fri, 05 Dec 2025 19:01:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43ffab5f05bdfab1aae8358b10a8bea75901175e290fd19a27208c1eff0b2c1`  
		Last Modified: Fri, 05 Dec 2025 19:02:37 GMT  
		Size: 457.9 KB (457911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36257f51f9bd72005b5bca50f100adce58df6181f62939b43cd5f9b2fbf64bc`  
		Last Modified: Fri, 05 Dec 2025 19:02:39 GMT  
		Size: 45.7 MB (45652892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d0e2e68d5cabe3cd1513e66176e71b22d9b4132b5b4656ce7dcf0887972f6a`  
		Last Modified: Fri, 05 Dec 2025 19:02:36 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:fd3fc5f284695a9259c06e41d82a9e5346ea5a227a031fd231130ca39d2f5eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.0 KB (853960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9013195dc3bcc0252d8cbcc9781957c995a5e66fb5a4486d3d4b83430e5284d0`

```dockerfile
```

-	Layers:
	-	`sha256:d7bc3ad1b0e96c82b93825e366d814cd7a0332ec0be5e87b35dbb94cedeef9c4`  
		Last Modified: Fri, 05 Dec 2025 19:10:24 GMT  
		Size: 841.2 KB (841194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e800839b2eb69cf977e6ad74a160e19ad92497be835a003e1192476a860515cf`  
		Last Modified: Fri, 05 Dec 2025 19:10:25 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json
