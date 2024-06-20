## `traefik:mimolette`

```console
$ docker pull traefik@sha256:16836110b9fb99debc3e08161ca0075fbef73a18aa07906f1b9e8c0cbbcb5bd0
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
$ docker pull traefik@sha256:0601b9ebbc56fa4104a568489a95dbe7be59388d38c9e316fffbba05211051e1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46845513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea7f1873a72e17424db4d1f3246e9d5ecbd5be3eba18ba6a7498b152dec7cc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 19:51:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 18 Jun 2024 18:23:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.5/traefik_v2.11.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 18 Jun 2024 18:23:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 18 Jun 2024 18:23:41 GMT
EXPOSE 80
# Tue, 18 Jun 2024 18:23:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 18:23:41 GMT
CMD ["traefik"]
# Tue, 18 Jun 2024 18:23:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063d5da2188cebebb3201442bac5e2e392e8ddea062e25cd77ce17d63272a4ba`  
		Last Modified: Thu, 30 May 2024 19:51:53 GMT  
		Size: 463.2 KB (463226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6e13c99967f12b50777071acf31dc53f769765916920fd43f650929112c6db`  
		Last Modified: Tue, 18 Jun 2024 18:24:23 GMT  
		Size: 42.8 MB (42759824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b34f47cb77b3488d8b76cd9c69f19074ab99b89c0fb7f4b107041e64f51d63`  
		Last Modified: Tue, 18 Jun 2024 18:24:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:eae8877a09cf154d9f503c3b32b863c4339a8eccd76910487414b2f91b7923b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44057278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4232bc5b4b273dcc084b8f53583ede51f09f2b9cc1ee395cf550a018fef7bd97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 19:49:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 18 Jun 2024 18:49:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.5/traefik_v2.11.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 18 Jun 2024 18:49:45 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 18 Jun 2024 18:49:45 GMT
EXPOSE 80
# Tue, 18 Jun 2024 18:49:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 18:49:46 GMT
CMD ["traefik"]
# Tue, 18 Jun 2024 18:49:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e0d37fb3a3fa24afbe2e75b8b155456fc23029b9d964091885b19c431ca1fa`  
		Last Modified: Thu, 30 May 2024 19:49:57 GMT  
		Size: 463.9 KB (463909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bdbca1b225cfa3a19728666f29a95dfc7e20097f503eafe78791f1b37a2db9`  
		Last Modified: Tue, 18 Jun 2024 18:50:29 GMT  
		Size: 40.2 MB (40227945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4b136e4a065aefcaa7b578f9d8adeafb4144866b20dc1305c77cc47738ea4`  
		Last Modified: Tue, 18 Jun 2024 18:50:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:63795157ef0313a52e10dd59de4b27da3e241446e6e7d1ef08f475b1694b6dab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44176678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f174747d8e8fe8cce6652d0e9430a59e20055a2a1c79b907a1b634618c7a63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 20:43:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 18 Jun 2024 18:55:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.5/traefik_v2.11.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 18 Jun 2024 18:55:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 18 Jun 2024 18:55:12 GMT
EXPOSE 80
# Tue, 18 Jun 2024 18:55:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 18:55:13 GMT
CMD ["traefik"]
# Tue, 18 Jun 2024 18:55:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33761638787616d48b5555dabc2c016480383aae25d9242a7b093c7e0b660e1f`  
		Last Modified: Thu, 30 May 2024 20:43:58 GMT  
		Size: 465.6 KB (465576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44c6751311f9a6dfe8a46a2a85946dce392ce930c5ff2cd2cb4ac4794c9e994`  
		Last Modified: Tue, 18 Jun 2024 18:55:49 GMT  
		Size: 39.6 MB (39623958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d63b65a9e79be59f83661aef2bb039ec5fc274630e1edc18dc028f8db629ea6`  
		Last Modified: Tue, 18 Jun 2024 18:55:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:1e5836d10319dce2ce91f2353090254fda56dc4e7a0b150804303e16711794b2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42534913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d471eeb7e631ab40796fe27f42e5cb3bdb3fd8933067f55c40ce065632a6fb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 19:29:22 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 18 Jun 2024 18:17:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.5/traefik_v2.11.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 18 Jun 2024 18:17:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 18 Jun 2024 18:17:20 GMT
EXPOSE 80
# Tue, 18 Jun 2024 18:17:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 18:17:21 GMT
CMD ["traefik"]
# Tue, 18 Jun 2024 18:17:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d99d4223e6b15fb67e3b010c6a956226b520efc8dd99c401d67aa092943715a`  
		Last Modified: Thu, 30 May 2024 19:29:56 GMT  
		Size: 466.0 KB (465958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5c538eebd240184fc4ae2c7b3f106bc6b69e1a9d421f4781e429f79c659920`  
		Last Modified: Tue, 18 Jun 2024 18:18:04 GMT  
		Size: 38.5 MB (38498740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be04f66a5790c6f3a6a8b237848316b64c0eb1e6e8919bcbf5957538ece8d7ea`  
		Last Modified: Tue, 18 Jun 2024 18:17:57 GMT  
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
