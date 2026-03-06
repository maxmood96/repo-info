<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.40`](#traefik21140)
-	[`traefik:2.11.40-nanoserver-ltsc2022`](#traefik21140-nanoserver-ltsc2022)
-	[`traefik:2.11.40-windowsservercore-ltsc2022`](#traefik21140-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.10`](#traefik3610)
-	[`traefik:3.6.10-nanoserver-ltsc2022`](#traefik3610-nanoserver-ltsc2022)
-	[`traefik:3.6.10-windowsservercore-ltsc2022`](#traefik3610-windowsservercore-ltsc2022)
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
-	[`traefik:v2.11.40`](#traefikv21140)
-	[`traefik:v2.11.40-nanoserver-ltsc2022`](#traefikv21140-nanoserver-ltsc2022)
-	[`traefik:v2.11.40-windowsservercore-ltsc2022`](#traefikv21140-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.10`](#traefikv3610)
-	[`traefik:v3.6.10-nanoserver-ltsc2022`](#traefikv3610-nanoserver-ltsc2022)
-	[`traefik:v3.6.10-windowsservercore-ltsc2022`](#traefikv3610-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:ad45e9eb6b148c6bc8d5dbe309412758d48d6027a37591057dc9d10fbfbe8ce5
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
$ docker pull traefik@sha256:4141f960ad1b2bfb6db4477bb162b22b74b4d2839bc1905e575aa987f8ce5032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51145725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e9a734e01337937b46e3fcde49fae6bb79d28126a6b9140ed666aab57a3af4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:54 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8d06f077ce014df93e73f77690387672dc9cc78186d2a9ad0b4fb620337fc5`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ffd095d3fef7be59b8e14b32c70ec50befe38ddbc6f888555a237d79b70d9`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 46.8 MB (46822592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36e028fc4795bea8f579b917962797c6994254329797c1f89d4a83ba373c7c`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:95a6b90bf617399b9c2565747ce9f2efe5b640b3dd973cd1f6ec2c2ab0a2bbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7814ec727ce635b406ebbc8e83a5d0805ceda8ce9a92e3ef1e6d377fa2b418bd`

```dockerfile
```

-	Layers:
	-	`sha256:e256ce114d98ecce6fdb27ae2bec60c08b3ab36ecb0f8b02749c3024a1305032`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69809d5af32da74f52b27b2cd0426c2c4d151bc5a4ac0a7ce99994ee66cf9dde`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:16cf819f2106576f1565b00cdf5589d0b5864a6b77ebaf45f4e30e1779b71b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e24f6c9a1ddcca343a996f7700f73707ec76eb70ea8b1faaf5049973e8586a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:38:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:38:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:38:20 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:38:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b51f970aca5177f1c85670a1603f0a0834d4cd4f93330cbac83f2c4f02e5225`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 461.4 KB (461438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7437a937530c084868102dadfcce425b3027b6408b8af33d980d814acba8b1`  
		Last Modified: Mon, 23 Feb 2026 21:38:29 GMT  
		Size: 42.9 MB (42852924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc245d5cb31da9dfc449bb660c82e9c888374b34f3856a32bf16390be1d39a7b`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:82e9d4ce47fe616d8257c2ef66ab777e9b31f92ee2449d7e45dc3b8c592a7c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7c55570778ab767c4151133be0792b4349d6319bcd2eaa7b4530fcfeb6b143`

```dockerfile
```

-	Layers:
	-	`sha256:a6620a90c2a22aaed3d56d2177be622f834fdf99a613d0915991b74400cf7ce9`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ec7bea4106e542d9047d61e154377013309322d2c4191cfc375f62bfafc058cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda5d86ee7ae74add53acd5b8ac5e18a98538566a3490988d11c685b8f5611ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:54 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21ee00ee287ddba3c5f811d4fe3d4419fccf30b6da5594f633472149eb8f013`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 463.0 KB (463008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2a60bf8dad1a0ac1bd069416701bcef22f4356794a94cde84ddd68536c5547`  
		Last Modified: Mon, 23 Feb 2026 21:38:21 GMT  
		Size: 42.1 MB (42109649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3010a02494f4b334b5b0e89ae86a18b5e320986cb9658a4cfccd0c6470107c8`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:7e45226ca8fb85ca74be88d9daea4639030da6a014bb8f0a1fd85c29dfa181e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c4381bfa18706fb2e6c136afe0113af6d6e2dc0fe00635b4c41ea93b8d3096`

```dockerfile
```

-	Layers:
	-	`sha256:b753ca3720bdb9d1de7c0600f8b05e0480f3a00a0e1e72ff793c9ce9bae77166`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94b5249558a368503a5afe7219a4ab573549a088a5952bd569cc35ea0d15d64`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:72de49b4971a323c5103a5efe288ee54399afe509d2339b5a9692b65975c219f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45356377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92127bfce7e47062db8059d6c02532e78775b89032047392236a5c10d0470d59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:44:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:44:45 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:44:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacf6756ca01da33eb1343fdb73db24339fd265d16ff1965f43b4032d82cd243`  
		Last Modified: Mon, 23 Feb 2026 21:45:48 GMT  
		Size: 41.1 MB (41062851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02ee61e2b5b77e97afbde074c5ca9d54280cadb0cb991a7abf7fa9006864ae`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:2393f4c9f1dbf83604afd8b4fa2b571e79b6c5287adf3cf930e99e61fc04e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc4ddf685452e799c5634717258cdc230553ba9b8d768d10264d09486bb5029`

```dockerfile
```

-	Layers:
	-	`sha256:b8ea2037120aa249714dd86f276402bdd22c8b8eab17e5000b6a59bbe7fdd08a`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17b0315d942408852fa446dcf22fb94577f8915c321a387bb7d79b4baf5f899`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:a35906bd691d546f5f2e946cac7b936a15ac51741508fbe36030661254790345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49473089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ad32cf8a10e3c697da7833bbedc3e11658766ac5cc2904be9f6d2eeff89270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:35:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
COPY entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:41:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 02:41:07 GMT
CMD ["traefik"]
# Tue, 24 Feb 2026 02:41:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e83e761e01f3ced55ef589660d62f3c7d941ba7c2bf18c026865126d409786`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2186276b174c86d37e4ae11e54a01e251a717eca87f0993c49a8a4abedb24705`  
		Last Modified: Tue, 24 Feb 2026 02:46:43 GMT  
		Size: 45.4 MB (45426242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7513d805749fba192cc532f7103babe6a13c70186119d9ad6a0e7362ee1d55`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:7fef2a04689e4c67b0b42d72a249cc3163f0aba8f0f2c7c4ecb279cfe3eb349d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6a71286171cc27109fee46fd4a02f2318a98a9672374670278b7aaceb4df14`

```dockerfile
```

-	Layers:
	-	`sha256:532c1b6978ded6fce46417b850b382f63f97aa83272bb6b63bfd429c98b04299`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e95c23fd3cc7af894d84f15b318b8381a3d031e9eb91b9dfa711e96dcf892ee`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:a5988cbb5582492f1a2c5860fe56c6fc34938c3bfa6ccc1620b05309d8e0c3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc93fe72a392e79fad47adb2a2976ed17a9e64af402dc168c087b8e6c96f5f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:39:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:40:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:40:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:40:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:40:05 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:40:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d77e277fa279c36b8a085ad39126da33bbede7e3cbe43a763eee1f9849ee11`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659eef48f55c32dafa6a449e605b8d0d3de25c662750b490210c2720a88e3060`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 45.3 MB (45289986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2fbd1160ca187b67fad3741295a22c0af10af653ca5640f88225d6e7505af0`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:e6f4126f8cc3fa5bd9a1ffd96afb31ec65972ce0eb2427a1456ee8c120c82e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8615db22523e5244a9ef2ce1dce4617c1c2fd20b2c0caef74bf4eeb1575d1`

```dockerfile
```

-	Layers:
	-	`sha256:acb9966b442f02f629d740055523bf01a7152d3670318cb6e67f47e757db8ed5`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d9e95be229d8aa7ed4fd70986a3c0c801f4d0b714bcac7517e872d1c632988`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:7a6d25af24298fdc59743425013802aa5f2da412121c1d52c42b1cc6e37b1f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:a51c805def98e1f8322d6e6216c8358df9f2482b9a446294b2e414ce2aceb544
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174284684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae00e14ed1c16c67180ea15a3101c85fd9894181e9cca64b022ec49f6f8a28b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 23 Feb 2026 22:10:43 GMT
RUN cmd /S /C #(nop) COPY file:677dd367ef885b943dfeb7dd6ae0505d21cacfee88c63efbfbd88e9aee14c18d in \ 
# Mon, 23 Feb 2026 22:10:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 23 Feb 2026 22:10:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 22:10:46 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38872888f2a7acde41b46ea37df53faa6e940850e2875068d96b756aa128a025`  
		Last Modified: Mon, 23 Feb 2026 22:11:32 GMT  
		Size: 47.6 MB (47635651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730f883abb10d33a1c4c2cc5eae6af7cfdc6080f993edc33f0725ddd10352268`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb23bb5e3066dfab26dddcc8f3fe310aef5129b939a7a71b93e5f1b62c7d1162`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7fadbaae6496d12c6ec4be179ae3ff5f594823ab4f831e480ef7dc736b5d33`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d11d387d1179524ecae4286fa59e0f827ab2351b4f87edcccd387ddb5ebd27a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:0e66061ff5f34964b89b047d1b3bf7a5d393bc949401811861a7164e718b9764
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910925531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fed6bd3d0f8ac52b59d3c3031e71cb5f2968b62b9efa8d60a45cb854131211`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:58:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:58:14 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:58:15 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:58:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb0a7566470e7fbec32969b07e4506fc816e4242492998a86b3379b2ba4c42`  
		Last Modified: Mon, 23 Feb 2026 21:58:58 GMT  
		Size: 48.3 MB (48263149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e503c1b5ea41e32b44fbdc3ede2779cf63ca6ca4179f183904eeedeb9f26d95a`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468357667205af6c0aaac8d3cc15777aaffc40f4fcdb68cb646cb03908cf67d`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4d7fba6084228c469070092a0ca19a95673fc988c5427acf52be6ad2c49945`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:ad45e9eb6b148c6bc8d5dbe309412758d48d6027a37591057dc9d10fbfbe8ce5
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
$ docker pull traefik@sha256:4141f960ad1b2bfb6db4477bb162b22b74b4d2839bc1905e575aa987f8ce5032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51145725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e9a734e01337937b46e3fcde49fae6bb79d28126a6b9140ed666aab57a3af4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:54 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8d06f077ce014df93e73f77690387672dc9cc78186d2a9ad0b4fb620337fc5`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ffd095d3fef7be59b8e14b32c70ec50befe38ddbc6f888555a237d79b70d9`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 46.8 MB (46822592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36e028fc4795bea8f579b917962797c6994254329797c1f89d4a83ba373c7c`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:95a6b90bf617399b9c2565747ce9f2efe5b640b3dd973cd1f6ec2c2ab0a2bbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7814ec727ce635b406ebbc8e83a5d0805ceda8ce9a92e3ef1e6d377fa2b418bd`

```dockerfile
```

-	Layers:
	-	`sha256:e256ce114d98ecce6fdb27ae2bec60c08b3ab36ecb0f8b02749c3024a1305032`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69809d5af32da74f52b27b2cd0426c2c4d151bc5a4ac0a7ce99994ee66cf9dde`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:16cf819f2106576f1565b00cdf5589d0b5864a6b77ebaf45f4e30e1779b71b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e24f6c9a1ddcca343a996f7700f73707ec76eb70ea8b1faaf5049973e8586a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:38:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:38:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:38:20 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:38:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b51f970aca5177f1c85670a1603f0a0834d4cd4f93330cbac83f2c4f02e5225`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 461.4 KB (461438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7437a937530c084868102dadfcce425b3027b6408b8af33d980d814acba8b1`  
		Last Modified: Mon, 23 Feb 2026 21:38:29 GMT  
		Size: 42.9 MB (42852924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc245d5cb31da9dfc449bb660c82e9c888374b34f3856a32bf16390be1d39a7b`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:82e9d4ce47fe616d8257c2ef66ab777e9b31f92ee2449d7e45dc3b8c592a7c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7c55570778ab767c4151133be0792b4349d6319bcd2eaa7b4530fcfeb6b143`

```dockerfile
```

-	Layers:
	-	`sha256:a6620a90c2a22aaed3d56d2177be622f834fdf99a613d0915991b74400cf7ce9`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ec7bea4106e542d9047d61e154377013309322d2c4191cfc375f62bfafc058cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda5d86ee7ae74add53acd5b8ac5e18a98538566a3490988d11c685b8f5611ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:54 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21ee00ee287ddba3c5f811d4fe3d4419fccf30b6da5594f633472149eb8f013`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 463.0 KB (463008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2a60bf8dad1a0ac1bd069416701bcef22f4356794a94cde84ddd68536c5547`  
		Last Modified: Mon, 23 Feb 2026 21:38:21 GMT  
		Size: 42.1 MB (42109649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3010a02494f4b334b5b0e89ae86a18b5e320986cb9658a4cfccd0c6470107c8`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:7e45226ca8fb85ca74be88d9daea4639030da6a014bb8f0a1fd85c29dfa181e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c4381bfa18706fb2e6c136afe0113af6d6e2dc0fe00635b4c41ea93b8d3096`

```dockerfile
```

-	Layers:
	-	`sha256:b753ca3720bdb9d1de7c0600f8b05e0480f3a00a0e1e72ff793c9ce9bae77166`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94b5249558a368503a5afe7219a4ab573549a088a5952bd569cc35ea0d15d64`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:72de49b4971a323c5103a5efe288ee54399afe509d2339b5a9692b65975c219f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45356377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92127bfce7e47062db8059d6c02532e78775b89032047392236a5c10d0470d59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:44:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:44:45 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:44:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacf6756ca01da33eb1343fdb73db24339fd265d16ff1965f43b4032d82cd243`  
		Last Modified: Mon, 23 Feb 2026 21:45:48 GMT  
		Size: 41.1 MB (41062851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02ee61e2b5b77e97afbde074c5ca9d54280cadb0cb991a7abf7fa9006864ae`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:2393f4c9f1dbf83604afd8b4fa2b571e79b6c5287adf3cf930e99e61fc04e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc4ddf685452e799c5634717258cdc230553ba9b8d768d10264d09486bb5029`

```dockerfile
```

-	Layers:
	-	`sha256:b8ea2037120aa249714dd86f276402bdd22c8b8eab17e5000b6a59bbe7fdd08a`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17b0315d942408852fa446dcf22fb94577f8915c321a387bb7d79b4baf5f899`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:a35906bd691d546f5f2e946cac7b936a15ac51741508fbe36030661254790345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49473089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ad32cf8a10e3c697da7833bbedc3e11658766ac5cc2904be9f6d2eeff89270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:35:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
COPY entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:41:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 02:41:07 GMT
CMD ["traefik"]
# Tue, 24 Feb 2026 02:41:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e83e761e01f3ced55ef589660d62f3c7d941ba7c2bf18c026865126d409786`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2186276b174c86d37e4ae11e54a01e251a717eca87f0993c49a8a4abedb24705`  
		Last Modified: Tue, 24 Feb 2026 02:46:43 GMT  
		Size: 45.4 MB (45426242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7513d805749fba192cc532f7103babe6a13c70186119d9ad6a0e7362ee1d55`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:7fef2a04689e4c67b0b42d72a249cc3163f0aba8f0f2c7c4ecb279cfe3eb349d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6a71286171cc27109fee46fd4a02f2318a98a9672374670278b7aaceb4df14`

```dockerfile
```

-	Layers:
	-	`sha256:532c1b6978ded6fce46417b850b382f63f97aa83272bb6b63bfd429c98b04299`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e95c23fd3cc7af894d84f15b318b8381a3d031e9eb91b9dfa711e96dcf892ee`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:a5988cbb5582492f1a2c5860fe56c6fc34938c3bfa6ccc1620b05309d8e0c3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc93fe72a392e79fad47adb2a2976ed17a9e64af402dc168c087b8e6c96f5f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:39:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:40:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:40:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:40:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:40:05 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:40:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d77e277fa279c36b8a085ad39126da33bbede7e3cbe43a763eee1f9849ee11`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659eef48f55c32dafa6a449e605b8d0d3de25c662750b490210c2720a88e3060`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 45.3 MB (45289986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2fbd1160ca187b67fad3741295a22c0af10af653ca5640f88225d6e7505af0`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:e6f4126f8cc3fa5bd9a1ffd96afb31ec65972ce0eb2427a1456ee8c120c82e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8615db22523e5244a9ef2ce1dce4617c1c2fd20b2c0caef74bf4eeb1575d1`

```dockerfile
```

-	Layers:
	-	`sha256:acb9966b442f02f629d740055523bf01a7152d3670318cb6e67f47e757db8ed5`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d9e95be229d8aa7ed4fd70986a3c0c801f4d0b714bcac7517e872d1c632988`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:7a6d25af24298fdc59743425013802aa5f2da412121c1d52c42b1cc6e37b1f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:a51c805def98e1f8322d6e6216c8358df9f2482b9a446294b2e414ce2aceb544
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174284684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae00e14ed1c16c67180ea15a3101c85fd9894181e9cca64b022ec49f6f8a28b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 23 Feb 2026 22:10:43 GMT
RUN cmd /S /C #(nop) COPY file:677dd367ef885b943dfeb7dd6ae0505d21cacfee88c63efbfbd88e9aee14c18d in \ 
# Mon, 23 Feb 2026 22:10:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 23 Feb 2026 22:10:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 22:10:46 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38872888f2a7acde41b46ea37df53faa6e940850e2875068d96b756aa128a025`  
		Last Modified: Mon, 23 Feb 2026 22:11:32 GMT  
		Size: 47.6 MB (47635651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730f883abb10d33a1c4c2cc5eae6af7cfdc6080f993edc33f0725ddd10352268`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb23bb5e3066dfab26dddcc8f3fe310aef5129b939a7a71b93e5f1b62c7d1162`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7fadbaae6496d12c6ec4be179ae3ff5f594823ab4f831e480ef7dc736b5d33`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d11d387d1179524ecae4286fa59e0f827ab2351b4f87edcccd387ddb5ebd27a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:0e66061ff5f34964b89b047d1b3bf7a5d393bc949401811861a7164e718b9764
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910925531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fed6bd3d0f8ac52b59d3c3031e71cb5f2968b62b9efa8d60a45cb854131211`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:58:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:58:14 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:58:15 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:58:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb0a7566470e7fbec32969b07e4506fc816e4242492998a86b3379b2ba4c42`  
		Last Modified: Mon, 23 Feb 2026 21:58:58 GMT  
		Size: 48.3 MB (48263149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e503c1b5ea41e32b44fbdc3ede2779cf63ca6ca4179f183904eeedeb9f26d95a`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468357667205af6c0aaac8d3cc15777aaffc40f4fcdb68cb646cb03908cf67d`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4d7fba6084228c469070092a0ca19a95673fc988c5427acf52be6ad2c49945`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.40`

**does not exist** (yet?)

## `traefik:2.11.40-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:2.11.40-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:3`

```console
$ docker pull traefik@sha256:9004e1cd1e33c5eb0b6ec02bc6cfda61fe9caca36751114b1c9c6662f01b264a
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
$ docker pull traefik@sha256:f67a287e3fdac92334fb44f291b6f264338964fd7e7a0e135b8e9e16da6d41d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52398801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1363849f5ded978b0f3cac5bc987a50efa16390f04c901c67b7f23b4ad50a108`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:52 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69b16dbe9a1607aff902a7d5704118bbd2bc20f15a1f23dda7da5c02a5fe97a`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd7a60bfeea59f33fb1ec9fad0c59c616003b3e8fd4a5e4faac495eebd86acf`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 48.1 MB (48075673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c596a59ba68b851af3b95b35e11c7c1f893726ae89f03ed5fb08db1096c0b0e4`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:491f3860ea2d70663d656246f29f14e5658a1744637da461e4a493413388aebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2851b10c3b79bf1f5d758d60c97a9b6ecbf22e0e4ffd1453505ade53cafa82`

```dockerfile
```

-	Layers:
	-	`sha256:89c2f8ffcce03acdd14af76df692906d70650cda5ba5bc5a1e5b9dd1e7a807de`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 843.1 KB (843100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afe2b0963e813e17f1f928c19d1c929dfa17378a67b128595f92127148de43e`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3ca153ac7a2feb40a6e7c753bc934312c2541baec6f1b5410cc8af7de3646f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47687176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f3d390622308f39d576f57627811d73c0f7574c05ea6dce33c71d219e6686f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:38:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:38:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:38:19 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:38:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3e978ee778f3b618cca62a4a462cb6a361b8034fc57d09610610316921b42`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99a1c33a617c42badfb20775968507fb27d8f8cd6728f9627d24a447ebc6f6a`  
		Last Modified: Mon, 23 Feb 2026 21:38:28 GMT  
		Size: 43.7 MB (43655541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123278dcdd5b55740047689571cb4e65c45dab1fbc1c82ce6b771ba934c3bf4c`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:d8759a6938af55d2dc163dff5357d735aca2deb48daeceaec724677b55136e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923d7f66fac7138bf3cd183d8b5ed985dfa70ef1987cc9f889d13af29569117`

```dockerfile
```

-	Layers:
	-	`sha256:5948bd375fa2600a6c2b02e48253db975805b56fbadac8853266781e92e7f387`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ee0eede00d38cc55f39c7cd554aee4df98723bd0197e2cc353febff7d8cf45bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47606676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b3f20d21e585ef763977bb931ad16fb1727cd85dc46f924abd2c50afd0dcc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ad60ba9b215c3dfe6fbdfeeea8698938fd44787f683d775384a397a1570702`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 463.0 KB (462985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc5e2f7f7ad9bff294bd9b659aea6b0e54bab73b06cf503a5158cfb93e6a7d4`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 42.9 MB (42946230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a838cc94626e57d024a9c1ad516a10ccfa5604e0b895329a2ecbda12ac42dbb0`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:684ea79188f81602565e2a670390682603234e932a639874377082e7152b2b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1d6335065015f71b7ac0c913176ac43af2d3f30b8ec0f883b527121b3c26a8`

```dockerfile
```

-	Layers:
	-	`sha256:9503e2b4dfba893d49f85b1b5e68d2efb306ca46dbc6633ed0ffa7a36bb26f15`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 842.6 KB (842554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e7792640924d2cb1713a5d3ec10f1da2d06b1f769ea14083879e8921e038cb`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:e741c69957cd3226603f44ccc6e001c9d41edbebb99556b64ce70856ed6ebfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45820228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00740f1ea6cb52978652c1c88dbab0b9fcbd6639261db71226a9b152e6695d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:44:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:44:45 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:44:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734d8fa47494fab233e193daa07f765351b62c5069a0bae2a39152afb06dc6f`  
		Last Modified: Mon, 23 Feb 2026 21:45:48 GMT  
		Size: 41.5 MB (41526702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02ee61e2b5b77e97afbde074c5ca9d54280cadb0cb991a7abf7fa9006864ae`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:097e6be0c3e16cbea0592234a28b6b60018e5d32f46dd0c2878360e5915b7288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3be937e2196db1d2e75a3567fdfea3b1698a38f76c2bce0dc78be0b34202329`

```dockerfile
```

-	Layers:
	-	`sha256:86854d38c4babb52db1b6c5863cc57507eb2630436b1f8d0d8b507860396d6a2`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d23f3f99805b7f228d8a7a21394aab79a87225852c825dc56fc5bd3e92eb1fc`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:eb01098b0bcd3646f698e7b0855ea9a5785f63345783524f6a337b316ac33dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50483003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc474f68be2e1c2663b850514a70065ef688f5ed2517305995a7265b2cfa807f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:35:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
COPY entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:35:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 02:35:14 GMT
CMD ["traefik"]
# Tue, 24 Feb 2026 02:35:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e83e761e01f3ced55ef589660d62f3c7d941ba7c2bf18c026865126d409786`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c763a5ea14c310e9208042a4bd71dbb1f67beaa30229bb10b6be8f2aeb68c2`  
		Last Modified: Tue, 24 Feb 2026 02:40:27 GMT  
		Size: 46.4 MB (46436156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac89de76912e22a103c365cd3e3997fd4027c140080093022bdfd0c315fa5707`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:0edf2cd86b067b1e2925b9cb1e16254b46ae45434a764245b33ee49a594860bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dc95c5daa230da213571a54f5799fdfe1f71a23ec14ffd6058b404f33103ca`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f694a95a4d44871c46609debbcb509d50bba6f6be9b4a46735e3efb4e1e2c`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 842.5 KB (842503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d27a12f083199ae685e2c02a1f1944bcbe6b2a6ff414b030d3586efc4994d8b`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:af6a148bbbc3544e2ead792d1df1ba77495f69dcc3419e3653d8d36c133ac919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50460742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43378e6316ff312c7ec91b13b5612dffb7b404555cf356813c29401c33e99276`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:39:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:39:57 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:39:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7ceb67b0194a6ba4f4badec8c1709c1d0eaa50ca1bcdcc9b3032cc18359a3`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3001c4417109fab86a61c94fe5b54752f1499a0d6240302a869c9416b3a44b`  
		Last Modified: Mon, 23 Feb 2026 21:41:16 GMT  
		Size: 46.3 MB (46273294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d42fdf72de7429c2f4cf3771fd87b1d7d051fe2b7d37a860979ebaff2c539`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:96e15fd60f99299c4054e028d5f78d00c8b104fc02477b277a1905ba638b680e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3ba2aacb6bb88cb964d1afed3f49a55e023f773925181bd5d31671f0833624`

```dockerfile
```

-	Layers:
	-	`sha256:a03c3ab0ade3067c81f995a0a62d2f323d60b3573d862c77732b1525525f25ff`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 842.4 KB (842449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fe3a7b0b3ca5cfc59f60587c0606ba59120e2ad277ba4c1f2a2a26d15bbd92`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:3aef91c172ca827e372b718b6da51e58e5d613ed156e7b1545b3d0ac44e333d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8ab0b4fd735d3f05d56c46107c14f18c69e84c374c370fcc663a5ab1d0b6251b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175488260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc42f1edd010f65a13b0deb282899401eac6e476af1cb7a811b5aab721dd59a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 23 Feb 2026 22:09:32 GMT
RUN cmd /S /C #(nop) COPY file:446d33bf3cb43dd9b08930d97b5980de726b2e7e2a3b964cc3f07a68650b1328 in \ 
# Mon, 23 Feb 2026 22:09:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 23 Feb 2026 22:09:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 22:09:36 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdce0ae5ea5f347db1dc87f4ab0e987abbd8d31406fa9a0dca2a6d525e3272bd`  
		Last Modified: Mon, 23 Feb 2026 22:10:22 GMT  
		Size: 48.8 MB (48839231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3cc3648513ddca8db55ea24b85088c148b58b85b2fa91de565ac2407cd81cc`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee51efeb9b7010f464fa83b96c5da1a25e2c68dab8237ddbae7129b7c7dfe61`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52eaad9519efc142a66a7676b80ad714ae1e93e2a4b9d0a8bb6aa5d19dba9fb`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:76e1a223bc200a4579781418ff80770fa163e2a7133b14ede32ba56fcfc16909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:aa6c45febeab2eefddfb0c4a96a4264bc1265261432f29a483b00d8997a71402
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912168854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028a3f3bac0de29b0c4ab11a3281c9f33fedfd2d6fab00e8402cb2ba83ad806e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:45:08 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:45:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:45:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f406a064c9213d2d4e7e3d50c235af90ecb975d188ce5ed2102c8d620eeb4f`  
		Last Modified: Mon, 23 Feb 2026 21:45:58 GMT  
		Size: 49.5 MB (49506380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204cfc419a02f90f5f10ef4ea45d32bfc4658e2ef0dc737969c0f46a9580f5f`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68134cba67c602ff14c309a5f2622964f8b960110006d5133a07000e36fe4a26`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1075592b3ec9c230e5c57316bc511e439da63912a597a0a37711723f736afe9`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:9004e1cd1e33c5eb0b6ec02bc6cfda61fe9caca36751114b1c9c6662f01b264a
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
$ docker pull traefik@sha256:f67a287e3fdac92334fb44f291b6f264338964fd7e7a0e135b8e9e16da6d41d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52398801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1363849f5ded978b0f3cac5bc987a50efa16390f04c901c67b7f23b4ad50a108`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:52 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69b16dbe9a1607aff902a7d5704118bbd2bc20f15a1f23dda7da5c02a5fe97a`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd7a60bfeea59f33fb1ec9fad0c59c616003b3e8fd4a5e4faac495eebd86acf`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 48.1 MB (48075673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c596a59ba68b851af3b95b35e11c7c1f893726ae89f03ed5fb08db1096c0b0e4`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:491f3860ea2d70663d656246f29f14e5658a1744637da461e4a493413388aebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2851b10c3b79bf1f5d758d60c97a9b6ecbf22e0e4ffd1453505ade53cafa82`

```dockerfile
```

-	Layers:
	-	`sha256:89c2f8ffcce03acdd14af76df692906d70650cda5ba5bc5a1e5b9dd1e7a807de`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 843.1 KB (843100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afe2b0963e813e17f1f928c19d1c929dfa17378a67b128595f92127148de43e`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3ca153ac7a2feb40a6e7c753bc934312c2541baec6f1b5410cc8af7de3646f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47687176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f3d390622308f39d576f57627811d73c0f7574c05ea6dce33c71d219e6686f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:38:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:38:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:38:19 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:38:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3e978ee778f3b618cca62a4a462cb6a361b8034fc57d09610610316921b42`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99a1c33a617c42badfb20775968507fb27d8f8cd6728f9627d24a447ebc6f6a`  
		Last Modified: Mon, 23 Feb 2026 21:38:28 GMT  
		Size: 43.7 MB (43655541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123278dcdd5b55740047689571cb4e65c45dab1fbc1c82ce6b771ba934c3bf4c`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:d8759a6938af55d2dc163dff5357d735aca2deb48daeceaec724677b55136e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923d7f66fac7138bf3cd183d8b5ed985dfa70ef1987cc9f889d13af29569117`

```dockerfile
```

-	Layers:
	-	`sha256:5948bd375fa2600a6c2b02e48253db975805b56fbadac8853266781e92e7f387`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ee0eede00d38cc55f39c7cd554aee4df98723bd0197e2cc353febff7d8cf45bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47606676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b3f20d21e585ef763977bb931ad16fb1727cd85dc46f924abd2c50afd0dcc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ad60ba9b215c3dfe6fbdfeeea8698938fd44787f683d775384a397a1570702`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 463.0 KB (462985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc5e2f7f7ad9bff294bd9b659aea6b0e54bab73b06cf503a5158cfb93e6a7d4`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 42.9 MB (42946230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a838cc94626e57d024a9c1ad516a10ccfa5604e0b895329a2ecbda12ac42dbb0`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:684ea79188f81602565e2a670390682603234e932a639874377082e7152b2b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1d6335065015f71b7ac0c913176ac43af2d3f30b8ec0f883b527121b3c26a8`

```dockerfile
```

-	Layers:
	-	`sha256:9503e2b4dfba893d49f85b1b5e68d2efb306ca46dbc6633ed0ffa7a36bb26f15`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 842.6 KB (842554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e7792640924d2cb1713a5d3ec10f1da2d06b1f769ea14083879e8921e038cb`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:e741c69957cd3226603f44ccc6e001c9d41edbebb99556b64ce70856ed6ebfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45820228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00740f1ea6cb52978652c1c88dbab0b9fcbd6639261db71226a9b152e6695d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:44:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:44:45 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:44:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734d8fa47494fab233e193daa07f765351b62c5069a0bae2a39152afb06dc6f`  
		Last Modified: Mon, 23 Feb 2026 21:45:48 GMT  
		Size: 41.5 MB (41526702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02ee61e2b5b77e97afbde074c5ca9d54280cadb0cb991a7abf7fa9006864ae`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:097e6be0c3e16cbea0592234a28b6b60018e5d32f46dd0c2878360e5915b7288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3be937e2196db1d2e75a3567fdfea3b1698a38f76c2bce0dc78be0b34202329`

```dockerfile
```

-	Layers:
	-	`sha256:86854d38c4babb52db1b6c5863cc57507eb2630436b1f8d0d8b507860396d6a2`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d23f3f99805b7f228d8a7a21394aab79a87225852c825dc56fc5bd3e92eb1fc`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:eb01098b0bcd3646f698e7b0855ea9a5785f63345783524f6a337b316ac33dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50483003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc474f68be2e1c2663b850514a70065ef688f5ed2517305995a7265b2cfa807f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:35:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
COPY entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:35:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 02:35:14 GMT
CMD ["traefik"]
# Tue, 24 Feb 2026 02:35:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e83e761e01f3ced55ef589660d62f3c7d941ba7c2bf18c026865126d409786`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c763a5ea14c310e9208042a4bd71dbb1f67beaa30229bb10b6be8f2aeb68c2`  
		Last Modified: Tue, 24 Feb 2026 02:40:27 GMT  
		Size: 46.4 MB (46436156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac89de76912e22a103c365cd3e3997fd4027c140080093022bdfd0c315fa5707`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0edf2cd86b067b1e2925b9cb1e16254b46ae45434a764245b33ee49a594860bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dc95c5daa230da213571a54f5799fdfe1f71a23ec14ffd6058b404f33103ca`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f694a95a4d44871c46609debbcb509d50bba6f6be9b4a46735e3efb4e1e2c`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 842.5 KB (842503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d27a12f083199ae685e2c02a1f1944bcbe6b2a6ff414b030d3586efc4994d8b`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:af6a148bbbc3544e2ead792d1df1ba77495f69dcc3419e3653d8d36c133ac919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50460742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43378e6316ff312c7ec91b13b5612dffb7b404555cf356813c29401c33e99276`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:39:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:39:57 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:39:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7ceb67b0194a6ba4f4badec8c1709c1d0eaa50ca1bcdcc9b3032cc18359a3`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3001c4417109fab86a61c94fe5b54752f1499a0d6240302a869c9416b3a44b`  
		Last Modified: Mon, 23 Feb 2026 21:41:16 GMT  
		Size: 46.3 MB (46273294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d42fdf72de7429c2f4cf3771fd87b1d7d051fe2b7d37a860979ebaff2c539`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:96e15fd60f99299c4054e028d5f78d00c8b104fc02477b277a1905ba638b680e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3ba2aacb6bb88cb964d1afed3f49a55e023f773925181bd5d31671f0833624`

```dockerfile
```

-	Layers:
	-	`sha256:a03c3ab0ade3067c81f995a0a62d2f323d60b3573d862c77732b1525525f25ff`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 842.4 KB (842449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fe3a7b0b3ca5cfc59f60587c0606ba59120e2ad277ba4c1f2a2a26d15bbd92`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:3aef91c172ca827e372b718b6da51e58e5d613ed156e7b1545b3d0ac44e333d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8ab0b4fd735d3f05d56c46107c14f18c69e84c374c370fcc663a5ab1d0b6251b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175488260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc42f1edd010f65a13b0deb282899401eac6e476af1cb7a811b5aab721dd59a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 23 Feb 2026 22:09:32 GMT
RUN cmd /S /C #(nop) COPY file:446d33bf3cb43dd9b08930d97b5980de726b2e7e2a3b964cc3f07a68650b1328 in \ 
# Mon, 23 Feb 2026 22:09:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 23 Feb 2026 22:09:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 22:09:36 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdce0ae5ea5f347db1dc87f4ab0e987abbd8d31406fa9a0dca2a6d525e3272bd`  
		Last Modified: Mon, 23 Feb 2026 22:10:22 GMT  
		Size: 48.8 MB (48839231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3cc3648513ddca8db55ea24b85088c148b58b85b2fa91de565ac2407cd81cc`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee51efeb9b7010f464fa83b96c5da1a25e2c68dab8237ddbae7129b7c7dfe61`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52eaad9519efc142a66a7676b80ad714ae1e93e2a4b9d0a8bb6aa5d19dba9fb`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:76e1a223bc200a4579781418ff80770fa163e2a7133b14ede32ba56fcfc16909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:aa6c45febeab2eefddfb0c4a96a4264bc1265261432f29a483b00d8997a71402
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912168854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028a3f3bac0de29b0c4ab11a3281c9f33fedfd2d6fab00e8402cb2ba83ad806e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:45:08 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:45:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:45:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f406a064c9213d2d4e7e3d50c235af90ecb975d188ce5ed2102c8d620eeb4f`  
		Last Modified: Mon, 23 Feb 2026 21:45:58 GMT  
		Size: 49.5 MB (49506380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204cfc419a02f90f5f10ef4ea45d32bfc4658e2ef0dc737969c0f46a9580f5f`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68134cba67c602ff14c309a5f2622964f8b960110006d5133a07000e36fe4a26`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1075592b3ec9c230e5c57316bc511e439da63912a597a0a37711723f736afe9`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.10`

**does not exist** (yet?)

## `traefik:3.6.10-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:3.6.10-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:latest`

```console
$ docker pull traefik@sha256:9004e1cd1e33c5eb0b6ec02bc6cfda61fe9caca36751114b1c9c6662f01b264a
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
$ docker pull traefik@sha256:f67a287e3fdac92334fb44f291b6f264338964fd7e7a0e135b8e9e16da6d41d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52398801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1363849f5ded978b0f3cac5bc987a50efa16390f04c901c67b7f23b4ad50a108`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:52 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69b16dbe9a1607aff902a7d5704118bbd2bc20f15a1f23dda7da5c02a5fe97a`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd7a60bfeea59f33fb1ec9fad0c59c616003b3e8fd4a5e4faac495eebd86acf`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 48.1 MB (48075673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c596a59ba68b851af3b95b35e11c7c1f893726ae89f03ed5fb08db1096c0b0e4`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:491f3860ea2d70663d656246f29f14e5658a1744637da461e4a493413388aebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2851b10c3b79bf1f5d758d60c97a9b6ecbf22e0e4ffd1453505ade53cafa82`

```dockerfile
```

-	Layers:
	-	`sha256:89c2f8ffcce03acdd14af76df692906d70650cda5ba5bc5a1e5b9dd1e7a807de`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 843.1 KB (843100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afe2b0963e813e17f1f928c19d1c929dfa17378a67b128595f92127148de43e`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3ca153ac7a2feb40a6e7c753bc934312c2541baec6f1b5410cc8af7de3646f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47687176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f3d390622308f39d576f57627811d73c0f7574c05ea6dce33c71d219e6686f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:38:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:38:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:38:19 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:38:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3e978ee778f3b618cca62a4a462cb6a361b8034fc57d09610610316921b42`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99a1c33a617c42badfb20775968507fb27d8f8cd6728f9627d24a447ebc6f6a`  
		Last Modified: Mon, 23 Feb 2026 21:38:28 GMT  
		Size: 43.7 MB (43655541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123278dcdd5b55740047689571cb4e65c45dab1fbc1c82ce6b771ba934c3bf4c`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:d8759a6938af55d2dc163dff5357d735aca2deb48daeceaec724677b55136e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923d7f66fac7138bf3cd183d8b5ed985dfa70ef1987cc9f889d13af29569117`

```dockerfile
```

-	Layers:
	-	`sha256:5948bd375fa2600a6c2b02e48253db975805b56fbadac8853266781e92e7f387`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ee0eede00d38cc55f39c7cd554aee4df98723bd0197e2cc353febff7d8cf45bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47606676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b3f20d21e585ef763977bb931ad16fb1727cd85dc46f924abd2c50afd0dcc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ad60ba9b215c3dfe6fbdfeeea8698938fd44787f683d775384a397a1570702`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 463.0 KB (462985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc5e2f7f7ad9bff294bd9b659aea6b0e54bab73b06cf503a5158cfb93e6a7d4`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 42.9 MB (42946230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a838cc94626e57d024a9c1ad516a10ccfa5604e0b895329a2ecbda12ac42dbb0`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:684ea79188f81602565e2a670390682603234e932a639874377082e7152b2b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1d6335065015f71b7ac0c913176ac43af2d3f30b8ec0f883b527121b3c26a8`

```dockerfile
```

-	Layers:
	-	`sha256:9503e2b4dfba893d49f85b1b5e68d2efb306ca46dbc6633ed0ffa7a36bb26f15`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 842.6 KB (842554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e7792640924d2cb1713a5d3ec10f1da2d06b1f769ea14083879e8921e038cb`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:e741c69957cd3226603f44ccc6e001c9d41edbebb99556b64ce70856ed6ebfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45820228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00740f1ea6cb52978652c1c88dbab0b9fcbd6639261db71226a9b152e6695d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:44:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:44:45 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:44:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734d8fa47494fab233e193daa07f765351b62c5069a0bae2a39152afb06dc6f`  
		Last Modified: Mon, 23 Feb 2026 21:45:48 GMT  
		Size: 41.5 MB (41526702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02ee61e2b5b77e97afbde074c5ca9d54280cadb0cb991a7abf7fa9006864ae`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:097e6be0c3e16cbea0592234a28b6b60018e5d32f46dd0c2878360e5915b7288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3be937e2196db1d2e75a3567fdfea3b1698a38f76c2bce0dc78be0b34202329`

```dockerfile
```

-	Layers:
	-	`sha256:86854d38c4babb52db1b6c5863cc57507eb2630436b1f8d0d8b507860396d6a2`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d23f3f99805b7f228d8a7a21394aab79a87225852c825dc56fc5bd3e92eb1fc`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:eb01098b0bcd3646f698e7b0855ea9a5785f63345783524f6a337b316ac33dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50483003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc474f68be2e1c2663b850514a70065ef688f5ed2517305995a7265b2cfa807f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:35:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
COPY entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:35:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 02:35:14 GMT
CMD ["traefik"]
# Tue, 24 Feb 2026 02:35:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e83e761e01f3ced55ef589660d62f3c7d941ba7c2bf18c026865126d409786`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c763a5ea14c310e9208042a4bd71dbb1f67beaa30229bb10b6be8f2aeb68c2`  
		Last Modified: Tue, 24 Feb 2026 02:40:27 GMT  
		Size: 46.4 MB (46436156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac89de76912e22a103c365cd3e3997fd4027c140080093022bdfd0c315fa5707`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:0edf2cd86b067b1e2925b9cb1e16254b46ae45434a764245b33ee49a594860bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dc95c5daa230da213571a54f5799fdfe1f71a23ec14ffd6058b404f33103ca`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f694a95a4d44871c46609debbcb509d50bba6f6be9b4a46735e3efb4e1e2c`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 842.5 KB (842503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d27a12f083199ae685e2c02a1f1944bcbe6b2a6ff414b030d3586efc4994d8b`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:af6a148bbbc3544e2ead792d1df1ba77495f69dcc3419e3653d8d36c133ac919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50460742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43378e6316ff312c7ec91b13b5612dffb7b404555cf356813c29401c33e99276`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:39:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:39:57 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:39:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7ceb67b0194a6ba4f4badec8c1709c1d0eaa50ca1bcdcc9b3032cc18359a3`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3001c4417109fab86a61c94fe5b54752f1499a0d6240302a869c9416b3a44b`  
		Last Modified: Mon, 23 Feb 2026 21:41:16 GMT  
		Size: 46.3 MB (46273294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d42fdf72de7429c2f4cf3771fd87b1d7d051fe2b7d37a860979ebaff2c539`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:96e15fd60f99299c4054e028d5f78d00c8b104fc02477b277a1905ba638b680e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3ba2aacb6bb88cb964d1afed3f49a55e023f773925181bd5d31671f0833624`

```dockerfile
```

-	Layers:
	-	`sha256:a03c3ab0ade3067c81f995a0a62d2f323d60b3573d862c77732b1525525f25ff`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 842.4 KB (842449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fe3a7b0b3ca5cfc59f60587c0606ba59120e2ad277ba4c1f2a2a26d15bbd92`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:ad45e9eb6b148c6bc8d5dbe309412758d48d6027a37591057dc9d10fbfbe8ce5
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
$ docker pull traefik@sha256:4141f960ad1b2bfb6db4477bb162b22b74b4d2839bc1905e575aa987f8ce5032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51145725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e9a734e01337937b46e3fcde49fae6bb79d28126a6b9140ed666aab57a3af4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:54 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8d06f077ce014df93e73f77690387672dc9cc78186d2a9ad0b4fb620337fc5`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ffd095d3fef7be59b8e14b32c70ec50befe38ddbc6f888555a237d79b70d9`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 46.8 MB (46822592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36e028fc4795bea8f579b917962797c6994254329797c1f89d4a83ba373c7c`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:95a6b90bf617399b9c2565747ce9f2efe5b640b3dd973cd1f6ec2c2ab0a2bbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7814ec727ce635b406ebbc8e83a5d0805ceda8ce9a92e3ef1e6d377fa2b418bd`

```dockerfile
```

-	Layers:
	-	`sha256:e256ce114d98ecce6fdb27ae2bec60c08b3ab36ecb0f8b02749c3024a1305032`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69809d5af32da74f52b27b2cd0426c2c4d151bc5a4ac0a7ce99994ee66cf9dde`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:16cf819f2106576f1565b00cdf5589d0b5864a6b77ebaf45f4e30e1779b71b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e24f6c9a1ddcca343a996f7700f73707ec76eb70ea8b1faaf5049973e8586a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:38:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:38:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:38:20 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:38:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b51f970aca5177f1c85670a1603f0a0834d4cd4f93330cbac83f2c4f02e5225`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 461.4 KB (461438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7437a937530c084868102dadfcce425b3027b6408b8af33d980d814acba8b1`  
		Last Modified: Mon, 23 Feb 2026 21:38:29 GMT  
		Size: 42.9 MB (42852924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc245d5cb31da9dfc449bb660c82e9c888374b34f3856a32bf16390be1d39a7b`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:82e9d4ce47fe616d8257c2ef66ab777e9b31f92ee2449d7e45dc3b8c592a7c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7c55570778ab767c4151133be0792b4349d6319bcd2eaa7b4530fcfeb6b143`

```dockerfile
```

-	Layers:
	-	`sha256:a6620a90c2a22aaed3d56d2177be622f834fdf99a613d0915991b74400cf7ce9`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ec7bea4106e542d9047d61e154377013309322d2c4191cfc375f62bfafc058cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda5d86ee7ae74add53acd5b8ac5e18a98538566a3490988d11c685b8f5611ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:54 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21ee00ee287ddba3c5f811d4fe3d4419fccf30b6da5594f633472149eb8f013`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 463.0 KB (463008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2a60bf8dad1a0ac1bd069416701bcef22f4356794a94cde84ddd68536c5547`  
		Last Modified: Mon, 23 Feb 2026 21:38:21 GMT  
		Size: 42.1 MB (42109649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3010a02494f4b334b5b0e89ae86a18b5e320986cb9658a4cfccd0c6470107c8`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:7e45226ca8fb85ca74be88d9daea4639030da6a014bb8f0a1fd85c29dfa181e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c4381bfa18706fb2e6c136afe0113af6d6e2dc0fe00635b4c41ea93b8d3096`

```dockerfile
```

-	Layers:
	-	`sha256:b753ca3720bdb9d1de7c0600f8b05e0480f3a00a0e1e72ff793c9ce9bae77166`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94b5249558a368503a5afe7219a4ab573549a088a5952bd569cc35ea0d15d64`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:72de49b4971a323c5103a5efe288ee54399afe509d2339b5a9692b65975c219f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45356377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92127bfce7e47062db8059d6c02532e78775b89032047392236a5c10d0470d59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:44:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:44:45 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:44:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacf6756ca01da33eb1343fdb73db24339fd265d16ff1965f43b4032d82cd243`  
		Last Modified: Mon, 23 Feb 2026 21:45:48 GMT  
		Size: 41.1 MB (41062851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02ee61e2b5b77e97afbde074c5ca9d54280cadb0cb991a7abf7fa9006864ae`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:2393f4c9f1dbf83604afd8b4fa2b571e79b6c5287adf3cf930e99e61fc04e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc4ddf685452e799c5634717258cdc230553ba9b8d768d10264d09486bb5029`

```dockerfile
```

-	Layers:
	-	`sha256:b8ea2037120aa249714dd86f276402bdd22c8b8eab17e5000b6a59bbe7fdd08a`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17b0315d942408852fa446dcf22fb94577f8915c321a387bb7d79b4baf5f899`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:a35906bd691d546f5f2e946cac7b936a15ac51741508fbe36030661254790345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49473089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ad32cf8a10e3c697da7833bbedc3e11658766ac5cc2904be9f6d2eeff89270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:35:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
COPY entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:41:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 02:41:07 GMT
CMD ["traefik"]
# Tue, 24 Feb 2026 02:41:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e83e761e01f3ced55ef589660d62f3c7d941ba7c2bf18c026865126d409786`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2186276b174c86d37e4ae11e54a01e251a717eca87f0993c49a8a4abedb24705`  
		Last Modified: Tue, 24 Feb 2026 02:46:43 GMT  
		Size: 45.4 MB (45426242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7513d805749fba192cc532f7103babe6a13c70186119d9ad6a0e7362ee1d55`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:7fef2a04689e4c67b0b42d72a249cc3163f0aba8f0f2c7c4ecb279cfe3eb349d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6a71286171cc27109fee46fd4a02f2318a98a9672374670278b7aaceb4df14`

```dockerfile
```

-	Layers:
	-	`sha256:532c1b6978ded6fce46417b850b382f63f97aa83272bb6b63bfd429c98b04299`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e95c23fd3cc7af894d84f15b318b8381a3d031e9eb91b9dfa711e96dcf892ee`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:a5988cbb5582492f1a2c5860fe56c6fc34938c3bfa6ccc1620b05309d8e0c3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc93fe72a392e79fad47adb2a2976ed17a9e64af402dc168c087b8e6c96f5f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:39:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:40:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:40:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:40:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:40:05 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:40:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d77e277fa279c36b8a085ad39126da33bbede7e3cbe43a763eee1f9849ee11`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659eef48f55c32dafa6a449e605b8d0d3de25c662750b490210c2720a88e3060`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 45.3 MB (45289986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2fbd1160ca187b67fad3741295a22c0af10af653ca5640f88225d6e7505af0`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:e6f4126f8cc3fa5bd9a1ffd96afb31ec65972ce0eb2427a1456ee8c120c82e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8615db22523e5244a9ef2ce1dce4617c1c2fd20b2c0caef74bf4eeb1575d1`

```dockerfile
```

-	Layers:
	-	`sha256:acb9966b442f02f629d740055523bf01a7152d3670318cb6e67f47e757db8ed5`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d9e95be229d8aa7ed4fd70986a3c0c801f4d0b714bcac7517e872d1c632988`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:7a6d25af24298fdc59743425013802aa5f2da412121c1d52c42b1cc6e37b1f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:a51c805def98e1f8322d6e6216c8358df9f2482b9a446294b2e414ce2aceb544
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174284684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae00e14ed1c16c67180ea15a3101c85fd9894181e9cca64b022ec49f6f8a28b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 23 Feb 2026 22:10:43 GMT
RUN cmd /S /C #(nop) COPY file:677dd367ef885b943dfeb7dd6ae0505d21cacfee88c63efbfbd88e9aee14c18d in \ 
# Mon, 23 Feb 2026 22:10:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 23 Feb 2026 22:10:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 22:10:46 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38872888f2a7acde41b46ea37df53faa6e940850e2875068d96b756aa128a025`  
		Last Modified: Mon, 23 Feb 2026 22:11:32 GMT  
		Size: 47.6 MB (47635651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730f883abb10d33a1c4c2cc5eae6af7cfdc6080f993edc33f0725ddd10352268`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb23bb5e3066dfab26dddcc8f3fe310aef5129b939a7a71b93e5f1b62c7d1162`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7fadbaae6496d12c6ec4be179ae3ff5f594823ab4f831e480ef7dc736b5d33`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d11d387d1179524ecae4286fa59e0f827ab2351b4f87edcccd387ddb5ebd27a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:0e66061ff5f34964b89b047d1b3bf7a5d393bc949401811861a7164e718b9764
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910925531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fed6bd3d0f8ac52b59d3c3031e71cb5f2968b62b9efa8d60a45cb854131211`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:58:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:58:14 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:58:15 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:58:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb0a7566470e7fbec32969b07e4506fc816e4242492998a86b3379b2ba4c42`  
		Last Modified: Mon, 23 Feb 2026 21:58:58 GMT  
		Size: 48.3 MB (48263149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e503c1b5ea41e32b44fbdc3ede2779cf63ca6ca4179f183904eeedeb9f26d95a`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468357667205af6c0aaac8d3cc15777aaffc40f4fcdb68cb646cb03908cf67d`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4d7fba6084228c469070092a0ca19a95673fc988c5427acf52be6ad2c49945`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:3aef91c172ca827e372b718b6da51e58e5d613ed156e7b1545b3d0ac44e333d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8ab0b4fd735d3f05d56c46107c14f18c69e84c374c370fcc663a5ab1d0b6251b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175488260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc42f1edd010f65a13b0deb282899401eac6e476af1cb7a811b5aab721dd59a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 23 Feb 2026 22:09:32 GMT
RUN cmd /S /C #(nop) COPY file:446d33bf3cb43dd9b08930d97b5980de726b2e7e2a3b964cc3f07a68650b1328 in \ 
# Mon, 23 Feb 2026 22:09:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 23 Feb 2026 22:09:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 22:09:36 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdce0ae5ea5f347db1dc87f4ab0e987abbd8d31406fa9a0dca2a6d525e3272bd`  
		Last Modified: Mon, 23 Feb 2026 22:10:22 GMT  
		Size: 48.8 MB (48839231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3cc3648513ddca8db55ea24b85088c148b58b85b2fa91de565ac2407cd81cc`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee51efeb9b7010f464fa83b96c5da1a25e2c68dab8237ddbae7129b7c7dfe61`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52eaad9519efc142a66a7676b80ad714ae1e93e2a4b9d0a8bb6aa5d19dba9fb`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:9004e1cd1e33c5eb0b6ec02bc6cfda61fe9caca36751114b1c9c6662f01b264a
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
$ docker pull traefik@sha256:f67a287e3fdac92334fb44f291b6f264338964fd7e7a0e135b8e9e16da6d41d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52398801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1363849f5ded978b0f3cac5bc987a50efa16390f04c901c67b7f23b4ad50a108`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:52 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69b16dbe9a1607aff902a7d5704118bbd2bc20f15a1f23dda7da5c02a5fe97a`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd7a60bfeea59f33fb1ec9fad0c59c616003b3e8fd4a5e4faac495eebd86acf`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 48.1 MB (48075673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c596a59ba68b851af3b95b35e11c7c1f893726ae89f03ed5fb08db1096c0b0e4`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:491f3860ea2d70663d656246f29f14e5658a1744637da461e4a493413388aebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2851b10c3b79bf1f5d758d60c97a9b6ecbf22e0e4ffd1453505ade53cafa82`

```dockerfile
```

-	Layers:
	-	`sha256:89c2f8ffcce03acdd14af76df692906d70650cda5ba5bc5a1e5b9dd1e7a807de`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 843.1 KB (843100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afe2b0963e813e17f1f928c19d1c929dfa17378a67b128595f92127148de43e`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3ca153ac7a2feb40a6e7c753bc934312c2541baec6f1b5410cc8af7de3646f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47687176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f3d390622308f39d576f57627811d73c0f7574c05ea6dce33c71d219e6686f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:38:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:38:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:38:19 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:38:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3e978ee778f3b618cca62a4a462cb6a361b8034fc57d09610610316921b42`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99a1c33a617c42badfb20775968507fb27d8f8cd6728f9627d24a447ebc6f6a`  
		Last Modified: Mon, 23 Feb 2026 21:38:28 GMT  
		Size: 43.7 MB (43655541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123278dcdd5b55740047689571cb4e65c45dab1fbc1c82ce6b771ba934c3bf4c`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:d8759a6938af55d2dc163dff5357d735aca2deb48daeceaec724677b55136e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923d7f66fac7138bf3cd183d8b5ed985dfa70ef1987cc9f889d13af29569117`

```dockerfile
```

-	Layers:
	-	`sha256:5948bd375fa2600a6c2b02e48253db975805b56fbadac8853266781e92e7f387`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ee0eede00d38cc55f39c7cd554aee4df98723bd0197e2cc353febff7d8cf45bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47606676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b3f20d21e585ef763977bb931ad16fb1727cd85dc46f924abd2c50afd0dcc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ad60ba9b215c3dfe6fbdfeeea8698938fd44787f683d775384a397a1570702`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 463.0 KB (462985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc5e2f7f7ad9bff294bd9b659aea6b0e54bab73b06cf503a5158cfb93e6a7d4`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 42.9 MB (42946230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a838cc94626e57d024a9c1ad516a10ccfa5604e0b895329a2ecbda12ac42dbb0`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:684ea79188f81602565e2a670390682603234e932a639874377082e7152b2b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1d6335065015f71b7ac0c913176ac43af2d3f30b8ec0f883b527121b3c26a8`

```dockerfile
```

-	Layers:
	-	`sha256:9503e2b4dfba893d49f85b1b5e68d2efb306ca46dbc6633ed0ffa7a36bb26f15`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 842.6 KB (842554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e7792640924d2cb1713a5d3ec10f1da2d06b1f769ea14083879e8921e038cb`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:e741c69957cd3226603f44ccc6e001c9d41edbebb99556b64ce70856ed6ebfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45820228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00740f1ea6cb52978652c1c88dbab0b9fcbd6639261db71226a9b152e6695d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:44:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:44:45 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:44:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734d8fa47494fab233e193daa07f765351b62c5069a0bae2a39152afb06dc6f`  
		Last Modified: Mon, 23 Feb 2026 21:45:48 GMT  
		Size: 41.5 MB (41526702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02ee61e2b5b77e97afbde074c5ca9d54280cadb0cb991a7abf7fa9006864ae`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:097e6be0c3e16cbea0592234a28b6b60018e5d32f46dd0c2878360e5915b7288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3be937e2196db1d2e75a3567fdfea3b1698a38f76c2bce0dc78be0b34202329`

```dockerfile
```

-	Layers:
	-	`sha256:86854d38c4babb52db1b6c5863cc57507eb2630436b1f8d0d8b507860396d6a2`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d23f3f99805b7f228d8a7a21394aab79a87225852c825dc56fc5bd3e92eb1fc`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:eb01098b0bcd3646f698e7b0855ea9a5785f63345783524f6a337b316ac33dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50483003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc474f68be2e1c2663b850514a70065ef688f5ed2517305995a7265b2cfa807f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:35:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
COPY entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:35:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 02:35:14 GMT
CMD ["traefik"]
# Tue, 24 Feb 2026 02:35:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e83e761e01f3ced55ef589660d62f3c7d941ba7c2bf18c026865126d409786`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c763a5ea14c310e9208042a4bd71dbb1f67beaa30229bb10b6be8f2aeb68c2`  
		Last Modified: Tue, 24 Feb 2026 02:40:27 GMT  
		Size: 46.4 MB (46436156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac89de76912e22a103c365cd3e3997fd4027c140080093022bdfd0c315fa5707`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:0edf2cd86b067b1e2925b9cb1e16254b46ae45434a764245b33ee49a594860bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dc95c5daa230da213571a54f5799fdfe1f71a23ec14ffd6058b404f33103ca`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f694a95a4d44871c46609debbcb509d50bba6f6be9b4a46735e3efb4e1e2c`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 842.5 KB (842503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d27a12f083199ae685e2c02a1f1944bcbe6b2a6ff414b030d3586efc4994d8b`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:af6a148bbbc3544e2ead792d1df1ba77495f69dcc3419e3653d8d36c133ac919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50460742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43378e6316ff312c7ec91b13b5612dffb7b404555cf356813c29401c33e99276`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:39:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:39:57 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:39:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7ceb67b0194a6ba4f4badec8c1709c1d0eaa50ca1bcdcc9b3032cc18359a3`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3001c4417109fab86a61c94fe5b54752f1499a0d6240302a869c9416b3a44b`  
		Last Modified: Mon, 23 Feb 2026 21:41:16 GMT  
		Size: 46.3 MB (46273294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d42fdf72de7429c2f4cf3771fd87b1d7d051fe2b7d37a860979ebaff2c539`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:96e15fd60f99299c4054e028d5f78d00c8b104fc02477b277a1905ba638b680e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3ba2aacb6bb88cb964d1afed3f49a55e023f773925181bd5d31671f0833624`

```dockerfile
```

-	Layers:
	-	`sha256:a03c3ab0ade3067c81f995a0a62d2f323d60b3573d862c77732b1525525f25ff`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 842.4 KB (842449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fe3a7b0b3ca5cfc59f60587c0606ba59120e2ad277ba4c1f2a2a26d15bbd92`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:3aef91c172ca827e372b718b6da51e58e5d613ed156e7b1545b3d0ac44e333d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8ab0b4fd735d3f05d56c46107c14f18c69e84c374c370fcc663a5ab1d0b6251b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175488260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc42f1edd010f65a13b0deb282899401eac6e476af1cb7a811b5aab721dd59a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 23 Feb 2026 22:09:32 GMT
RUN cmd /S /C #(nop) COPY file:446d33bf3cb43dd9b08930d97b5980de726b2e7e2a3b964cc3f07a68650b1328 in \ 
# Mon, 23 Feb 2026 22:09:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 23 Feb 2026 22:09:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 22:09:36 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdce0ae5ea5f347db1dc87f4ab0e987abbd8d31406fa9a0dca2a6d525e3272bd`  
		Last Modified: Mon, 23 Feb 2026 22:10:22 GMT  
		Size: 48.8 MB (48839231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3cc3648513ddca8db55ea24b85088c148b58b85b2fa91de565ac2407cd81cc`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee51efeb9b7010f464fa83b96c5da1a25e2c68dab8237ddbae7129b7c7dfe61`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52eaad9519efc142a66a7676b80ad714ae1e93e2a4b9d0a8bb6aa5d19dba9fb`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:76e1a223bc200a4579781418ff80770fa163e2a7133b14ede32ba56fcfc16909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:aa6c45febeab2eefddfb0c4a96a4264bc1265261432f29a483b00d8997a71402
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912168854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028a3f3bac0de29b0c4ab11a3281c9f33fedfd2d6fab00e8402cb2ba83ad806e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:45:08 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:45:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:45:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f406a064c9213d2d4e7e3d50c235af90ecb975d188ce5ed2102c8d620eeb4f`  
		Last Modified: Mon, 23 Feb 2026 21:45:58 GMT  
		Size: 49.5 MB (49506380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204cfc419a02f90f5f10ef4ea45d32bfc4658e2ef0dc737969c0f46a9580f5f`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68134cba67c602ff14c309a5f2622964f8b960110006d5133a07000e36fe4a26`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1075592b3ec9c230e5c57316bc511e439da63912a597a0a37711723f736afe9`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:ad45e9eb6b148c6bc8d5dbe309412758d48d6027a37591057dc9d10fbfbe8ce5
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
$ docker pull traefik@sha256:4141f960ad1b2bfb6db4477bb162b22b74b4d2839bc1905e575aa987f8ce5032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51145725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e9a734e01337937b46e3fcde49fae6bb79d28126a6b9140ed666aab57a3af4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:54 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8d06f077ce014df93e73f77690387672dc9cc78186d2a9ad0b4fb620337fc5`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ffd095d3fef7be59b8e14b32c70ec50befe38ddbc6f888555a237d79b70d9`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 46.8 MB (46822592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36e028fc4795bea8f579b917962797c6994254329797c1f89d4a83ba373c7c`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:95a6b90bf617399b9c2565747ce9f2efe5b640b3dd973cd1f6ec2c2ab0a2bbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7814ec727ce635b406ebbc8e83a5d0805ceda8ce9a92e3ef1e6d377fa2b418bd`

```dockerfile
```

-	Layers:
	-	`sha256:e256ce114d98ecce6fdb27ae2bec60c08b3ab36ecb0f8b02749c3024a1305032`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69809d5af32da74f52b27b2cd0426c2c4d151bc5a4ac0a7ce99994ee66cf9dde`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:16cf819f2106576f1565b00cdf5589d0b5864a6b77ebaf45f4e30e1779b71b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e24f6c9a1ddcca343a996f7700f73707ec76eb70ea8b1faaf5049973e8586a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:38:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:38:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:38:20 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:38:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b51f970aca5177f1c85670a1603f0a0834d4cd4f93330cbac83f2c4f02e5225`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 461.4 KB (461438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7437a937530c084868102dadfcce425b3027b6408b8af33d980d814acba8b1`  
		Last Modified: Mon, 23 Feb 2026 21:38:29 GMT  
		Size: 42.9 MB (42852924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc245d5cb31da9dfc449bb660c82e9c888374b34f3856a32bf16390be1d39a7b`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:82e9d4ce47fe616d8257c2ef66ab777e9b31f92ee2449d7e45dc3b8c592a7c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7c55570778ab767c4151133be0792b4349d6319bcd2eaa7b4530fcfeb6b143`

```dockerfile
```

-	Layers:
	-	`sha256:a6620a90c2a22aaed3d56d2177be622f834fdf99a613d0915991b74400cf7ce9`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ec7bea4106e542d9047d61e154377013309322d2c4191cfc375f62bfafc058cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda5d86ee7ae74add53acd5b8ac5e18a98538566a3490988d11c685b8f5611ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:54 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21ee00ee287ddba3c5f811d4fe3d4419fccf30b6da5594f633472149eb8f013`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 463.0 KB (463008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2a60bf8dad1a0ac1bd069416701bcef22f4356794a94cde84ddd68536c5547`  
		Last Modified: Mon, 23 Feb 2026 21:38:21 GMT  
		Size: 42.1 MB (42109649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3010a02494f4b334b5b0e89ae86a18b5e320986cb9658a4cfccd0c6470107c8`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:7e45226ca8fb85ca74be88d9daea4639030da6a014bb8f0a1fd85c29dfa181e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c4381bfa18706fb2e6c136afe0113af6d6e2dc0fe00635b4c41ea93b8d3096`

```dockerfile
```

-	Layers:
	-	`sha256:b753ca3720bdb9d1de7c0600f8b05e0480f3a00a0e1e72ff793c9ce9bae77166`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94b5249558a368503a5afe7219a4ab573549a088a5952bd569cc35ea0d15d64`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:72de49b4971a323c5103a5efe288ee54399afe509d2339b5a9692b65975c219f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45356377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92127bfce7e47062db8059d6c02532e78775b89032047392236a5c10d0470d59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:44:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:44:45 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:44:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacf6756ca01da33eb1343fdb73db24339fd265d16ff1965f43b4032d82cd243`  
		Last Modified: Mon, 23 Feb 2026 21:45:48 GMT  
		Size: 41.1 MB (41062851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02ee61e2b5b77e97afbde074c5ca9d54280cadb0cb991a7abf7fa9006864ae`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:2393f4c9f1dbf83604afd8b4fa2b571e79b6c5287adf3cf930e99e61fc04e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc4ddf685452e799c5634717258cdc230553ba9b8d768d10264d09486bb5029`

```dockerfile
```

-	Layers:
	-	`sha256:b8ea2037120aa249714dd86f276402bdd22c8b8eab17e5000b6a59bbe7fdd08a`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17b0315d942408852fa446dcf22fb94577f8915c321a387bb7d79b4baf5f899`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:a35906bd691d546f5f2e946cac7b936a15ac51741508fbe36030661254790345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49473089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ad32cf8a10e3c697da7833bbedc3e11658766ac5cc2904be9f6d2eeff89270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:35:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
COPY entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:41:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 02:41:07 GMT
CMD ["traefik"]
# Tue, 24 Feb 2026 02:41:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e83e761e01f3ced55ef589660d62f3c7d941ba7c2bf18c026865126d409786`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2186276b174c86d37e4ae11e54a01e251a717eca87f0993c49a8a4abedb24705`  
		Last Modified: Tue, 24 Feb 2026 02:46:43 GMT  
		Size: 45.4 MB (45426242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7513d805749fba192cc532f7103babe6a13c70186119d9ad6a0e7362ee1d55`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:7fef2a04689e4c67b0b42d72a249cc3163f0aba8f0f2c7c4ecb279cfe3eb349d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6a71286171cc27109fee46fd4a02f2318a98a9672374670278b7aaceb4df14`

```dockerfile
```

-	Layers:
	-	`sha256:532c1b6978ded6fce46417b850b382f63f97aa83272bb6b63bfd429c98b04299`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e95c23fd3cc7af894d84f15b318b8381a3d031e9eb91b9dfa711e96dcf892ee`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:a5988cbb5582492f1a2c5860fe56c6fc34938c3bfa6ccc1620b05309d8e0c3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc93fe72a392e79fad47adb2a2976ed17a9e64af402dc168c087b8e6c96f5f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:39:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:40:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:40:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:40:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:40:05 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:40:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d77e277fa279c36b8a085ad39126da33bbede7e3cbe43a763eee1f9849ee11`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659eef48f55c32dafa6a449e605b8d0d3de25c662750b490210c2720a88e3060`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 45.3 MB (45289986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2fbd1160ca187b67fad3741295a22c0af10af653ca5640f88225d6e7505af0`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:e6f4126f8cc3fa5bd9a1ffd96afb31ec65972ce0eb2427a1456ee8c120c82e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8615db22523e5244a9ef2ce1dce4617c1c2fd20b2c0caef74bf4eeb1575d1`

```dockerfile
```

-	Layers:
	-	`sha256:acb9966b442f02f629d740055523bf01a7152d3670318cb6e67f47e757db8ed5`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d9e95be229d8aa7ed4fd70986a3c0c801f4d0b714bcac7517e872d1c632988`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:7a6d25af24298fdc59743425013802aa5f2da412121c1d52c42b1cc6e37b1f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:a51c805def98e1f8322d6e6216c8358df9f2482b9a446294b2e414ce2aceb544
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174284684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae00e14ed1c16c67180ea15a3101c85fd9894181e9cca64b022ec49f6f8a28b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 23 Feb 2026 22:10:43 GMT
RUN cmd /S /C #(nop) COPY file:677dd367ef885b943dfeb7dd6ae0505d21cacfee88c63efbfbd88e9aee14c18d in \ 
# Mon, 23 Feb 2026 22:10:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 23 Feb 2026 22:10:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 22:10:46 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38872888f2a7acde41b46ea37df53faa6e940850e2875068d96b756aa128a025`  
		Last Modified: Mon, 23 Feb 2026 22:11:32 GMT  
		Size: 47.6 MB (47635651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730f883abb10d33a1c4c2cc5eae6af7cfdc6080f993edc33f0725ddd10352268`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb23bb5e3066dfab26dddcc8f3fe310aef5129b939a7a71b93e5f1b62c7d1162`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7fadbaae6496d12c6ec4be179ae3ff5f594823ab4f831e480ef7dc736b5d33`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d11d387d1179524ecae4286fa59e0f827ab2351b4f87edcccd387ddb5ebd27a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:0e66061ff5f34964b89b047d1b3bf7a5d393bc949401811861a7164e718b9764
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910925531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fed6bd3d0f8ac52b59d3c3031e71cb5f2968b62b9efa8d60a45cb854131211`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:58:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:58:14 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:58:15 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:58:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb0a7566470e7fbec32969b07e4506fc816e4242492998a86b3379b2ba4c42`  
		Last Modified: Mon, 23 Feb 2026 21:58:58 GMT  
		Size: 48.3 MB (48263149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e503c1b5ea41e32b44fbdc3ede2779cf63ca6ca4179f183904eeedeb9f26d95a`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468357667205af6c0aaac8d3cc15777aaffc40f4fcdb68cb646cb03908cf67d`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4d7fba6084228c469070092a0ca19a95673fc988c5427acf52be6ad2c49945`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:ad45e9eb6b148c6bc8d5dbe309412758d48d6027a37591057dc9d10fbfbe8ce5
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
$ docker pull traefik@sha256:4141f960ad1b2bfb6db4477bb162b22b74b4d2839bc1905e575aa987f8ce5032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51145725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e9a734e01337937b46e3fcde49fae6bb79d28126a6b9140ed666aab57a3af4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:54 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8d06f077ce014df93e73f77690387672dc9cc78186d2a9ad0b4fb620337fc5`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ffd095d3fef7be59b8e14b32c70ec50befe38ddbc6f888555a237d79b70d9`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 46.8 MB (46822592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36e028fc4795bea8f579b917962797c6994254329797c1f89d4a83ba373c7c`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:95a6b90bf617399b9c2565747ce9f2efe5b640b3dd973cd1f6ec2c2ab0a2bbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7814ec727ce635b406ebbc8e83a5d0805ceda8ce9a92e3ef1e6d377fa2b418bd`

```dockerfile
```

-	Layers:
	-	`sha256:e256ce114d98ecce6fdb27ae2bec60c08b3ab36ecb0f8b02749c3024a1305032`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69809d5af32da74f52b27b2cd0426c2c4d151bc5a4ac0a7ce99994ee66cf9dde`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:16cf819f2106576f1565b00cdf5589d0b5864a6b77ebaf45f4e30e1779b71b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e24f6c9a1ddcca343a996f7700f73707ec76eb70ea8b1faaf5049973e8586a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:38:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:38:20 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:38:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:38:20 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:38:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b51f970aca5177f1c85670a1603f0a0834d4cd4f93330cbac83f2c4f02e5225`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 461.4 KB (461438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7437a937530c084868102dadfcce425b3027b6408b8af33d980d814acba8b1`  
		Last Modified: Mon, 23 Feb 2026 21:38:29 GMT  
		Size: 42.9 MB (42852924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc245d5cb31da9dfc449bb660c82e9c888374b34f3856a32bf16390be1d39a7b`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:82e9d4ce47fe616d8257c2ef66ab777e9b31f92ee2449d7e45dc3b8c592a7c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7c55570778ab767c4151133be0792b4349d6319bcd2eaa7b4530fcfeb6b143`

```dockerfile
```

-	Layers:
	-	`sha256:a6620a90c2a22aaed3d56d2177be622f834fdf99a613d0915991b74400cf7ce9`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ec7bea4106e542d9047d61e154377013309322d2c4191cfc375f62bfafc058cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46770115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda5d86ee7ae74add53acd5b8ac5e18a98538566a3490988d11c685b8f5611ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:54 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:54 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21ee00ee287ddba3c5f811d4fe3d4419fccf30b6da5594f633472149eb8f013`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 463.0 KB (463008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2a60bf8dad1a0ac1bd069416701bcef22f4356794a94cde84ddd68536c5547`  
		Last Modified: Mon, 23 Feb 2026 21:38:21 GMT  
		Size: 42.1 MB (42109649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3010a02494f4b334b5b0e89ae86a18b5e320986cb9658a4cfccd0c6470107c8`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:7e45226ca8fb85ca74be88d9daea4639030da6a014bb8f0a1fd85c29dfa181e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c4381bfa18706fb2e6c136afe0113af6d6e2dc0fe00635b4c41ea93b8d3096`

```dockerfile
```

-	Layers:
	-	`sha256:b753ca3720bdb9d1de7c0600f8b05e0480f3a00a0e1e72ff793c9ce9bae77166`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94b5249558a368503a5afe7219a4ab573549a088a5952bd569cc35ea0d15d64`  
		Last Modified: Mon, 23 Feb 2026 21:38:19 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:72de49b4971a323c5103a5efe288ee54399afe509d2339b5a9692b65975c219f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45356377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92127bfce7e47062db8059d6c02532e78775b89032047392236a5c10d0470d59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:44:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:44:45 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:44:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacf6756ca01da33eb1343fdb73db24339fd265d16ff1965f43b4032d82cd243`  
		Last Modified: Mon, 23 Feb 2026 21:45:48 GMT  
		Size: 41.1 MB (41062851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02ee61e2b5b77e97afbde074c5ca9d54280cadb0cb991a7abf7fa9006864ae`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:2393f4c9f1dbf83604afd8b4fa2b571e79b6c5287adf3cf930e99e61fc04e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc4ddf685452e799c5634717258cdc230553ba9b8d768d10264d09486bb5029`

```dockerfile
```

-	Layers:
	-	`sha256:b8ea2037120aa249714dd86f276402bdd22c8b8eab17e5000b6a59bbe7fdd08a`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17b0315d942408852fa446dcf22fb94577f8915c321a387bb7d79b4baf5f899`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:a35906bd691d546f5f2e946cac7b936a15ac51741508fbe36030661254790345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49473089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ad32cf8a10e3c697da7833bbedc3e11658766ac5cc2904be9f6d2eeff89270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:35:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
COPY entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 02:41:07 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:41:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 02:41:07 GMT
CMD ["traefik"]
# Tue, 24 Feb 2026 02:41:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e83e761e01f3ced55ef589660d62f3c7d941ba7c2bf18c026865126d409786`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2186276b174c86d37e4ae11e54a01e251a717eca87f0993c49a8a4abedb24705`  
		Last Modified: Tue, 24 Feb 2026 02:46:43 GMT  
		Size: 45.4 MB (45426242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7513d805749fba192cc532f7103babe6a13c70186119d9ad6a0e7362ee1d55`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:7fef2a04689e4c67b0b42d72a249cc3163f0aba8f0f2c7c4ecb279cfe3eb349d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6a71286171cc27109fee46fd4a02f2318a98a9672374670278b7aaceb4df14`

```dockerfile
```

-	Layers:
	-	`sha256:532c1b6978ded6fce46417b850b382f63f97aa83272bb6b63bfd429c98b04299`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e95c23fd3cc7af894d84f15b318b8381a3d031e9eb91b9dfa711e96dcf892ee`  
		Last Modified: Tue, 24 Feb 2026 02:46:36 GMT  
		Size: 12.6 KB (12558 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:a5988cbb5582492f1a2c5860fe56c6fc34938c3bfa6ccc1620b05309d8e0c3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc93fe72a392e79fad47adb2a2976ed17a9e64af402dc168c087b8e6c96f5f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:39:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:40:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:40:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:40:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:40:05 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:40:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d77e277fa279c36b8a085ad39126da33bbede7e3cbe43a763eee1f9849ee11`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659eef48f55c32dafa6a449e605b8d0d3de25c662750b490210c2720a88e3060`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 45.3 MB (45289986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2fbd1160ca187b67fad3741295a22c0af10af653ca5640f88225d6e7505af0`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:e6f4126f8cc3fa5bd9a1ffd96afb31ec65972ce0eb2427a1456ee8c120c82e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8615db22523e5244a9ef2ce1dce4617c1c2fd20b2c0caef74bf4eeb1575d1`

```dockerfile
```

-	Layers:
	-	`sha256:acb9966b442f02f629d740055523bf01a7152d3670318cb6e67f47e757db8ed5`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d9e95be229d8aa7ed4fd70986a3c0c801f4d0b714bcac7517e872d1c632988`  
		Last Modified: Mon, 23 Feb 2026 21:41:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:7a6d25af24298fdc59743425013802aa5f2da412121c1d52c42b1cc6e37b1f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:a51c805def98e1f8322d6e6216c8358df9f2482b9a446294b2e414ce2aceb544
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174284684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae00e14ed1c16c67180ea15a3101c85fd9894181e9cca64b022ec49f6f8a28b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 23 Feb 2026 22:10:43 GMT
RUN cmd /S /C #(nop) COPY file:677dd367ef885b943dfeb7dd6ae0505d21cacfee88c63efbfbd88e9aee14c18d in \ 
# Mon, 23 Feb 2026 22:10:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 23 Feb 2026 22:10:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 22:10:46 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38872888f2a7acde41b46ea37df53faa6e940850e2875068d96b756aa128a025`  
		Last Modified: Mon, 23 Feb 2026 22:11:32 GMT  
		Size: 47.6 MB (47635651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730f883abb10d33a1c4c2cc5eae6af7cfdc6080f993edc33f0725ddd10352268`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb23bb5e3066dfab26dddcc8f3fe310aef5129b939a7a71b93e5f1b62c7d1162`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7fadbaae6496d12c6ec4be179ae3ff5f594823ab4f831e480ef7dc736b5d33`  
		Last Modified: Mon, 23 Feb 2026 22:10:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d11d387d1179524ecae4286fa59e0f827ab2351b4f87edcccd387ddb5ebd27a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:0e66061ff5f34964b89b047d1b3bf7a5d393bc949401811861a7164e718b9764
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910925531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fed6bd3d0f8ac52b59d3c3031e71cb5f2968b62b9efa8d60a45cb854131211`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:58:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.38/traefik_v2.11.38_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:58:14 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:58:15 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:58:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.38 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb0a7566470e7fbec32969b07e4506fc816e4242492998a86b3379b2ba4c42`  
		Last Modified: Mon, 23 Feb 2026 21:58:58 GMT  
		Size: 48.3 MB (48263149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e503c1b5ea41e32b44fbdc3ede2779cf63ca6ca4179f183904eeedeb9f26d95a`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468357667205af6c0aaac8d3cc15777aaffc40f4fcdb68cb646cb03908cf67d`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4d7fba6084228c469070092a0ca19a95673fc988c5427acf52be6ad2c49945`  
		Last Modified: Mon, 23 Feb 2026 21:58:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.40`

**does not exist** (yet?)

## `traefik:v2.11.40-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:v2.11.40-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:v3`

```console
$ docker pull traefik@sha256:9004e1cd1e33c5eb0b6ec02bc6cfda61fe9caca36751114b1c9c6662f01b264a
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
$ docker pull traefik@sha256:f67a287e3fdac92334fb44f291b6f264338964fd7e7a0e135b8e9e16da6d41d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52398801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1363849f5ded978b0f3cac5bc987a50efa16390f04c901c67b7f23b4ad50a108`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:52 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69b16dbe9a1607aff902a7d5704118bbd2bc20f15a1f23dda7da5c02a5fe97a`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd7a60bfeea59f33fb1ec9fad0c59c616003b3e8fd4a5e4faac495eebd86acf`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 48.1 MB (48075673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c596a59ba68b851af3b95b35e11c7c1f893726ae89f03ed5fb08db1096c0b0e4`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:491f3860ea2d70663d656246f29f14e5658a1744637da461e4a493413388aebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2851b10c3b79bf1f5d758d60c97a9b6ecbf22e0e4ffd1453505ade53cafa82`

```dockerfile
```

-	Layers:
	-	`sha256:89c2f8ffcce03acdd14af76df692906d70650cda5ba5bc5a1e5b9dd1e7a807de`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 843.1 KB (843100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afe2b0963e813e17f1f928c19d1c929dfa17378a67b128595f92127148de43e`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3ca153ac7a2feb40a6e7c753bc934312c2541baec6f1b5410cc8af7de3646f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47687176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f3d390622308f39d576f57627811d73c0f7574c05ea6dce33c71d219e6686f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:38:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:38:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:38:19 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:38:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3e978ee778f3b618cca62a4a462cb6a361b8034fc57d09610610316921b42`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99a1c33a617c42badfb20775968507fb27d8f8cd6728f9627d24a447ebc6f6a`  
		Last Modified: Mon, 23 Feb 2026 21:38:28 GMT  
		Size: 43.7 MB (43655541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123278dcdd5b55740047689571cb4e65c45dab1fbc1c82ce6b771ba934c3bf4c`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:d8759a6938af55d2dc163dff5357d735aca2deb48daeceaec724677b55136e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923d7f66fac7138bf3cd183d8b5ed985dfa70ef1987cc9f889d13af29569117`

```dockerfile
```

-	Layers:
	-	`sha256:5948bd375fa2600a6c2b02e48253db975805b56fbadac8853266781e92e7f387`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ee0eede00d38cc55f39c7cd554aee4df98723bd0197e2cc353febff7d8cf45bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47606676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b3f20d21e585ef763977bb931ad16fb1727cd85dc46f924abd2c50afd0dcc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ad60ba9b215c3dfe6fbdfeeea8698938fd44787f683d775384a397a1570702`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 463.0 KB (462985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc5e2f7f7ad9bff294bd9b659aea6b0e54bab73b06cf503a5158cfb93e6a7d4`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 42.9 MB (42946230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a838cc94626e57d024a9c1ad516a10ccfa5604e0b895329a2ecbda12ac42dbb0`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:684ea79188f81602565e2a670390682603234e932a639874377082e7152b2b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1d6335065015f71b7ac0c913176ac43af2d3f30b8ec0f883b527121b3c26a8`

```dockerfile
```

-	Layers:
	-	`sha256:9503e2b4dfba893d49f85b1b5e68d2efb306ca46dbc6633ed0ffa7a36bb26f15`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 842.6 KB (842554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e7792640924d2cb1713a5d3ec10f1da2d06b1f769ea14083879e8921e038cb`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:e741c69957cd3226603f44ccc6e001c9d41edbebb99556b64ce70856ed6ebfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45820228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00740f1ea6cb52978652c1c88dbab0b9fcbd6639261db71226a9b152e6695d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:44:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:44:45 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:44:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734d8fa47494fab233e193daa07f765351b62c5069a0bae2a39152afb06dc6f`  
		Last Modified: Mon, 23 Feb 2026 21:45:48 GMT  
		Size: 41.5 MB (41526702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02ee61e2b5b77e97afbde074c5ca9d54280cadb0cb991a7abf7fa9006864ae`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:097e6be0c3e16cbea0592234a28b6b60018e5d32f46dd0c2878360e5915b7288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3be937e2196db1d2e75a3567fdfea3b1698a38f76c2bce0dc78be0b34202329`

```dockerfile
```

-	Layers:
	-	`sha256:86854d38c4babb52db1b6c5863cc57507eb2630436b1f8d0d8b507860396d6a2`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d23f3f99805b7f228d8a7a21394aab79a87225852c825dc56fc5bd3e92eb1fc`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:eb01098b0bcd3646f698e7b0855ea9a5785f63345783524f6a337b316ac33dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50483003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc474f68be2e1c2663b850514a70065ef688f5ed2517305995a7265b2cfa807f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:35:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
COPY entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:35:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 02:35:14 GMT
CMD ["traefik"]
# Tue, 24 Feb 2026 02:35:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e83e761e01f3ced55ef589660d62f3c7d941ba7c2bf18c026865126d409786`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c763a5ea14c310e9208042a4bd71dbb1f67beaa30229bb10b6be8f2aeb68c2`  
		Last Modified: Tue, 24 Feb 2026 02:40:27 GMT  
		Size: 46.4 MB (46436156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac89de76912e22a103c365cd3e3997fd4027c140080093022bdfd0c315fa5707`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:0edf2cd86b067b1e2925b9cb1e16254b46ae45434a764245b33ee49a594860bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dc95c5daa230da213571a54f5799fdfe1f71a23ec14ffd6058b404f33103ca`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f694a95a4d44871c46609debbcb509d50bba6f6be9b4a46735e3efb4e1e2c`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 842.5 KB (842503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d27a12f083199ae685e2c02a1f1944bcbe6b2a6ff414b030d3586efc4994d8b`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:af6a148bbbc3544e2ead792d1df1ba77495f69dcc3419e3653d8d36c133ac919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50460742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43378e6316ff312c7ec91b13b5612dffb7b404555cf356813c29401c33e99276`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:39:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:39:57 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:39:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7ceb67b0194a6ba4f4badec8c1709c1d0eaa50ca1bcdcc9b3032cc18359a3`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3001c4417109fab86a61c94fe5b54752f1499a0d6240302a869c9416b3a44b`  
		Last Modified: Mon, 23 Feb 2026 21:41:16 GMT  
		Size: 46.3 MB (46273294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d42fdf72de7429c2f4cf3771fd87b1d7d051fe2b7d37a860979ebaff2c539`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:96e15fd60f99299c4054e028d5f78d00c8b104fc02477b277a1905ba638b680e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3ba2aacb6bb88cb964d1afed3f49a55e023f773925181bd5d31671f0833624`

```dockerfile
```

-	Layers:
	-	`sha256:a03c3ab0ade3067c81f995a0a62d2f323d60b3573d862c77732b1525525f25ff`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 842.4 KB (842449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fe3a7b0b3ca5cfc59f60587c0606ba59120e2ad277ba4c1f2a2a26d15bbd92`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:3aef91c172ca827e372b718b6da51e58e5d613ed156e7b1545b3d0ac44e333d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8ab0b4fd735d3f05d56c46107c14f18c69e84c374c370fcc663a5ab1d0b6251b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175488260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc42f1edd010f65a13b0deb282899401eac6e476af1cb7a811b5aab721dd59a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 23 Feb 2026 22:09:32 GMT
RUN cmd /S /C #(nop) COPY file:446d33bf3cb43dd9b08930d97b5980de726b2e7e2a3b964cc3f07a68650b1328 in \ 
# Mon, 23 Feb 2026 22:09:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 23 Feb 2026 22:09:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 22:09:36 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdce0ae5ea5f347db1dc87f4ab0e987abbd8d31406fa9a0dca2a6d525e3272bd`  
		Last Modified: Mon, 23 Feb 2026 22:10:22 GMT  
		Size: 48.8 MB (48839231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3cc3648513ddca8db55ea24b85088c148b58b85b2fa91de565ac2407cd81cc`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee51efeb9b7010f464fa83b96c5da1a25e2c68dab8237ddbae7129b7c7dfe61`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52eaad9519efc142a66a7676b80ad714ae1e93e2a4b9d0a8bb6aa5d19dba9fb`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:76e1a223bc200a4579781418ff80770fa163e2a7133b14ede32ba56fcfc16909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:aa6c45febeab2eefddfb0c4a96a4264bc1265261432f29a483b00d8997a71402
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912168854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028a3f3bac0de29b0c4ab11a3281c9f33fedfd2d6fab00e8402cb2ba83ad806e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:45:08 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:45:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:45:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f406a064c9213d2d4e7e3d50c235af90ecb975d188ce5ed2102c8d620eeb4f`  
		Last Modified: Mon, 23 Feb 2026 21:45:58 GMT  
		Size: 49.5 MB (49506380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204cfc419a02f90f5f10ef4ea45d32bfc4658e2ef0dc737969c0f46a9580f5f`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68134cba67c602ff14c309a5f2622964f8b960110006d5133a07000e36fe4a26`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1075592b3ec9c230e5c57316bc511e439da63912a597a0a37711723f736afe9`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:9004e1cd1e33c5eb0b6ec02bc6cfda61fe9caca36751114b1c9c6662f01b264a
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
$ docker pull traefik@sha256:f67a287e3fdac92334fb44f291b6f264338964fd7e7a0e135b8e9e16da6d41d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52398801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1363849f5ded978b0f3cac5bc987a50efa16390f04c901c67b7f23b4ad50a108`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:50 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:52 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69b16dbe9a1607aff902a7d5704118bbd2bc20f15a1f23dda7da5c02a5fe97a`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd7a60bfeea59f33fb1ec9fad0c59c616003b3e8fd4a5e4faac495eebd86acf`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 48.1 MB (48075673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c596a59ba68b851af3b95b35e11c7c1f893726ae89f03ed5fb08db1096c0b0e4`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:491f3860ea2d70663d656246f29f14e5658a1744637da461e4a493413388aebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2851b10c3b79bf1f5d758d60c97a9b6ecbf22e0e4ffd1453505ade53cafa82`

```dockerfile
```

-	Layers:
	-	`sha256:89c2f8ffcce03acdd14af76df692906d70650cda5ba5bc5a1e5b9dd1e7a807de`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 843.1 KB (843100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afe2b0963e813e17f1f928c19d1c929dfa17378a67b128595f92127148de43e`  
		Last Modified: Mon, 23 Feb 2026 21:38:13 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3ca153ac7a2feb40a6e7c753bc934312c2541baec6f1b5410cc8af7de3646f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47687176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f3d390622308f39d576f57627811d73c0f7574c05ea6dce33c71d219e6686f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:38:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:38:19 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:38:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:38:19 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:38:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3e978ee778f3b618cca62a4a462cb6a361b8034fc57d09610610316921b42`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99a1c33a617c42badfb20775968507fb27d8f8cd6728f9627d24a447ebc6f6a`  
		Last Modified: Mon, 23 Feb 2026 21:38:28 GMT  
		Size: 43.7 MB (43655541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123278dcdd5b55740047689571cb4e65c45dab1fbc1c82ce6b771ba934c3bf4c`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:d8759a6938af55d2dc163dff5357d735aca2deb48daeceaec724677b55136e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9923d7f66fac7138bf3cd183d8b5ed985dfa70ef1987cc9f889d13af29569117`

```dockerfile
```

-	Layers:
	-	`sha256:5948bd375fa2600a6c2b02e48253db975805b56fbadac8853266781e92e7f387`  
		Last Modified: Mon, 23 Feb 2026 21:38:27 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ee0eede00d38cc55f39c7cd554aee4df98723bd0197e2cc353febff7d8cf45bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47606676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b3f20d21e585ef763977bb931ad16fb1727cd85dc46f924abd2c50afd0dcc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:37:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:37:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:37:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:37:51 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:37:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ad60ba9b215c3dfe6fbdfeeea8698938fd44787f683d775384a397a1570702`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 463.0 KB (462985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc5e2f7f7ad9bff294bd9b659aea6b0e54bab73b06cf503a5158cfb93e6a7d4`  
		Last Modified: Mon, 23 Feb 2026 21:38:17 GMT  
		Size: 42.9 MB (42946230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a838cc94626e57d024a9c1ad516a10ccfa5604e0b895329a2ecbda12ac42dbb0`  
		Last Modified: Mon, 23 Feb 2026 21:38:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:684ea79188f81602565e2a670390682603234e932a639874377082e7152b2b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1d6335065015f71b7ac0c913176ac43af2d3f30b8ec0f883b527121b3c26a8`

```dockerfile
```

-	Layers:
	-	`sha256:9503e2b4dfba893d49f85b1b5e68d2efb306ca46dbc6633ed0ffa7a36bb26f15`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 842.6 KB (842554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e7792640924d2cb1713a5d3ec10f1da2d06b1f769ea14083879e8921e038cb`  
		Last Modified: Mon, 23 Feb 2026 21:38:16 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:e741c69957cd3226603f44ccc6e001c9d41edbebb99556b64ce70856ed6ebfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45820228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00740f1ea6cb52978652c1c88dbab0b9fcbd6639261db71226a9b152e6695d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:44:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:44:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:44:45 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:44:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734d8fa47494fab233e193daa07f765351b62c5069a0bae2a39152afb06dc6f`  
		Last Modified: Mon, 23 Feb 2026 21:45:48 GMT  
		Size: 41.5 MB (41526702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02ee61e2b5b77e97afbde074c5ca9d54280cadb0cb991a7abf7fa9006864ae`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:097e6be0c3e16cbea0592234a28b6b60018e5d32f46dd0c2878360e5915b7288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3be937e2196db1d2e75a3567fdfea3b1698a38f76c2bce0dc78be0b34202329`

```dockerfile
```

-	Layers:
	-	`sha256:86854d38c4babb52db1b6c5863cc57507eb2630436b1f8d0d8b507860396d6a2`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 842.5 KB (842507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d23f3f99805b7f228d8a7a21394aab79a87225852c825dc56fc5bd3e92eb1fc`  
		Last Modified: Mon, 23 Feb 2026 21:45:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:eb01098b0bcd3646f698e7b0855ea9a5785f63345783524f6a337b316ac33dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50483003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc474f68be2e1c2663b850514a70065ef688f5ed2517305995a7265b2cfa807f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:35:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
COPY entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 02:35:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:35:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 02:35:14 GMT
CMD ["traefik"]
# Tue, 24 Feb 2026 02:35:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e83e761e01f3ced55ef589660d62f3c7d941ba7c2bf18c026865126d409786`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c763a5ea14c310e9208042a4bd71dbb1f67beaa30229bb10b6be8f2aeb68c2`  
		Last Modified: Tue, 24 Feb 2026 02:40:27 GMT  
		Size: 46.4 MB (46436156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac89de76912e22a103c365cd3e3997fd4027c140080093022bdfd0c315fa5707`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0edf2cd86b067b1e2925b9cb1e16254b46ae45434a764245b33ee49a594860bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dc95c5daa230da213571a54f5799fdfe1f71a23ec14ffd6058b404f33103ca`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f694a95a4d44871c46609debbcb509d50bba6f6be9b4a46735e3efb4e1e2c`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 842.5 KB (842503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d27a12f083199ae685e2c02a1f1944bcbe6b2a6ff414b030d3586efc4994d8b`  
		Last Modified: Tue, 24 Feb 2026 02:40:20 GMT  
		Size: 12.8 KB (12835 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:af6a148bbbc3544e2ead792d1df1ba77495f69dcc3419e3653d8d36c133ac919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50460742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43378e6316ff312c7ec91b13b5612dffb7b404555cf356813c29401c33e99276`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 21:39:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
COPY entrypoint.sh / # buildkit
# Mon, 23 Feb 2026 21:39:57 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 21:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 21:39:57 GMT
CMD ["traefik"]
# Mon, 23 Feb 2026 21:39:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7ceb67b0194a6ba4f4badec8c1709c1d0eaa50ca1bcdcc9b3032cc18359a3`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3001c4417109fab86a61c94fe5b54752f1499a0d6240302a869c9416b3a44b`  
		Last Modified: Mon, 23 Feb 2026 21:41:16 GMT  
		Size: 46.3 MB (46273294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d42fdf72de7429c2f4cf3771fd87b1d7d051fe2b7d37a860979ebaff2c539`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:96e15fd60f99299c4054e028d5f78d00c8b104fc02477b277a1905ba638b680e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3ba2aacb6bb88cb964d1afed3f49a55e023f773925181bd5d31671f0833624`

```dockerfile
```

-	Layers:
	-	`sha256:a03c3ab0ade3067c81f995a0a62d2f323d60b3573d862c77732b1525525f25ff`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 842.4 KB (842449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fe3a7b0b3ca5cfc59f60587c0606ba59120e2ad277ba4c1f2a2a26d15bbd92`  
		Last Modified: Mon, 23 Feb 2026 21:41:15 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:3aef91c172ca827e372b718b6da51e58e5d613ed156e7b1545b3d0ac44e333d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8ab0b4fd735d3f05d56c46107c14f18c69e84c374c370fcc663a5ab1d0b6251b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175488260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc42f1edd010f65a13b0deb282899401eac6e476af1cb7a811b5aab721dd59a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 23 Feb 2026 22:09:32 GMT
RUN cmd /S /C #(nop) COPY file:446d33bf3cb43dd9b08930d97b5980de726b2e7e2a3b964cc3f07a68650b1328 in \ 
# Mon, 23 Feb 2026 22:09:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 23 Feb 2026 22:09:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 22:09:36 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdce0ae5ea5f347db1dc87f4ab0e987abbd8d31406fa9a0dca2a6d525e3272bd`  
		Last Modified: Mon, 23 Feb 2026 22:10:22 GMT  
		Size: 48.8 MB (48839231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3cc3648513ddca8db55ea24b85088c148b58b85b2fa91de565ac2407cd81cc`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee51efeb9b7010f464fa83b96c5da1a25e2c68dab8237ddbae7129b7c7dfe61`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52eaad9519efc142a66a7676b80ad714ae1e93e2a4b9d0a8bb6aa5d19dba9fb`  
		Last Modified: Mon, 23 Feb 2026 22:09:39 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:76e1a223bc200a4579781418ff80770fa163e2a7133b14ede32ba56fcfc16909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:aa6c45febeab2eefddfb0c4a96a4264bc1265261432f29a483b00d8997a71402
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912168854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028a3f3bac0de29b0c4ab11a3281c9f33fedfd2d6fab00e8402cb2ba83ad806e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:45:08 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:45:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:45:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f406a064c9213d2d4e7e3d50c235af90ecb975d188ce5ed2102c8d620eeb4f`  
		Last Modified: Mon, 23 Feb 2026 21:45:58 GMT  
		Size: 49.5 MB (49506380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204cfc419a02f90f5f10ef4ea45d32bfc4658e2ef0dc737969c0f46a9580f5f`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68134cba67c602ff14c309a5f2622964f8b960110006d5133a07000e36fe4a26`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1075592b3ec9c230e5c57316bc511e439da63912a597a0a37711723f736afe9`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.10`

**does not exist** (yet?)

## `traefik:v3.6.10-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:v3.6.10-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:76e1a223bc200a4579781418ff80770fa163e2a7133b14ede32ba56fcfc16909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:aa6c45febeab2eefddfb0c4a96a4264bc1265261432f29a483b00d8997a71402
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912168854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028a3f3bac0de29b0c4ab11a3281c9f33fedfd2d6fab00e8402cb2ba83ad806e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Mon, 23 Feb 2026 21:43:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Feb 2026 21:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.9/traefik_v3.6.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Feb 2026 21:45:08 GMT
EXPOSE 80
# Mon, 23 Feb 2026 21:45:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Feb 2026 21:45:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7b1c878b3eefb266a32f0d08a70d5c32c9d84f975ba77bdbb427bb074ea126`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f406a064c9213d2d4e7e3d50c235af90ecb975d188ce5ed2102c8d620eeb4f`  
		Last Modified: Mon, 23 Feb 2026 21:45:58 GMT  
		Size: 49.5 MB (49506380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204cfc419a02f90f5f10ef4ea45d32bfc4658e2ef0dc737969c0f46a9580f5f`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68134cba67c602ff14c309a5f2622964f8b960110006d5133a07000e36fe4a26`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1075592b3ec9c230e5c57316bc511e439da63912a597a0a37711723f736afe9`  
		Last Modified: Mon, 23 Feb 2026 21:45:16 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
