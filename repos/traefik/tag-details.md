<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.35`](#traefik21135)
-	[`traefik:2.11.35-nanoserver-ltsc2022`](#traefik21135-nanoserver-ltsc2022)
-	[`traefik:2.11.35-windowsservercore-ltsc2022`](#traefik21135-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.7`](#traefik367)
-	[`traefik:3.6.7-nanoserver-ltsc2022`](#traefik367-nanoserver-ltsc2022)
-	[`traefik:3.6.7-windowsservercore-ltsc2022`](#traefik367-windowsservercore-ltsc2022)
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
-	[`traefik:v2.11.35`](#traefikv21135)
-	[`traefik:v2.11.35-nanoserver-ltsc2022`](#traefikv21135-nanoserver-ltsc2022)
-	[`traefik:v2.11.35-windowsservercore-ltsc2022`](#traefikv21135-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.7`](#traefikv367)
-	[`traefik:v3.6.7-nanoserver-ltsc2022`](#traefikv367-nanoserver-ltsc2022)
-	[`traefik:v3.6.7-windowsservercore-ltsc2022`](#traefikv367-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:fd45c6ea00e3c5d32bcf62fb3876aea090ba5fdbd5ae731bad48d35fb43ceb1a
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
$ docker pull traefik@sha256:612c89864e7ac32b573e7be254dd4c6b68e5d217d53e249bdf7503130aeb11de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51042502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df4bd8edf7db488f03c12d3ce0c62d324effa59761abc439622fcea5bedce65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:43 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c4ddced18ed75187de87b15a5d23e86ccd862033caa7e00d7181b6edeadc5`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 460.9 KB (460932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c574e4af8d35e3333ce42ac7a0739ac88eec4090aa8b204642fa4265b016ddd`  
		Last Modified: Wed, 28 Jan 2026 02:38:08 GMT  
		Size: 46.7 MB (46719380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14156968410c1e462e73d08ce573ce06e5c5e0969e5c76720019e86f4988b7`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:f19b06e1d234ffa2d151d45302d2f1cb7ae91e1fba9265c8b77eac2073222ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c612ac9bc3a1c8abf87667a76a1df19cec5d3d58c97de94d84a723a0acbd99ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3f6d6b78074aecea6293113e1b345379a4274c93c7ad0530b5a325ec6bedda`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e959a9417f0d4699dfd5d51998c6e7429b70515c75f60e6fed5f67a1b0311656`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:925796a4673bc537d65aa0ae0139fa65bf334bda6632743eeb911110ee205176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46824135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd966b67c3ff2a8e68273be9e3d20a21dc7d1ef10eb2fc10e8adb8459f4bc68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:39 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29939696f88331c61ec5e486fe45913d97a0310d35c757b552a44e7413fc2d7`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 461.4 KB (461430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e98299083ecd07c280a3ad29d3e23fdd9b6b62b01c06164379c546feb334599`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 42.8 MB (42792514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004fa5b88695b49bd44f01244238389c5cfe10f27a9097309e6aa39e9a94779d`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:1ea0b25c3611919ecdf148563d4d8a72fff06fe37433a9f037977a3710a59433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfaddf282c8ac8a90fc84a4c29b420b23808d93ba5137af1907423f5159b2dc2`

```dockerfile
```

-	Layers:
	-	`sha256:e73fa92aa495e2c477df3ca9eaf8793d89a7a164440d9d53c9afbfb0faabbe76`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5fa72d8d2ae7a83fe6caaaf0da348c02dd7506dea208b8b45648f67a58e3c0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47282746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9834c39f0607d08a9e184b6913c5492d5ecd1ac05c3a93253120c34b97e2dd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84e353c8cb1f5fb57b56ad40d428e76ac886e0d6c13da80c91b169c4e809787`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 463.0 KB (462994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d60b3fc12278ac2a5f9ce1b48ada7c4f4d5a3bf2b27a59e41281d056c5ad767`  
		Last Modified: Wed, 28 Jan 2026 02:38:31 GMT  
		Size: 42.6 MB (42622292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693733590cef860ce7b8084c3d6f9a9da06db18cfea46c5c66698395e77f2c70`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:a4f33e252a2d22f38011a65014058bbe032afb1e256538a2d0ecc39fe1cc031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aecf21660742223941c89b0ac90d49fef61d72fb66c6dd668497b5f89f6bc4`

```dockerfile
```

-	Layers:
	-	`sha256:ff041315db89151f33827fa5b4c8d1bbdcf1667943dd96fc469d9176f702ce7c`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da432fc8bdf0e99119f830a5e7a36540750b612d2c642bf669754f774856a9c6`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:ba1d0ef8f12d283ca9b9622e7ff8f8e4bd7393bca854ec1587173ac2321daf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2f811ce50d6e342494f89c95983176a88dcfe97ce9b1f3fc6d21b6dfeee398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 04:00:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 04:00:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:00:22 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 04:00:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1039e39cc46b6f1e1d99cf2d4e92f2d584ad42fb35d90c54f8774821a7f119`  
		Last Modified: Wed, 28 Jan 2026 04:01:14 GMT  
		Size: 41.0 MB (40952931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec62ead6c448599d750c453e6377a877a960b0c1c26e8a3cb6f0224eaf948dd1`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:2d6c5b0fddf8698a4717cd4702ba07bfac14339f4771103228d71384ff98e0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d2da991b59de4d4df0aa82d7b6f4b57690c61cf2686b09b7585caae09cfe15`

```dockerfile
```

-	Layers:
	-	`sha256:c8aa7e6b7bd0d2ca6530308301729284503ead7a79506d190ecc192bf9e58b8a`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26728fec798488598efe7a4e1faeb5d86cea7cfd465ae526b7b976065242d162`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:36 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:3adc5b154d0b9eff4dc3f0c41150b6db6c6ada1298092215794f64a4c1da5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c5ce88b8f342d8239dc4eca55d22a04b8200c8f02fe7a85de5a5ec90151e31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:06:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:06:02 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:06:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999cb461062f5fb156b9f3c9b2b687a5eb86c5e89ea7bee7f9fd0645988a9617`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 461.7 KB (461734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acdd44168278ba562f227698748549c7bbcca2b2600de5da8811f18d2c064b5`  
		Last Modified: Wed, 28 Jan 2026 03:06:51 GMT  
		Size: 45.2 MB (45248293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d006bc7e2968e96d32ec16c4b9607c21a9173f1222254decae36989d0f1df22`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:13efae389f81475137ec6d31ed93bec8bd22775c7917a001a89ba3a9075a909f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddee29bb5465a0d60addada3740e0be6956cc6c6532a0f59a8376764df2d8fb3`

```dockerfile
```

-	Layers:
	-	`sha256:879dbe771db52c3ad517661f201e9d7cd19f415c5fc94236335313992e0395ea`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08394b52bf7ab24561ab804dca495746bed450019eda53b3c5186a1ef0d9f861`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:fd45c6ea00e3c5d32bcf62fb3876aea090ba5fdbd5ae731bad48d35fb43ceb1a
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
$ docker pull traefik@sha256:612c89864e7ac32b573e7be254dd4c6b68e5d217d53e249bdf7503130aeb11de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51042502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df4bd8edf7db488f03c12d3ce0c62d324effa59761abc439622fcea5bedce65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:43 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c4ddced18ed75187de87b15a5d23e86ccd862033caa7e00d7181b6edeadc5`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 460.9 KB (460932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c574e4af8d35e3333ce42ac7a0739ac88eec4090aa8b204642fa4265b016ddd`  
		Last Modified: Wed, 28 Jan 2026 02:38:08 GMT  
		Size: 46.7 MB (46719380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14156968410c1e462e73d08ce573ce06e5c5e0969e5c76720019e86f4988b7`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:f19b06e1d234ffa2d151d45302d2f1cb7ae91e1fba9265c8b77eac2073222ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c612ac9bc3a1c8abf87667a76a1df19cec5d3d58c97de94d84a723a0acbd99ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3f6d6b78074aecea6293113e1b345379a4274c93c7ad0530b5a325ec6bedda`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e959a9417f0d4699dfd5d51998c6e7429b70515c75f60e6fed5f67a1b0311656`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:925796a4673bc537d65aa0ae0139fa65bf334bda6632743eeb911110ee205176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46824135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd966b67c3ff2a8e68273be9e3d20a21dc7d1ef10eb2fc10e8adb8459f4bc68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:39 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29939696f88331c61ec5e486fe45913d97a0310d35c757b552a44e7413fc2d7`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 461.4 KB (461430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e98299083ecd07c280a3ad29d3e23fdd9b6b62b01c06164379c546feb334599`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 42.8 MB (42792514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004fa5b88695b49bd44f01244238389c5cfe10f27a9097309e6aa39e9a94779d`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:1ea0b25c3611919ecdf148563d4d8a72fff06fe37433a9f037977a3710a59433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfaddf282c8ac8a90fc84a4c29b420b23808d93ba5137af1907423f5159b2dc2`

```dockerfile
```

-	Layers:
	-	`sha256:e73fa92aa495e2c477df3ca9eaf8793d89a7a164440d9d53c9afbfb0faabbe76`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5fa72d8d2ae7a83fe6caaaf0da348c02dd7506dea208b8b45648f67a58e3c0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47282746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9834c39f0607d08a9e184b6913c5492d5ecd1ac05c3a93253120c34b97e2dd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84e353c8cb1f5fb57b56ad40d428e76ac886e0d6c13da80c91b169c4e809787`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 463.0 KB (462994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d60b3fc12278ac2a5f9ce1b48ada7c4f4d5a3bf2b27a59e41281d056c5ad767`  
		Last Modified: Wed, 28 Jan 2026 02:38:31 GMT  
		Size: 42.6 MB (42622292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693733590cef860ce7b8084c3d6f9a9da06db18cfea46c5c66698395e77f2c70`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a4f33e252a2d22f38011a65014058bbe032afb1e256538a2d0ecc39fe1cc031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aecf21660742223941c89b0ac90d49fef61d72fb66c6dd668497b5f89f6bc4`

```dockerfile
```

-	Layers:
	-	`sha256:ff041315db89151f33827fa5b4c8d1bbdcf1667943dd96fc469d9176f702ce7c`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da432fc8bdf0e99119f830a5e7a36540750b612d2c642bf669754f774856a9c6`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:ba1d0ef8f12d283ca9b9622e7ff8f8e4bd7393bca854ec1587173ac2321daf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2f811ce50d6e342494f89c95983176a88dcfe97ce9b1f3fc6d21b6dfeee398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 04:00:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 04:00:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:00:22 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 04:00:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1039e39cc46b6f1e1d99cf2d4e92f2d584ad42fb35d90c54f8774821a7f119`  
		Last Modified: Wed, 28 Jan 2026 04:01:14 GMT  
		Size: 41.0 MB (40952931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec62ead6c448599d750c453e6377a877a960b0c1c26e8a3cb6f0224eaf948dd1`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:2d6c5b0fddf8698a4717cd4702ba07bfac14339f4771103228d71384ff98e0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d2da991b59de4d4df0aa82d7b6f4b57690c61cf2686b09b7585caae09cfe15`

```dockerfile
```

-	Layers:
	-	`sha256:c8aa7e6b7bd0d2ca6530308301729284503ead7a79506d190ecc192bf9e58b8a`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26728fec798488598efe7a4e1faeb5d86cea7cfd465ae526b7b976065242d162`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:36 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:3adc5b154d0b9eff4dc3f0c41150b6db6c6ada1298092215794f64a4c1da5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c5ce88b8f342d8239dc4eca55d22a04b8200c8f02fe7a85de5a5ec90151e31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:06:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:06:02 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:06:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999cb461062f5fb156b9f3c9b2b687a5eb86c5e89ea7bee7f9fd0645988a9617`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 461.7 KB (461734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acdd44168278ba562f227698748549c7bbcca2b2600de5da8811f18d2c064b5`  
		Last Modified: Wed, 28 Jan 2026 03:06:51 GMT  
		Size: 45.2 MB (45248293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d006bc7e2968e96d32ec16c4b9607c21a9173f1222254decae36989d0f1df22`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:13efae389f81475137ec6d31ed93bec8bd22775c7917a001a89ba3a9075a909f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddee29bb5465a0d60addada3740e0be6956cc6c6532a0f59a8376764df2d8fb3`

```dockerfile
```

-	Layers:
	-	`sha256:879dbe771db52c3ad517661f201e9d7cd19f415c5fc94236335313992e0395ea`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08394b52bf7ab24561ab804dca495746bed450019eda53b3c5186a1ef0d9f861`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.35`

```console
$ docker pull traefik@sha256:fd45c6ea00e3c5d32bcf62fb3876aea090ba5fdbd5ae731bad48d35fb43ceb1a
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

### `traefik:2.11.35` - linux; amd64

```console
$ docker pull traefik@sha256:612c89864e7ac32b573e7be254dd4c6b68e5d217d53e249bdf7503130aeb11de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51042502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df4bd8edf7db488f03c12d3ce0c62d324effa59761abc439622fcea5bedce65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:43 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c4ddced18ed75187de87b15a5d23e86ccd862033caa7e00d7181b6edeadc5`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 460.9 KB (460932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c574e4af8d35e3333ce42ac7a0739ac88eec4090aa8b204642fa4265b016ddd`  
		Last Modified: Wed, 28 Jan 2026 02:38:08 GMT  
		Size: 46.7 MB (46719380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14156968410c1e462e73d08ce573ce06e5c5e0969e5c76720019e86f4988b7`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:f19b06e1d234ffa2d151d45302d2f1cb7ae91e1fba9265c8b77eac2073222ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c612ac9bc3a1c8abf87667a76a1df19cec5d3d58c97de94d84a723a0acbd99ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3f6d6b78074aecea6293113e1b345379a4274c93c7ad0530b5a325ec6bedda`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e959a9417f0d4699dfd5d51998c6e7429b70515c75f60e6fed5f67a1b0311656`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.35` - linux; arm variant v6

```console
$ docker pull traefik@sha256:925796a4673bc537d65aa0ae0139fa65bf334bda6632743eeb911110ee205176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46824135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd966b67c3ff2a8e68273be9e3d20a21dc7d1ef10eb2fc10e8adb8459f4bc68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:39 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29939696f88331c61ec5e486fe45913d97a0310d35c757b552a44e7413fc2d7`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 461.4 KB (461430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e98299083ecd07c280a3ad29d3e23fdd9b6b62b01c06164379c546feb334599`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 42.8 MB (42792514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004fa5b88695b49bd44f01244238389c5cfe10f27a9097309e6aa39e9a94779d`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:1ea0b25c3611919ecdf148563d4d8a72fff06fe37433a9f037977a3710a59433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfaddf282c8ac8a90fc84a4c29b420b23808d93ba5137af1907423f5159b2dc2`

```dockerfile
```

-	Layers:
	-	`sha256:e73fa92aa495e2c477df3ca9eaf8793d89a7a164440d9d53c9afbfb0faabbe76`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.35` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5fa72d8d2ae7a83fe6caaaf0da348c02dd7506dea208b8b45648f67a58e3c0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47282746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9834c39f0607d08a9e184b6913c5492d5ecd1ac05c3a93253120c34b97e2dd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84e353c8cb1f5fb57b56ad40d428e76ac886e0d6c13da80c91b169c4e809787`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 463.0 KB (462994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d60b3fc12278ac2a5f9ce1b48ada7c4f4d5a3bf2b27a59e41281d056c5ad767`  
		Last Modified: Wed, 28 Jan 2026 02:38:31 GMT  
		Size: 42.6 MB (42622292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693733590cef860ce7b8084c3d6f9a9da06db18cfea46c5c66698395e77f2c70`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:a4f33e252a2d22f38011a65014058bbe032afb1e256538a2d0ecc39fe1cc031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aecf21660742223941c89b0ac90d49fef61d72fb66c6dd668497b5f89f6bc4`

```dockerfile
```

-	Layers:
	-	`sha256:ff041315db89151f33827fa5b4c8d1bbdcf1667943dd96fc469d9176f702ce7c`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da432fc8bdf0e99119f830a5e7a36540750b612d2c642bf669754f774856a9c6`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.35` - linux; ppc64le

```console
$ docker pull traefik@sha256:ba1d0ef8f12d283ca9b9622e7ff8f8e4bd7393bca854ec1587173ac2321daf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2f811ce50d6e342494f89c95983176a88dcfe97ce9b1f3fc6d21b6dfeee398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 04:00:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 04:00:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:00:22 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 04:00:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1039e39cc46b6f1e1d99cf2d4e92f2d584ad42fb35d90c54f8774821a7f119`  
		Last Modified: Wed, 28 Jan 2026 04:01:14 GMT  
		Size: 41.0 MB (40952931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec62ead6c448599d750c453e6377a877a960b0c1c26e8a3cb6f0224eaf948dd1`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:2d6c5b0fddf8698a4717cd4702ba07bfac14339f4771103228d71384ff98e0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d2da991b59de4d4df0aa82d7b6f4b57690c61cf2686b09b7585caae09cfe15`

```dockerfile
```

-	Layers:
	-	`sha256:c8aa7e6b7bd0d2ca6530308301729284503ead7a79506d190ecc192bf9e58b8a`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26728fec798488598efe7a4e1faeb5d86cea7cfd465ae526b7b976065242d162`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.35` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:36 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.35` - linux; s390x

```console
$ docker pull traefik@sha256:3adc5b154d0b9eff4dc3f0c41150b6db6c6ada1298092215794f64a4c1da5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c5ce88b8f342d8239dc4eca55d22a04b8200c8f02fe7a85de5a5ec90151e31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:06:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:06:02 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:06:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999cb461062f5fb156b9f3c9b2b687a5eb86c5e89ea7bee7f9fd0645988a9617`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 461.7 KB (461734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acdd44168278ba562f227698748549c7bbcca2b2600de5da8811f18d2c064b5`  
		Last Modified: Wed, 28 Jan 2026 03:06:51 GMT  
		Size: 45.2 MB (45248293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d006bc7e2968e96d32ec16c4b9607c21a9173f1222254decae36989d0f1df22`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:13efae389f81475137ec6d31ed93bec8bd22775c7917a001a89ba3a9075a909f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddee29bb5465a0d60addada3740e0be6956cc6c6532a0f59a8376764df2d8fb3`

```dockerfile
```

-	Layers:
	-	`sha256:879dbe771db52c3ad517661f201e9d7cd19f415c5fc94236335313992e0395ea`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08394b52bf7ab24561ab804dca495746bed450019eda53b3c5186a1ef0d9f861`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.35-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11.35-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.35-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:2.11.35-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:140d1fe3ba042682b8c93e8d0fdff043f9d6b27654bd9e84599d7ed220cf2ec7
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:140d1fe3ba042682b8c93e8d0fdff043f9d6b27654bd9e84599d7ed220cf2ec7
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.7`

```console
$ docker pull traefik@sha256:140d1fe3ba042682b8c93e8d0fdff043f9d6b27654bd9e84599d7ed220cf2ec7
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

### `traefik:3.6.7` - linux; amd64

```console
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.7` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6.7-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6.7-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.7-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3.6.7-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:140d1fe3ba042682b8c93e8d0fdff043f9d6b27654bd9e84599d7ed220cf2ec7
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:fd45c6ea00e3c5d32bcf62fb3876aea090ba5fdbd5ae731bad48d35fb43ceb1a
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
$ docker pull traefik@sha256:612c89864e7ac32b573e7be254dd4c6b68e5d217d53e249bdf7503130aeb11de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51042502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df4bd8edf7db488f03c12d3ce0c62d324effa59761abc439622fcea5bedce65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:43 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c4ddced18ed75187de87b15a5d23e86ccd862033caa7e00d7181b6edeadc5`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 460.9 KB (460932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c574e4af8d35e3333ce42ac7a0739ac88eec4090aa8b204642fa4265b016ddd`  
		Last Modified: Wed, 28 Jan 2026 02:38:08 GMT  
		Size: 46.7 MB (46719380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14156968410c1e462e73d08ce573ce06e5c5e0969e5c76720019e86f4988b7`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:f19b06e1d234ffa2d151d45302d2f1cb7ae91e1fba9265c8b77eac2073222ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c612ac9bc3a1c8abf87667a76a1df19cec5d3d58c97de94d84a723a0acbd99ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3f6d6b78074aecea6293113e1b345379a4274c93c7ad0530b5a325ec6bedda`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e959a9417f0d4699dfd5d51998c6e7429b70515c75f60e6fed5f67a1b0311656`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:925796a4673bc537d65aa0ae0139fa65bf334bda6632743eeb911110ee205176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46824135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd966b67c3ff2a8e68273be9e3d20a21dc7d1ef10eb2fc10e8adb8459f4bc68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:39 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29939696f88331c61ec5e486fe45913d97a0310d35c757b552a44e7413fc2d7`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 461.4 KB (461430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e98299083ecd07c280a3ad29d3e23fdd9b6b62b01c06164379c546feb334599`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 42.8 MB (42792514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004fa5b88695b49bd44f01244238389c5cfe10f27a9097309e6aa39e9a94779d`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:1ea0b25c3611919ecdf148563d4d8a72fff06fe37433a9f037977a3710a59433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfaddf282c8ac8a90fc84a4c29b420b23808d93ba5137af1907423f5159b2dc2`

```dockerfile
```

-	Layers:
	-	`sha256:e73fa92aa495e2c477df3ca9eaf8793d89a7a164440d9d53c9afbfb0faabbe76`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5fa72d8d2ae7a83fe6caaaf0da348c02dd7506dea208b8b45648f67a58e3c0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47282746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9834c39f0607d08a9e184b6913c5492d5ecd1ac05c3a93253120c34b97e2dd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84e353c8cb1f5fb57b56ad40d428e76ac886e0d6c13da80c91b169c4e809787`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 463.0 KB (462994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d60b3fc12278ac2a5f9ce1b48ada7c4f4d5a3bf2b27a59e41281d056c5ad767`  
		Last Modified: Wed, 28 Jan 2026 02:38:31 GMT  
		Size: 42.6 MB (42622292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693733590cef860ce7b8084c3d6f9a9da06db18cfea46c5c66698395e77f2c70`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:a4f33e252a2d22f38011a65014058bbe032afb1e256538a2d0ecc39fe1cc031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aecf21660742223941c89b0ac90d49fef61d72fb66c6dd668497b5f89f6bc4`

```dockerfile
```

-	Layers:
	-	`sha256:ff041315db89151f33827fa5b4c8d1bbdcf1667943dd96fc469d9176f702ce7c`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da432fc8bdf0e99119f830a5e7a36540750b612d2c642bf669754f774856a9c6`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:ba1d0ef8f12d283ca9b9622e7ff8f8e4bd7393bca854ec1587173ac2321daf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2f811ce50d6e342494f89c95983176a88dcfe97ce9b1f3fc6d21b6dfeee398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 04:00:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 04:00:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:00:22 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 04:00:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1039e39cc46b6f1e1d99cf2d4e92f2d584ad42fb35d90c54f8774821a7f119`  
		Last Modified: Wed, 28 Jan 2026 04:01:14 GMT  
		Size: 41.0 MB (40952931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec62ead6c448599d750c453e6377a877a960b0c1c26e8a3cb6f0224eaf948dd1`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:2d6c5b0fddf8698a4717cd4702ba07bfac14339f4771103228d71384ff98e0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d2da991b59de4d4df0aa82d7b6f4b57690c61cf2686b09b7585caae09cfe15`

```dockerfile
```

-	Layers:
	-	`sha256:c8aa7e6b7bd0d2ca6530308301729284503ead7a79506d190ecc192bf9e58b8a`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26728fec798488598efe7a4e1faeb5d86cea7cfd465ae526b7b976065242d162`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:36 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:3adc5b154d0b9eff4dc3f0c41150b6db6c6ada1298092215794f64a4c1da5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c5ce88b8f342d8239dc4eca55d22a04b8200c8f02fe7a85de5a5ec90151e31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:06:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:06:02 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:06:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999cb461062f5fb156b9f3c9b2b687a5eb86c5e89ea7bee7f9fd0645988a9617`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 461.7 KB (461734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acdd44168278ba562f227698748549c7bbcca2b2600de5da8811f18d2c064b5`  
		Last Modified: Wed, 28 Jan 2026 03:06:51 GMT  
		Size: 45.2 MB (45248293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d006bc7e2968e96d32ec16c4b9607c21a9173f1222254decae36989d0f1df22`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:13efae389f81475137ec6d31ed93bec8bd22775c7917a001a89ba3a9075a909f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddee29bb5465a0d60addada3740e0be6956cc6c6532a0f59a8376764df2d8fb3`

```dockerfile
```

-	Layers:
	-	`sha256:879dbe771db52c3ad517661f201e9d7cd19f415c5fc94236335313992e0395ea`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08394b52bf7ab24561ab804dca495746bed450019eda53b3c5186a1ef0d9f861`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:140d1fe3ba042682b8c93e8d0fdff043f9d6b27654bd9e84599d7ed220cf2ec7
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:fd45c6ea00e3c5d32bcf62fb3876aea090ba5fdbd5ae731bad48d35fb43ceb1a
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
$ docker pull traefik@sha256:612c89864e7ac32b573e7be254dd4c6b68e5d217d53e249bdf7503130aeb11de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51042502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df4bd8edf7db488f03c12d3ce0c62d324effa59761abc439622fcea5bedce65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:43 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c4ddced18ed75187de87b15a5d23e86ccd862033caa7e00d7181b6edeadc5`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 460.9 KB (460932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c574e4af8d35e3333ce42ac7a0739ac88eec4090aa8b204642fa4265b016ddd`  
		Last Modified: Wed, 28 Jan 2026 02:38:08 GMT  
		Size: 46.7 MB (46719380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14156968410c1e462e73d08ce573ce06e5c5e0969e5c76720019e86f4988b7`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:f19b06e1d234ffa2d151d45302d2f1cb7ae91e1fba9265c8b77eac2073222ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c612ac9bc3a1c8abf87667a76a1df19cec5d3d58c97de94d84a723a0acbd99ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3f6d6b78074aecea6293113e1b345379a4274c93c7ad0530b5a325ec6bedda`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e959a9417f0d4699dfd5d51998c6e7429b70515c75f60e6fed5f67a1b0311656`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:925796a4673bc537d65aa0ae0139fa65bf334bda6632743eeb911110ee205176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46824135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd966b67c3ff2a8e68273be9e3d20a21dc7d1ef10eb2fc10e8adb8459f4bc68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:39 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29939696f88331c61ec5e486fe45913d97a0310d35c757b552a44e7413fc2d7`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 461.4 KB (461430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e98299083ecd07c280a3ad29d3e23fdd9b6b62b01c06164379c546feb334599`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 42.8 MB (42792514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004fa5b88695b49bd44f01244238389c5cfe10f27a9097309e6aa39e9a94779d`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:1ea0b25c3611919ecdf148563d4d8a72fff06fe37433a9f037977a3710a59433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfaddf282c8ac8a90fc84a4c29b420b23808d93ba5137af1907423f5159b2dc2`

```dockerfile
```

-	Layers:
	-	`sha256:e73fa92aa495e2c477df3ca9eaf8793d89a7a164440d9d53c9afbfb0faabbe76`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5fa72d8d2ae7a83fe6caaaf0da348c02dd7506dea208b8b45648f67a58e3c0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47282746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9834c39f0607d08a9e184b6913c5492d5ecd1ac05c3a93253120c34b97e2dd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84e353c8cb1f5fb57b56ad40d428e76ac886e0d6c13da80c91b169c4e809787`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 463.0 KB (462994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d60b3fc12278ac2a5f9ce1b48ada7c4f4d5a3bf2b27a59e41281d056c5ad767`  
		Last Modified: Wed, 28 Jan 2026 02:38:31 GMT  
		Size: 42.6 MB (42622292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693733590cef860ce7b8084c3d6f9a9da06db18cfea46c5c66698395e77f2c70`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:a4f33e252a2d22f38011a65014058bbe032afb1e256538a2d0ecc39fe1cc031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aecf21660742223941c89b0ac90d49fef61d72fb66c6dd668497b5f89f6bc4`

```dockerfile
```

-	Layers:
	-	`sha256:ff041315db89151f33827fa5b4c8d1bbdcf1667943dd96fc469d9176f702ce7c`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da432fc8bdf0e99119f830a5e7a36540750b612d2c642bf669754f774856a9c6`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:ba1d0ef8f12d283ca9b9622e7ff8f8e4bd7393bca854ec1587173ac2321daf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2f811ce50d6e342494f89c95983176a88dcfe97ce9b1f3fc6d21b6dfeee398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 04:00:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 04:00:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:00:22 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 04:00:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1039e39cc46b6f1e1d99cf2d4e92f2d584ad42fb35d90c54f8774821a7f119`  
		Last Modified: Wed, 28 Jan 2026 04:01:14 GMT  
		Size: 41.0 MB (40952931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec62ead6c448599d750c453e6377a877a960b0c1c26e8a3cb6f0224eaf948dd1`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:2d6c5b0fddf8698a4717cd4702ba07bfac14339f4771103228d71384ff98e0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d2da991b59de4d4df0aa82d7b6f4b57690c61cf2686b09b7585caae09cfe15`

```dockerfile
```

-	Layers:
	-	`sha256:c8aa7e6b7bd0d2ca6530308301729284503ead7a79506d190ecc192bf9e58b8a`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26728fec798488598efe7a4e1faeb5d86cea7cfd465ae526b7b976065242d162`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:36 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:3adc5b154d0b9eff4dc3f0c41150b6db6c6ada1298092215794f64a4c1da5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c5ce88b8f342d8239dc4eca55d22a04b8200c8f02fe7a85de5a5ec90151e31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:06:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:06:02 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:06:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999cb461062f5fb156b9f3c9b2b687a5eb86c5e89ea7bee7f9fd0645988a9617`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 461.7 KB (461734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acdd44168278ba562f227698748549c7bbcca2b2600de5da8811f18d2c064b5`  
		Last Modified: Wed, 28 Jan 2026 03:06:51 GMT  
		Size: 45.2 MB (45248293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d006bc7e2968e96d32ec16c4b9607c21a9173f1222254decae36989d0f1df22`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:13efae389f81475137ec6d31ed93bec8bd22775c7917a001a89ba3a9075a909f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddee29bb5465a0d60addada3740e0be6956cc6c6532a0f59a8376764df2d8fb3`

```dockerfile
```

-	Layers:
	-	`sha256:879dbe771db52c3ad517661f201e9d7cd19f415c5fc94236335313992e0395ea`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08394b52bf7ab24561ab804dca495746bed450019eda53b3c5186a1ef0d9f861`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:fd45c6ea00e3c5d32bcf62fb3876aea090ba5fdbd5ae731bad48d35fb43ceb1a
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
$ docker pull traefik@sha256:612c89864e7ac32b573e7be254dd4c6b68e5d217d53e249bdf7503130aeb11de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51042502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df4bd8edf7db488f03c12d3ce0c62d324effa59761abc439622fcea5bedce65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:43 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c4ddced18ed75187de87b15a5d23e86ccd862033caa7e00d7181b6edeadc5`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 460.9 KB (460932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c574e4af8d35e3333ce42ac7a0739ac88eec4090aa8b204642fa4265b016ddd`  
		Last Modified: Wed, 28 Jan 2026 02:38:08 GMT  
		Size: 46.7 MB (46719380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14156968410c1e462e73d08ce573ce06e5c5e0969e5c76720019e86f4988b7`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:f19b06e1d234ffa2d151d45302d2f1cb7ae91e1fba9265c8b77eac2073222ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c612ac9bc3a1c8abf87667a76a1df19cec5d3d58c97de94d84a723a0acbd99ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3f6d6b78074aecea6293113e1b345379a4274c93c7ad0530b5a325ec6bedda`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e959a9417f0d4699dfd5d51998c6e7429b70515c75f60e6fed5f67a1b0311656`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:925796a4673bc537d65aa0ae0139fa65bf334bda6632743eeb911110ee205176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46824135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd966b67c3ff2a8e68273be9e3d20a21dc7d1ef10eb2fc10e8adb8459f4bc68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:39 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29939696f88331c61ec5e486fe45913d97a0310d35c757b552a44e7413fc2d7`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 461.4 KB (461430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e98299083ecd07c280a3ad29d3e23fdd9b6b62b01c06164379c546feb334599`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 42.8 MB (42792514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004fa5b88695b49bd44f01244238389c5cfe10f27a9097309e6aa39e9a94779d`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:1ea0b25c3611919ecdf148563d4d8a72fff06fe37433a9f037977a3710a59433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfaddf282c8ac8a90fc84a4c29b420b23808d93ba5137af1907423f5159b2dc2`

```dockerfile
```

-	Layers:
	-	`sha256:e73fa92aa495e2c477df3ca9eaf8793d89a7a164440d9d53c9afbfb0faabbe76`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5fa72d8d2ae7a83fe6caaaf0da348c02dd7506dea208b8b45648f67a58e3c0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47282746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9834c39f0607d08a9e184b6913c5492d5ecd1ac05c3a93253120c34b97e2dd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84e353c8cb1f5fb57b56ad40d428e76ac886e0d6c13da80c91b169c4e809787`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 463.0 KB (462994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d60b3fc12278ac2a5f9ce1b48ada7c4f4d5a3bf2b27a59e41281d056c5ad767`  
		Last Modified: Wed, 28 Jan 2026 02:38:31 GMT  
		Size: 42.6 MB (42622292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693733590cef860ce7b8084c3d6f9a9da06db18cfea46c5c66698395e77f2c70`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a4f33e252a2d22f38011a65014058bbe032afb1e256538a2d0ecc39fe1cc031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aecf21660742223941c89b0ac90d49fef61d72fb66c6dd668497b5f89f6bc4`

```dockerfile
```

-	Layers:
	-	`sha256:ff041315db89151f33827fa5b4c8d1bbdcf1667943dd96fc469d9176f702ce7c`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da432fc8bdf0e99119f830a5e7a36540750b612d2c642bf669754f774856a9c6`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:ba1d0ef8f12d283ca9b9622e7ff8f8e4bd7393bca854ec1587173ac2321daf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2f811ce50d6e342494f89c95983176a88dcfe97ce9b1f3fc6d21b6dfeee398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 04:00:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 04:00:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:00:22 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 04:00:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1039e39cc46b6f1e1d99cf2d4e92f2d584ad42fb35d90c54f8774821a7f119`  
		Last Modified: Wed, 28 Jan 2026 04:01:14 GMT  
		Size: 41.0 MB (40952931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec62ead6c448599d750c453e6377a877a960b0c1c26e8a3cb6f0224eaf948dd1`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:2d6c5b0fddf8698a4717cd4702ba07bfac14339f4771103228d71384ff98e0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d2da991b59de4d4df0aa82d7b6f4b57690c61cf2686b09b7585caae09cfe15`

```dockerfile
```

-	Layers:
	-	`sha256:c8aa7e6b7bd0d2ca6530308301729284503ead7a79506d190ecc192bf9e58b8a`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26728fec798488598efe7a4e1faeb5d86cea7cfd465ae526b7b976065242d162`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:36 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:3adc5b154d0b9eff4dc3f0c41150b6db6c6ada1298092215794f64a4c1da5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c5ce88b8f342d8239dc4eca55d22a04b8200c8f02fe7a85de5a5ec90151e31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:06:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:06:02 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:06:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999cb461062f5fb156b9f3c9b2b687a5eb86c5e89ea7bee7f9fd0645988a9617`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 461.7 KB (461734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acdd44168278ba562f227698748549c7bbcca2b2600de5da8811f18d2c064b5`  
		Last Modified: Wed, 28 Jan 2026 03:06:51 GMT  
		Size: 45.2 MB (45248293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d006bc7e2968e96d32ec16c4b9607c21a9173f1222254decae36989d0f1df22`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:13efae389f81475137ec6d31ed93bec8bd22775c7917a001a89ba3a9075a909f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddee29bb5465a0d60addada3740e0be6956cc6c6532a0f59a8376764df2d8fb3`

```dockerfile
```

-	Layers:
	-	`sha256:879dbe771db52c3ad517661f201e9d7cd19f415c5fc94236335313992e0395ea`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08394b52bf7ab24561ab804dca495746bed450019eda53b3c5186a1ef0d9f861`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.35`

```console
$ docker pull traefik@sha256:fd45c6ea00e3c5d32bcf62fb3876aea090ba5fdbd5ae731bad48d35fb43ceb1a
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

### `traefik:v2.11.35` - linux; amd64

```console
$ docker pull traefik@sha256:612c89864e7ac32b573e7be254dd4c6b68e5d217d53e249bdf7503130aeb11de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51042502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df4bd8edf7db488f03c12d3ce0c62d324effa59761abc439622fcea5bedce65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:43 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c4ddced18ed75187de87b15a5d23e86ccd862033caa7e00d7181b6edeadc5`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 460.9 KB (460932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c574e4af8d35e3333ce42ac7a0739ac88eec4090aa8b204642fa4265b016ddd`  
		Last Modified: Wed, 28 Jan 2026 02:38:08 GMT  
		Size: 46.7 MB (46719380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14156968410c1e462e73d08ce573ce06e5c5e0969e5c76720019e86f4988b7`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:f19b06e1d234ffa2d151d45302d2f1cb7ae91e1fba9265c8b77eac2073222ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c612ac9bc3a1c8abf87667a76a1df19cec5d3d58c97de94d84a723a0acbd99ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3f6d6b78074aecea6293113e1b345379a4274c93c7ad0530b5a325ec6bedda`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e959a9417f0d4699dfd5d51998c6e7429b70515c75f60e6fed5f67a1b0311656`  
		Last Modified: Wed, 28 Jan 2026 02:38:07 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.35` - linux; arm variant v6

```console
$ docker pull traefik@sha256:925796a4673bc537d65aa0ae0139fa65bf334bda6632743eeb911110ee205176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46824135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd966b67c3ff2a8e68273be9e3d20a21dc7d1ef10eb2fc10e8adb8459f4bc68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:39 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29939696f88331c61ec5e486fe45913d97a0310d35c757b552a44e7413fc2d7`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 461.4 KB (461430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e98299083ecd07c280a3ad29d3e23fdd9b6b62b01c06164379c546feb334599`  
		Last Modified: Wed, 28 Jan 2026 02:56:48 GMT  
		Size: 42.8 MB (42792514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004fa5b88695b49bd44f01244238389c5cfe10f27a9097309e6aa39e9a94779d`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:1ea0b25c3611919ecdf148563d4d8a72fff06fe37433a9f037977a3710a59433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfaddf282c8ac8a90fc84a4c29b420b23808d93ba5137af1907423f5159b2dc2`

```dockerfile
```

-	Layers:
	-	`sha256:e73fa92aa495e2c477df3ca9eaf8793d89a7a164440d9d53c9afbfb0faabbe76`  
		Last Modified: Wed, 28 Jan 2026 02:56:47 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.35` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5fa72d8d2ae7a83fe6caaaf0da348c02dd7506dea208b8b45648f67a58e3c0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47282746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9834c39f0607d08a9e184b6913c5492d5ecd1ac05c3a93253120c34b97e2dd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84e353c8cb1f5fb57b56ad40d428e76ac886e0d6c13da80c91b169c4e809787`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 463.0 KB (462994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d60b3fc12278ac2a5f9ce1b48ada7c4f4d5a3bf2b27a59e41281d056c5ad767`  
		Last Modified: Wed, 28 Jan 2026 02:38:31 GMT  
		Size: 42.6 MB (42622292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693733590cef860ce7b8084c3d6f9a9da06db18cfea46c5c66698395e77f2c70`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:a4f33e252a2d22f38011a65014058bbe032afb1e256538a2d0ecc39fe1cc031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aecf21660742223941c89b0ac90d49fef61d72fb66c6dd668497b5f89f6bc4`

```dockerfile
```

-	Layers:
	-	`sha256:ff041315db89151f33827fa5b4c8d1bbdcf1667943dd96fc469d9176f702ce7c`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da432fc8bdf0e99119f830a5e7a36540750b612d2c642bf669754f774856a9c6`  
		Last Modified: Wed, 28 Jan 2026 02:38:30 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.35` - linux; ppc64le

```console
$ docker pull traefik@sha256:ba1d0ef8f12d283ca9b9622e7ff8f8e4bd7393bca854ec1587173ac2321daf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2f811ce50d6e342494f89c95983176a88dcfe97ce9b1f3fc6d21b6dfeee398`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 04:00:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 04:00:22 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 04:00:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 04:00:22 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 04:00:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1039e39cc46b6f1e1d99cf2d4e92f2d584ad42fb35d90c54f8774821a7f119`  
		Last Modified: Wed, 28 Jan 2026 04:01:14 GMT  
		Size: 41.0 MB (40952931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec62ead6c448599d750c453e6377a877a960b0c1c26e8a3cb6f0224eaf948dd1`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:2d6c5b0fddf8698a4717cd4702ba07bfac14339f4771103228d71384ff98e0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d2da991b59de4d4df0aa82d7b6f4b57690c61cf2686b09b7585caae09cfe15`

```dockerfile
```

-	Layers:
	-	`sha256:c8aa7e6b7bd0d2ca6530308301729284503ead7a79506d190ecc192bf9e58b8a`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26728fec798488598efe7a4e1faeb5d86cea7cfd465ae526b7b976065242d162`  
		Last Modified: Wed, 28 Jan 2026 04:01:13 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.35` - linux; riscv64

```console
$ docker pull traefik@sha256:1bb550f23710150a0f8629759ca269686be18835c93a120c8a1042697c00f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49370747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855538d46c2caca4847e9347abff49de20a54de7084dfb06518a84f8741642a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:43:12 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:43:12 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:43:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c89edb9cec0112584aaefe2c3feb8fdca4cc93696fb4509d5fe167782dd14`  
		Last Modified: Sun, 18 Jan 2026 21:48:36 GMT  
		Size: 45.3 MB (45325181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7364b694a7c94a209a40e6c4b6ae7889df7df47114744c8fc0d2790458263e0`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:65366d6b2445130003ed8f8703a47de058250a5597e5f951f693aca20914888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240e9bb617ddcbe998d89cd408903fbee1c4c5d8517062f55f13815c041fc2a`

```dockerfile
```

-	Layers:
	-	`sha256:3fc64f0d8cea94f66131ab104ea1633a2dea5b3587a364690cd15e4804e923a9`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b567289c2ce260f593e61636c160970eabeafc9134517df0ced1beeb368905`  
		Last Modified: Sun, 18 Jan 2026 21:48:29 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.35` - linux; s390x

```console
$ docker pull traefik@sha256:3adc5b154d0b9eff4dc3f0c41150b6db6c6ada1298092215794f64a4c1da5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c5ce88b8f342d8239dc4eca55d22a04b8200c8f02fe7a85de5a5ec90151e31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:06:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:06:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:06:02 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:06:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999cb461062f5fb156b9f3c9b2b687a5eb86c5e89ea7bee7f9fd0645988a9617`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 461.7 KB (461734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acdd44168278ba562f227698748549c7bbcca2b2600de5da8811f18d2c064b5`  
		Last Modified: Wed, 28 Jan 2026 03:06:51 GMT  
		Size: 45.2 MB (45248293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d006bc7e2968e96d32ec16c4b9607c21a9173f1222254decae36989d0f1df22`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.35` - unknown; unknown

```console
$ docker pull traefik@sha256:13efae389f81475137ec6d31ed93bec8bd22775c7917a001a89ba3a9075a909f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddee29bb5465a0d60addada3740e0be6956cc6c6532a0f59a8376764df2d8fb3`

```dockerfile
```

-	Layers:
	-	`sha256:879dbe771db52c3ad517661f201e9d7cd19f415c5fc94236335313992e0395ea`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08394b52bf7ab24561ab804dca495746bed450019eda53b3c5186a1ef0d9f861`  
		Last Modified: Wed, 28 Jan 2026 03:06:50 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.35-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b04ad5acec3c2dad74099933aa88d46fba8191ff72ce1b571fbdb9484456e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11.35-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:1928bb31f9725da9dd8fb069d66216f5ac70678b4c37d088d8b7321abe3dc2a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174213581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4369e96d7e35e05b7a89c9e27ce80566cbb9435d8d2d4d719b3c563668a833`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:47:19 GMT
RUN cmd /S /C #(nop) COPY file:ca82921d2032fa5b8ee65273c6fc351bb0537191d1a25030286c1896d98a0a9a in \ 
# Wed, 14 Jan 2026 19:47:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:47:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:47:22 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d4d3d461436674bef507cb50e4d9893e0a7b8e77c72c2a02d7c46fecd31f3`  
		Last Modified: Wed, 14 Jan 2026 19:47:56 GMT  
		Size: 47.5 MB (47513573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba506580710ab71d2679e0af02e8aa1d653092e8b8e67f890541015594af69`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782183109822a540f7709b4e364ab1256aedc8d2408a8aefd41a319e324237b`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f738b5878e4d3675d23d3565d626c723439fed2a673c7de178be99cb3693db5`  
		Last Modified: Wed, 14 Jan 2026 19:47:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.35-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e92c135e15b2a35aa4c887b2c5b4d345ffff4273264b6512239ebf59154ee7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2.11.35-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:950e52c00b25ccd158cd37afb3bceb0cc166233ca39eb7f75a4d75cf1aa6ec9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883800950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1451ac18f9fad230040dedad2bf2c36a205722b0ff35f3107ca1fc6548e2c1b8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 18:02:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:03:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.35/traefik_v2.11.35_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:03:58 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:04:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:04:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.35 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d55a3b703ec4a5271eedc5a26f3a3dceaee707add239883d28583f9ecafa4e1`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb461075d3a8f940e4306e47ace0ecd50811e2c5e36003493b0831fa0423832d`  
		Last Modified: Wed, 14 Jan 2026 18:04:56 GMT  
		Size: 48.1 MB (48136547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea01129fedb7f368e0625bf4754b34c18d4d32ec5914f3cda5bc72f55196d6`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c380d9fda086e65cd87431ca1a9a976f208184a791727330f128c4792e2c7`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df31d1b75121595c986af5e7bc72f907314612fc0a55e96548907e974b3dd46`  
		Last Modified: Wed, 14 Jan 2026 18:04:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:140d1fe3ba042682b8c93e8d0fdff043f9d6b27654bd9e84599d7ed220cf2ec7
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:140d1fe3ba042682b8c93e8d0fdff043f9d6b27654bd9e84599d7ed220cf2ec7
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
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.7`

```console
$ docker pull traefik@sha256:140d1fe3ba042682b8c93e8d0fdff043f9d6b27654bd9e84599d7ed220cf2ec7
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

### `traefik:v3.6.7` - linux; amd64

```console
$ docker pull traefik@sha256:7e35533bb474b848dc796ea34d53fbde8c22b1040bf8226ecb5876378b9ea950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52180450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91528df1690f7da08360dcbbcb92b3ea483eeceb9f136d309f17506a5bd3f58d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:09 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:37:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:37:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:11 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:37:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef63511ea6cc551df1833d4a4c9137344cad4bdad0a04b38b17af1d2f50b90bb`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 460.9 KB (460945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738e5cb835ebe5aa828cfcc67fa8911a3f1af6ab778a94684287e1800e952a4`  
		Last Modified: Wed, 28 Jan 2026 02:37:35 GMT  
		Size: 47.9 MB (47857314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6813f70c64beb361b343bcb3993b2ceb053e9a835463e271f3e17dc2b2d075`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:8c9968aba234f00db1347ff7dabf197cef9f014fb57f058b797a413299584996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2c451eeeac76e6f100115f164413d1fed17b1accbf32782a3e9a53f66121c`

```dockerfile
```

-	Layers:
	-	`sha256:de090bfc966b5574411f420b20c7b3193a519a0b7ae18461edd119467ffc097c`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 843.1 KB (843104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaf3d82f8b8a4dd904f83dfe80996a47ede9cd049c4726403c531ddcee1b572`  
		Last Modified: Wed, 28 Jan 2026 02:37:33 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f446661f1b8df612bcc1552d58bc3f6dd2055b9a4cb63d217f040ddf86c3c6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47437542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cd7b4df27afd4cd61fd39b0b2aa6e289d618cab6c60cd1cb85f406ec177ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:56:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:26 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:56:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5555c7bebfb94b8d544821979750e16a6d7821c7b325e99c01b3abbe8c886b5`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 461.4 KB (461439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ed4616733c80c040c885ac938f5364ecb88bb05c57d4f7939a9397a66277d9`  
		Last Modified: Wed, 28 Jan 2026 02:56:36 GMT  
		Size: 43.4 MB (43405912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2991dff0e77855b33c79d3dd3f8a087cc2b5cb444c2fe8a9f7c08f8fea75e`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:2257fdac009f128474135d8b7fb1ae3a2fe444cdd1715bd08d36d4f3c1d760f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d9334c83d2f902ee95329754982c0fd8839ef6a98846ab694a0deb117dce55`

```dockerfile
```

-	Layers:
	-	`sha256:bb0407ccaa0ebcb7f6f822104499a36b8e679f36d4c617b8f2eb29743ac907f9`  
		Last Modified: Wed, 28 Jan 2026 02:56:34 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:08e593279b2b9bb05485c2634d2827da71248a6763cb34cb5c59a43af9175936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26afdb0ffcf732789f136d219cad2d4eb403d3afa6e738c37578722327ca8a1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:04 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 02:38:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 02:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:38:07 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 02:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f08b87113335320dcad70226846e60536dd465db5333542a79403ac6eb050d`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 463.0 KB (462965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cc2ea807a49fcbd3b468fde1ddc8269e1b6922993eae0d08af0e28b8a0b0f8`  
		Last Modified: Wed, 28 Jan 2026 02:38:34 GMT  
		Size: 43.5 MB (43459939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265091c8315e6086a6f38b68ac2d457c7a0c4bb9f7049c6019190d3260e3b48`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:048a869435912cbffe845a38d473dd09d85ddd07c2a813a5228816446d515474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8111883e97b30ac92a263c69daccc02fe821ecd271435bedbf763f0ab6f7a2bc`

```dockerfile
```

-	Layers:
	-	`sha256:d51472638ba10f293357b82b83018f90ab765299b12387c8126efaf64eae1aaf`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 842.6 KB (842558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11638e8c5137ab8d57e5d459213b51c6ecce73ebdf7dd698532e80e8b0ab1d6c`  
		Last Modified: Wed, 28 Jan 2026 02:38:33 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; ppc64le

```console
$ docker pull traefik@sha256:85ee0ef4d55d1b2663e0bb8bba052b239f26c2437ecc033d15f8159005cfa6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45598510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc88c1f92e51294531818e8a182c61e0edc86abe2f8679865e945a47b905661f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:59:36 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:59:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:59:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:59:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:59:41 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:59:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9af28832adf73eec0e9a821c28620a6fb0f3c567424390e6c50cf548f93c0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 463.5 KB (463517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446f8f0e07efe54b8c73ae9fd01274e2b5148fdb6e5a9b8bdde07b8a5f32841`  
		Last Modified: Wed, 28 Jan 2026 04:00:40 GMT  
		Size: 41.3 MB (41304981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774843020142e4920492071fff9f88c4042fdeecddc96978c9fa92b8b5a09ff1`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:dc92a19520c1c4e1c827b02350df9256cbcc19d9c2c91d22682f74a5c3db2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435a2ac9750eaf0d3c154f52472946d42c018e3a236f4296d1afa8772272be5`

```dockerfile
```

-	Layers:
	-	`sha256:acc55be44af45a67bc9e29c2a3978d13f3554a8cb5b66dfdf427099ea6084a1b`  
		Last Modified: Wed, 28 Jan 2026 04:00:42 GMT  
		Size: 842.5 KB (842511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ebfef096aaebbacbd4ab557ae4fd6f66f57d19255bf65c456f5496584f7cb0`  
		Last Modified: Wed, 28 Jan 2026 04:00:36 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; riscv64

```console
$ docker pull traefik@sha256:004ed5d75082b8078360a8ca2f6f17ebc1c8e2cd01fa796bf74a4a6e690d038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e543b7f47b91758c1e3d680ebcf79774270c525bea9e7134f95946ff4a937fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Sun, 18 Jan 2026 21:37:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
COPY entrypoint.sh / # buildkit
# Sun, 18 Jan 2026 21:37:22 GMT
EXPOSE map[80/tcp:{}]
# Sun, 18 Jan 2026 21:37:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 18 Jan 2026 21:37:22 GMT
CMD ["traefik"]
# Sun, 18 Jan 2026 21:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6050919dcc147463011bfb7da4ddca06017004c11be2a6a0c980c90384f8`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 461.3 KB (461258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbb293ec8439ba983be91d39ac2c4cf81a68affcf9c67c5fe1652b102fc8b4`  
		Last Modified: Sun, 18 Jan 2026 21:42:32 GMT  
		Size: 46.3 MB (46288071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e00a6a754f5ce20d032e02ab76461193be533319714d2069b2a3bad90001d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:8e76fe3daf885cfe4c45c1625155941824d1da253a05a2b5a8e862b807e3e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8222691b871221146b165e35a26c4ab4b27ef26aef5a7f5493d2bd44381b1`

```dockerfile
```

-	Layers:
	-	`sha256:db4d4f4cec2855a7b42d89e132cb4db5364b111a5a7407815666568b1111a00d`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd053e3102bd3d2f0e7332831bb27c6800fe2f11acc7ec4e37734069df9584`  
		Last Modified: Sun, 18 Jan 2026 21:42:25 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.7` - linux; s390x

```console
$ docker pull traefik@sha256:6221de4db419ed9e451d2d1e612ca4fce29b94c81ccf9b8c5ff8f382134c4c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50325014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2ae6473e8713a3fcde5a759f712e5539b3e2a4f9d9fbf94401c4803ae3769`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 28 Jan 2026 03:05:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 28 Jan 2026 03:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:58 GMT
CMD ["traefik"]
# Wed, 28 Jan 2026 03:05:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ca57aba8cfcfa12eb156a94d0295c7489ec6231dc03e5e49f4add2a7b404c`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 461.7 KB (461722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da2dce8c6c65a0b37684d43fabdaa27953d5fba743c3c9ac4cbcd4b1956321f`  
		Last Modified: Wed, 28 Jan 2026 03:06:48 GMT  
		Size: 46.1 MB (46137589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf497f1afb91c76487418a1a777a527e647ab749dc33f27f3f13d3ce54071a2`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.7` - unknown; unknown

```console
$ docker pull traefik@sha256:2b3b5f130e36d06c951effbe08fc40c48cbf9cf4641989a8a7ccd743d1e389df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a643e4280f172c4aee8f9dd31eba2a13c4d79f4e3b4a5c54d915a6fdb533dcf`

```dockerfile
```

-	Layers:
	-	`sha256:d3a8aa2b0cf3d33165892df90fe4ccf6bfe060185d4b0520648d1f3aad12a344`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 842.5 KB (842453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c5f235c7cfc8c8767f5e3ec1350298bc88906cc55cd4b154dbec13a3941416`  
		Last Modified: Wed, 28 Jan 2026 03:06:47 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6.7-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:70ab03badc6bd7b609c0d4b064968a2abd6303d95f301679318595eb7b652ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6.7-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:84f61eff044e06cbccd14c57a6810a756ac1aca95cd81b60b4fa4d1f3b3d2cc4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175315505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c270c622d0b442b0943d6e0f675fb670dc919c610f34cb0745ca8725e510a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Wed, 14 Jan 2026 19:45:39 GMT
RUN cmd /S /C #(nop) COPY file:383ec3f9f7f20a8b5d30f0773ac25dddea172011225bfe7e8e5dc613804e0c7e in \ 
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 14 Jan 2026 19:45:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 19:45:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c6d167a3eb8d9ce763b64a7aa6fe1e5dc9849ebed072a5a8d14d32c497ee6`  
		Last Modified: Wed, 14 Jan 2026 19:46:23 GMT  
		Size: 48.6 MB (48615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30356d58936c9746b91cb07a9eb9e8ee4850fdab81e5f7965ec355a8da03f3c0`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7c16f3a5ef4a2619c20a73f3e695f97ed4d015c292461720d358828a5da46a`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28ced4369f147f14d7146eef947ff8b477b540582b58b43dcdf24c6234999c`  
		Last Modified: Wed, 14 Jan 2026 19:45:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.7-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3.6.7-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
