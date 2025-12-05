<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.32`](#traefik21132)
-	[`traefik:2.11.32-nanoserver-ltsc2022`](#traefik21132-nanoserver-ltsc2022)
-	[`traefik:2.11.32-windowsservercore-ltsc2022`](#traefik21132-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.2`](#traefik362)
-	[`traefik:3.6.2-nanoserver-ltsc2022`](#traefik362-nanoserver-ltsc2022)
-	[`traefik:3.6.2-windowsservercore-ltsc2022`](#traefik362-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-nanoserver-ltsc2022`](#traefikmimolette-nanoserver-ltsc2022)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:nanoserver-ltsc2022`](#traefiknanoserver-ltsc2022)
-	[`traefik:ramequin`](#traefikramequin)
-	[`traefik:ramequin-nanoserver-ltsc2022`](#traefikramequin-nanoserver-ltsc2022)
-	[`traefik:ramequin-windowsservercore-ltsc2022`](#traefikramequin-windowsservercore-ltsc2022)
-	[`traefik:v2`](#traefikv2)
-	[`traefik:v2-nanoserver-ltsc2022`](#traefikv2-nanoserver-ltsc2022)
-	[`traefik:v2-windowsservercore-ltsc2022`](#traefikv2-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-nanoserver-ltsc2022`](#traefikv211-nanoserver-ltsc2022)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.32`](#traefikv21132)
-	[`traefik:v2.11.32-nanoserver-ltsc2022`](#traefikv21132-nanoserver-ltsc2022)
-	[`traefik:v2.11.32-windowsservercore-ltsc2022`](#traefikv21132-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.2`](#traefikv362)
-	[`traefik:v3.6.2-nanoserver-ltsc2022`](#traefikv362-nanoserver-ltsc2022)
-	[`traefik:v3.6.2-windowsservercore-ltsc2022`](#traefikv362-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:b83fc239b8bdb5d0ac94c097d92d9a85ac82ea82d535fdd44ce85c29c683078e
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

### `traefik:2` - linux; amd64

```console
$ docker pull traefik@sha256:ac8c824bff35528ab36cb5245a8e488b419555e3b1b5672f4a2f4dc5b8a81da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50978940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce622bd2eac1031b22b2a724e52d8f615eca7eea0679e112a09235f4b17c7fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:05 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:08 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6f9c66e581dc9a0a73c65a91c09c8c25658e76ca0c42313eb493037f79bb81`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 456.9 KB (456939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f65172c40aa9ef7f8e79c49e6bf6a4ce5a81e3d6ed6c068ecaf903c644eba3e`  
		Last Modified: Thu, 04 Dec 2025 19:24:12 GMT  
		Size: 46.7 MB (46719180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d007db28390cd93183e7930d1e72ebe8ea62d5c2047982518002be0af321b66`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:b5c4cf6445eabd54dbbc99c02744ce44c18c069957f2e6cda738fd06736fa04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7997e68f2d9ee4a7810bb994211873a40085ba0376fd0434fc8f97efeabfde35`

```dockerfile
```

-	Layers:
	-	`sha256:9fdea8c65335538554420bb2f73ee610e77b35a8d99a41f66500f065275f7eef`  
		Last Modified: Thu, 04 Dec 2025 22:09:38 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618029352157666e0f7ada57d0b9772e84b7d8813d76014b9e425ac7d906c921`  
		Last Modified: Thu, 04 Dec 2025 22:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:00cacb5e3b75272d0963554604f16ee2f93e2caf8d774fb308ee3a2682b3fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46746429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b47a4e1eed2a3590b56e42a9bb20a814f235d05069e5aa8da45d25abfdaeb4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:10 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df693b807706002f19e426395418816460fb1a346f714d70e1c2c8afe374fd6`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 457.7 KB (457743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ef2971fe1a98ac7085996aa7023b6ccebf3897ef0483117b06b73d62b21aea`  
		Last Modified: Thu, 04 Dec 2025 19:23:35 GMT  
		Size: 42.8 MB (42784237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03516caee00078a85faefe1fd7d687c9cf8683b6dcfd8b57471545e1a9539870`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:aed9768db2bd35f301e0230caa1d2ffb2251a131320be645d6974c55e86618c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951f2a74272fc9c6c92170e2f27e242079597091a9506042db0401721e2db134`

```dockerfile
```

-	Layers:
	-	`sha256:1de50cb82d5378e594bac4e56dd225fa1d5f34bec27ee27fd9551913bc11fe3c`  
		Last Modified: Thu, 04 Dec 2025 22:09:42 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e578a9c8a06c07bb518641ab52b497b2fefce64c57a13530ae9731e0f35f6519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47214110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322725a91b8aa0f09e823c8879e728fab22810cdbec06bb669998e14e2f20e3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:53 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f4dc86542d7de98a768f4c0aee00ee4babe24157a4398e0e57604d2128efe`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923727f8d2ecf48712183a704dc223b5f52c03513cacfd1154f1ec815b66e8c`  
		Last Modified: Thu, 04 Dec 2025 19:21:01 GMT  
		Size: 42.6 MB (42616644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cb010135a022802cdc49ad86685907a4b7fec67e04d2ef6c5fa3b3dfbd504c`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:9a47c8fe962fefb1ab75eca20fce3174ae6107399c354c08787946583e9a53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82df1b830714c487e63a0e3cc2de51b9ae86fb219c7ede49b7055db217ff0f1`

```dockerfile
```

-	Layers:
	-	`sha256:d92cd312fa7dfcb46d339b39a908f09c05c04111ce94b03096f121b2b2ba238f`  
		Last Modified: Thu, 04 Dec 2025 22:09:46 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e6e0053f14ec312f9f3a94120e5153aa376985a6462fe8cb55509fc1495a7`  
		Last Modified: Thu, 04 Dec 2025 22:09:47 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:705d054c3866fdb6718a38957a67bcf193b38faa9ff5aaf8bc1da18af25bc516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45146924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de90c8d7f80a5aad7df4da00b1051b98930c54c8ababf669deb6d0d2d04a4f17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:34 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d260e1c1ba83417069742e33ef3dca0b56b4fb4a494c1c02755de510ec75e4a`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 459.4 KB (459433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e72a719bd9cd6a8f63be96d8d4c6575cad6c06a10e9ffaf1ecf0b582ff2542e`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 41.0 MB (40954880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a71f904fae4ec8c94264d8912ca717e59c7ec5031afd18f2f3f7bffdd5b1fe`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:3a46754ca761744e0f8883b9bfcd1684e663ac55b467b3a3b6923f51ff444d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d326368736c8a7420af0299583f8308601f8c1058845300561361b987ee13fad`

```dockerfile
```

-	Layers:
	-	`sha256:c4385ecde488f23523e5f1a690f599ee5de4f852330ed63b9cb8f58e461d00a9`  
		Last Modified: Thu, 04 Dec 2025 22:09:50 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b23d28dedd26705c13315cf1cee4006037cd5639347b33b5a7c069bd7e5b9d8`  
		Last Modified: Thu, 04 Dec 2025 22:09:51 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:6ce21e040bd4e2552427746ac5d0436d21f5f70bb0eadd8cf84a6e0fa0f6c8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49360723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8cc7abc990629392d3d289ac957e498bae15a9e836b0eade383931b77229b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:39 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d51ac067c25bf77fc5f6d25393d578c35080ea1d6d82d5c52dc00d5152699a6`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 457.9 KB (457913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36796f5fe181a6d2eb8fe90a5ca86fe909a756cc7cd57ccfb29dc3dc22620391`  
		Last Modified: Thu, 04 Dec 2025 19:21:04 GMT  
		Size: 45.3 MB (45253196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415c08db574d0b987b7070e71f49cbb2b58fa19861291d64c90e0dccde610b4`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:821663597494279db90cb3041862160bec3dcfe15162cb71c8b6f6fc3508aedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c48cbe3f7f2e42ad7e85328cc0e03b561857f85c793e37e796b4dc15269f8cd`

```dockerfile
```

-	Layers:
	-	`sha256:c41f76c95136d09bef36ea43a6eaf5869d09c21fc9edb28948b6c0e690332bc3`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61aaab597727c9c099570e7d5b30d607529858bc616081953993f6d88744a2a`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:138d7a87225e5c01a2b5db9301d7c6aab20073cd7798753fd81fe1e858cec83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2a60f1cc89f202977266b2a1651a9650ba802f4c066ca5931e59f3d404e1a042
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173864697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bece513a73e007d0e19209b413a84a7322d006eeddf299964b71efbec9b7e9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 04 Dec 2025 19:45:19 GMT
RUN cmd /S /C #(nop) COPY file:c5fd63825ca3af125acc7c0933cfb57a0080ecc168578d5b8882a0a05ef47bf4 in \ 
# Thu, 04 Dec 2025 19:45:21 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 04 Dec 2025 19:45:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:45:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473330b82e6af6d0613f521c11967f24228b1f1db3525d5ba2397c60eb96a81`  
		Last Modified: Thu, 04 Dec 2025 19:46:15 GMT  
		Size: 47.5 MB (47512441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9567c173a49fe4d5f69532267d8341eb54a40a659c6097e17856f13db5c3781e`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2dbeb0f2c54c414b81ad494b02482f528225d6ff22f9d7df5e139d19bb13bf`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c9666ee73f9d459e7e07b81222cd91048ae7e032a8e09a8888641e8ad861c7`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:dcec3000efc0d552358fd44f95644e5e908de7d472a63df0edb574de81517645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2988f00eaf0aeedcab04b601936c36fb3f454008611b35134e846a5f4e26b158
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818121188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31715b9a396950e980e3b2579d073169b112b7a318a9ac5c170d1f0e3edc930b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 04 Dec 2025 19:23:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Dec 2025 19:25:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 04 Dec 2025 19:25:38 GMT
EXPOSE 80
# Thu, 04 Dec 2025 19:25:40 GMT
ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bf6b095296831cd4d5f34d58fa0959fd7ef42e2dc9efd551c55d16e533b161`  
		Last Modified: Thu, 04 Dec 2025 19:38:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bac6613489c4597256f38308be766d6b69566e37eae1ec90fd75668f5ddd323`  
		Last Modified: Thu, 04 Dec 2025 19:38:29 GMT  
		Size: 48.2 MB (48154462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4a3d7b533059c5b4c90f6ad2b5cf3cf561ffd5341fa82b23cb2200e3604e15`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f85135e09953edf14105875b914705d2e9163f065e361f6df0548ce9a9ce7`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de324d8f25e723e0020dda62e746d4c7d464d758c0e6ecf94b2b5b741d0b25d0`  
		Last Modified: Thu, 04 Dec 2025 19:38:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:b83fc239b8bdb5d0ac94c097d92d9a85ac82ea82d535fdd44ce85c29c683078e
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

### `traefik:2.11` - linux; amd64

```console
$ docker pull traefik@sha256:ac8c824bff35528ab36cb5245a8e488b419555e3b1b5672f4a2f4dc5b8a81da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50978940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce622bd2eac1031b22b2a724e52d8f615eca7eea0679e112a09235f4b17c7fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:05 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:08 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6f9c66e581dc9a0a73c65a91c09c8c25658e76ca0c42313eb493037f79bb81`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 456.9 KB (456939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f65172c40aa9ef7f8e79c49e6bf6a4ce5a81e3d6ed6c068ecaf903c644eba3e`  
		Last Modified: Thu, 04 Dec 2025 19:24:12 GMT  
		Size: 46.7 MB (46719180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d007db28390cd93183e7930d1e72ebe8ea62d5c2047982518002be0af321b66`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:b5c4cf6445eabd54dbbc99c02744ce44c18c069957f2e6cda738fd06736fa04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7997e68f2d9ee4a7810bb994211873a40085ba0376fd0434fc8f97efeabfde35`

```dockerfile
```

-	Layers:
	-	`sha256:9fdea8c65335538554420bb2f73ee610e77b35a8d99a41f66500f065275f7eef`  
		Last Modified: Thu, 04 Dec 2025 22:09:38 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618029352157666e0f7ada57d0b9772e84b7d8813d76014b9e425ac7d906c921`  
		Last Modified: Thu, 04 Dec 2025 22:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:00cacb5e3b75272d0963554604f16ee2f93e2caf8d774fb308ee3a2682b3fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46746429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b47a4e1eed2a3590b56e42a9bb20a814f235d05069e5aa8da45d25abfdaeb4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:10 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df693b807706002f19e426395418816460fb1a346f714d70e1c2c8afe374fd6`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 457.7 KB (457743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ef2971fe1a98ac7085996aa7023b6ccebf3897ef0483117b06b73d62b21aea`  
		Last Modified: Thu, 04 Dec 2025 19:23:35 GMT  
		Size: 42.8 MB (42784237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03516caee00078a85faefe1fd7d687c9cf8683b6dcfd8b57471545e1a9539870`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:aed9768db2bd35f301e0230caa1d2ffb2251a131320be645d6974c55e86618c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951f2a74272fc9c6c92170e2f27e242079597091a9506042db0401721e2db134`

```dockerfile
```

-	Layers:
	-	`sha256:1de50cb82d5378e594bac4e56dd225fa1d5f34bec27ee27fd9551913bc11fe3c`  
		Last Modified: Thu, 04 Dec 2025 22:09:42 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e578a9c8a06c07bb518641ab52b497b2fefce64c57a13530ae9731e0f35f6519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47214110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322725a91b8aa0f09e823c8879e728fab22810cdbec06bb669998e14e2f20e3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:53 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f4dc86542d7de98a768f4c0aee00ee4babe24157a4398e0e57604d2128efe`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923727f8d2ecf48712183a704dc223b5f52c03513cacfd1154f1ec815b66e8c`  
		Last Modified: Thu, 04 Dec 2025 19:21:01 GMT  
		Size: 42.6 MB (42616644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cb010135a022802cdc49ad86685907a4b7fec67e04d2ef6c5fa3b3dfbd504c`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:9a47c8fe962fefb1ab75eca20fce3174ae6107399c354c08787946583e9a53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82df1b830714c487e63a0e3cc2de51b9ae86fb219c7ede49b7055db217ff0f1`

```dockerfile
```

-	Layers:
	-	`sha256:d92cd312fa7dfcb46d339b39a908f09c05c04111ce94b03096f121b2b2ba238f`  
		Last Modified: Thu, 04 Dec 2025 22:09:46 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e6e0053f14ec312f9f3a94120e5153aa376985a6462fe8cb55509fc1495a7`  
		Last Modified: Thu, 04 Dec 2025 22:09:47 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:705d054c3866fdb6718a38957a67bcf193b38faa9ff5aaf8bc1da18af25bc516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45146924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de90c8d7f80a5aad7df4da00b1051b98930c54c8ababf669deb6d0d2d04a4f17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:34 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d260e1c1ba83417069742e33ef3dca0b56b4fb4a494c1c02755de510ec75e4a`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 459.4 KB (459433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e72a719bd9cd6a8f63be96d8d4c6575cad6c06a10e9ffaf1ecf0b582ff2542e`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 41.0 MB (40954880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a71f904fae4ec8c94264d8912ca717e59c7ec5031afd18f2f3f7bffdd5b1fe`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:3a46754ca761744e0f8883b9bfcd1684e663ac55b467b3a3b6923f51ff444d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d326368736c8a7420af0299583f8308601f8c1058845300561361b987ee13fad`

```dockerfile
```

-	Layers:
	-	`sha256:c4385ecde488f23523e5f1a690f599ee5de4f852330ed63b9cb8f58e461d00a9`  
		Last Modified: Thu, 04 Dec 2025 22:09:50 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b23d28dedd26705c13315cf1cee4006037cd5639347b33b5a7c069bd7e5b9d8`  
		Last Modified: Thu, 04 Dec 2025 22:09:51 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:6ce21e040bd4e2552427746ac5d0436d21f5f70bb0eadd8cf84a6e0fa0f6c8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49360723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8cc7abc990629392d3d289ac957e498bae15a9e836b0eade383931b77229b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:39 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d51ac067c25bf77fc5f6d25393d578c35080ea1d6d82d5c52dc00d5152699a6`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 457.9 KB (457913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36796f5fe181a6d2eb8fe90a5ca86fe909a756cc7cd57ccfb29dc3dc22620391`  
		Last Modified: Thu, 04 Dec 2025 19:21:04 GMT  
		Size: 45.3 MB (45253196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415c08db574d0b987b7070e71f49cbb2b58fa19861291d64c90e0dccde610b4`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:821663597494279db90cb3041862160bec3dcfe15162cb71c8b6f6fc3508aedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c48cbe3f7f2e42ad7e85328cc0e03b561857f85c793e37e796b4dc15269f8cd`

```dockerfile
```

-	Layers:
	-	`sha256:c41f76c95136d09bef36ea43a6eaf5869d09c21fc9edb28948b6c0e690332bc3`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61aaab597727c9c099570e7d5b30d607529858bc616081953993f6d88744a2a`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:138d7a87225e5c01a2b5db9301d7c6aab20073cd7798753fd81fe1e858cec83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2a60f1cc89f202977266b2a1651a9650ba802f4c066ca5931e59f3d404e1a042
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173864697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bece513a73e007d0e19209b413a84a7322d006eeddf299964b71efbec9b7e9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 04 Dec 2025 19:45:19 GMT
RUN cmd /S /C #(nop) COPY file:c5fd63825ca3af125acc7c0933cfb57a0080ecc168578d5b8882a0a05ef47bf4 in \ 
# Thu, 04 Dec 2025 19:45:21 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 04 Dec 2025 19:45:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:45:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473330b82e6af6d0613f521c11967f24228b1f1db3525d5ba2397c60eb96a81`  
		Last Modified: Thu, 04 Dec 2025 19:46:15 GMT  
		Size: 47.5 MB (47512441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9567c173a49fe4d5f69532267d8341eb54a40a659c6097e17856f13db5c3781e`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2dbeb0f2c54c414b81ad494b02482f528225d6ff22f9d7df5e139d19bb13bf`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c9666ee73f9d459e7e07b81222cd91048ae7e032a8e09a8888641e8ad861c7`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:dcec3000efc0d552358fd44f95644e5e908de7d472a63df0edb574de81517645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2988f00eaf0aeedcab04b601936c36fb3f454008611b35134e846a5f4e26b158
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818121188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31715b9a396950e980e3b2579d073169b112b7a318a9ac5c170d1f0e3edc930b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 04 Dec 2025 19:23:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Dec 2025 19:25:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 04 Dec 2025 19:25:38 GMT
EXPOSE 80
# Thu, 04 Dec 2025 19:25:40 GMT
ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bf6b095296831cd4d5f34d58fa0959fd7ef42e2dc9efd551c55d16e533b161`  
		Last Modified: Thu, 04 Dec 2025 19:38:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bac6613489c4597256f38308be766d6b69566e37eae1ec90fd75668f5ddd323`  
		Last Modified: Thu, 04 Dec 2025 19:38:29 GMT  
		Size: 48.2 MB (48154462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4a3d7b533059c5b4c90f6ad2b5cf3cf561ffd5341fa82b23cb2200e3604e15`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f85135e09953edf14105875b914705d2e9163f065e361f6df0548ce9a9ce7`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de324d8f25e723e0020dda62e746d4c7d464d758c0e6ecf94b2b5b741d0b25d0`  
		Last Modified: Thu, 04 Dec 2025 19:38:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.32`

```console
$ docker pull traefik@sha256:79f8665f38c397ee91c7398208117561dbe1b519ce2e2a1c32ebea7855a6c49e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:2.11.32` - linux; amd64

```console
$ docker pull traefik@sha256:ac8c824bff35528ab36cb5245a8e488b419555e3b1b5672f4a2f4dc5b8a81da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50978940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce622bd2eac1031b22b2a724e52d8f615eca7eea0679e112a09235f4b17c7fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:05 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:08 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6f9c66e581dc9a0a73c65a91c09c8c25658e76ca0c42313eb493037f79bb81`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 456.9 KB (456939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f65172c40aa9ef7f8e79c49e6bf6a4ce5a81e3d6ed6c068ecaf903c644eba3e`  
		Last Modified: Thu, 04 Dec 2025 19:24:12 GMT  
		Size: 46.7 MB (46719180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d007db28390cd93183e7930d1e72ebe8ea62d5c2047982518002be0af321b66`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.32` - unknown; unknown

```console
$ docker pull traefik@sha256:b5c4cf6445eabd54dbbc99c02744ce44c18c069957f2e6cda738fd06736fa04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7997e68f2d9ee4a7810bb994211873a40085ba0376fd0434fc8f97efeabfde35`

```dockerfile
```

-	Layers:
	-	`sha256:9fdea8c65335538554420bb2f73ee610e77b35a8d99a41f66500f065275f7eef`  
		Last Modified: Thu, 04 Dec 2025 22:09:38 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618029352157666e0f7ada57d0b9772e84b7d8813d76014b9e425ac7d906c921`  
		Last Modified: Thu, 04 Dec 2025 22:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.32` - linux; arm variant v6

```console
$ docker pull traefik@sha256:00cacb5e3b75272d0963554604f16ee2f93e2caf8d774fb308ee3a2682b3fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46746429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b47a4e1eed2a3590b56e42a9bb20a814f235d05069e5aa8da45d25abfdaeb4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:10 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df693b807706002f19e426395418816460fb1a346f714d70e1c2c8afe374fd6`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 457.7 KB (457743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ef2971fe1a98ac7085996aa7023b6ccebf3897ef0483117b06b73d62b21aea`  
		Last Modified: Thu, 04 Dec 2025 19:23:35 GMT  
		Size: 42.8 MB (42784237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03516caee00078a85faefe1fd7d687c9cf8683b6dcfd8b57471545e1a9539870`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.32` - unknown; unknown

```console
$ docker pull traefik@sha256:aed9768db2bd35f301e0230caa1d2ffb2251a131320be645d6974c55e86618c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951f2a74272fc9c6c92170e2f27e242079597091a9506042db0401721e2db134`

```dockerfile
```

-	Layers:
	-	`sha256:1de50cb82d5378e594bac4e56dd225fa1d5f34bec27ee27fd9551913bc11fe3c`  
		Last Modified: Thu, 04 Dec 2025 22:09:42 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.32` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e578a9c8a06c07bb518641ab52b497b2fefce64c57a13530ae9731e0f35f6519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47214110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322725a91b8aa0f09e823c8879e728fab22810cdbec06bb669998e14e2f20e3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:53 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f4dc86542d7de98a768f4c0aee00ee4babe24157a4398e0e57604d2128efe`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923727f8d2ecf48712183a704dc223b5f52c03513cacfd1154f1ec815b66e8c`  
		Last Modified: Thu, 04 Dec 2025 19:21:01 GMT  
		Size: 42.6 MB (42616644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cb010135a022802cdc49ad86685907a4b7fec67e04d2ef6c5fa3b3dfbd504c`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.32` - unknown; unknown

```console
$ docker pull traefik@sha256:9a47c8fe962fefb1ab75eca20fce3174ae6107399c354c08787946583e9a53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82df1b830714c487e63a0e3cc2de51b9ae86fb219c7ede49b7055db217ff0f1`

```dockerfile
```

-	Layers:
	-	`sha256:d92cd312fa7dfcb46d339b39a908f09c05c04111ce94b03096f121b2b2ba238f`  
		Last Modified: Thu, 04 Dec 2025 22:09:46 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e6e0053f14ec312f9f3a94120e5153aa376985a6462fe8cb55509fc1495a7`  
		Last Modified: Thu, 04 Dec 2025 22:09:47 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.32` - linux; ppc64le

```console
$ docker pull traefik@sha256:705d054c3866fdb6718a38957a67bcf193b38faa9ff5aaf8bc1da18af25bc516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45146924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de90c8d7f80a5aad7df4da00b1051b98930c54c8ababf669deb6d0d2d04a4f17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:34 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d260e1c1ba83417069742e33ef3dca0b56b4fb4a494c1c02755de510ec75e4a`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 459.4 KB (459433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e72a719bd9cd6a8f63be96d8d4c6575cad6c06a10e9ffaf1ecf0b582ff2542e`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 41.0 MB (40954880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a71f904fae4ec8c94264d8912ca717e59c7ec5031afd18f2f3f7bffdd5b1fe`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.32` - unknown; unknown

```console
$ docker pull traefik@sha256:3a46754ca761744e0f8883b9bfcd1684e663ac55b467b3a3b6923f51ff444d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d326368736c8a7420af0299583f8308601f8c1058845300561361b987ee13fad`

```dockerfile
```

-	Layers:
	-	`sha256:c4385ecde488f23523e5f1a690f599ee5de4f852330ed63b9cb8f58e461d00a9`  
		Last Modified: Thu, 04 Dec 2025 22:09:50 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b23d28dedd26705c13315cf1cee4006037cd5639347b33b5a7c069bd7e5b9d8`  
		Last Modified: Thu, 04 Dec 2025 22:09:51 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.32` - linux; s390x

```console
$ docker pull traefik@sha256:6ce21e040bd4e2552427746ac5d0436d21f5f70bb0eadd8cf84a6e0fa0f6c8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49360723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8cc7abc990629392d3d289ac957e498bae15a9e836b0eade383931b77229b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:39 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d51ac067c25bf77fc5f6d25393d578c35080ea1d6d82d5c52dc00d5152699a6`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 457.9 KB (457913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36796f5fe181a6d2eb8fe90a5ca86fe909a756cc7cd57ccfb29dc3dc22620391`  
		Last Modified: Thu, 04 Dec 2025 19:21:04 GMT  
		Size: 45.3 MB (45253196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415c08db574d0b987b7070e71f49cbb2b58fa19861291d64c90e0dccde610b4`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.32` - unknown; unknown

```console
$ docker pull traefik@sha256:821663597494279db90cb3041862160bec3dcfe15162cb71c8b6f6fc3508aedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c48cbe3f7f2e42ad7e85328cc0e03b561857f85c793e37e796b4dc15269f8cd`

```dockerfile
```

-	Layers:
	-	`sha256:c41f76c95136d09bef36ea43a6eaf5869d09c21fc9edb28948b6c0e690332bc3`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61aaab597727c9c099570e7d5b30d607529858bc616081953993f6d88744a2a`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.32-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:138d7a87225e5c01a2b5db9301d7c6aab20073cd7798753fd81fe1e858cec83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11.32-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2a60f1cc89f202977266b2a1651a9650ba802f4c066ca5931e59f3d404e1a042
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173864697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bece513a73e007d0e19209b413a84a7322d006eeddf299964b71efbec9b7e9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 04 Dec 2025 19:45:19 GMT
RUN cmd /S /C #(nop) COPY file:c5fd63825ca3af125acc7c0933cfb57a0080ecc168578d5b8882a0a05ef47bf4 in \ 
# Thu, 04 Dec 2025 19:45:21 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 04 Dec 2025 19:45:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:45:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473330b82e6af6d0613f521c11967f24228b1f1db3525d5ba2397c60eb96a81`  
		Last Modified: Thu, 04 Dec 2025 19:46:15 GMT  
		Size: 47.5 MB (47512441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9567c173a49fe4d5f69532267d8341eb54a40a659c6097e17856f13db5c3781e`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2dbeb0f2c54c414b81ad494b02482f528225d6ff22f9d7df5e139d19bb13bf`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c9666ee73f9d459e7e07b81222cd91048ae7e032a8e09a8888641e8ad861c7`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.32-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:dcec3000efc0d552358fd44f95644e5e908de7d472a63df0edb574de81517645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11.32-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2988f00eaf0aeedcab04b601936c36fb3f454008611b35134e846a5f4e26b158
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818121188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31715b9a396950e980e3b2579d073169b112b7a318a9ac5c170d1f0e3edc930b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 04 Dec 2025 19:23:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Dec 2025 19:25:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 04 Dec 2025 19:25:38 GMT
EXPOSE 80
# Thu, 04 Dec 2025 19:25:40 GMT
ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bf6b095296831cd4d5f34d58fa0959fd7ef42e2dc9efd551c55d16e533b161`  
		Last Modified: Thu, 04 Dec 2025 19:38:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bac6613489c4597256f38308be766d6b69566e37eae1ec90fd75668f5ddd323`  
		Last Modified: Thu, 04 Dec 2025 19:38:29 GMT  
		Size: 48.2 MB (48154462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4a3d7b533059c5b4c90f6ad2b5cf3cf561ffd5341fa82b23cb2200e3604e15`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f85135e09953edf14105875b914705d2e9163f065e361f6df0548ce9a9ce7`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de324d8f25e723e0020dda62e746d4c7d464d758c0e6ecf94b2b5b741d0b25d0`  
		Last Modified: Thu, 04 Dec 2025 19:38:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:aaf0f6185419a50c74651448c1a5bf4606bd2d2ddb7b8749eed505d55bf8b8ea
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

### `traefik:3` - linux; amd64

```console
$ docker pull traefik@sha256:ec4fce4588f239530c79af7e2dd873877e51a5548cc51cfbf318ae6e1727e138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e55c25c9dc924eb86e34957cea11335f48f3eeb87c12b8472434db39a43f143`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 21:48:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 21:48:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 21:48:13 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 21:48:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fcf41ae4fe549fc66069c1d9a3dfc8c7684a19fae6345f38239a84543cb451`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 456.9 KB (456932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff51e48e8c41ee2aebd058d15b97b4f47b6722fac2a08e226f835df67d4418e2`  
		Last Modified: Tue, 18 Nov 2025 21:49:19 GMT  
		Size: 47.4 MB (47433025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e2292afa9f7b52254e57efeb2deac56f51163f1572a1da072bbecc4e1b757`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:4261a87ee97389d6ecbdb5e8d8a673aa7ab3655675e2f1d1d84dd3825e26bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b750f1805931f0b564bfd7f3749094595eeefa65812c77aed1c1c9326a8d96c7`

```dockerfile
```

-	Layers:
	-	`sha256:dd4ab2e6afc636d1939980a8bf3d9cea3ddcd13a44c1d2295ba738ef261d09d7`  
		Last Modified: Tue, 18 Nov 2025 22:12:05 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24afbeef114a9fcc5c689c830f8392110a29eb89171b2436f0186680ce002e14`  
		Last Modified: Tue, 18 Nov 2025 22:12:06 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:561b6e0f7d5f408c12d49170ad858a17c8fae6f0b685bccc027abdbc34bf98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25de55986ee18f2435d5c74bf6032a3a2e15353a695c8f7a9859a5bbede5e41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:28:50 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78109e37152b41df02ee2c237f740f003151ef213dd9c81e925a61e13a562e8e`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 457.7 KB (457742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cda1c04505fd255242fdece0301c166e8cec8bf2ab4dd1ac4debf3cd00bdff`  
		Last Modified: Tue, 18 Nov 2025 19:29:15 GMT  
		Size: 43.0 MB (42954733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece82213e301e010af11f5ebf09d08ea08de287de016f8cc954c3781b03eddcd`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:0009cf7a9ecccca8185f9089f56ac6cf92a7f3bcb3c43151132fef8c0e523439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb979678d6660d672ff7cb2a3a8f96887af931403b91c76d4f6b1342a169b49`

```dockerfile
```

-	Layers:
	-	`sha256:f937ea1ee9c88faa49302bc9ddc4cab7f1a4cda765d2fe7becd38622c625bf67`  
		Last Modified: Tue, 18 Nov 2025 22:12:09 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58ccae90050988e9890eedfb1c6548b82c1ca60e807d97517daaddb6312a557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9f1b556d725190bc03627caf6f7b39276b3aed3745b9c0701e408acbf0ea39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:25:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:25:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:25:43 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:25:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417edc5cf59f87d70cf22c79d067722d6949576117ec0bcff04e50d6a4edfab9`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594c719740f22165cd53b9aac15e8797c888a46b8036d0defd56bb322e1be2c`  
		Last Modified: Tue, 18 Nov 2025 19:26:44 GMT  
		Size: 43.1 MB (43148307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6369fe0dab57aea1446d2fc8db9da1e6d27db7b2847c04b4f90f4cd6d20ef21`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:29d930fed1539847060dfbc2bffe8beb811209e24903d0773c44de8a84ae446a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef50f53cba8be23e4bc4cc3aadc3d445801d4160a1931dbe8be09db5a661943f`

```dockerfile
```

-	Layers:
	-	`sha256:c15e382f6e16857c9e88493b9b05152c009ab9bcb9708326208db496e2692923`  
		Last Modified: Tue, 18 Nov 2025 22:12:12 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a64dd22de08febf3ec2ebeb77c873765b75b1b6561f00b63357b5c1266bb013`  
		Last Modified: Tue, 18 Nov 2025 22:12:13 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a690dd84bed67e8e18f8d4c04b90f73774e3895300207e88d4ebfef99dedd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45323965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff3c8eb0949ee6dfda7c4c8ce8a9058548e947d4be56670a9e1143f8b80b891`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 22:02:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 22:02:04 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 22:02:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7131cbb6f2ed0728075b7863f72b456c451d363f035bc26eb4dc639ff1ea91f`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 459.4 KB (459444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163ecef57ee3319b1b03d664f61a15b5798d00e5e693105671fdfca70b48572`  
		Last Modified: Tue, 18 Nov 2025 22:03:14 GMT  
		Size: 41.1 MB (41131911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e085ee6011d283be1359ca019b8b510565abcf3ba44bfceaea6351deca17429`  
		Last Modified: Tue, 18 Nov 2025 22:03:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:3be7a65febed98487068f4f3636c8b42574da05615fee85f690ccecc964a78f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806e17ee732263c18ab393c230c85c74af69797ff07837c6e0641265849c22`

```dockerfile
```

-	Layers:
	-	`sha256:f086e4046623395e3cb574d6480d4e05e3552ba71b387734b5f8f6c43500b78b`  
		Last Modified: Tue, 18 Nov 2025 22:12:17 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb34f7412305f709ba275808c9588d9a7a5e7cae6d9b1aa5d2f56928804c72d8`  
		Last Modified: Tue, 18 Nov 2025 22:12:18 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:dd5c5f868d64632d40e1fc02d154a6850871bd88b605ea430630aa7d2d70d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49696840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af8810d338f1bd1a4b4fb764de8b01c082104bd2f4f216724435a0d18961f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 20 Nov 2025 19:45:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:45:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Nov 2025 19:45:33 GMT
CMD ["traefik"]
# Thu, 20 Nov 2025 19:45:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:77490f998c3cacffe82e080079ee717eb224ae54ff7776969eb02d5e3083c297`  
		Last Modified: Thu, 20 Nov 2025 19:51:39 GMT  
		Size: 45.7 MB (45723955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f9fa6da824b71d504b2b5252daaa9d5aadf78e571c9f9d79aeff67f5907e6`  
		Last Modified: Thu, 20 Nov 2025 19:51:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:fc3215167bc91ea171842167fc09a79120e6f3d8d340a1e637804cdf56b71e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8091b4062673a8ea24b34c56fb441d17a6afb43e0dba564e3c8c16b9b0197`

```dockerfile
```

-	Layers:
	-	`sha256:92e1bb99aa3bbe7baa5d5f23f96ff12db288cb6426dc299879f820a396c7350c`  
		Last Modified: Thu, 20 Nov 2025 22:09:41 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c52c6da61f97cda07d7683b99b6ba1f2d1c8068ca37f64d0f288b2fc103fa5`  
		Last Modified: Thu, 20 Nov 2025 22:09:42 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:a1b3be8672939a4d2913ba3c9da9d86056337dae16b5a8f4fecfb429e436f8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088adf79d3c254dcb80a82265220f63d1f8fca26800fbeadc494b8be29f98de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:27:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:27:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:27:20 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:27:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ed3289785c33bee42da1326ef857e710b7e549418a49847e37717014d7961`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 457.9 KB (457907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372adc29fa3a207abdcada906a4729dc818037b9435d9fdaa2924029ec613d48`  
		Last Modified: Tue, 18 Nov 2025 19:28:24 GMT  
		Size: 45.6 MB (45580906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372305cc3de919e1c11bc8d295332bdaf8f42010ae5f98aa46d1329a692b3dad`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:1946888eecd66b91618fb7d72586307879f92142a83d2f84d72f46f5c8a1e84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b5ef23c86249042fde863ab1bdd6f7993028c3ff3aed03c4abf2e0c54138a`

```dockerfile
```

-	Layers:
	-	`sha256:74d6354101a69d21a00a0cecffd02193b2e3627c0a13b454031455557a7f3176`  
		Last Modified: Tue, 18 Nov 2025 22:12:23 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71b6f477949b4d7f2c93d8566c67d23e4e91dbbef5f68bf83bc2f72db5b190b`  
		Last Modified: Tue, 18 Nov 2025 22:12:24 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:aaf0f6185419a50c74651448c1a5bf4606bd2d2ddb7b8749eed505d55bf8b8ea
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

### `traefik:3.6` - linux; amd64

```console
$ docker pull traefik@sha256:ec4fce4588f239530c79af7e2dd873877e51a5548cc51cfbf318ae6e1727e138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e55c25c9dc924eb86e34957cea11335f48f3eeb87c12b8472434db39a43f143`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 21:48:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 21:48:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 21:48:13 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 21:48:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fcf41ae4fe549fc66069c1d9a3dfc8c7684a19fae6345f38239a84543cb451`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 456.9 KB (456932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff51e48e8c41ee2aebd058d15b97b4f47b6722fac2a08e226f835df67d4418e2`  
		Last Modified: Tue, 18 Nov 2025 21:49:19 GMT  
		Size: 47.4 MB (47433025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e2292afa9f7b52254e57efeb2deac56f51163f1572a1da072bbecc4e1b757`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4261a87ee97389d6ecbdb5e8d8a673aa7ab3655675e2f1d1d84dd3825e26bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b750f1805931f0b564bfd7f3749094595eeefa65812c77aed1c1c9326a8d96c7`

```dockerfile
```

-	Layers:
	-	`sha256:dd4ab2e6afc636d1939980a8bf3d9cea3ddcd13a44c1d2295ba738ef261d09d7`  
		Last Modified: Tue, 18 Nov 2025 22:12:05 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24afbeef114a9fcc5c689c830f8392110a29eb89171b2436f0186680ce002e14`  
		Last Modified: Tue, 18 Nov 2025 22:12:06 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:561b6e0f7d5f408c12d49170ad858a17c8fae6f0b685bccc027abdbc34bf98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25de55986ee18f2435d5c74bf6032a3a2e15353a695c8f7a9859a5bbede5e41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:28:50 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78109e37152b41df02ee2c237f740f003151ef213dd9c81e925a61e13a562e8e`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 457.7 KB (457742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cda1c04505fd255242fdece0301c166e8cec8bf2ab4dd1ac4debf3cd00bdff`  
		Last Modified: Tue, 18 Nov 2025 19:29:15 GMT  
		Size: 43.0 MB (42954733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece82213e301e010af11f5ebf09d08ea08de287de016f8cc954c3781b03eddcd`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0009cf7a9ecccca8185f9089f56ac6cf92a7f3bcb3c43151132fef8c0e523439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb979678d6660d672ff7cb2a3a8f96887af931403b91c76d4f6b1342a169b49`

```dockerfile
```

-	Layers:
	-	`sha256:f937ea1ee9c88faa49302bc9ddc4cab7f1a4cda765d2fe7becd38622c625bf67`  
		Last Modified: Tue, 18 Nov 2025 22:12:09 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58ccae90050988e9890eedfb1c6548b82c1ca60e807d97517daaddb6312a557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9f1b556d725190bc03627caf6f7b39276b3aed3745b9c0701e408acbf0ea39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:25:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:25:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:25:43 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:25:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417edc5cf59f87d70cf22c79d067722d6949576117ec0bcff04e50d6a4edfab9`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594c719740f22165cd53b9aac15e8797c888a46b8036d0defd56bb322e1be2c`  
		Last Modified: Tue, 18 Nov 2025 19:26:44 GMT  
		Size: 43.1 MB (43148307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6369fe0dab57aea1446d2fc8db9da1e6d27db7b2847c04b4f90f4cd6d20ef21`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:29d930fed1539847060dfbc2bffe8beb811209e24903d0773c44de8a84ae446a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef50f53cba8be23e4bc4cc3aadc3d445801d4160a1931dbe8be09db5a661943f`

```dockerfile
```

-	Layers:
	-	`sha256:c15e382f6e16857c9e88493b9b05152c009ab9bcb9708326208db496e2692923`  
		Last Modified: Tue, 18 Nov 2025 22:12:12 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a64dd22de08febf3ec2ebeb77c873765b75b1b6561f00b63357b5c1266bb013`  
		Last Modified: Tue, 18 Nov 2025 22:12:13 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a690dd84bed67e8e18f8d4c04b90f73774e3895300207e88d4ebfef99dedd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45323965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff3c8eb0949ee6dfda7c4c8ce8a9058548e947d4be56670a9e1143f8b80b891`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 22:02:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 22:02:04 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 22:02:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7131cbb6f2ed0728075b7863f72b456c451d363f035bc26eb4dc639ff1ea91f`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 459.4 KB (459444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163ecef57ee3319b1b03d664f61a15b5798d00e5e693105671fdfca70b48572`  
		Last Modified: Tue, 18 Nov 2025 22:03:14 GMT  
		Size: 41.1 MB (41131911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e085ee6011d283be1359ca019b8b510565abcf3ba44bfceaea6351deca17429`  
		Last Modified: Tue, 18 Nov 2025 22:03:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:3be7a65febed98487068f4f3636c8b42574da05615fee85f690ccecc964a78f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806e17ee732263c18ab393c230c85c74af69797ff07837c6e0641265849c22`

```dockerfile
```

-	Layers:
	-	`sha256:f086e4046623395e3cb574d6480d4e05e3552ba71b387734b5f8f6c43500b78b`  
		Last Modified: Tue, 18 Nov 2025 22:12:17 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb34f7412305f709ba275808c9588d9a7a5e7cae6d9b1aa5d2f56928804c72d8`  
		Last Modified: Tue, 18 Nov 2025 22:12:18 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:dd5c5f868d64632d40e1fc02d154a6850871bd88b605ea430630aa7d2d70d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49696840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af8810d338f1bd1a4b4fb764de8b01c082104bd2f4f216724435a0d18961f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 20 Nov 2025 19:45:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:45:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Nov 2025 19:45:33 GMT
CMD ["traefik"]
# Thu, 20 Nov 2025 19:45:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:77490f998c3cacffe82e080079ee717eb224ae54ff7776969eb02d5e3083c297`  
		Last Modified: Thu, 20 Nov 2025 19:51:39 GMT  
		Size: 45.7 MB (45723955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f9fa6da824b71d504b2b5252daaa9d5aadf78e571c9f9d79aeff67f5907e6`  
		Last Modified: Thu, 20 Nov 2025 19:51:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:fc3215167bc91ea171842167fc09a79120e6f3d8d340a1e637804cdf56b71e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8091b4062673a8ea24b34c56fb441d17a6afb43e0dba564e3c8c16b9b0197`

```dockerfile
```

-	Layers:
	-	`sha256:92e1bb99aa3bbe7baa5d5f23f96ff12db288cb6426dc299879f820a396c7350c`  
		Last Modified: Thu, 20 Nov 2025 22:09:41 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c52c6da61f97cda07d7683b99b6ba1f2d1c8068ca37f64d0f288b2fc103fa5`  
		Last Modified: Thu, 20 Nov 2025 22:09:42 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:a1b3be8672939a4d2913ba3c9da9d86056337dae16b5a8f4fecfb429e436f8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088adf79d3c254dcb80a82265220f63d1f8fca26800fbeadc494b8be29f98de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:27:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:27:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:27:20 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:27:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ed3289785c33bee42da1326ef857e710b7e549418a49847e37717014d7961`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 457.9 KB (457907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372adc29fa3a207abdcada906a4729dc818037b9435d9fdaa2924029ec613d48`  
		Last Modified: Tue, 18 Nov 2025 19:28:24 GMT  
		Size: 45.6 MB (45580906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372305cc3de919e1c11bc8d295332bdaf8f42010ae5f98aa46d1329a692b3dad`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:1946888eecd66b91618fb7d72586307879f92142a83d2f84d72f46f5c8a1e84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b5ef23c86249042fde863ab1bdd6f7993028c3ff3aed03c4abf2e0c54138a`

```dockerfile
```

-	Layers:
	-	`sha256:74d6354101a69d21a00a0cecffd02193b2e3627c0a13b454031455557a7f3176`  
		Last Modified: Tue, 18 Nov 2025 22:12:23 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71b6f477949b4d7f2c93d8566c67d23e4e91dbbef5f68bf83bc2f72db5b190b`  
		Last Modified: Tue, 18 Nov 2025 22:12:24 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.2`

```console
$ docker pull traefik@sha256:aaf0f6185419a50c74651448c1a5bf4606bd2d2ddb7b8749eed505d55bf8b8ea
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

### `traefik:3.6.2` - linux; amd64

```console
$ docker pull traefik@sha256:ec4fce4588f239530c79af7e2dd873877e51a5548cc51cfbf318ae6e1727e138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e55c25c9dc924eb86e34957cea11335f48f3eeb87c12b8472434db39a43f143`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 21:48:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 21:48:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 21:48:13 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 21:48:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fcf41ae4fe549fc66069c1d9a3dfc8c7684a19fae6345f38239a84543cb451`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 456.9 KB (456932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff51e48e8c41ee2aebd058d15b97b4f47b6722fac2a08e226f835df67d4418e2`  
		Last Modified: Tue, 18 Nov 2025 21:49:19 GMT  
		Size: 47.4 MB (47433025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e2292afa9f7b52254e57efeb2deac56f51163f1572a1da072bbecc4e1b757`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:4261a87ee97389d6ecbdb5e8d8a673aa7ab3655675e2f1d1d84dd3825e26bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b750f1805931f0b564bfd7f3749094595eeefa65812c77aed1c1c9326a8d96c7`

```dockerfile
```

-	Layers:
	-	`sha256:dd4ab2e6afc636d1939980a8bf3d9cea3ddcd13a44c1d2295ba738ef261d09d7`  
		Last Modified: Tue, 18 Nov 2025 22:12:05 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24afbeef114a9fcc5c689c830f8392110a29eb89171b2436f0186680ce002e14`  
		Last Modified: Tue, 18 Nov 2025 22:12:06 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:561b6e0f7d5f408c12d49170ad858a17c8fae6f0b685bccc027abdbc34bf98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25de55986ee18f2435d5c74bf6032a3a2e15353a695c8f7a9859a5bbede5e41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:28:50 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78109e37152b41df02ee2c237f740f003151ef213dd9c81e925a61e13a562e8e`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 457.7 KB (457742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cda1c04505fd255242fdece0301c166e8cec8bf2ab4dd1ac4debf3cd00bdff`  
		Last Modified: Tue, 18 Nov 2025 19:29:15 GMT  
		Size: 43.0 MB (42954733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece82213e301e010af11f5ebf09d08ea08de287de016f8cc954c3781b03eddcd`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:0009cf7a9ecccca8185f9089f56ac6cf92a7f3bcb3c43151132fef8c0e523439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb979678d6660d672ff7cb2a3a8f96887af931403b91c76d4f6b1342a169b49`

```dockerfile
```

-	Layers:
	-	`sha256:f937ea1ee9c88faa49302bc9ddc4cab7f1a4cda765d2fe7becd38622c625bf67`  
		Last Modified: Tue, 18 Nov 2025 22:12:09 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58ccae90050988e9890eedfb1c6548b82c1ca60e807d97517daaddb6312a557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9f1b556d725190bc03627caf6f7b39276b3aed3745b9c0701e408acbf0ea39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:25:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:25:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:25:43 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:25:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417edc5cf59f87d70cf22c79d067722d6949576117ec0bcff04e50d6a4edfab9`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594c719740f22165cd53b9aac15e8797c888a46b8036d0defd56bb322e1be2c`  
		Last Modified: Tue, 18 Nov 2025 19:26:44 GMT  
		Size: 43.1 MB (43148307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6369fe0dab57aea1446d2fc8db9da1e6d27db7b2847c04b4f90f4cd6d20ef21`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:29d930fed1539847060dfbc2bffe8beb811209e24903d0773c44de8a84ae446a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef50f53cba8be23e4bc4cc3aadc3d445801d4160a1931dbe8be09db5a661943f`

```dockerfile
```

-	Layers:
	-	`sha256:c15e382f6e16857c9e88493b9b05152c009ab9bcb9708326208db496e2692923`  
		Last Modified: Tue, 18 Nov 2025 22:12:12 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a64dd22de08febf3ec2ebeb77c873765b75b1b6561f00b63357b5c1266bb013`  
		Last Modified: Tue, 18 Nov 2025 22:12:13 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.2` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a690dd84bed67e8e18f8d4c04b90f73774e3895300207e88d4ebfef99dedd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45323965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff3c8eb0949ee6dfda7c4c8ce8a9058548e947d4be56670a9e1143f8b80b891`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 22:02:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 22:02:04 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 22:02:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7131cbb6f2ed0728075b7863f72b456c451d363f035bc26eb4dc639ff1ea91f`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 459.4 KB (459444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163ecef57ee3319b1b03d664f61a15b5798d00e5e693105671fdfca70b48572`  
		Last Modified: Tue, 18 Nov 2025 22:03:14 GMT  
		Size: 41.1 MB (41131911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e085ee6011d283be1359ca019b8b510565abcf3ba44bfceaea6351deca17429`  
		Last Modified: Tue, 18 Nov 2025 22:03:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:3be7a65febed98487068f4f3636c8b42574da05615fee85f690ccecc964a78f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806e17ee732263c18ab393c230c85c74af69797ff07837c6e0641265849c22`

```dockerfile
```

-	Layers:
	-	`sha256:f086e4046623395e3cb574d6480d4e05e3552ba71b387734b5f8f6c43500b78b`  
		Last Modified: Tue, 18 Nov 2025 22:12:17 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb34f7412305f709ba275808c9588d9a7a5e7cae6d9b1aa5d2f56928804c72d8`  
		Last Modified: Tue, 18 Nov 2025 22:12:18 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.2` - linux; riscv64

```console
$ docker pull traefik@sha256:dd5c5f868d64632d40e1fc02d154a6850871bd88b605ea430630aa7d2d70d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49696840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af8810d338f1bd1a4b4fb764de8b01c082104bd2f4f216724435a0d18961f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 20 Nov 2025 19:45:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:45:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Nov 2025 19:45:33 GMT
CMD ["traefik"]
# Thu, 20 Nov 2025 19:45:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:77490f998c3cacffe82e080079ee717eb224ae54ff7776969eb02d5e3083c297`  
		Last Modified: Thu, 20 Nov 2025 19:51:39 GMT  
		Size: 45.7 MB (45723955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f9fa6da824b71d504b2b5252daaa9d5aadf78e571c9f9d79aeff67f5907e6`  
		Last Modified: Thu, 20 Nov 2025 19:51:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:fc3215167bc91ea171842167fc09a79120e6f3d8d340a1e637804cdf56b71e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8091b4062673a8ea24b34c56fb441d17a6afb43e0dba564e3c8c16b9b0197`

```dockerfile
```

-	Layers:
	-	`sha256:92e1bb99aa3bbe7baa5d5f23f96ff12db288cb6426dc299879f820a396c7350c`  
		Last Modified: Thu, 20 Nov 2025 22:09:41 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c52c6da61f97cda07d7683b99b6ba1f2d1c8068ca37f64d0f288b2fc103fa5`  
		Last Modified: Thu, 20 Nov 2025 22:09:42 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.2` - linux; s390x

```console
$ docker pull traefik@sha256:a1b3be8672939a4d2913ba3c9da9d86056337dae16b5a8f4fecfb429e436f8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088adf79d3c254dcb80a82265220f63d1f8fca26800fbeadc494b8be29f98de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:27:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:27:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:27:20 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:27:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ed3289785c33bee42da1326ef857e710b7e549418a49847e37717014d7961`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 457.9 KB (457907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372adc29fa3a207abdcada906a4729dc818037b9435d9fdaa2924029ec613d48`  
		Last Modified: Tue, 18 Nov 2025 19:28:24 GMT  
		Size: 45.6 MB (45580906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372305cc3de919e1c11bc8d295332bdaf8f42010ae5f98aa46d1329a692b3dad`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:1946888eecd66b91618fb7d72586307879f92142a83d2f84d72f46f5c8a1e84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b5ef23c86249042fde863ab1bdd6f7993028c3ff3aed03c4abf2e0c54138a`

```dockerfile
```

-	Layers:
	-	`sha256:74d6354101a69d21a00a0cecffd02193b2e3627c0a13b454031455557a7f3176`  
		Last Modified: Tue, 18 Nov 2025 22:12:23 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71b6f477949b4d7f2c93d8566c67d23e4e91dbbef5f68bf83bc2f72db5b190b`  
		Last Modified: Tue, 18 Nov 2025 22:12:24 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6.2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6.2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:aaf0f6185419a50c74651448c1a5bf4606bd2d2ddb7b8749eed505d55bf8b8ea
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

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:ec4fce4588f239530c79af7e2dd873877e51a5548cc51cfbf318ae6e1727e138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e55c25c9dc924eb86e34957cea11335f48f3eeb87c12b8472434db39a43f143`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 21:48:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 21:48:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 21:48:13 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 21:48:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fcf41ae4fe549fc66069c1d9a3dfc8c7684a19fae6345f38239a84543cb451`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 456.9 KB (456932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff51e48e8c41ee2aebd058d15b97b4f47b6722fac2a08e226f835df67d4418e2`  
		Last Modified: Tue, 18 Nov 2025 21:49:19 GMT  
		Size: 47.4 MB (47433025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e2292afa9f7b52254e57efeb2deac56f51163f1572a1da072bbecc4e1b757`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:4261a87ee97389d6ecbdb5e8d8a673aa7ab3655675e2f1d1d84dd3825e26bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b750f1805931f0b564bfd7f3749094595eeefa65812c77aed1c1c9326a8d96c7`

```dockerfile
```

-	Layers:
	-	`sha256:dd4ab2e6afc636d1939980a8bf3d9cea3ddcd13a44c1d2295ba738ef261d09d7`  
		Last Modified: Tue, 18 Nov 2025 22:12:05 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24afbeef114a9fcc5c689c830f8392110a29eb89171b2436f0186680ce002e14`  
		Last Modified: Tue, 18 Nov 2025 22:12:06 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:561b6e0f7d5f408c12d49170ad858a17c8fae6f0b685bccc027abdbc34bf98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25de55986ee18f2435d5c74bf6032a3a2e15353a695c8f7a9859a5bbede5e41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:28:50 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78109e37152b41df02ee2c237f740f003151ef213dd9c81e925a61e13a562e8e`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 457.7 KB (457742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cda1c04505fd255242fdece0301c166e8cec8bf2ab4dd1ac4debf3cd00bdff`  
		Last Modified: Tue, 18 Nov 2025 19:29:15 GMT  
		Size: 43.0 MB (42954733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece82213e301e010af11f5ebf09d08ea08de287de016f8cc954c3781b03eddcd`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:0009cf7a9ecccca8185f9089f56ac6cf92a7f3bcb3c43151132fef8c0e523439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb979678d6660d672ff7cb2a3a8f96887af931403b91c76d4f6b1342a169b49`

```dockerfile
```

-	Layers:
	-	`sha256:f937ea1ee9c88faa49302bc9ddc4cab7f1a4cda765d2fe7becd38622c625bf67`  
		Last Modified: Tue, 18 Nov 2025 22:12:09 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58ccae90050988e9890eedfb1c6548b82c1ca60e807d97517daaddb6312a557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9f1b556d725190bc03627caf6f7b39276b3aed3745b9c0701e408acbf0ea39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:25:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:25:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:25:43 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:25:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417edc5cf59f87d70cf22c79d067722d6949576117ec0bcff04e50d6a4edfab9`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594c719740f22165cd53b9aac15e8797c888a46b8036d0defd56bb322e1be2c`  
		Last Modified: Tue, 18 Nov 2025 19:26:44 GMT  
		Size: 43.1 MB (43148307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6369fe0dab57aea1446d2fc8db9da1e6d27db7b2847c04b4f90f4cd6d20ef21`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:29d930fed1539847060dfbc2bffe8beb811209e24903d0773c44de8a84ae446a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef50f53cba8be23e4bc4cc3aadc3d445801d4160a1931dbe8be09db5a661943f`

```dockerfile
```

-	Layers:
	-	`sha256:c15e382f6e16857c9e88493b9b05152c009ab9bcb9708326208db496e2692923`  
		Last Modified: Tue, 18 Nov 2025 22:12:12 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a64dd22de08febf3ec2ebeb77c873765b75b1b6561f00b63357b5c1266bb013`  
		Last Modified: Tue, 18 Nov 2025 22:12:13 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a690dd84bed67e8e18f8d4c04b90f73774e3895300207e88d4ebfef99dedd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45323965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff3c8eb0949ee6dfda7c4c8ce8a9058548e947d4be56670a9e1143f8b80b891`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 22:02:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 22:02:04 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 22:02:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7131cbb6f2ed0728075b7863f72b456c451d363f035bc26eb4dc639ff1ea91f`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 459.4 KB (459444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163ecef57ee3319b1b03d664f61a15b5798d00e5e693105671fdfca70b48572`  
		Last Modified: Tue, 18 Nov 2025 22:03:14 GMT  
		Size: 41.1 MB (41131911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e085ee6011d283be1359ca019b8b510565abcf3ba44bfceaea6351deca17429`  
		Last Modified: Tue, 18 Nov 2025 22:03:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:3be7a65febed98487068f4f3636c8b42574da05615fee85f690ccecc964a78f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806e17ee732263c18ab393c230c85c74af69797ff07837c6e0641265849c22`

```dockerfile
```

-	Layers:
	-	`sha256:f086e4046623395e3cb574d6480d4e05e3552ba71b387734b5f8f6c43500b78b`  
		Last Modified: Tue, 18 Nov 2025 22:12:17 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb34f7412305f709ba275808c9588d9a7a5e7cae6d9b1aa5d2f56928804c72d8`  
		Last Modified: Tue, 18 Nov 2025 22:12:18 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:dd5c5f868d64632d40e1fc02d154a6850871bd88b605ea430630aa7d2d70d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49696840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af8810d338f1bd1a4b4fb764de8b01c082104bd2f4f216724435a0d18961f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 20 Nov 2025 19:45:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:45:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Nov 2025 19:45:33 GMT
CMD ["traefik"]
# Thu, 20 Nov 2025 19:45:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:77490f998c3cacffe82e080079ee717eb224ae54ff7776969eb02d5e3083c297`  
		Last Modified: Thu, 20 Nov 2025 19:51:39 GMT  
		Size: 45.7 MB (45723955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f9fa6da824b71d504b2b5252daaa9d5aadf78e571c9f9d79aeff67f5907e6`  
		Last Modified: Thu, 20 Nov 2025 19:51:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:fc3215167bc91ea171842167fc09a79120e6f3d8d340a1e637804cdf56b71e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8091b4062673a8ea24b34c56fb441d17a6afb43e0dba564e3c8c16b9b0197`

```dockerfile
```

-	Layers:
	-	`sha256:92e1bb99aa3bbe7baa5d5f23f96ff12db288cb6426dc299879f820a396c7350c`  
		Last Modified: Thu, 20 Nov 2025 22:09:41 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c52c6da61f97cda07d7683b99b6ba1f2d1c8068ca37f64d0f288b2fc103fa5`  
		Last Modified: Thu, 20 Nov 2025 22:09:42 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:a1b3be8672939a4d2913ba3c9da9d86056337dae16b5a8f4fecfb429e436f8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088adf79d3c254dcb80a82265220f63d1f8fca26800fbeadc494b8be29f98de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:27:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:27:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:27:20 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:27:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ed3289785c33bee42da1326ef857e710b7e549418a49847e37717014d7961`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 457.9 KB (457907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372adc29fa3a207abdcada906a4729dc818037b9435d9fdaa2924029ec613d48`  
		Last Modified: Tue, 18 Nov 2025 19:28:24 GMT  
		Size: 45.6 MB (45580906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372305cc3de919e1c11bc8d295332bdaf8f42010ae5f98aa46d1329a692b3dad`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:1946888eecd66b91618fb7d72586307879f92142a83d2f84d72f46f5c8a1e84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b5ef23c86249042fde863ab1bdd6f7993028c3ff3aed03c4abf2e0c54138a`

```dockerfile
```

-	Layers:
	-	`sha256:74d6354101a69d21a00a0cecffd02193b2e3627c0a13b454031455557a7f3176`  
		Last Modified: Tue, 18 Nov 2025 22:12:23 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71b6f477949b4d7f2c93d8566c67d23e4e91dbbef5f68bf83bc2f72db5b190b`  
		Last Modified: Tue, 18 Nov 2025 22:12:24 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:b83fc239b8bdb5d0ac94c097d92d9a85ac82ea82d535fdd44ce85c29c683078e
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

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:ac8c824bff35528ab36cb5245a8e488b419555e3b1b5672f4a2f4dc5b8a81da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50978940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce622bd2eac1031b22b2a724e52d8f615eca7eea0679e112a09235f4b17c7fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:05 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:08 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6f9c66e581dc9a0a73c65a91c09c8c25658e76ca0c42313eb493037f79bb81`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 456.9 KB (456939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f65172c40aa9ef7f8e79c49e6bf6a4ce5a81e3d6ed6c068ecaf903c644eba3e`  
		Last Modified: Thu, 04 Dec 2025 19:24:12 GMT  
		Size: 46.7 MB (46719180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d007db28390cd93183e7930d1e72ebe8ea62d5c2047982518002be0af321b66`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:b5c4cf6445eabd54dbbc99c02744ce44c18c069957f2e6cda738fd06736fa04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7997e68f2d9ee4a7810bb994211873a40085ba0376fd0434fc8f97efeabfde35`

```dockerfile
```

-	Layers:
	-	`sha256:9fdea8c65335538554420bb2f73ee610e77b35a8d99a41f66500f065275f7eef`  
		Last Modified: Thu, 04 Dec 2025 22:09:38 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618029352157666e0f7ada57d0b9772e84b7d8813d76014b9e425ac7d906c921`  
		Last Modified: Thu, 04 Dec 2025 22:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:00cacb5e3b75272d0963554604f16ee2f93e2caf8d774fb308ee3a2682b3fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46746429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b47a4e1eed2a3590b56e42a9bb20a814f235d05069e5aa8da45d25abfdaeb4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:10 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df693b807706002f19e426395418816460fb1a346f714d70e1c2c8afe374fd6`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 457.7 KB (457743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ef2971fe1a98ac7085996aa7023b6ccebf3897ef0483117b06b73d62b21aea`  
		Last Modified: Thu, 04 Dec 2025 19:23:35 GMT  
		Size: 42.8 MB (42784237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03516caee00078a85faefe1fd7d687c9cf8683b6dcfd8b57471545e1a9539870`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:aed9768db2bd35f301e0230caa1d2ffb2251a131320be645d6974c55e86618c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951f2a74272fc9c6c92170e2f27e242079597091a9506042db0401721e2db134`

```dockerfile
```

-	Layers:
	-	`sha256:1de50cb82d5378e594bac4e56dd225fa1d5f34bec27ee27fd9551913bc11fe3c`  
		Last Modified: Thu, 04 Dec 2025 22:09:42 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e578a9c8a06c07bb518641ab52b497b2fefce64c57a13530ae9731e0f35f6519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47214110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322725a91b8aa0f09e823c8879e728fab22810cdbec06bb669998e14e2f20e3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:53 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f4dc86542d7de98a768f4c0aee00ee4babe24157a4398e0e57604d2128efe`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923727f8d2ecf48712183a704dc223b5f52c03513cacfd1154f1ec815b66e8c`  
		Last Modified: Thu, 04 Dec 2025 19:21:01 GMT  
		Size: 42.6 MB (42616644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cb010135a022802cdc49ad86685907a4b7fec67e04d2ef6c5fa3b3dfbd504c`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:9a47c8fe962fefb1ab75eca20fce3174ae6107399c354c08787946583e9a53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82df1b830714c487e63a0e3cc2de51b9ae86fb219c7ede49b7055db217ff0f1`

```dockerfile
```

-	Layers:
	-	`sha256:d92cd312fa7dfcb46d339b39a908f09c05c04111ce94b03096f121b2b2ba238f`  
		Last Modified: Thu, 04 Dec 2025 22:09:46 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e6e0053f14ec312f9f3a94120e5153aa376985a6462fe8cb55509fc1495a7`  
		Last Modified: Thu, 04 Dec 2025 22:09:47 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:705d054c3866fdb6718a38957a67bcf193b38faa9ff5aaf8bc1da18af25bc516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45146924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de90c8d7f80a5aad7df4da00b1051b98930c54c8ababf669deb6d0d2d04a4f17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:34 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d260e1c1ba83417069742e33ef3dca0b56b4fb4a494c1c02755de510ec75e4a`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 459.4 KB (459433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e72a719bd9cd6a8f63be96d8d4c6575cad6c06a10e9ffaf1ecf0b582ff2542e`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 41.0 MB (40954880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a71f904fae4ec8c94264d8912ca717e59c7ec5031afd18f2f3f7bffdd5b1fe`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:3a46754ca761744e0f8883b9bfcd1684e663ac55b467b3a3b6923f51ff444d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d326368736c8a7420af0299583f8308601f8c1058845300561361b987ee13fad`

```dockerfile
```

-	Layers:
	-	`sha256:c4385ecde488f23523e5f1a690f599ee5de4f852330ed63b9cb8f58e461d00a9`  
		Last Modified: Thu, 04 Dec 2025 22:09:50 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b23d28dedd26705c13315cf1cee4006037cd5639347b33b5a7c069bd7e5b9d8`  
		Last Modified: Thu, 04 Dec 2025 22:09:51 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:6ce21e040bd4e2552427746ac5d0436d21f5f70bb0eadd8cf84a6e0fa0f6c8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49360723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8cc7abc990629392d3d289ac957e498bae15a9e836b0eade383931b77229b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:39 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d51ac067c25bf77fc5f6d25393d578c35080ea1d6d82d5c52dc00d5152699a6`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 457.9 KB (457913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36796f5fe181a6d2eb8fe90a5ca86fe909a756cc7cd57ccfb29dc3dc22620391`  
		Last Modified: Thu, 04 Dec 2025 19:21:04 GMT  
		Size: 45.3 MB (45253196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415c08db574d0b987b7070e71f49cbb2b58fa19861291d64c90e0dccde610b4`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:821663597494279db90cb3041862160bec3dcfe15162cb71c8b6f6fc3508aedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c48cbe3f7f2e42ad7e85328cc0e03b561857f85c793e37e796b4dc15269f8cd`

```dockerfile
```

-	Layers:
	-	`sha256:c41f76c95136d09bef36ea43a6eaf5869d09c21fc9edb28948b6c0e690332bc3`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61aaab597727c9c099570e7d5b30d607529858bc616081953993f6d88744a2a`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:138d7a87225e5c01a2b5db9301d7c6aab20073cd7798753fd81fe1e858cec83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2a60f1cc89f202977266b2a1651a9650ba802f4c066ca5931e59f3d404e1a042
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173864697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bece513a73e007d0e19209b413a84a7322d006eeddf299964b71efbec9b7e9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 04 Dec 2025 19:45:19 GMT
RUN cmd /S /C #(nop) COPY file:c5fd63825ca3af125acc7c0933cfb57a0080ecc168578d5b8882a0a05ef47bf4 in \ 
# Thu, 04 Dec 2025 19:45:21 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 04 Dec 2025 19:45:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:45:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473330b82e6af6d0613f521c11967f24228b1f1db3525d5ba2397c60eb96a81`  
		Last Modified: Thu, 04 Dec 2025 19:46:15 GMT  
		Size: 47.5 MB (47512441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9567c173a49fe4d5f69532267d8341eb54a40a659c6097e17856f13db5c3781e`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2dbeb0f2c54c414b81ad494b02482f528225d6ff22f9d7df5e139d19bb13bf`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c9666ee73f9d459e7e07b81222cd91048ae7e032a8e09a8888641e8ad861c7`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:dcec3000efc0d552358fd44f95644e5e908de7d472a63df0edb574de81517645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2988f00eaf0aeedcab04b601936c36fb3f454008611b35134e846a5f4e26b158
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818121188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31715b9a396950e980e3b2579d073169b112b7a318a9ac5c170d1f0e3edc930b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 04 Dec 2025 19:23:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Dec 2025 19:25:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 04 Dec 2025 19:25:38 GMT
EXPOSE 80
# Thu, 04 Dec 2025 19:25:40 GMT
ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bf6b095296831cd4d5f34d58fa0959fd7ef42e2dc9efd551c55d16e533b161`  
		Last Modified: Thu, 04 Dec 2025 19:38:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bac6613489c4597256f38308be766d6b69566e37eae1ec90fd75668f5ddd323`  
		Last Modified: Thu, 04 Dec 2025 19:38:29 GMT  
		Size: 48.2 MB (48154462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4a3d7b533059c5b4c90f6ad2b5cf3cf561ffd5341fa82b23cb2200e3604e15`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f85135e09953edf14105875b914705d2e9163f065e361f6df0548ce9a9ce7`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de324d8f25e723e0020dda62e746d4c7d464d758c0e6ecf94b2b5b741d0b25d0`  
		Last Modified: Thu, 04 Dec 2025 19:38:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:aaf0f6185419a50c74651448c1a5bf4606bd2d2ddb7b8749eed505d55bf8b8ea
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
$ docker pull traefik@sha256:ec4fce4588f239530c79af7e2dd873877e51a5548cc51cfbf318ae6e1727e138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e55c25c9dc924eb86e34957cea11335f48f3eeb87c12b8472434db39a43f143`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 21:48:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 21:48:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 21:48:13 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 21:48:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fcf41ae4fe549fc66069c1d9a3dfc8c7684a19fae6345f38239a84543cb451`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 456.9 KB (456932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff51e48e8c41ee2aebd058d15b97b4f47b6722fac2a08e226f835df67d4418e2`  
		Last Modified: Tue, 18 Nov 2025 21:49:19 GMT  
		Size: 47.4 MB (47433025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e2292afa9f7b52254e57efeb2deac56f51163f1572a1da072bbecc4e1b757`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:4261a87ee97389d6ecbdb5e8d8a673aa7ab3655675e2f1d1d84dd3825e26bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b750f1805931f0b564bfd7f3749094595eeefa65812c77aed1c1c9326a8d96c7`

```dockerfile
```

-	Layers:
	-	`sha256:dd4ab2e6afc636d1939980a8bf3d9cea3ddcd13a44c1d2295ba738ef261d09d7`  
		Last Modified: Tue, 18 Nov 2025 22:12:05 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24afbeef114a9fcc5c689c830f8392110a29eb89171b2436f0186680ce002e14`  
		Last Modified: Tue, 18 Nov 2025 22:12:06 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:561b6e0f7d5f408c12d49170ad858a17c8fae6f0b685bccc027abdbc34bf98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25de55986ee18f2435d5c74bf6032a3a2e15353a695c8f7a9859a5bbede5e41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:28:50 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78109e37152b41df02ee2c237f740f003151ef213dd9c81e925a61e13a562e8e`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 457.7 KB (457742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cda1c04505fd255242fdece0301c166e8cec8bf2ab4dd1ac4debf3cd00bdff`  
		Last Modified: Tue, 18 Nov 2025 19:29:15 GMT  
		Size: 43.0 MB (42954733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece82213e301e010af11f5ebf09d08ea08de287de016f8cc954c3781b03eddcd`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:0009cf7a9ecccca8185f9089f56ac6cf92a7f3bcb3c43151132fef8c0e523439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb979678d6660d672ff7cb2a3a8f96887af931403b91c76d4f6b1342a169b49`

```dockerfile
```

-	Layers:
	-	`sha256:f937ea1ee9c88faa49302bc9ddc4cab7f1a4cda765d2fe7becd38622c625bf67`  
		Last Modified: Tue, 18 Nov 2025 22:12:09 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58ccae90050988e9890eedfb1c6548b82c1ca60e807d97517daaddb6312a557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9f1b556d725190bc03627caf6f7b39276b3aed3745b9c0701e408acbf0ea39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:25:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:25:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:25:43 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:25:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417edc5cf59f87d70cf22c79d067722d6949576117ec0bcff04e50d6a4edfab9`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594c719740f22165cd53b9aac15e8797c888a46b8036d0defd56bb322e1be2c`  
		Last Modified: Tue, 18 Nov 2025 19:26:44 GMT  
		Size: 43.1 MB (43148307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6369fe0dab57aea1446d2fc8db9da1e6d27db7b2847c04b4f90f4cd6d20ef21`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:29d930fed1539847060dfbc2bffe8beb811209e24903d0773c44de8a84ae446a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef50f53cba8be23e4bc4cc3aadc3d445801d4160a1931dbe8be09db5a661943f`

```dockerfile
```

-	Layers:
	-	`sha256:c15e382f6e16857c9e88493b9b05152c009ab9bcb9708326208db496e2692923`  
		Last Modified: Tue, 18 Nov 2025 22:12:12 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a64dd22de08febf3ec2ebeb77c873765b75b1b6561f00b63357b5c1266bb013`  
		Last Modified: Tue, 18 Nov 2025 22:12:13 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a690dd84bed67e8e18f8d4c04b90f73774e3895300207e88d4ebfef99dedd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45323965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff3c8eb0949ee6dfda7c4c8ce8a9058548e947d4be56670a9e1143f8b80b891`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 22:02:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 22:02:04 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 22:02:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7131cbb6f2ed0728075b7863f72b456c451d363f035bc26eb4dc639ff1ea91f`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 459.4 KB (459444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163ecef57ee3319b1b03d664f61a15b5798d00e5e693105671fdfca70b48572`  
		Last Modified: Tue, 18 Nov 2025 22:03:14 GMT  
		Size: 41.1 MB (41131911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e085ee6011d283be1359ca019b8b510565abcf3ba44bfceaea6351deca17429`  
		Last Modified: Tue, 18 Nov 2025 22:03:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:3be7a65febed98487068f4f3636c8b42574da05615fee85f690ccecc964a78f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806e17ee732263c18ab393c230c85c74af69797ff07837c6e0641265849c22`

```dockerfile
```

-	Layers:
	-	`sha256:f086e4046623395e3cb574d6480d4e05e3552ba71b387734b5f8f6c43500b78b`  
		Last Modified: Tue, 18 Nov 2025 22:12:17 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb34f7412305f709ba275808c9588d9a7a5e7cae6d9b1aa5d2f56928804c72d8`  
		Last Modified: Tue, 18 Nov 2025 22:12:18 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:dd5c5f868d64632d40e1fc02d154a6850871bd88b605ea430630aa7d2d70d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49696840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af8810d338f1bd1a4b4fb764de8b01c082104bd2f4f216724435a0d18961f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 20 Nov 2025 19:45:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:45:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Nov 2025 19:45:33 GMT
CMD ["traefik"]
# Thu, 20 Nov 2025 19:45:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:77490f998c3cacffe82e080079ee717eb224ae54ff7776969eb02d5e3083c297`  
		Last Modified: Thu, 20 Nov 2025 19:51:39 GMT  
		Size: 45.7 MB (45723955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f9fa6da824b71d504b2b5252daaa9d5aadf78e571c9f9d79aeff67f5907e6`  
		Last Modified: Thu, 20 Nov 2025 19:51:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:fc3215167bc91ea171842167fc09a79120e6f3d8d340a1e637804cdf56b71e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8091b4062673a8ea24b34c56fb441d17a6afb43e0dba564e3c8c16b9b0197`

```dockerfile
```

-	Layers:
	-	`sha256:92e1bb99aa3bbe7baa5d5f23f96ff12db288cb6426dc299879f820a396c7350c`  
		Last Modified: Thu, 20 Nov 2025 22:09:41 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c52c6da61f97cda07d7683b99b6ba1f2d1c8068ca37f64d0f288b2fc103fa5`  
		Last Modified: Thu, 20 Nov 2025 22:09:42 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:a1b3be8672939a4d2913ba3c9da9d86056337dae16b5a8f4fecfb429e436f8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088adf79d3c254dcb80a82265220f63d1f8fca26800fbeadc494b8be29f98de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:27:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:27:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:27:20 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:27:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ed3289785c33bee42da1326ef857e710b7e549418a49847e37717014d7961`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 457.9 KB (457907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372adc29fa3a207abdcada906a4729dc818037b9435d9fdaa2924029ec613d48`  
		Last Modified: Tue, 18 Nov 2025 19:28:24 GMT  
		Size: 45.6 MB (45580906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372305cc3de919e1c11bc8d295332bdaf8f42010ae5f98aa46d1329a692b3dad`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:1946888eecd66b91618fb7d72586307879f92142a83d2f84d72f46f5c8a1e84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b5ef23c86249042fde863ab1bdd6f7993028c3ff3aed03c4abf2e0c54138a`

```dockerfile
```

-	Layers:
	-	`sha256:74d6354101a69d21a00a0cecffd02193b2e3627c0a13b454031455557a7f3176`  
		Last Modified: Tue, 18 Nov 2025 22:12:23 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71b6f477949b4d7f2c93d8566c67d23e4e91dbbef5f68bf83bc2f72db5b190b`  
		Last Modified: Tue, 18 Nov 2025 22:12:24 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:b83fc239b8bdb5d0ac94c097d92d9a85ac82ea82d535fdd44ce85c29c683078e
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

### `traefik:v2` - linux; amd64

```console
$ docker pull traefik@sha256:ac8c824bff35528ab36cb5245a8e488b419555e3b1b5672f4a2f4dc5b8a81da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50978940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce622bd2eac1031b22b2a724e52d8f615eca7eea0679e112a09235f4b17c7fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:05 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:08 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6f9c66e581dc9a0a73c65a91c09c8c25658e76ca0c42313eb493037f79bb81`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 456.9 KB (456939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f65172c40aa9ef7f8e79c49e6bf6a4ce5a81e3d6ed6c068ecaf903c644eba3e`  
		Last Modified: Thu, 04 Dec 2025 19:24:12 GMT  
		Size: 46.7 MB (46719180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d007db28390cd93183e7930d1e72ebe8ea62d5c2047982518002be0af321b66`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:b5c4cf6445eabd54dbbc99c02744ce44c18c069957f2e6cda738fd06736fa04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7997e68f2d9ee4a7810bb994211873a40085ba0376fd0434fc8f97efeabfde35`

```dockerfile
```

-	Layers:
	-	`sha256:9fdea8c65335538554420bb2f73ee610e77b35a8d99a41f66500f065275f7eef`  
		Last Modified: Thu, 04 Dec 2025 22:09:38 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618029352157666e0f7ada57d0b9772e84b7d8813d76014b9e425ac7d906c921`  
		Last Modified: Thu, 04 Dec 2025 22:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:00cacb5e3b75272d0963554604f16ee2f93e2caf8d774fb308ee3a2682b3fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46746429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b47a4e1eed2a3590b56e42a9bb20a814f235d05069e5aa8da45d25abfdaeb4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:10 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df693b807706002f19e426395418816460fb1a346f714d70e1c2c8afe374fd6`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 457.7 KB (457743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ef2971fe1a98ac7085996aa7023b6ccebf3897ef0483117b06b73d62b21aea`  
		Last Modified: Thu, 04 Dec 2025 19:23:35 GMT  
		Size: 42.8 MB (42784237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03516caee00078a85faefe1fd7d687c9cf8683b6dcfd8b57471545e1a9539870`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:aed9768db2bd35f301e0230caa1d2ffb2251a131320be645d6974c55e86618c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951f2a74272fc9c6c92170e2f27e242079597091a9506042db0401721e2db134`

```dockerfile
```

-	Layers:
	-	`sha256:1de50cb82d5378e594bac4e56dd225fa1d5f34bec27ee27fd9551913bc11fe3c`  
		Last Modified: Thu, 04 Dec 2025 22:09:42 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e578a9c8a06c07bb518641ab52b497b2fefce64c57a13530ae9731e0f35f6519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47214110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322725a91b8aa0f09e823c8879e728fab22810cdbec06bb669998e14e2f20e3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:53 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f4dc86542d7de98a768f4c0aee00ee4babe24157a4398e0e57604d2128efe`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923727f8d2ecf48712183a704dc223b5f52c03513cacfd1154f1ec815b66e8c`  
		Last Modified: Thu, 04 Dec 2025 19:21:01 GMT  
		Size: 42.6 MB (42616644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cb010135a022802cdc49ad86685907a4b7fec67e04d2ef6c5fa3b3dfbd504c`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:9a47c8fe962fefb1ab75eca20fce3174ae6107399c354c08787946583e9a53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82df1b830714c487e63a0e3cc2de51b9ae86fb219c7ede49b7055db217ff0f1`

```dockerfile
```

-	Layers:
	-	`sha256:d92cd312fa7dfcb46d339b39a908f09c05c04111ce94b03096f121b2b2ba238f`  
		Last Modified: Thu, 04 Dec 2025 22:09:46 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e6e0053f14ec312f9f3a94120e5153aa376985a6462fe8cb55509fc1495a7`  
		Last Modified: Thu, 04 Dec 2025 22:09:47 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:705d054c3866fdb6718a38957a67bcf193b38faa9ff5aaf8bc1da18af25bc516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45146924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de90c8d7f80a5aad7df4da00b1051b98930c54c8ababf669deb6d0d2d04a4f17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:34 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d260e1c1ba83417069742e33ef3dca0b56b4fb4a494c1c02755de510ec75e4a`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 459.4 KB (459433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e72a719bd9cd6a8f63be96d8d4c6575cad6c06a10e9ffaf1ecf0b582ff2542e`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 41.0 MB (40954880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a71f904fae4ec8c94264d8912ca717e59c7ec5031afd18f2f3f7bffdd5b1fe`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:3a46754ca761744e0f8883b9bfcd1684e663ac55b467b3a3b6923f51ff444d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d326368736c8a7420af0299583f8308601f8c1058845300561361b987ee13fad`

```dockerfile
```

-	Layers:
	-	`sha256:c4385ecde488f23523e5f1a690f599ee5de4f852330ed63b9cb8f58e461d00a9`  
		Last Modified: Thu, 04 Dec 2025 22:09:50 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b23d28dedd26705c13315cf1cee4006037cd5639347b33b5a7c069bd7e5b9d8`  
		Last Modified: Thu, 04 Dec 2025 22:09:51 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:6ce21e040bd4e2552427746ac5d0436d21f5f70bb0eadd8cf84a6e0fa0f6c8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49360723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8cc7abc990629392d3d289ac957e498bae15a9e836b0eade383931b77229b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:39 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d51ac067c25bf77fc5f6d25393d578c35080ea1d6d82d5c52dc00d5152699a6`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 457.9 KB (457913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36796f5fe181a6d2eb8fe90a5ca86fe909a756cc7cd57ccfb29dc3dc22620391`  
		Last Modified: Thu, 04 Dec 2025 19:21:04 GMT  
		Size: 45.3 MB (45253196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415c08db574d0b987b7070e71f49cbb2b58fa19861291d64c90e0dccde610b4`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:821663597494279db90cb3041862160bec3dcfe15162cb71c8b6f6fc3508aedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c48cbe3f7f2e42ad7e85328cc0e03b561857f85c793e37e796b4dc15269f8cd`

```dockerfile
```

-	Layers:
	-	`sha256:c41f76c95136d09bef36ea43a6eaf5869d09c21fc9edb28948b6c0e690332bc3`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61aaab597727c9c099570e7d5b30d607529858bc616081953993f6d88744a2a`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:138d7a87225e5c01a2b5db9301d7c6aab20073cd7798753fd81fe1e858cec83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2a60f1cc89f202977266b2a1651a9650ba802f4c066ca5931e59f3d404e1a042
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173864697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bece513a73e007d0e19209b413a84a7322d006eeddf299964b71efbec9b7e9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 04 Dec 2025 19:45:19 GMT
RUN cmd /S /C #(nop) COPY file:c5fd63825ca3af125acc7c0933cfb57a0080ecc168578d5b8882a0a05ef47bf4 in \ 
# Thu, 04 Dec 2025 19:45:21 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 04 Dec 2025 19:45:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:45:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473330b82e6af6d0613f521c11967f24228b1f1db3525d5ba2397c60eb96a81`  
		Last Modified: Thu, 04 Dec 2025 19:46:15 GMT  
		Size: 47.5 MB (47512441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9567c173a49fe4d5f69532267d8341eb54a40a659c6097e17856f13db5c3781e`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2dbeb0f2c54c414b81ad494b02482f528225d6ff22f9d7df5e139d19bb13bf`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c9666ee73f9d459e7e07b81222cd91048ae7e032a8e09a8888641e8ad861c7`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:dcec3000efc0d552358fd44f95644e5e908de7d472a63df0edb574de81517645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2988f00eaf0aeedcab04b601936c36fb3f454008611b35134e846a5f4e26b158
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818121188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31715b9a396950e980e3b2579d073169b112b7a318a9ac5c170d1f0e3edc930b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 04 Dec 2025 19:23:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Dec 2025 19:25:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 04 Dec 2025 19:25:38 GMT
EXPOSE 80
# Thu, 04 Dec 2025 19:25:40 GMT
ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bf6b095296831cd4d5f34d58fa0959fd7ef42e2dc9efd551c55d16e533b161`  
		Last Modified: Thu, 04 Dec 2025 19:38:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bac6613489c4597256f38308be766d6b69566e37eae1ec90fd75668f5ddd323`  
		Last Modified: Thu, 04 Dec 2025 19:38:29 GMT  
		Size: 48.2 MB (48154462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4a3d7b533059c5b4c90f6ad2b5cf3cf561ffd5341fa82b23cb2200e3604e15`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f85135e09953edf14105875b914705d2e9163f065e361f6df0548ce9a9ce7`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de324d8f25e723e0020dda62e746d4c7d464d758c0e6ecf94b2b5b741d0b25d0`  
		Last Modified: Thu, 04 Dec 2025 19:38:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:b83fc239b8bdb5d0ac94c097d92d9a85ac82ea82d535fdd44ce85c29c683078e
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

### `traefik:v2.11` - linux; amd64

```console
$ docker pull traefik@sha256:ac8c824bff35528ab36cb5245a8e488b419555e3b1b5672f4a2f4dc5b8a81da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50978940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce622bd2eac1031b22b2a724e52d8f615eca7eea0679e112a09235f4b17c7fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:05 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:08 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6f9c66e581dc9a0a73c65a91c09c8c25658e76ca0c42313eb493037f79bb81`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 456.9 KB (456939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f65172c40aa9ef7f8e79c49e6bf6a4ce5a81e3d6ed6c068ecaf903c644eba3e`  
		Last Modified: Thu, 04 Dec 2025 19:24:12 GMT  
		Size: 46.7 MB (46719180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d007db28390cd93183e7930d1e72ebe8ea62d5c2047982518002be0af321b66`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:b5c4cf6445eabd54dbbc99c02744ce44c18c069957f2e6cda738fd06736fa04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7997e68f2d9ee4a7810bb994211873a40085ba0376fd0434fc8f97efeabfde35`

```dockerfile
```

-	Layers:
	-	`sha256:9fdea8c65335538554420bb2f73ee610e77b35a8d99a41f66500f065275f7eef`  
		Last Modified: Thu, 04 Dec 2025 22:09:38 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618029352157666e0f7ada57d0b9772e84b7d8813d76014b9e425ac7d906c921`  
		Last Modified: Thu, 04 Dec 2025 22:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:00cacb5e3b75272d0963554604f16ee2f93e2caf8d774fb308ee3a2682b3fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46746429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b47a4e1eed2a3590b56e42a9bb20a814f235d05069e5aa8da45d25abfdaeb4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:10 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df693b807706002f19e426395418816460fb1a346f714d70e1c2c8afe374fd6`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 457.7 KB (457743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ef2971fe1a98ac7085996aa7023b6ccebf3897ef0483117b06b73d62b21aea`  
		Last Modified: Thu, 04 Dec 2025 19:23:35 GMT  
		Size: 42.8 MB (42784237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03516caee00078a85faefe1fd7d687c9cf8683b6dcfd8b57471545e1a9539870`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:aed9768db2bd35f301e0230caa1d2ffb2251a131320be645d6974c55e86618c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951f2a74272fc9c6c92170e2f27e242079597091a9506042db0401721e2db134`

```dockerfile
```

-	Layers:
	-	`sha256:1de50cb82d5378e594bac4e56dd225fa1d5f34bec27ee27fd9551913bc11fe3c`  
		Last Modified: Thu, 04 Dec 2025 22:09:42 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e578a9c8a06c07bb518641ab52b497b2fefce64c57a13530ae9731e0f35f6519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47214110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322725a91b8aa0f09e823c8879e728fab22810cdbec06bb669998e14e2f20e3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:53 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f4dc86542d7de98a768f4c0aee00ee4babe24157a4398e0e57604d2128efe`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923727f8d2ecf48712183a704dc223b5f52c03513cacfd1154f1ec815b66e8c`  
		Last Modified: Thu, 04 Dec 2025 19:21:01 GMT  
		Size: 42.6 MB (42616644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cb010135a022802cdc49ad86685907a4b7fec67e04d2ef6c5fa3b3dfbd504c`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:9a47c8fe962fefb1ab75eca20fce3174ae6107399c354c08787946583e9a53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82df1b830714c487e63a0e3cc2de51b9ae86fb219c7ede49b7055db217ff0f1`

```dockerfile
```

-	Layers:
	-	`sha256:d92cd312fa7dfcb46d339b39a908f09c05c04111ce94b03096f121b2b2ba238f`  
		Last Modified: Thu, 04 Dec 2025 22:09:46 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e6e0053f14ec312f9f3a94120e5153aa376985a6462fe8cb55509fc1495a7`  
		Last Modified: Thu, 04 Dec 2025 22:09:47 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:705d054c3866fdb6718a38957a67bcf193b38faa9ff5aaf8bc1da18af25bc516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45146924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de90c8d7f80a5aad7df4da00b1051b98930c54c8ababf669deb6d0d2d04a4f17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:34 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d260e1c1ba83417069742e33ef3dca0b56b4fb4a494c1c02755de510ec75e4a`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 459.4 KB (459433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e72a719bd9cd6a8f63be96d8d4c6575cad6c06a10e9ffaf1ecf0b582ff2542e`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 41.0 MB (40954880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a71f904fae4ec8c94264d8912ca717e59c7ec5031afd18f2f3f7bffdd5b1fe`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:3a46754ca761744e0f8883b9bfcd1684e663ac55b467b3a3b6923f51ff444d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d326368736c8a7420af0299583f8308601f8c1058845300561361b987ee13fad`

```dockerfile
```

-	Layers:
	-	`sha256:c4385ecde488f23523e5f1a690f599ee5de4f852330ed63b9cb8f58e461d00a9`  
		Last Modified: Thu, 04 Dec 2025 22:09:50 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b23d28dedd26705c13315cf1cee4006037cd5639347b33b5a7c069bd7e5b9d8`  
		Last Modified: Thu, 04 Dec 2025 22:09:51 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:d2369d1a056936faca65d8e93331f6c15206edae8de08cd19101b17fda585c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86529b2beb0c64eeca37a77d5f26cf86430efeaf90a846871cccc51dc5f32c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:25:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:25:00 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:25:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d39b914768ddc25dc0c8a18d22db328f98cdcd95023baf8462083cc310d921ce`  
		Last Modified: Thu, 13 Nov 2025 19:30:49 GMT  
		Size: 45.3 MB (45254914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc3958099a89f085a5a97e30da325962e143b71700d8a163253f5b051b6c21`  
		Last Modified: Thu, 13 Nov 2025 19:30:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:ec2d880cdd0b6e91da3f758bd0998f306a24cc79dd232279aac53560f8d6cb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b6f9edf3a8d37082eb7d6a876184f6f889fe39a5088c25682aae0a7979915`

```dockerfile
```

-	Layers:
	-	`sha256:a6bad9481934565b57441774a105e811329aea7a68a817a24b57b77744f16651`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 853.1 KB (853068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eab8c394838eaf7fb4899e4b320cf259da9cf52fe633bfe96cdb36ea996c1a`  
		Last Modified: Thu, 13 Nov 2025 22:09:53 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:6ce21e040bd4e2552427746ac5d0436d21f5f70bb0eadd8cf84a6e0fa0f6c8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49360723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8cc7abc990629392d3d289ac957e498bae15a9e836b0eade383931b77229b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:39 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d51ac067c25bf77fc5f6d25393d578c35080ea1d6d82d5c52dc00d5152699a6`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 457.9 KB (457913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36796f5fe181a6d2eb8fe90a5ca86fe909a756cc7cd57ccfb29dc3dc22620391`  
		Last Modified: Thu, 04 Dec 2025 19:21:04 GMT  
		Size: 45.3 MB (45253196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415c08db574d0b987b7070e71f49cbb2b58fa19861291d64c90e0dccde610b4`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:821663597494279db90cb3041862160bec3dcfe15162cb71c8b6f6fc3508aedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c48cbe3f7f2e42ad7e85328cc0e03b561857f85c793e37e796b4dc15269f8cd`

```dockerfile
```

-	Layers:
	-	`sha256:c41f76c95136d09bef36ea43a6eaf5869d09c21fc9edb28948b6c0e690332bc3`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61aaab597727c9c099570e7d5b30d607529858bc616081953993f6d88744a2a`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:138d7a87225e5c01a2b5db9301d7c6aab20073cd7798753fd81fe1e858cec83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2a60f1cc89f202977266b2a1651a9650ba802f4c066ca5931e59f3d404e1a042
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173864697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bece513a73e007d0e19209b413a84a7322d006eeddf299964b71efbec9b7e9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 04 Dec 2025 19:45:19 GMT
RUN cmd /S /C #(nop) COPY file:c5fd63825ca3af125acc7c0933cfb57a0080ecc168578d5b8882a0a05ef47bf4 in \ 
# Thu, 04 Dec 2025 19:45:21 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 04 Dec 2025 19:45:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:45:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473330b82e6af6d0613f521c11967f24228b1f1db3525d5ba2397c60eb96a81`  
		Last Modified: Thu, 04 Dec 2025 19:46:15 GMT  
		Size: 47.5 MB (47512441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9567c173a49fe4d5f69532267d8341eb54a40a659c6097e17856f13db5c3781e`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2dbeb0f2c54c414b81ad494b02482f528225d6ff22f9d7df5e139d19bb13bf`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c9666ee73f9d459e7e07b81222cd91048ae7e032a8e09a8888641e8ad861c7`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:dcec3000efc0d552358fd44f95644e5e908de7d472a63df0edb574de81517645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2988f00eaf0aeedcab04b601936c36fb3f454008611b35134e846a5f4e26b158
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818121188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31715b9a396950e980e3b2579d073169b112b7a318a9ac5c170d1f0e3edc930b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 04 Dec 2025 19:23:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Dec 2025 19:25:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 04 Dec 2025 19:25:38 GMT
EXPOSE 80
# Thu, 04 Dec 2025 19:25:40 GMT
ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bf6b095296831cd4d5f34d58fa0959fd7ef42e2dc9efd551c55d16e533b161`  
		Last Modified: Thu, 04 Dec 2025 19:38:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bac6613489c4597256f38308be766d6b69566e37eae1ec90fd75668f5ddd323`  
		Last Modified: Thu, 04 Dec 2025 19:38:29 GMT  
		Size: 48.2 MB (48154462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4a3d7b533059c5b4c90f6ad2b5cf3cf561ffd5341fa82b23cb2200e3604e15`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f85135e09953edf14105875b914705d2e9163f065e361f6df0548ce9a9ce7`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de324d8f25e723e0020dda62e746d4c7d464d758c0e6ecf94b2b5b741d0b25d0`  
		Last Modified: Thu, 04 Dec 2025 19:38:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.32`

```console
$ docker pull traefik@sha256:79f8665f38c397ee91c7398208117561dbe1b519ce2e2a1c32ebea7855a6c49e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v2.11.32` - linux; amd64

```console
$ docker pull traefik@sha256:ac8c824bff35528ab36cb5245a8e488b419555e3b1b5672f4a2f4dc5b8a81da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50978940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce622bd2eac1031b22b2a724e52d8f615eca7eea0679e112a09235f4b17c7fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:05 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:08 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:08 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6f9c66e581dc9a0a73c65a91c09c8c25658e76ca0c42313eb493037f79bb81`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 456.9 KB (456939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f65172c40aa9ef7f8e79c49e6bf6a4ce5a81e3d6ed6c068ecaf903c644eba3e`  
		Last Modified: Thu, 04 Dec 2025 19:24:12 GMT  
		Size: 46.7 MB (46719180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d007db28390cd93183e7930d1e72ebe8ea62d5c2047982518002be0af321b66`  
		Last Modified: Thu, 04 Dec 2025 19:23:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.32` - unknown; unknown

```console
$ docker pull traefik@sha256:b5c4cf6445eabd54dbbc99c02744ce44c18c069957f2e6cda738fd06736fa04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7997e68f2d9ee4a7810bb994211873a40085ba0376fd0434fc8f97efeabfde35`

```dockerfile
```

-	Layers:
	-	`sha256:9fdea8c65335538554420bb2f73ee610e77b35a8d99a41f66500f065275f7eef`  
		Last Modified: Thu, 04 Dec 2025 22:09:38 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618029352157666e0f7ada57d0b9772e84b7d8813d76014b9e425ac7d906c921`  
		Last Modified: Thu, 04 Dec 2025 22:09:39 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.32` - linux; arm variant v6

```console
$ docker pull traefik@sha256:00cacb5e3b75272d0963554604f16ee2f93e2caf8d774fb308ee3a2682b3fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46746429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b47a4e1eed2a3590b56e42a9bb20a814f235d05069e5aa8da45d25abfdaeb4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:23:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:23:10 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:23:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:23:10 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:23:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df693b807706002f19e426395418816460fb1a346f714d70e1c2c8afe374fd6`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 457.7 KB (457743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ef2971fe1a98ac7085996aa7023b6ccebf3897ef0483117b06b73d62b21aea`  
		Last Modified: Thu, 04 Dec 2025 19:23:35 GMT  
		Size: 42.8 MB (42784237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03516caee00078a85faefe1fd7d687c9cf8683b6dcfd8b57471545e1a9539870`  
		Last Modified: Thu, 04 Dec 2025 19:23:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.32` - unknown; unknown

```console
$ docker pull traefik@sha256:aed9768db2bd35f301e0230caa1d2ffb2251a131320be645d6974c55e86618c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951f2a74272fc9c6c92170e2f27e242079597091a9506042db0401721e2db134`

```dockerfile
```

-	Layers:
	-	`sha256:1de50cb82d5378e594bac4e56dd225fa1d5f34bec27ee27fd9551913bc11fe3c`  
		Last Modified: Thu, 04 Dec 2025 22:09:42 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.32` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e578a9c8a06c07bb518641ab52b497b2fefce64c57a13530ae9731e0f35f6519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47214110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322725a91b8aa0f09e823c8879e728fab22810cdbec06bb669998e14e2f20e3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:53 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:53 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f4dc86542d7de98a768f4c0aee00ee4babe24157a4398e0e57604d2128efe`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923727f8d2ecf48712183a704dc223b5f52c03513cacfd1154f1ec815b66e8c`  
		Last Modified: Thu, 04 Dec 2025 19:21:01 GMT  
		Size: 42.6 MB (42616644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cb010135a022802cdc49ad86685907a4b7fec67e04d2ef6c5fa3b3dfbd504c`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.32` - unknown; unknown

```console
$ docker pull traefik@sha256:9a47c8fe962fefb1ab75eca20fce3174ae6107399c354c08787946583e9a53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82df1b830714c487e63a0e3cc2de51b9ae86fb219c7ede49b7055db217ff0f1`

```dockerfile
```

-	Layers:
	-	`sha256:d92cd312fa7dfcb46d339b39a908f09c05c04111ce94b03096f121b2b2ba238f`  
		Last Modified: Thu, 04 Dec 2025 22:09:46 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e6e0053f14ec312f9f3a94120e5153aa376985a6462fe8cb55509fc1495a7`  
		Last Modified: Thu, 04 Dec 2025 22:09:47 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.32` - linux; ppc64le

```console
$ docker pull traefik@sha256:705d054c3866fdb6718a38957a67bcf193b38faa9ff5aaf8bc1da18af25bc516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45146924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de90c8d7f80a5aad7df4da00b1051b98930c54c8ababf669deb6d0d2d04a4f17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:34 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d260e1c1ba83417069742e33ef3dca0b56b4fb4a494c1c02755de510ec75e4a`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 459.4 KB (459433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e72a719bd9cd6a8f63be96d8d4c6575cad6c06a10e9ffaf1ecf0b582ff2542e`  
		Last Modified: Thu, 04 Dec 2025 19:20:56 GMT  
		Size: 41.0 MB (40954880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a71f904fae4ec8c94264d8912ca717e59c7ec5031afd18f2f3f7bffdd5b1fe`  
		Last Modified: Thu, 04 Dec 2025 19:20:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.32` - unknown; unknown

```console
$ docker pull traefik@sha256:3a46754ca761744e0f8883b9bfcd1684e663ac55b467b3a3b6923f51ff444d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d326368736c8a7420af0299583f8308601f8c1058845300561361b987ee13fad`

```dockerfile
```

-	Layers:
	-	`sha256:c4385ecde488f23523e5f1a690f599ee5de4f852330ed63b9cb8f58e461d00a9`  
		Last Modified: Thu, 04 Dec 2025 22:09:50 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b23d28dedd26705c13315cf1cee4006037cd5639347b33b5a7c069bd7e5b9d8`  
		Last Modified: Thu, 04 Dec 2025 22:09:51 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.32` - linux; s390x

```console
$ docker pull traefik@sha256:6ce21e040bd4e2552427746ac5d0436d21f5f70bb0eadd8cf84a6e0fa0f6c8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49360723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8cc7abc990629392d3d289ac957e498bae15a9e836b0eade383931b77229b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:19:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Dec 2025 19:19:39 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Dec 2025 19:19:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:19:39 GMT
CMD ["traefik"]
# Thu, 04 Dec 2025 19:19:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d51ac067c25bf77fc5f6d25393d578c35080ea1d6d82d5c52dc00d5152699a6`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 457.9 KB (457913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36796f5fe181a6d2eb8fe90a5ca86fe909a756cc7cd57ccfb29dc3dc22620391`  
		Last Modified: Thu, 04 Dec 2025 19:21:04 GMT  
		Size: 45.3 MB (45253196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d415c08db574d0b987b7070e71f49cbb2b58fa19861291d64c90e0dccde610b4`  
		Last Modified: Thu, 04 Dec 2025 19:20:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.32` - unknown; unknown

```console
$ docker pull traefik@sha256:821663597494279db90cb3041862160bec3dcfe15162cb71c8b6f6fc3508aedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c48cbe3f7f2e42ad7e85328cc0e03b561857f85c793e37e796b4dc15269f8cd`

```dockerfile
```

-	Layers:
	-	`sha256:c41f76c95136d09bef36ea43a6eaf5869d09c21fc9edb28948b6c0e690332bc3`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61aaab597727c9c099570e7d5b30d607529858bc616081953993f6d88744a2a`  
		Last Modified: Thu, 04 Dec 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.32-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:138d7a87225e5c01a2b5db9301d7c6aab20073cd7798753fd81fe1e858cec83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11.32-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2a60f1cc89f202977266b2a1651a9650ba802f4c066ca5931e59f3d404e1a042
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173864697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bece513a73e007d0e19209b413a84a7322d006eeddf299964b71efbec9b7e9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 04 Dec 2025 19:45:19 GMT
RUN cmd /S /C #(nop) COPY file:c5fd63825ca3af125acc7c0933cfb57a0080ecc168578d5b8882a0a05ef47bf4 in \ 
# Thu, 04 Dec 2025 19:45:21 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 04 Dec 2025 19:45:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:45:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473330b82e6af6d0613f521c11967f24228b1f1db3525d5ba2397c60eb96a81`  
		Last Modified: Thu, 04 Dec 2025 19:46:15 GMT  
		Size: 47.5 MB (47512441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9567c173a49fe4d5f69532267d8341eb54a40a659c6097e17856f13db5c3781e`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2dbeb0f2c54c414b81ad494b02482f528225d6ff22f9d7df5e139d19bb13bf`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c9666ee73f9d459e7e07b81222cd91048ae7e032a8e09a8888641e8ad861c7`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.32-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:dcec3000efc0d552358fd44f95644e5e908de7d472a63df0edb574de81517645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11.32-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2988f00eaf0aeedcab04b601936c36fb3f454008611b35134e846a5f4e26b158
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818121188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31715b9a396950e980e3b2579d073169b112b7a318a9ac5c170d1f0e3edc930b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 04 Dec 2025 19:23:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Dec 2025 19:25:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 04 Dec 2025 19:25:38 GMT
EXPOSE 80
# Thu, 04 Dec 2025 19:25:40 GMT
ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bf6b095296831cd4d5f34d58fa0959fd7ef42e2dc9efd551c55d16e533b161`  
		Last Modified: Thu, 04 Dec 2025 19:38:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bac6613489c4597256f38308be766d6b69566e37eae1ec90fd75668f5ddd323`  
		Last Modified: Thu, 04 Dec 2025 19:38:29 GMT  
		Size: 48.2 MB (48154462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4a3d7b533059c5b4c90f6ad2b5cf3cf561ffd5341fa82b23cb2200e3604e15`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f85135e09953edf14105875b914705d2e9163f065e361f6df0548ce9a9ce7`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de324d8f25e723e0020dda62e746d4c7d464d758c0e6ecf94b2b5b741d0b25d0`  
		Last Modified: Thu, 04 Dec 2025 19:38:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:aaf0f6185419a50c74651448c1a5bf4606bd2d2ddb7b8749eed505d55bf8b8ea
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

### `traefik:v3` - linux; amd64

```console
$ docker pull traefik@sha256:ec4fce4588f239530c79af7e2dd873877e51a5548cc51cfbf318ae6e1727e138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e55c25c9dc924eb86e34957cea11335f48f3eeb87c12b8472434db39a43f143`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 21:48:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 21:48:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 21:48:13 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 21:48:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fcf41ae4fe549fc66069c1d9a3dfc8c7684a19fae6345f38239a84543cb451`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 456.9 KB (456932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff51e48e8c41ee2aebd058d15b97b4f47b6722fac2a08e226f835df67d4418e2`  
		Last Modified: Tue, 18 Nov 2025 21:49:19 GMT  
		Size: 47.4 MB (47433025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e2292afa9f7b52254e57efeb2deac56f51163f1572a1da072bbecc4e1b757`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:4261a87ee97389d6ecbdb5e8d8a673aa7ab3655675e2f1d1d84dd3825e26bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b750f1805931f0b564bfd7f3749094595eeefa65812c77aed1c1c9326a8d96c7`

```dockerfile
```

-	Layers:
	-	`sha256:dd4ab2e6afc636d1939980a8bf3d9cea3ddcd13a44c1d2295ba738ef261d09d7`  
		Last Modified: Tue, 18 Nov 2025 22:12:05 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24afbeef114a9fcc5c689c830f8392110a29eb89171b2436f0186680ce002e14`  
		Last Modified: Tue, 18 Nov 2025 22:12:06 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:561b6e0f7d5f408c12d49170ad858a17c8fae6f0b685bccc027abdbc34bf98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25de55986ee18f2435d5c74bf6032a3a2e15353a695c8f7a9859a5bbede5e41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:28:50 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78109e37152b41df02ee2c237f740f003151ef213dd9c81e925a61e13a562e8e`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 457.7 KB (457742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cda1c04505fd255242fdece0301c166e8cec8bf2ab4dd1ac4debf3cd00bdff`  
		Last Modified: Tue, 18 Nov 2025 19:29:15 GMT  
		Size: 43.0 MB (42954733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece82213e301e010af11f5ebf09d08ea08de287de016f8cc954c3781b03eddcd`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:0009cf7a9ecccca8185f9089f56ac6cf92a7f3bcb3c43151132fef8c0e523439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb979678d6660d672ff7cb2a3a8f96887af931403b91c76d4f6b1342a169b49`

```dockerfile
```

-	Layers:
	-	`sha256:f937ea1ee9c88faa49302bc9ddc4cab7f1a4cda765d2fe7becd38622c625bf67`  
		Last Modified: Tue, 18 Nov 2025 22:12:09 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58ccae90050988e9890eedfb1c6548b82c1ca60e807d97517daaddb6312a557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9f1b556d725190bc03627caf6f7b39276b3aed3745b9c0701e408acbf0ea39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:25:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:25:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:25:43 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:25:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417edc5cf59f87d70cf22c79d067722d6949576117ec0bcff04e50d6a4edfab9`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594c719740f22165cd53b9aac15e8797c888a46b8036d0defd56bb322e1be2c`  
		Last Modified: Tue, 18 Nov 2025 19:26:44 GMT  
		Size: 43.1 MB (43148307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6369fe0dab57aea1446d2fc8db9da1e6d27db7b2847c04b4f90f4cd6d20ef21`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:29d930fed1539847060dfbc2bffe8beb811209e24903d0773c44de8a84ae446a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef50f53cba8be23e4bc4cc3aadc3d445801d4160a1931dbe8be09db5a661943f`

```dockerfile
```

-	Layers:
	-	`sha256:c15e382f6e16857c9e88493b9b05152c009ab9bcb9708326208db496e2692923`  
		Last Modified: Tue, 18 Nov 2025 22:12:12 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a64dd22de08febf3ec2ebeb77c873765b75b1b6561f00b63357b5c1266bb013`  
		Last Modified: Tue, 18 Nov 2025 22:12:13 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a690dd84bed67e8e18f8d4c04b90f73774e3895300207e88d4ebfef99dedd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45323965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff3c8eb0949ee6dfda7c4c8ce8a9058548e947d4be56670a9e1143f8b80b891`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 22:02:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 22:02:04 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 22:02:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7131cbb6f2ed0728075b7863f72b456c451d363f035bc26eb4dc639ff1ea91f`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 459.4 KB (459444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163ecef57ee3319b1b03d664f61a15b5798d00e5e693105671fdfca70b48572`  
		Last Modified: Tue, 18 Nov 2025 22:03:14 GMT  
		Size: 41.1 MB (41131911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e085ee6011d283be1359ca019b8b510565abcf3ba44bfceaea6351deca17429`  
		Last Modified: Tue, 18 Nov 2025 22:03:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:3be7a65febed98487068f4f3636c8b42574da05615fee85f690ccecc964a78f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806e17ee732263c18ab393c230c85c74af69797ff07837c6e0641265849c22`

```dockerfile
```

-	Layers:
	-	`sha256:f086e4046623395e3cb574d6480d4e05e3552ba71b387734b5f8f6c43500b78b`  
		Last Modified: Tue, 18 Nov 2025 22:12:17 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb34f7412305f709ba275808c9588d9a7a5e7cae6d9b1aa5d2f56928804c72d8`  
		Last Modified: Tue, 18 Nov 2025 22:12:18 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:dd5c5f868d64632d40e1fc02d154a6850871bd88b605ea430630aa7d2d70d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49696840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af8810d338f1bd1a4b4fb764de8b01c082104bd2f4f216724435a0d18961f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 20 Nov 2025 19:45:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:45:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Nov 2025 19:45:33 GMT
CMD ["traefik"]
# Thu, 20 Nov 2025 19:45:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:77490f998c3cacffe82e080079ee717eb224ae54ff7776969eb02d5e3083c297`  
		Last Modified: Thu, 20 Nov 2025 19:51:39 GMT  
		Size: 45.7 MB (45723955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f9fa6da824b71d504b2b5252daaa9d5aadf78e571c9f9d79aeff67f5907e6`  
		Last Modified: Thu, 20 Nov 2025 19:51:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:fc3215167bc91ea171842167fc09a79120e6f3d8d340a1e637804cdf56b71e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8091b4062673a8ea24b34c56fb441d17a6afb43e0dba564e3c8c16b9b0197`

```dockerfile
```

-	Layers:
	-	`sha256:92e1bb99aa3bbe7baa5d5f23f96ff12db288cb6426dc299879f820a396c7350c`  
		Last Modified: Thu, 20 Nov 2025 22:09:41 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c52c6da61f97cda07d7683b99b6ba1f2d1c8068ca37f64d0f288b2fc103fa5`  
		Last Modified: Thu, 20 Nov 2025 22:09:42 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:a1b3be8672939a4d2913ba3c9da9d86056337dae16b5a8f4fecfb429e436f8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088adf79d3c254dcb80a82265220f63d1f8fca26800fbeadc494b8be29f98de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:27:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:27:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:27:20 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:27:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ed3289785c33bee42da1326ef857e710b7e549418a49847e37717014d7961`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 457.9 KB (457907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372adc29fa3a207abdcada906a4729dc818037b9435d9fdaa2924029ec613d48`  
		Last Modified: Tue, 18 Nov 2025 19:28:24 GMT  
		Size: 45.6 MB (45580906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372305cc3de919e1c11bc8d295332bdaf8f42010ae5f98aa46d1329a692b3dad`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:1946888eecd66b91618fb7d72586307879f92142a83d2f84d72f46f5c8a1e84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b5ef23c86249042fde863ab1bdd6f7993028c3ff3aed03c4abf2e0c54138a`

```dockerfile
```

-	Layers:
	-	`sha256:74d6354101a69d21a00a0cecffd02193b2e3627c0a13b454031455557a7f3176`  
		Last Modified: Tue, 18 Nov 2025 22:12:23 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71b6f477949b4d7f2c93d8566c67d23e4e91dbbef5f68bf83bc2f72db5b190b`  
		Last Modified: Tue, 18 Nov 2025 22:12:24 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:aaf0f6185419a50c74651448c1a5bf4606bd2d2ddb7b8749eed505d55bf8b8ea
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

### `traefik:v3.6` - linux; amd64

```console
$ docker pull traefik@sha256:ec4fce4588f239530c79af7e2dd873877e51a5548cc51cfbf318ae6e1727e138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e55c25c9dc924eb86e34957cea11335f48f3eeb87c12b8472434db39a43f143`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 21:48:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 21:48:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 21:48:13 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 21:48:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fcf41ae4fe549fc66069c1d9a3dfc8c7684a19fae6345f38239a84543cb451`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 456.9 KB (456932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff51e48e8c41ee2aebd058d15b97b4f47b6722fac2a08e226f835df67d4418e2`  
		Last Modified: Tue, 18 Nov 2025 21:49:19 GMT  
		Size: 47.4 MB (47433025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e2292afa9f7b52254e57efeb2deac56f51163f1572a1da072bbecc4e1b757`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4261a87ee97389d6ecbdb5e8d8a673aa7ab3655675e2f1d1d84dd3825e26bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b750f1805931f0b564bfd7f3749094595eeefa65812c77aed1c1c9326a8d96c7`

```dockerfile
```

-	Layers:
	-	`sha256:dd4ab2e6afc636d1939980a8bf3d9cea3ddcd13a44c1d2295ba738ef261d09d7`  
		Last Modified: Tue, 18 Nov 2025 22:12:05 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24afbeef114a9fcc5c689c830f8392110a29eb89171b2436f0186680ce002e14`  
		Last Modified: Tue, 18 Nov 2025 22:12:06 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:561b6e0f7d5f408c12d49170ad858a17c8fae6f0b685bccc027abdbc34bf98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25de55986ee18f2435d5c74bf6032a3a2e15353a695c8f7a9859a5bbede5e41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:28:50 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78109e37152b41df02ee2c237f740f003151ef213dd9c81e925a61e13a562e8e`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 457.7 KB (457742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cda1c04505fd255242fdece0301c166e8cec8bf2ab4dd1ac4debf3cd00bdff`  
		Last Modified: Tue, 18 Nov 2025 19:29:15 GMT  
		Size: 43.0 MB (42954733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece82213e301e010af11f5ebf09d08ea08de287de016f8cc954c3781b03eddcd`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0009cf7a9ecccca8185f9089f56ac6cf92a7f3bcb3c43151132fef8c0e523439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb979678d6660d672ff7cb2a3a8f96887af931403b91c76d4f6b1342a169b49`

```dockerfile
```

-	Layers:
	-	`sha256:f937ea1ee9c88faa49302bc9ddc4cab7f1a4cda765d2fe7becd38622c625bf67`  
		Last Modified: Tue, 18 Nov 2025 22:12:09 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58ccae90050988e9890eedfb1c6548b82c1ca60e807d97517daaddb6312a557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9f1b556d725190bc03627caf6f7b39276b3aed3745b9c0701e408acbf0ea39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:25:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:25:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:25:43 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:25:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417edc5cf59f87d70cf22c79d067722d6949576117ec0bcff04e50d6a4edfab9`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594c719740f22165cd53b9aac15e8797c888a46b8036d0defd56bb322e1be2c`  
		Last Modified: Tue, 18 Nov 2025 19:26:44 GMT  
		Size: 43.1 MB (43148307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6369fe0dab57aea1446d2fc8db9da1e6d27db7b2847c04b4f90f4cd6d20ef21`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:29d930fed1539847060dfbc2bffe8beb811209e24903d0773c44de8a84ae446a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef50f53cba8be23e4bc4cc3aadc3d445801d4160a1931dbe8be09db5a661943f`

```dockerfile
```

-	Layers:
	-	`sha256:c15e382f6e16857c9e88493b9b05152c009ab9bcb9708326208db496e2692923`  
		Last Modified: Tue, 18 Nov 2025 22:12:12 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a64dd22de08febf3ec2ebeb77c873765b75b1b6561f00b63357b5c1266bb013`  
		Last Modified: Tue, 18 Nov 2025 22:12:13 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a690dd84bed67e8e18f8d4c04b90f73774e3895300207e88d4ebfef99dedd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45323965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff3c8eb0949ee6dfda7c4c8ce8a9058548e947d4be56670a9e1143f8b80b891`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 22:02:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 22:02:04 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 22:02:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7131cbb6f2ed0728075b7863f72b456c451d363f035bc26eb4dc639ff1ea91f`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 459.4 KB (459444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163ecef57ee3319b1b03d664f61a15b5798d00e5e693105671fdfca70b48572`  
		Last Modified: Tue, 18 Nov 2025 22:03:14 GMT  
		Size: 41.1 MB (41131911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e085ee6011d283be1359ca019b8b510565abcf3ba44bfceaea6351deca17429`  
		Last Modified: Tue, 18 Nov 2025 22:03:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:3be7a65febed98487068f4f3636c8b42574da05615fee85f690ccecc964a78f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806e17ee732263c18ab393c230c85c74af69797ff07837c6e0641265849c22`

```dockerfile
```

-	Layers:
	-	`sha256:f086e4046623395e3cb574d6480d4e05e3552ba71b387734b5f8f6c43500b78b`  
		Last Modified: Tue, 18 Nov 2025 22:12:17 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb34f7412305f709ba275808c9588d9a7a5e7cae6d9b1aa5d2f56928804c72d8`  
		Last Modified: Tue, 18 Nov 2025 22:12:18 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:dd5c5f868d64632d40e1fc02d154a6850871bd88b605ea430630aa7d2d70d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49696840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af8810d338f1bd1a4b4fb764de8b01c082104bd2f4f216724435a0d18961f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 20 Nov 2025 19:45:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:45:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Nov 2025 19:45:33 GMT
CMD ["traefik"]
# Thu, 20 Nov 2025 19:45:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:77490f998c3cacffe82e080079ee717eb224ae54ff7776969eb02d5e3083c297`  
		Last Modified: Thu, 20 Nov 2025 19:51:39 GMT  
		Size: 45.7 MB (45723955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f9fa6da824b71d504b2b5252daaa9d5aadf78e571c9f9d79aeff67f5907e6`  
		Last Modified: Thu, 20 Nov 2025 19:51:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:fc3215167bc91ea171842167fc09a79120e6f3d8d340a1e637804cdf56b71e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8091b4062673a8ea24b34c56fb441d17a6afb43e0dba564e3c8c16b9b0197`

```dockerfile
```

-	Layers:
	-	`sha256:92e1bb99aa3bbe7baa5d5f23f96ff12db288cb6426dc299879f820a396c7350c`  
		Last Modified: Thu, 20 Nov 2025 22:09:41 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c52c6da61f97cda07d7683b99b6ba1f2d1c8068ca37f64d0f288b2fc103fa5`  
		Last Modified: Thu, 20 Nov 2025 22:09:42 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:a1b3be8672939a4d2913ba3c9da9d86056337dae16b5a8f4fecfb429e436f8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088adf79d3c254dcb80a82265220f63d1f8fca26800fbeadc494b8be29f98de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:27:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:27:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:27:20 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:27:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ed3289785c33bee42da1326ef857e710b7e549418a49847e37717014d7961`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 457.9 KB (457907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372adc29fa3a207abdcada906a4729dc818037b9435d9fdaa2924029ec613d48`  
		Last Modified: Tue, 18 Nov 2025 19:28:24 GMT  
		Size: 45.6 MB (45580906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372305cc3de919e1c11bc8d295332bdaf8f42010ae5f98aa46d1329a692b3dad`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:1946888eecd66b91618fb7d72586307879f92142a83d2f84d72f46f5c8a1e84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b5ef23c86249042fde863ab1bdd6f7993028c3ff3aed03c4abf2e0c54138a`

```dockerfile
```

-	Layers:
	-	`sha256:74d6354101a69d21a00a0cecffd02193b2e3627c0a13b454031455557a7f3176`  
		Last Modified: Tue, 18 Nov 2025 22:12:23 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71b6f477949b4d7f2c93d8566c67d23e4e91dbbef5f68bf83bc2f72db5b190b`  
		Last Modified: Tue, 18 Nov 2025 22:12:24 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.2`

```console
$ docker pull traefik@sha256:aaf0f6185419a50c74651448c1a5bf4606bd2d2ddb7b8749eed505d55bf8b8ea
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

### `traefik:v3.6.2` - linux; amd64

```console
$ docker pull traefik@sha256:ec4fce4588f239530c79af7e2dd873877e51a5548cc51cfbf318ae6e1727e138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e55c25c9dc924eb86e34957cea11335f48f3eeb87c12b8472434db39a43f143`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 21:48:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 21:48:13 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 21:48:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 21:48:13 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 21:48:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fcf41ae4fe549fc66069c1d9a3dfc8c7684a19fae6345f38239a84543cb451`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 456.9 KB (456932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff51e48e8c41ee2aebd058d15b97b4f47b6722fac2a08e226f835df67d4418e2`  
		Last Modified: Tue, 18 Nov 2025 21:49:19 GMT  
		Size: 47.4 MB (47433025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e2292afa9f7b52254e57efeb2deac56f51163f1572a1da072bbecc4e1b757`  
		Last Modified: Tue, 18 Nov 2025 21:49:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:4261a87ee97389d6ecbdb5e8d8a673aa7ab3655675e2f1d1d84dd3825e26bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b750f1805931f0b564bfd7f3749094595eeefa65812c77aed1c1c9326a8d96c7`

```dockerfile
```

-	Layers:
	-	`sha256:dd4ab2e6afc636d1939980a8bf3d9cea3ddcd13a44c1d2295ba738ef261d09d7`  
		Last Modified: Tue, 18 Nov 2025 22:12:05 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24afbeef114a9fcc5c689c830f8392110a29eb89171b2436f0186680ce002e14`  
		Last Modified: Tue, 18 Nov 2025 22:12:06 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:561b6e0f7d5f408c12d49170ad858a17c8fae6f0b685bccc027abdbc34bf98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25de55986ee18f2435d5c74bf6032a3a2e15353a695c8f7a9859a5bbede5e41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:28:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:28:50 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78109e37152b41df02ee2c237f740f003151ef213dd9c81e925a61e13a562e8e`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 457.7 KB (457742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cda1c04505fd255242fdece0301c166e8cec8bf2ab4dd1ac4debf3cd00bdff`  
		Last Modified: Tue, 18 Nov 2025 19:29:15 GMT  
		Size: 43.0 MB (42954733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece82213e301e010af11f5ebf09d08ea08de287de016f8cc954c3781b03eddcd`  
		Last Modified: Tue, 18 Nov 2025 19:29:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:0009cf7a9ecccca8185f9089f56ac6cf92a7f3bcb3c43151132fef8c0e523439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb979678d6660d672ff7cb2a3a8f96887af931403b91c76d4f6b1342a169b49`

```dockerfile
```

-	Layers:
	-	`sha256:f937ea1ee9c88faa49302bc9ddc4cab7f1a4cda765d2fe7becd38622c625bf67`  
		Last Modified: Tue, 18 Nov 2025 22:12:09 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58ccae90050988e9890eedfb1c6548b82c1ca60e807d97517daaddb6312a557a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9f1b556d725190bc03627caf6f7b39276b3aed3745b9c0701e408acbf0ea39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:25:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:25:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:25:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:25:43 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:25:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417edc5cf59f87d70cf22c79d067722d6949576117ec0bcff04e50d6a4edfab9`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594c719740f22165cd53b9aac15e8797c888a46b8036d0defd56bb322e1be2c`  
		Last Modified: Tue, 18 Nov 2025 19:26:44 GMT  
		Size: 43.1 MB (43148307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6369fe0dab57aea1446d2fc8db9da1e6d27db7b2847c04b4f90f4cd6d20ef21`  
		Last Modified: Tue, 18 Nov 2025 19:26:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:29d930fed1539847060dfbc2bffe8beb811209e24903d0773c44de8a84ae446a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef50f53cba8be23e4bc4cc3aadc3d445801d4160a1931dbe8be09db5a661943f`

```dockerfile
```

-	Layers:
	-	`sha256:c15e382f6e16857c9e88493b9b05152c009ab9bcb9708326208db496e2692923`  
		Last Modified: Tue, 18 Nov 2025 22:12:12 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a64dd22de08febf3ec2ebeb77c873765b75b1b6561f00b63357b5c1266bb013`  
		Last Modified: Tue, 18 Nov 2025 22:12:13 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.2` - linux; ppc64le

```console
$ docker pull traefik@sha256:9a690dd84bed67e8e18f8d4c04b90f73774e3895300207e88d4ebfef99dedd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45323965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff3c8eb0949ee6dfda7c4c8ce8a9058548e947d4be56670a9e1143f8b80b891`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 22:02:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 22:02:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 22:02:04 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 22:02:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7131cbb6f2ed0728075b7863f72b456c451d363f035bc26eb4dc639ff1ea91f`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 459.4 KB (459444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9163ecef57ee3319b1b03d664f61a15b5798d00e5e693105671fdfca70b48572`  
		Last Modified: Tue, 18 Nov 2025 22:03:14 GMT  
		Size: 41.1 MB (41131911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e085ee6011d283be1359ca019b8b510565abcf3ba44bfceaea6351deca17429`  
		Last Modified: Tue, 18 Nov 2025 22:03:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:3be7a65febed98487068f4f3636c8b42574da05615fee85f690ccecc964a78f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02806e17ee732263c18ab393c230c85c74af69797ff07837c6e0641265849c22`

```dockerfile
```

-	Layers:
	-	`sha256:f086e4046623395e3cb574d6480d4e05e3552ba71b387734b5f8f6c43500b78b`  
		Last Modified: Tue, 18 Nov 2025 22:12:17 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb34f7412305f709ba275808c9588d9a7a5e7cae6d9b1aa5d2f56928804c72d8`  
		Last Modified: Tue, 18 Nov 2025 22:12:18 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.2` - linux; riscv64

```console
$ docker pull traefik@sha256:dd5c5f868d64632d40e1fc02d154a6850871bd88b605ea430630aa7d2d70d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49696840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af8810d338f1bd1a4b4fb764de8b01c082104bd2f4f216724435a0d18961f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 20 Nov 2025 19:45:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 20 Nov 2025 19:45:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:45:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Nov 2025 19:45:33 GMT
CMD ["traefik"]
# Thu, 20 Nov 2025 19:45:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:77490f998c3cacffe82e080079ee717eb224ae54ff7776969eb02d5e3083c297`  
		Last Modified: Thu, 20 Nov 2025 19:51:39 GMT  
		Size: 45.7 MB (45723955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f9fa6da824b71d504b2b5252daaa9d5aadf78e571c9f9d79aeff67f5907e6`  
		Last Modified: Thu, 20 Nov 2025 19:51:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:fc3215167bc91ea171842167fc09a79120e6f3d8d340a1e637804cdf56b71e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a8091b4062673a8ea24b34c56fb441d17a6afb43e0dba564e3c8c16b9b0197`

```dockerfile
```

-	Layers:
	-	`sha256:92e1bb99aa3bbe7baa5d5f23f96ff12db288cb6426dc299879f820a396c7350c`  
		Last Modified: Thu, 20 Nov 2025 22:09:41 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c52c6da61f97cda07d7683b99b6ba1f2d1c8068ca37f64d0f288b2fc103fa5`  
		Last Modified: Thu, 20 Nov 2025 22:09:42 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.2` - linux; s390x

```console
$ docker pull traefik@sha256:a1b3be8672939a4d2913ba3c9da9d86056337dae16b5a8f4fecfb429e436f8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088adf79d3c254dcb80a82265220f63d1f8fca26800fbeadc494b8be29f98de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 19:27:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 19:27:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 19:27:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 19:27:20 GMT
CMD ["traefik"]
# Tue, 18 Nov 2025 19:27:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ed3289785c33bee42da1326ef857e710b7e549418a49847e37717014d7961`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 457.9 KB (457907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372adc29fa3a207abdcada906a4729dc818037b9435d9fdaa2924029ec613d48`  
		Last Modified: Tue, 18 Nov 2025 19:28:24 GMT  
		Size: 45.6 MB (45580906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372305cc3de919e1c11bc8d295332bdaf8f42010ae5f98aa46d1329a692b3dad`  
		Last Modified: Tue, 18 Nov 2025 19:28:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.2` - unknown; unknown

```console
$ docker pull traefik@sha256:1946888eecd66b91618fb7d72586307879f92142a83d2f84d72f46f5c8a1e84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b5ef23c86249042fde863ab1bdd6f7993028c3ff3aed03c4abf2e0c54138a`

```dockerfile
```

-	Layers:
	-	`sha256:74d6354101a69d21a00a0cecffd02193b2e3627c0a13b454031455557a7f3176`  
		Last Modified: Tue, 18 Nov 2025 22:12:23 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71b6f477949b4d7f2c93d8566c67d23e4e91dbbef5f68bf83bc2f72db5b190b`  
		Last Modified: Tue, 18 Nov 2025 22:12:24 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6.2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b687f8531ffbf1b27af4de8de9d67769aaedade778a29b2ee7ceac95e996737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6.2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:1d3385c8b05387c30c13615fdd861644a25b15ad6916d116fb34c50fea93204d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e91cb2c299271605f4a3ebbc38d35372329f221ac955b3514e7dc9d1f43f58d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 19:59:02 GMT
RUN cmd /S /C #(nop) COPY file:c2033131badc9e1bc747f51db227adfae7870619eaa9dfc139a85e037f98b2da in \ 
# Tue, 18 Nov 2025 19:59:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 18 Nov 2025 19:59:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:59:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6b77b67fd369a033eaefba0e01c649969aa3597ce1ad9a3c815aee73d1c37`  
		Last Modified: Tue, 18 Nov 2025 20:00:06 GMT  
		Size: 48.2 MB (48174996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbecf2219993fc91dbd9eca27b92011e84c0b0f679a14749d37b3474d4cf516d`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b1b474c55386e361a81fc357ef054eb7834e723c7075e5a0bdf8ea12250e8`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb4af60e516887c37b4cd757b1fe22066c2cfefc09d352fd9c97522b20438b0`  
		Last Modified: Tue, 18 Nov 2025 19:59:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
