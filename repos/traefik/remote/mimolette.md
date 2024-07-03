## `traefik:mimolette`

```console
$ docker pull traefik@sha256:0526f80f04dd06d82ad87b3cc4a4bc199460262864ce7dad06a21ef9c4057ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:d07c3bc7add1eda720449dc170153c26bf3f2677aa3e59f9db1b1664ce4784d8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46906686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096793d0951851a19098649d71e8c89dbacac5abd901c04d512a75e5e04a9ea8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:35:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 02 Jul 2024 22:20:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.6/traefik_v2.11.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 02 Jul 2024 22:20:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 02 Jul 2024 22:20:34 GMT
EXPOSE 80
# Tue, 02 Jul 2024 22:20:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 22:20:34 GMT
CMD ["traefik"]
# Tue, 02 Jul 2024 22:20:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:73221eaff9b44a8282039acdbcb37da1fed2c1f035f9820cc0db27e5c2c54ff2`  
		Last Modified: Tue, 02 Jul 2024 22:21:39 GMT  
		Size: 42.8 MB (42819330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fa227fafcdc5f0a09332a8c619f4ac1572fa1c49f470f724543db8ba97d9a0`  
		Last Modified: Tue, 02 Jul 2024 22:21:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9eb2e1aee3e8a93cdd0d5948b12a592ea5e65e3dc2a5cb9a5837b0fd94bc92d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44097822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca10c2c8fe9450452f29cb2899f05c21f0b9e68366cea193d7425239aa1c2bf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:59:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 02 Jul 2024 22:18:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.6/traefik_v2.11.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 02 Jul 2024 22:18:45 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 02 Jul 2024 22:18:45 GMT
EXPOSE 80
# Tue, 02 Jul 2024 22:18:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 22:18:46 GMT
CMD ["traefik"]
# Tue, 02 Jul 2024 22:18:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bb11cd18ed4c958bc12821f88f0fb614fc25364cec6ed9c666f024fd3701edf9`  
		Last Modified: Tue, 02 Jul 2024 22:19:51 GMT  
		Size: 40.3 MB (40266486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ee072df3e05843d8355a89dcc8ec97e8e17db8746d851733157b1927a12422`  
		Last Modified: Tue, 02 Jul 2024 22:19:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e629a2b9931cc7421daf60628a3dd7a64b17e056be27338ae103677a3c465b15
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44233032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89cfecd7465261a06f1e2ff00d03fc6d29fc0034421ec57f2fad7c359bb3402`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:25:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 02 Jul 2024 21:51:41 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.6/traefik_v2.11.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 02 Jul 2024 21:51:42 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 02 Jul 2024 21:51:42 GMT
EXPOSE 80
# Tue, 02 Jul 2024 21:51:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 21:51:43 GMT
CMD ["traefik"]
# Tue, 02 Jul 2024 21:51:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d9f78e5793ae43efebf39a37d561c8d97e4718c95545b63941c41bd9f67c186b`  
		Last Modified: Tue, 02 Jul 2024 21:52:38 GMT  
		Size: 39.7 MB (39678381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3734893d3e05bc4d6ce61a6dd3f972cff31e735a16c4e66b3c9cbd97558e5e2f`  
		Last Modified: Tue, 02 Jul 2024 21:52:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:fa7005ce354d14f2749711d00e73e51d44e9f7d9357c56a9c472d655cf353aab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42581474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f6e79dfcddc4f2396677c352dfa39370218105f240a4206ec67bc9f4ed17e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 23:22:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 03 Jul 2024 01:05:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.6/traefik_v2.11.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 03 Jul 2024 01:05:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 03 Jul 2024 01:05:41 GMT
EXPOSE 80
# Wed, 03 Jul 2024 01:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 01:05:42 GMT
CMD ["traefik"]
# Wed, 03 Jul 2024 01:05:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:3b5f1d3905c308e4d267277c0ba0a432fb9d198cc75489b3878c3bee8238b33c`  
		Last Modified: Wed, 03 Jul 2024 01:06:44 GMT  
		Size: 38.5 MB (38543554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34e08d3f2e5381f7396fb75fcb48af62f8bb70e15db11aadac5bfbf1908ac30`  
		Last Modified: Wed, 03 Jul 2024 01:06:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:27bb03309cfd63f53ebe513504755dded40501cab89933b21c82fd396aafa88f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45312328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3385eafeec0467ed9f4f47662c5385920ca968d6e0a1a574904c4b1d4eb8b6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:34:03 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 03 Jul 2024 01:13:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.6/traefik_v2.11.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 03 Jul 2024 01:13:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 03 Jul 2024 01:13:29 GMT
EXPOSE 80
# Wed, 03 Jul 2024 01:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 01:13:30 GMT
CMD ["traefik"]
# Wed, 03 Jul 2024 01:13:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:11cd5eb81899f321dabee8a008561b146fcc489c204a26375772b48645e00f07`  
		Last Modified: Wed, 03 Jul 2024 01:16:28 GMT  
		Size: 41.5 MB (41477086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14ab49275534cb77ec69207763dbd308e831d2ec2236850813a88107a06235e`  
		Last Modified: Wed, 03 Jul 2024 01:15:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:8b48a1ca64e51ee6b6e4b3981899cca2900ca0597daddd2c90b53c31b914addc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45646006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa1b632e3cbb69aea85f53d3cd7bf60e661eadfa3e4873f34420ea29e335a48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 22:21:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 03 Jul 2024 00:42:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.6/traefik_v2.11.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 03 Jul 2024 00:42:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 03 Jul 2024 00:42:16 GMT
EXPOSE 80
# Wed, 03 Jul 2024 00:42:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 00:42:17 GMT
CMD ["traefik"]
# Wed, 03 Jul 2024 00:42:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:ebc3315a94ac50aa3a0018be3ea8138694dd083de90bccfc4d9b59f5706f502b`  
		Last Modified: Wed, 03 Jul 2024 00:43:13 GMT  
		Size: 41.7 MB (41719709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c299369dbc20d83d205693ae1cf41e0d7728d13c2747d6f978c4297ca862b30`  
		Last Modified: Wed, 03 Jul 2024 00:43:06 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
