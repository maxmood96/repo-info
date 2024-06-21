## `traefik:mimolette`

```console
$ docker pull traefik@sha256:eff67fb6195d2a281cad0cdb59f6f42ea6f4b99934a97188e00751d549fa5222
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
$ docker pull traefik@sha256:bb99890d2a99a3e41caeb5100f97813e295dcb6fa581f0e0540a1070efe6b539
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46847183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d3db58883574ac724b41c966bbb976c762f4395fcdadbf49aadb72a314401a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:35:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 21 Jun 2024 02:35:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.5/traefik_v2.11.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 21 Jun 2024 02:35:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 21 Jun 2024 02:35:27 GMT
EXPOSE 80
# Fri, 21 Jun 2024 02:35:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Jun 2024 02:35:27 GMT
CMD ["traefik"]
# Fri, 21 Jun 2024 02:35:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dd96e192718f89b7fb933ba0ea5d44233e4241c88f28a540aae672e6702b0626`  
		Last Modified: Fri, 21 Jun 2024 02:36:06 GMT  
		Size: 42.8 MB (42759826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac997659cb617a0d21f2f57e709bf8ac22649fd15a3636c0d1cfd785495478df`  
		Last Modified: Fri, 21 Jun 2024 02:36:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d3735f691ecc08505287ef527d119362ba72d176ba83b6c20ae118f11988a448
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44059260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869af0eeb9b9703f7727c55bbe63b99e0b5fd62908769c4c2eb86b314b013d94`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:59:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 21 Jun 2024 02:00:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.5/traefik_v2.11.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 21 Jun 2024 02:00:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 21 Jun 2024 02:00:02 GMT
EXPOSE 80
# Fri, 21 Jun 2024 02:00:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Jun 2024 02:00:02 GMT
CMD ["traefik"]
# Fri, 21 Jun 2024 02:00:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:86a0ea5201ef16b143aa49f1736f65b2d492d14ddbb459ff5f061c9ce7dfd4f8`  
		Last Modified: Fri, 21 Jun 2024 02:00:42 GMT  
		Size: 40.2 MB (40227924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0e6eef83d12e606a0747da67863a111759134e488b4b5562c9036446c23b93`  
		Last Modified: Fri, 21 Jun 2024 02:00:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fef6c2f1911f0b591471b7868240a9d7f609a9bb4cb23291a9b2324f8716b61b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44178610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e784e5e03405863995911933bc9e2a0ffba4feb49ab10fbca5516f05a6ca912e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:25:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 21 Jun 2024 00:26:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.5/traefik_v2.11.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 21 Jun 2024 00:26:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 21 Jun 2024 00:26:16 GMT
EXPOSE 80
# Fri, 21 Jun 2024 00:26:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Jun 2024 00:26:17 GMT
CMD ["traefik"]
# Fri, 21 Jun 2024 00:26:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:b94cb3309c5dbd8762f63c9d8a73ba726405a039fd71a11e1234d5b5556a3c1d`  
		Last Modified: Fri, 21 Jun 2024 00:30:57 GMT  
		Size: 39.6 MB (39623958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51efa67ef282696bd9868f5748530048fd44274f0d6e7350011f7e3ff961f3a`  
		Last Modified: Fri, 21 Jun 2024 00:30:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:dd026776fa3ff2b73352432e23f736a66a47c8907de98276ea692f79157e0bcb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42536661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45b6b7b51ab368eff54ae09f6308bcbf6f87b79a6d3fcbe8e7b90c0873ad752`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 23:22:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jun 2024 23:22:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.5/traefik_v2.11.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jun 2024 23:22:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jun 2024 23:22:23 GMT
EXPOSE 80
# Thu, 20 Jun 2024 23:22:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jun 2024 23:22:23 GMT
CMD ["traefik"]
# Thu, 20 Jun 2024 23:22:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:101de29dc982493983f34024bc0ca9459003370cd85a736028723e690ce9856d`  
		Last Modified: Thu, 20 Jun 2024 23:23:01 GMT  
		Size: 38.5 MB (38498740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe106454381878deac1126d66d63f4904e4a2557851de6c96d9e870d37b6f59e`  
		Last Modified: Thu, 20 Jun 2024 23:22:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:8eaf19e05083b1c7fcdfab0918e789b7c8267aacade23bafcbe3db0f885a9183
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45275414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76c8274e96460ba7bed7d52aa615c4180054c0e57ae796fb671738f226206a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:34:03 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jun 2024 18:35:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.5/traefik_v2.11.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jun 2024 18:35:09 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jun 2024 18:35:10 GMT
EXPOSE 80
# Thu, 20 Jun 2024 18:35:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jun 2024 18:35:11 GMT
CMD ["traefik"]
# Thu, 20 Jun 2024 18:35:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:feae9632fec62a046777a81481c83991497f8f3a88123d06159e6e2a7b72ac37`  
		Last Modified: Thu, 20 Jun 2024 18:37:09 GMT  
		Size: 41.4 MB (41440172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0290c1d9d6ed4a46f8d3db54e852701386843132200dbc05559285148ab01170`  
		Last Modified: Thu, 20 Jun 2024 18:36:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:a6ef97b9b6c7b4056ff8a07b508af37da85fd5e3d1af3c34da9918d61b6610ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45603729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184b0e4321ecfa928d303b2645e1f9a5e2a0985db7c27194005cc992fbd1cad1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 19:44:18 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 18 Jun 2024 18:43:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.5/traefik_v2.11.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 18 Jun 2024 18:43:42 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 18 Jun 2024 18:43:42 GMT
EXPOSE 80
# Tue, 18 Jun 2024 18:43:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 18:43:42 GMT
CMD ["traefik"]
# Tue, 18 Jun 2024 18:43:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:343d416c217be5792bc359d949cc77931e0a727019bda7581b9de3dfa5b4d4a8`  
		Last Modified: Tue, 18 Jun 2024 18:44:35 GMT  
		Size: 41.7 MB (41678837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c08e45dc6def1bb667f70fe422f71b92710cf726ac15a727986c3baaad85b29`  
		Last Modified: Tue, 18 Jun 2024 18:44:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
