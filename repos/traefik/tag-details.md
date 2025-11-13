<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.31`](#traefik21131)
-	[`traefik:2.11.31-nanoserver-ltsc2022`](#traefik21131-nanoserver-ltsc2022)
-	[`traefik:2.11.31-windowsservercore-ltsc2022`](#traefik21131-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.1`](#traefik361)
-	[`traefik:3.6.1-nanoserver-ltsc2022`](#traefik361-nanoserver-ltsc2022)
-	[`traefik:3.6.1-windowsservercore-ltsc2022`](#traefik361-windowsservercore-ltsc2022)
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
-	[`traefik:v2.11.31`](#traefikv21131)
-	[`traefik:v2.11.31-nanoserver-ltsc2022`](#traefikv21131-nanoserver-ltsc2022)
-	[`traefik:v2.11.31-windowsservercore-ltsc2022`](#traefikv21131-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.1`](#traefikv361)
-	[`traefik:v3.6.1-nanoserver-ltsc2022`](#traefikv361-nanoserver-ltsc2022)
-	[`traefik:v3.6.1-windowsservercore-ltsc2022`](#traefikv361-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
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
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
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
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.31`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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

### `traefik:2.11.31` - linux; amd64

```console
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.31` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.31` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.31` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.31` - linux; riscv64

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

### `traefik:2.11.31` - unknown; unknown

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

### `traefik:2.11.31` - linux; s390x

```console
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.31-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11.31-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.31-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11.31-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:fd5932c796f7e2db9fd6bff485ef693d53797f0ee8ad03dc68aa424ea6f21958
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
$ docker pull traefik@sha256:2ba9a6e99daf342de4268279e3f90cdfc1f9d33349b04384be145247a1ef3871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2908c092e5b20b852f9891b365aa5ec46cf2691388fc2e0d33e9d9758bdf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:51 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc116d93e45b7dd6b0e202416a0f87f43cf074bcfbb3840135a3af3955ac5d25`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 456.9 KB (456917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a5be716dde6c158836ea784748160c7e3cce4d05b9e87cf4acf2347554549f`  
		Last Modified: Thu, 13 Nov 2025 19:14:27 GMT  
		Size: 47.4 MB (47433229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12cf03b5b74f31ef0947aa472eefd4fce22995a01973c8144abc637c1f2dfd5`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:e1492e6f42f11978c617abd8b4a21fa865da7ccf11d4bc414b2f6f42eeb67f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7465e314b58062e784680b370d540481a673e78fcf4ca5a8aecccac959980f27`

```dockerfile
```

-	Layers:
	-	`sha256:6670fb0d409908f002c851c5511d0789b795e1816e3121ae259510739cd2254f`  
		Last Modified: Thu, 13 Nov 2025 22:10:33 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6397e1ae01371742c023d5b67c10c9bae0091c72d66b61bcef294dfb8b3952dc`  
		Last Modified: Thu, 13 Nov 2025 22:10:34 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a1d1ac9647edbc2ebf71f02fae36dfb0987f723cb75b2cc34af2662370f6456a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67b9222909a6f3f190f23a5b870f4a022ab35a0b91b895e52f4046d2a01e753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:29 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478833cf572b525173b83aac05920d7faa1767c3ed6bbd77da3163b2cae6b4ae`  
		Last Modified: Thu, 13 Nov 2025 19:13:47 GMT  
		Size: 43.0 MB (42954559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f0e437df47d735153b26cdcc66b1480166934e38f869439d841027f4cc35`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:fc0aee6221bc5414887c9dcadbfdd1ba7686dad6dd77cb727c90ed52c68b2d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2e97386835fa649ec5cd112c3daa4840f3aeefcd7869d3bc8e77781d546c4c`

```dockerfile
```

-	Layers:
	-	`sha256:9b41a77347fa9f26071f17808c1bcf672554222d5d3b4858f24c1c9f2a357b1a`  
		Last Modified: Thu, 13 Nov 2025 22:10:37 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:66932e80d0538da2b2bfe95902efb6fb24a4dc8d9023ce126c6c955f3f1b278a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e894f1bea0e7d825598088e385632ba9365e4b3ad19dc744ccc3fae07cfdb90f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:18 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:20 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3ddfe0bafb1dd910204e794eb628e45b2afe738326d376a5d70eb30f71700e`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79149dff62553ad73224fdf1d11e93d2e70271346ce5a640d52318bb16187596`  
		Last Modified: Thu, 13 Nov 2025 19:13:55 GMT  
		Size: 43.1 MB (43147895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c562cf25ba9f3495b524dee77caa4d1a63314ea71d4196f860e1e26110938e50`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:2b781dfc72ea4be899e6dcea154da96b7ab2a1113f2d5bba19505cd763ce6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9db86cb954917ea716d604cd9839ae3bb1a618c8eec0b46a3e5a57f08ff5a13`

```dockerfile
```

-	Layers:
	-	`sha256:f29ef1727b2134afdfaaf9fb8cb788b01c1f38c533e1cf4092ffa33cebe3b0b0`  
		Last Modified: Thu, 13 Nov 2025 22:10:41 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c90bf4d7b399b4f868701dd3105b7460edd45bf27da061130e0f78d2d043ae5`  
		Last Modified: Thu, 13 Nov 2025 22:10:42 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:5516f662db0b5b3a08843cb2cf973c4a96acf8d450b700b90740eaa5b9e6c34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45322769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d853e9906b1afe1b346f887775f021ca14f984ddeceb11018c0dec475a9a781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:34 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:2a3cc0606b72cc9a105fb59921dc520b2e4355ee7288429aac12513223e0c311`  
		Last Modified: Thu, 13 Nov 2025 19:13:49 GMT  
		Size: 41.1 MB (41130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea2c564ccf61d08c50f750859aad773b368d89040a3ccd29460a760f570961d`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:a0db86a66b16086329348f82dd6db984be72f8f63cd3ea987e00b854fe7856c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618c579126c296a23a35616d335fde341f56191af6cb1fbc29365bfd45c8b460`

```dockerfile
```

-	Layers:
	-	`sha256:ef79b9555be7f951cf5bb85482945d7e54b04d827c2bf096422b0894f1f64fbe`  
		Last Modified: Thu, 13 Nov 2025 22:10:46 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b03fdc549077b0aa8f4eaf5155939c7cd8e2aa7702f091044d88ea9cc03aab1`  
		Last Modified: Thu, 13 Nov 2025 22:10:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:0910886c34c7016f6bfa06f64d1a96afae257d413bb907f657dde7321ae18175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49697126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cce600707e0c46bf7c2b43bce29f05a80e06680700bbdd22644278dbae058b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:18:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:18:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:400bcb23c4605b2e8cc974b06cde9c1359c3968eb7ee5aa439bdbce64755104a`  
		Last Modified: Thu, 13 Nov 2025 19:24:31 GMT  
		Size: 45.7 MB (45724240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477939e0570f35a4b3c6751eab88b3262bb2f6ff48c0318d48bc0c5c45675e3`  
		Last Modified: Thu, 13 Nov 2025 19:24:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:23f5618d53a892148332d57d2ede8d2ee3a8732b7c2dc4b4b54fb816d1d02cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16fa0ba1cab63862239e6082e020a6d21cd4c1de30dc575124f8bdddd6888b3`

```dockerfile
```

-	Layers:
	-	`sha256:36e2999ec319d68f804befceb99d7113aa3974a80a46d0dfb07467cd67523ae9`  
		Last Modified: Thu, 13 Nov 2025 22:10:50 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88060a1568c1937b8510e18b59b41987917f281f321d7b1813972ddbe0a4b695`  
		Last Modified: Thu, 13 Nov 2025 22:10:51 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:57684c57a1e49162f19d657da824d7ea22db26d21eec658cd0bbe68831fd751a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21675f9c8f81318c4c9156f56b9396310b1aefab6e32b8c0237f1d6f420c52d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a010ab16ebfec2b479bc3e300311d009b17476cfe9f80b381b98b0889a839b`  
		Last Modified: Thu, 13 Nov 2025 19:14:42 GMT  
		Size: 45.6 MB (45580717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe2eb642ef817cbf966363ea05d39709a4cbc5d6d2cadb14cecf82956987fcf`  
		Last Modified: Thu, 13 Nov 2025 19:14:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:0f2b3c058a353077b5c72a214ba374ed6df3f7ca72b6d693bbcbb2ac22e6907c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d23d4f2dce825ea204e8e7e5e35683a8725152fb93217969af0631c12286063`

```dockerfile
```

-	Layers:
	-	`sha256:8d9063a18078a6f67adffb6db83e0f78ac4edb1938dff287a82188702bd1cbba`  
		Last Modified: Thu, 13 Nov 2025 22:10:56 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7579dd78d953d239f24779388eb6e7c8ab4459d802f30dda62d2b2f3cf784b`  
		Last Modified: Thu, 13 Nov 2025 22:10:57 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5d6ca30e329165e96c56f1fd156f70c5c2577de35d688f876c97f635163a0785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:b9196e194acf30722e1a9dedf988332b2ebb2552efe7a36ff22cf302aff457e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174526254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0578d8bc4ef5c2cfdd7f48f0c7333cb0a0098cff3cc429ff29897f0186d79e0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:15:07 GMT
RUN cmd /S /C #(nop) COPY file:df006074126428890c75ce9f22baebfdec5a264a990fb6ef8bc8a4b313a3e0e2 in \ 
# Thu, 13 Nov 2025 20:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:15:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90be197a6e9f4e660c67d7abdfdc3ba4e85494254c85ee2c65d1d7d124c64e`  
		Last Modified: Thu, 13 Nov 2025 20:16:02 GMT  
		Size: 48.2 MB (48174025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907fdb6b48a6dbb9bab1403d6fccf06dc677b3b3bf0b8e8f38f14dbed63a73ae`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5bd4f08e951abc1038d0efdc2e7b742ddb0b8f372e30cc6725eabbe83d1e2c`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e577efa40922862889ab39b0ac9aef080548ff69bc03d42197b8c1d80f02ad`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:9c67fc3881910b007a12d907b8df88ae83f70c9587e232d5327473052c680ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:724408b3ccca658b88ac1461cc089a271002fb9e2c5131d3ff30312e89043bc0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818795877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1214d81eb3bbd278e5a08de4e240c31c61b750ac1b03562f8725f4448aab341`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:24:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:24:50 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:24:51 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:24:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:25b20ab24b3f2281ff269a84b2b6019053b1dadcb1229fc0dcc0ce962f0ad701`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2d0c7a5b72413426fcd192c7803ae2597b6d6e53797b4d647bf4b03adc456`  
		Last Modified: Thu, 13 Nov 2025 19:25:57 GMT  
		Size: 48.8 MB (48829162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d265d05fa488ae24de5bb4a67509b668a3c411fb2326470ca65ecb85b8cadfb`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9a4faafbd41fe83f32192c4866c1a3ddbcb5f0c83cced89ffba313cc4b727e`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ac1488c6eb1af5018f2b64e40a535357b72ecc8918336d498fdfcad8479e52`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:fd5932c796f7e2db9fd6bff485ef693d53797f0ee8ad03dc68aa424ea6f21958
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
$ docker pull traefik@sha256:2ba9a6e99daf342de4268279e3f90cdfc1f9d33349b04384be145247a1ef3871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2908c092e5b20b852f9891b365aa5ec46cf2691388fc2e0d33e9d9758bdf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:51 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc116d93e45b7dd6b0e202416a0f87f43cf074bcfbb3840135a3af3955ac5d25`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 456.9 KB (456917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a5be716dde6c158836ea784748160c7e3cce4d05b9e87cf4acf2347554549f`  
		Last Modified: Thu, 13 Nov 2025 19:14:27 GMT  
		Size: 47.4 MB (47433229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12cf03b5b74f31ef0947aa472eefd4fce22995a01973c8144abc637c1f2dfd5`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:e1492e6f42f11978c617abd8b4a21fa865da7ccf11d4bc414b2f6f42eeb67f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7465e314b58062e784680b370d540481a673e78fcf4ca5a8aecccac959980f27`

```dockerfile
```

-	Layers:
	-	`sha256:6670fb0d409908f002c851c5511d0789b795e1816e3121ae259510739cd2254f`  
		Last Modified: Thu, 13 Nov 2025 22:10:33 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6397e1ae01371742c023d5b67c10c9bae0091c72d66b61bcef294dfb8b3952dc`  
		Last Modified: Thu, 13 Nov 2025 22:10:34 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a1d1ac9647edbc2ebf71f02fae36dfb0987f723cb75b2cc34af2662370f6456a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67b9222909a6f3f190f23a5b870f4a022ab35a0b91b895e52f4046d2a01e753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:29 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478833cf572b525173b83aac05920d7faa1767c3ed6bbd77da3163b2cae6b4ae`  
		Last Modified: Thu, 13 Nov 2025 19:13:47 GMT  
		Size: 43.0 MB (42954559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f0e437df47d735153b26cdcc66b1480166934e38f869439d841027f4cc35`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:fc0aee6221bc5414887c9dcadbfdd1ba7686dad6dd77cb727c90ed52c68b2d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2e97386835fa649ec5cd112c3daa4840f3aeefcd7869d3bc8e77781d546c4c`

```dockerfile
```

-	Layers:
	-	`sha256:9b41a77347fa9f26071f17808c1bcf672554222d5d3b4858f24c1c9f2a357b1a`  
		Last Modified: Thu, 13 Nov 2025 22:10:37 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:66932e80d0538da2b2bfe95902efb6fb24a4dc8d9023ce126c6c955f3f1b278a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e894f1bea0e7d825598088e385632ba9365e4b3ad19dc744ccc3fae07cfdb90f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:18 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:20 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3ddfe0bafb1dd910204e794eb628e45b2afe738326d376a5d70eb30f71700e`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79149dff62553ad73224fdf1d11e93d2e70271346ce5a640d52318bb16187596`  
		Last Modified: Thu, 13 Nov 2025 19:13:55 GMT  
		Size: 43.1 MB (43147895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c562cf25ba9f3495b524dee77caa4d1a63314ea71d4196f860e1e26110938e50`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:2b781dfc72ea4be899e6dcea154da96b7ab2a1113f2d5bba19505cd763ce6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9db86cb954917ea716d604cd9839ae3bb1a618c8eec0b46a3e5a57f08ff5a13`

```dockerfile
```

-	Layers:
	-	`sha256:f29ef1727b2134afdfaaf9fb8cb788b01c1f38c533e1cf4092ffa33cebe3b0b0`  
		Last Modified: Thu, 13 Nov 2025 22:10:41 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c90bf4d7b399b4f868701dd3105b7460edd45bf27da061130e0f78d2d043ae5`  
		Last Modified: Thu, 13 Nov 2025 22:10:42 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:5516f662db0b5b3a08843cb2cf973c4a96acf8d450b700b90740eaa5b9e6c34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45322769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d853e9906b1afe1b346f887775f021ca14f984ddeceb11018c0dec475a9a781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:34 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:2a3cc0606b72cc9a105fb59921dc520b2e4355ee7288429aac12513223e0c311`  
		Last Modified: Thu, 13 Nov 2025 19:13:49 GMT  
		Size: 41.1 MB (41130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea2c564ccf61d08c50f750859aad773b368d89040a3ccd29460a760f570961d`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:a0db86a66b16086329348f82dd6db984be72f8f63cd3ea987e00b854fe7856c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618c579126c296a23a35616d335fde341f56191af6cb1fbc29365bfd45c8b460`

```dockerfile
```

-	Layers:
	-	`sha256:ef79b9555be7f951cf5bb85482945d7e54b04d827c2bf096422b0894f1f64fbe`  
		Last Modified: Thu, 13 Nov 2025 22:10:46 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b03fdc549077b0aa8f4eaf5155939c7cd8e2aa7702f091044d88ea9cc03aab1`  
		Last Modified: Thu, 13 Nov 2025 22:10:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:0910886c34c7016f6bfa06f64d1a96afae257d413bb907f657dde7321ae18175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49697126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cce600707e0c46bf7c2b43bce29f05a80e06680700bbdd22644278dbae058b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:18:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:18:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:400bcb23c4605b2e8cc974b06cde9c1359c3968eb7ee5aa439bdbce64755104a`  
		Last Modified: Thu, 13 Nov 2025 19:24:31 GMT  
		Size: 45.7 MB (45724240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477939e0570f35a4b3c6751eab88b3262bb2f6ff48c0318d48bc0c5c45675e3`  
		Last Modified: Thu, 13 Nov 2025 19:24:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:23f5618d53a892148332d57d2ede8d2ee3a8732b7c2dc4b4b54fb816d1d02cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16fa0ba1cab63862239e6082e020a6d21cd4c1de30dc575124f8bdddd6888b3`

```dockerfile
```

-	Layers:
	-	`sha256:36e2999ec319d68f804befceb99d7113aa3974a80a46d0dfb07467cd67523ae9`  
		Last Modified: Thu, 13 Nov 2025 22:10:50 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88060a1568c1937b8510e18b59b41987917f281f321d7b1813972ddbe0a4b695`  
		Last Modified: Thu, 13 Nov 2025 22:10:51 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:57684c57a1e49162f19d657da824d7ea22db26d21eec658cd0bbe68831fd751a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21675f9c8f81318c4c9156f56b9396310b1aefab6e32b8c0237f1d6f420c52d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a010ab16ebfec2b479bc3e300311d009b17476cfe9f80b381b98b0889a839b`  
		Last Modified: Thu, 13 Nov 2025 19:14:42 GMT  
		Size: 45.6 MB (45580717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe2eb642ef817cbf966363ea05d39709a4cbc5d6d2cadb14cecf82956987fcf`  
		Last Modified: Thu, 13 Nov 2025 19:14:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0f2b3c058a353077b5c72a214ba374ed6df3f7ca72b6d693bbcbb2ac22e6907c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d23d4f2dce825ea204e8e7e5e35683a8725152fb93217969af0631c12286063`

```dockerfile
```

-	Layers:
	-	`sha256:8d9063a18078a6f67adffb6db83e0f78ac4edb1938dff287a82188702bd1cbba`  
		Last Modified: Thu, 13 Nov 2025 22:10:56 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7579dd78d953d239f24779388eb6e7c8ab4459d802f30dda62d2b2f3cf784b`  
		Last Modified: Thu, 13 Nov 2025 22:10:57 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5d6ca30e329165e96c56f1fd156f70c5c2577de35d688f876c97f635163a0785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:b9196e194acf30722e1a9dedf988332b2ebb2552efe7a36ff22cf302aff457e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174526254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0578d8bc4ef5c2cfdd7f48f0c7333cb0a0098cff3cc429ff29897f0186d79e0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:15:07 GMT
RUN cmd /S /C #(nop) COPY file:df006074126428890c75ce9f22baebfdec5a264a990fb6ef8bc8a4b313a3e0e2 in \ 
# Thu, 13 Nov 2025 20:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:15:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90be197a6e9f4e660c67d7abdfdc3ba4e85494254c85ee2c65d1d7d124c64e`  
		Last Modified: Thu, 13 Nov 2025 20:16:02 GMT  
		Size: 48.2 MB (48174025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907fdb6b48a6dbb9bab1403d6fccf06dc677b3b3bf0b8e8f38f14dbed63a73ae`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5bd4f08e951abc1038d0efdc2e7b742ddb0b8f372e30cc6725eabbe83d1e2c`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e577efa40922862889ab39b0ac9aef080548ff69bc03d42197b8c1d80f02ad`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:9c67fc3881910b007a12d907b8df88ae83f70c9587e232d5327473052c680ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:724408b3ccca658b88ac1461cc089a271002fb9e2c5131d3ff30312e89043bc0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818795877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1214d81eb3bbd278e5a08de4e240c31c61b750ac1b03562f8725f4448aab341`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:24:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:24:50 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:24:51 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:24:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:25b20ab24b3f2281ff269a84b2b6019053b1dadcb1229fc0dcc0ce962f0ad701`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2d0c7a5b72413426fcd192c7803ae2597b6d6e53797b4d647bf4b03adc456`  
		Last Modified: Thu, 13 Nov 2025 19:25:57 GMT  
		Size: 48.8 MB (48829162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d265d05fa488ae24de5bb4a67509b668a3c411fb2326470ca65ecb85b8cadfb`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9a4faafbd41fe83f32192c4866c1a3ddbcb5f0c83cced89ffba313cc4b727e`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ac1488c6eb1af5018f2b64e40a535357b72ecc8918336d498fdfcad8479e52`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.1`

```console
$ docker pull traefik@sha256:fd5932c796f7e2db9fd6bff485ef693d53797f0ee8ad03dc68aa424ea6f21958
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

### `traefik:3.6.1` - linux; amd64

```console
$ docker pull traefik@sha256:2ba9a6e99daf342de4268279e3f90cdfc1f9d33349b04384be145247a1ef3871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2908c092e5b20b852f9891b365aa5ec46cf2691388fc2e0d33e9d9758bdf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:51 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc116d93e45b7dd6b0e202416a0f87f43cf074bcfbb3840135a3af3955ac5d25`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 456.9 KB (456917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a5be716dde6c158836ea784748160c7e3cce4d05b9e87cf4acf2347554549f`  
		Last Modified: Thu, 13 Nov 2025 19:14:27 GMT  
		Size: 47.4 MB (47433229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12cf03b5b74f31ef0947aa472eefd4fce22995a01973c8144abc637c1f2dfd5`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:e1492e6f42f11978c617abd8b4a21fa865da7ccf11d4bc414b2f6f42eeb67f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7465e314b58062e784680b370d540481a673e78fcf4ca5a8aecccac959980f27`

```dockerfile
```

-	Layers:
	-	`sha256:6670fb0d409908f002c851c5511d0789b795e1816e3121ae259510739cd2254f`  
		Last Modified: Thu, 13 Nov 2025 22:10:33 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6397e1ae01371742c023d5b67c10c9bae0091c72d66b61bcef294dfb8b3952dc`  
		Last Modified: Thu, 13 Nov 2025 22:10:34 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a1d1ac9647edbc2ebf71f02fae36dfb0987f723cb75b2cc34af2662370f6456a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67b9222909a6f3f190f23a5b870f4a022ab35a0b91b895e52f4046d2a01e753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:29 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478833cf572b525173b83aac05920d7faa1767c3ed6bbd77da3163b2cae6b4ae`  
		Last Modified: Thu, 13 Nov 2025 19:13:47 GMT  
		Size: 43.0 MB (42954559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f0e437df47d735153b26cdcc66b1480166934e38f869439d841027f4cc35`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:fc0aee6221bc5414887c9dcadbfdd1ba7686dad6dd77cb727c90ed52c68b2d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2e97386835fa649ec5cd112c3daa4840f3aeefcd7869d3bc8e77781d546c4c`

```dockerfile
```

-	Layers:
	-	`sha256:9b41a77347fa9f26071f17808c1bcf672554222d5d3b4858f24c1c9f2a357b1a`  
		Last Modified: Thu, 13 Nov 2025 22:10:37 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:66932e80d0538da2b2bfe95902efb6fb24a4dc8d9023ce126c6c955f3f1b278a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e894f1bea0e7d825598088e385632ba9365e4b3ad19dc744ccc3fae07cfdb90f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:18 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:20 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3ddfe0bafb1dd910204e794eb628e45b2afe738326d376a5d70eb30f71700e`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79149dff62553ad73224fdf1d11e93d2e70271346ce5a640d52318bb16187596`  
		Last Modified: Thu, 13 Nov 2025 19:13:55 GMT  
		Size: 43.1 MB (43147895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c562cf25ba9f3495b524dee77caa4d1a63314ea71d4196f860e1e26110938e50`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:2b781dfc72ea4be899e6dcea154da96b7ab2a1113f2d5bba19505cd763ce6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9db86cb954917ea716d604cd9839ae3bb1a618c8eec0b46a3e5a57f08ff5a13`

```dockerfile
```

-	Layers:
	-	`sha256:f29ef1727b2134afdfaaf9fb8cb788b01c1f38c533e1cf4092ffa33cebe3b0b0`  
		Last Modified: Thu, 13 Nov 2025 22:10:41 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c90bf4d7b399b4f868701dd3105b7460edd45bf27da061130e0f78d2d043ae5`  
		Last Modified: Thu, 13 Nov 2025 22:10:42 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.1` - linux; ppc64le

```console
$ docker pull traefik@sha256:5516f662db0b5b3a08843cb2cf973c4a96acf8d450b700b90740eaa5b9e6c34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45322769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d853e9906b1afe1b346f887775f021ca14f984ddeceb11018c0dec475a9a781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:34 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:2a3cc0606b72cc9a105fb59921dc520b2e4355ee7288429aac12513223e0c311`  
		Last Modified: Thu, 13 Nov 2025 19:13:49 GMT  
		Size: 41.1 MB (41130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea2c564ccf61d08c50f750859aad773b368d89040a3ccd29460a760f570961d`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:a0db86a66b16086329348f82dd6db984be72f8f63cd3ea987e00b854fe7856c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618c579126c296a23a35616d335fde341f56191af6cb1fbc29365bfd45c8b460`

```dockerfile
```

-	Layers:
	-	`sha256:ef79b9555be7f951cf5bb85482945d7e54b04d827c2bf096422b0894f1f64fbe`  
		Last Modified: Thu, 13 Nov 2025 22:10:46 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b03fdc549077b0aa8f4eaf5155939c7cd8e2aa7702f091044d88ea9cc03aab1`  
		Last Modified: Thu, 13 Nov 2025 22:10:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.1` - linux; riscv64

```console
$ docker pull traefik@sha256:0910886c34c7016f6bfa06f64d1a96afae257d413bb907f657dde7321ae18175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49697126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cce600707e0c46bf7c2b43bce29f05a80e06680700bbdd22644278dbae058b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:18:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:18:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:400bcb23c4605b2e8cc974b06cde9c1359c3968eb7ee5aa439bdbce64755104a`  
		Last Modified: Thu, 13 Nov 2025 19:24:31 GMT  
		Size: 45.7 MB (45724240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477939e0570f35a4b3c6751eab88b3262bb2f6ff48c0318d48bc0c5c45675e3`  
		Last Modified: Thu, 13 Nov 2025 19:24:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:23f5618d53a892148332d57d2ede8d2ee3a8732b7c2dc4b4b54fb816d1d02cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16fa0ba1cab63862239e6082e020a6d21cd4c1de30dc575124f8bdddd6888b3`

```dockerfile
```

-	Layers:
	-	`sha256:36e2999ec319d68f804befceb99d7113aa3974a80a46d0dfb07467cd67523ae9`  
		Last Modified: Thu, 13 Nov 2025 22:10:50 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88060a1568c1937b8510e18b59b41987917f281f321d7b1813972ddbe0a4b695`  
		Last Modified: Thu, 13 Nov 2025 22:10:51 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.1` - linux; s390x

```console
$ docker pull traefik@sha256:57684c57a1e49162f19d657da824d7ea22db26d21eec658cd0bbe68831fd751a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21675f9c8f81318c4c9156f56b9396310b1aefab6e32b8c0237f1d6f420c52d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a010ab16ebfec2b479bc3e300311d009b17476cfe9f80b381b98b0889a839b`  
		Last Modified: Thu, 13 Nov 2025 19:14:42 GMT  
		Size: 45.6 MB (45580717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe2eb642ef817cbf966363ea05d39709a4cbc5d6d2cadb14cecf82956987fcf`  
		Last Modified: Thu, 13 Nov 2025 19:14:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:0f2b3c058a353077b5c72a214ba374ed6df3f7ca72b6d693bbcbb2ac22e6907c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d23d4f2dce825ea204e8e7e5e35683a8725152fb93217969af0631c12286063`

```dockerfile
```

-	Layers:
	-	`sha256:8d9063a18078a6f67adffb6db83e0f78ac4edb1938dff287a82188702bd1cbba`  
		Last Modified: Thu, 13 Nov 2025 22:10:56 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7579dd78d953d239f24779388eb6e7c8ab4459d802f30dda62d2b2f3cf784b`  
		Last Modified: Thu, 13 Nov 2025 22:10:57 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6.1-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5d6ca30e329165e96c56f1fd156f70c5c2577de35d688f876c97f635163a0785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6.1-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:b9196e194acf30722e1a9dedf988332b2ebb2552efe7a36ff22cf302aff457e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174526254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0578d8bc4ef5c2cfdd7f48f0c7333cb0a0098cff3cc429ff29897f0186d79e0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:15:07 GMT
RUN cmd /S /C #(nop) COPY file:df006074126428890c75ce9f22baebfdec5a264a990fb6ef8bc8a4b313a3e0e2 in \ 
# Thu, 13 Nov 2025 20:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:15:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90be197a6e9f4e660c67d7abdfdc3ba4e85494254c85ee2c65d1d7d124c64e`  
		Last Modified: Thu, 13 Nov 2025 20:16:02 GMT  
		Size: 48.2 MB (48174025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907fdb6b48a6dbb9bab1403d6fccf06dc677b3b3bf0b8e8f38f14dbed63a73ae`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5bd4f08e951abc1038d0efdc2e7b742ddb0b8f372e30cc6725eabbe83d1e2c`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e577efa40922862889ab39b0ac9aef080548ff69bc03d42197b8c1d80f02ad`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.1-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:9c67fc3881910b007a12d907b8df88ae83f70c9587e232d5327473052c680ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:724408b3ccca658b88ac1461cc089a271002fb9e2c5131d3ff30312e89043bc0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818795877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1214d81eb3bbd278e5a08de4e240c31c61b750ac1b03562f8725f4448aab341`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:24:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:24:50 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:24:51 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:24:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:25b20ab24b3f2281ff269a84b2b6019053b1dadcb1229fc0dcc0ce962f0ad701`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2d0c7a5b72413426fcd192c7803ae2597b6d6e53797b4d647bf4b03adc456`  
		Last Modified: Thu, 13 Nov 2025 19:25:57 GMT  
		Size: 48.8 MB (48829162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d265d05fa488ae24de5bb4a67509b668a3c411fb2326470ca65ecb85b8cadfb`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9a4faafbd41fe83f32192c4866c1a3ddbcb5f0c83cced89ffba313cc4b727e`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ac1488c6eb1af5018f2b64e40a535357b72ecc8918336d498fdfcad8479e52`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:fd5932c796f7e2db9fd6bff485ef693d53797f0ee8ad03dc68aa424ea6f21958
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
$ docker pull traefik@sha256:2ba9a6e99daf342de4268279e3f90cdfc1f9d33349b04384be145247a1ef3871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2908c092e5b20b852f9891b365aa5ec46cf2691388fc2e0d33e9d9758bdf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:51 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc116d93e45b7dd6b0e202416a0f87f43cf074bcfbb3840135a3af3955ac5d25`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 456.9 KB (456917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a5be716dde6c158836ea784748160c7e3cce4d05b9e87cf4acf2347554549f`  
		Last Modified: Thu, 13 Nov 2025 19:14:27 GMT  
		Size: 47.4 MB (47433229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12cf03b5b74f31ef0947aa472eefd4fce22995a01973c8144abc637c1f2dfd5`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:e1492e6f42f11978c617abd8b4a21fa865da7ccf11d4bc414b2f6f42eeb67f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7465e314b58062e784680b370d540481a673e78fcf4ca5a8aecccac959980f27`

```dockerfile
```

-	Layers:
	-	`sha256:6670fb0d409908f002c851c5511d0789b795e1816e3121ae259510739cd2254f`  
		Last Modified: Thu, 13 Nov 2025 22:10:33 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6397e1ae01371742c023d5b67c10c9bae0091c72d66b61bcef294dfb8b3952dc`  
		Last Modified: Thu, 13 Nov 2025 22:10:34 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a1d1ac9647edbc2ebf71f02fae36dfb0987f723cb75b2cc34af2662370f6456a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67b9222909a6f3f190f23a5b870f4a022ab35a0b91b895e52f4046d2a01e753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:29 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478833cf572b525173b83aac05920d7faa1767c3ed6bbd77da3163b2cae6b4ae`  
		Last Modified: Thu, 13 Nov 2025 19:13:47 GMT  
		Size: 43.0 MB (42954559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f0e437df47d735153b26cdcc66b1480166934e38f869439d841027f4cc35`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:fc0aee6221bc5414887c9dcadbfdd1ba7686dad6dd77cb727c90ed52c68b2d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2e97386835fa649ec5cd112c3daa4840f3aeefcd7869d3bc8e77781d546c4c`

```dockerfile
```

-	Layers:
	-	`sha256:9b41a77347fa9f26071f17808c1bcf672554222d5d3b4858f24c1c9f2a357b1a`  
		Last Modified: Thu, 13 Nov 2025 22:10:37 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:66932e80d0538da2b2bfe95902efb6fb24a4dc8d9023ce126c6c955f3f1b278a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e894f1bea0e7d825598088e385632ba9365e4b3ad19dc744ccc3fae07cfdb90f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:18 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:20 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3ddfe0bafb1dd910204e794eb628e45b2afe738326d376a5d70eb30f71700e`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79149dff62553ad73224fdf1d11e93d2e70271346ce5a640d52318bb16187596`  
		Last Modified: Thu, 13 Nov 2025 19:13:55 GMT  
		Size: 43.1 MB (43147895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c562cf25ba9f3495b524dee77caa4d1a63314ea71d4196f860e1e26110938e50`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:2b781dfc72ea4be899e6dcea154da96b7ab2a1113f2d5bba19505cd763ce6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9db86cb954917ea716d604cd9839ae3bb1a618c8eec0b46a3e5a57f08ff5a13`

```dockerfile
```

-	Layers:
	-	`sha256:f29ef1727b2134afdfaaf9fb8cb788b01c1f38c533e1cf4092ffa33cebe3b0b0`  
		Last Modified: Thu, 13 Nov 2025 22:10:41 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c90bf4d7b399b4f868701dd3105b7460edd45bf27da061130e0f78d2d043ae5`  
		Last Modified: Thu, 13 Nov 2025 22:10:42 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:5516f662db0b5b3a08843cb2cf973c4a96acf8d450b700b90740eaa5b9e6c34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45322769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d853e9906b1afe1b346f887775f021ca14f984ddeceb11018c0dec475a9a781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:34 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:2a3cc0606b72cc9a105fb59921dc520b2e4355ee7288429aac12513223e0c311`  
		Last Modified: Thu, 13 Nov 2025 19:13:49 GMT  
		Size: 41.1 MB (41130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea2c564ccf61d08c50f750859aad773b368d89040a3ccd29460a760f570961d`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:a0db86a66b16086329348f82dd6db984be72f8f63cd3ea987e00b854fe7856c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618c579126c296a23a35616d335fde341f56191af6cb1fbc29365bfd45c8b460`

```dockerfile
```

-	Layers:
	-	`sha256:ef79b9555be7f951cf5bb85482945d7e54b04d827c2bf096422b0894f1f64fbe`  
		Last Modified: Thu, 13 Nov 2025 22:10:46 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b03fdc549077b0aa8f4eaf5155939c7cd8e2aa7702f091044d88ea9cc03aab1`  
		Last Modified: Thu, 13 Nov 2025 22:10:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:0910886c34c7016f6bfa06f64d1a96afae257d413bb907f657dde7321ae18175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49697126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cce600707e0c46bf7c2b43bce29f05a80e06680700bbdd22644278dbae058b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:18:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:18:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:400bcb23c4605b2e8cc974b06cde9c1359c3968eb7ee5aa439bdbce64755104a`  
		Last Modified: Thu, 13 Nov 2025 19:24:31 GMT  
		Size: 45.7 MB (45724240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477939e0570f35a4b3c6751eab88b3262bb2f6ff48c0318d48bc0c5c45675e3`  
		Last Modified: Thu, 13 Nov 2025 19:24:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:23f5618d53a892148332d57d2ede8d2ee3a8732b7c2dc4b4b54fb816d1d02cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16fa0ba1cab63862239e6082e020a6d21cd4c1de30dc575124f8bdddd6888b3`

```dockerfile
```

-	Layers:
	-	`sha256:36e2999ec319d68f804befceb99d7113aa3974a80a46d0dfb07467cd67523ae9`  
		Last Modified: Thu, 13 Nov 2025 22:10:50 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88060a1568c1937b8510e18b59b41987917f281f321d7b1813972ddbe0a4b695`  
		Last Modified: Thu, 13 Nov 2025 22:10:51 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:57684c57a1e49162f19d657da824d7ea22db26d21eec658cd0bbe68831fd751a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21675f9c8f81318c4c9156f56b9396310b1aefab6e32b8c0237f1d6f420c52d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a010ab16ebfec2b479bc3e300311d009b17476cfe9f80b381b98b0889a839b`  
		Last Modified: Thu, 13 Nov 2025 19:14:42 GMT  
		Size: 45.6 MB (45580717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe2eb642ef817cbf966363ea05d39709a4cbc5d6d2cadb14cecf82956987fcf`  
		Last Modified: Thu, 13 Nov 2025 19:14:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:0f2b3c058a353077b5c72a214ba374ed6df3f7ca72b6d693bbcbb2ac22e6907c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d23d4f2dce825ea204e8e7e5e35683a8725152fb93217969af0631c12286063`

```dockerfile
```

-	Layers:
	-	`sha256:8d9063a18078a6f67adffb6db83e0f78ac4edb1938dff287a82188702bd1cbba`  
		Last Modified: Thu, 13 Nov 2025 22:10:56 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7579dd78d953d239f24779388eb6e7c8ab4459d802f30dda62d2b2f3cf784b`  
		Last Modified: Thu, 13 Nov 2025 22:10:57 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
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
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5d6ca30e329165e96c56f1fd156f70c5c2577de35d688f876c97f635163a0785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:b9196e194acf30722e1a9dedf988332b2ebb2552efe7a36ff22cf302aff457e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174526254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0578d8bc4ef5c2cfdd7f48f0c7333cb0a0098cff3cc429ff29897f0186d79e0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:15:07 GMT
RUN cmd /S /C #(nop) COPY file:df006074126428890c75ce9f22baebfdec5a264a990fb6ef8bc8a4b313a3e0e2 in \ 
# Thu, 13 Nov 2025 20:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:15:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90be197a6e9f4e660c67d7abdfdc3ba4e85494254c85ee2c65d1d7d124c64e`  
		Last Modified: Thu, 13 Nov 2025 20:16:02 GMT  
		Size: 48.2 MB (48174025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907fdb6b48a6dbb9bab1403d6fccf06dc677b3b3bf0b8e8f38f14dbed63a73ae`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5bd4f08e951abc1038d0efdc2e7b742ddb0b8f372e30cc6725eabbe83d1e2c`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e577efa40922862889ab39b0ac9aef080548ff69bc03d42197b8c1d80f02ad`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:fd5932c796f7e2db9fd6bff485ef693d53797f0ee8ad03dc68aa424ea6f21958
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
$ docker pull traefik@sha256:2ba9a6e99daf342de4268279e3f90cdfc1f9d33349b04384be145247a1ef3871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2908c092e5b20b852f9891b365aa5ec46cf2691388fc2e0d33e9d9758bdf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:51 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc116d93e45b7dd6b0e202416a0f87f43cf074bcfbb3840135a3af3955ac5d25`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 456.9 KB (456917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a5be716dde6c158836ea784748160c7e3cce4d05b9e87cf4acf2347554549f`  
		Last Modified: Thu, 13 Nov 2025 19:14:27 GMT  
		Size: 47.4 MB (47433229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12cf03b5b74f31ef0947aa472eefd4fce22995a01973c8144abc637c1f2dfd5`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:e1492e6f42f11978c617abd8b4a21fa865da7ccf11d4bc414b2f6f42eeb67f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7465e314b58062e784680b370d540481a673e78fcf4ca5a8aecccac959980f27`

```dockerfile
```

-	Layers:
	-	`sha256:6670fb0d409908f002c851c5511d0789b795e1816e3121ae259510739cd2254f`  
		Last Modified: Thu, 13 Nov 2025 22:10:33 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6397e1ae01371742c023d5b67c10c9bae0091c72d66b61bcef294dfb8b3952dc`  
		Last Modified: Thu, 13 Nov 2025 22:10:34 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a1d1ac9647edbc2ebf71f02fae36dfb0987f723cb75b2cc34af2662370f6456a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67b9222909a6f3f190f23a5b870f4a022ab35a0b91b895e52f4046d2a01e753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:29 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478833cf572b525173b83aac05920d7faa1767c3ed6bbd77da3163b2cae6b4ae`  
		Last Modified: Thu, 13 Nov 2025 19:13:47 GMT  
		Size: 43.0 MB (42954559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f0e437df47d735153b26cdcc66b1480166934e38f869439d841027f4cc35`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:fc0aee6221bc5414887c9dcadbfdd1ba7686dad6dd77cb727c90ed52c68b2d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2e97386835fa649ec5cd112c3daa4840f3aeefcd7869d3bc8e77781d546c4c`

```dockerfile
```

-	Layers:
	-	`sha256:9b41a77347fa9f26071f17808c1bcf672554222d5d3b4858f24c1c9f2a357b1a`  
		Last Modified: Thu, 13 Nov 2025 22:10:37 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:66932e80d0538da2b2bfe95902efb6fb24a4dc8d9023ce126c6c955f3f1b278a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e894f1bea0e7d825598088e385632ba9365e4b3ad19dc744ccc3fae07cfdb90f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:18 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:20 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3ddfe0bafb1dd910204e794eb628e45b2afe738326d376a5d70eb30f71700e`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79149dff62553ad73224fdf1d11e93d2e70271346ce5a640d52318bb16187596`  
		Last Modified: Thu, 13 Nov 2025 19:13:55 GMT  
		Size: 43.1 MB (43147895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c562cf25ba9f3495b524dee77caa4d1a63314ea71d4196f860e1e26110938e50`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:2b781dfc72ea4be899e6dcea154da96b7ab2a1113f2d5bba19505cd763ce6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9db86cb954917ea716d604cd9839ae3bb1a618c8eec0b46a3e5a57f08ff5a13`

```dockerfile
```

-	Layers:
	-	`sha256:f29ef1727b2134afdfaaf9fb8cb788b01c1f38c533e1cf4092ffa33cebe3b0b0`  
		Last Modified: Thu, 13 Nov 2025 22:10:41 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c90bf4d7b399b4f868701dd3105b7460edd45bf27da061130e0f78d2d043ae5`  
		Last Modified: Thu, 13 Nov 2025 22:10:42 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:5516f662db0b5b3a08843cb2cf973c4a96acf8d450b700b90740eaa5b9e6c34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45322769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d853e9906b1afe1b346f887775f021ca14f984ddeceb11018c0dec475a9a781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:34 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:2a3cc0606b72cc9a105fb59921dc520b2e4355ee7288429aac12513223e0c311`  
		Last Modified: Thu, 13 Nov 2025 19:13:49 GMT  
		Size: 41.1 MB (41130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea2c564ccf61d08c50f750859aad773b368d89040a3ccd29460a760f570961d`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:a0db86a66b16086329348f82dd6db984be72f8f63cd3ea987e00b854fe7856c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618c579126c296a23a35616d335fde341f56191af6cb1fbc29365bfd45c8b460`

```dockerfile
```

-	Layers:
	-	`sha256:ef79b9555be7f951cf5bb85482945d7e54b04d827c2bf096422b0894f1f64fbe`  
		Last Modified: Thu, 13 Nov 2025 22:10:46 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b03fdc549077b0aa8f4eaf5155939c7cd8e2aa7702f091044d88ea9cc03aab1`  
		Last Modified: Thu, 13 Nov 2025 22:10:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:0910886c34c7016f6bfa06f64d1a96afae257d413bb907f657dde7321ae18175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49697126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cce600707e0c46bf7c2b43bce29f05a80e06680700bbdd22644278dbae058b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:18:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:18:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:400bcb23c4605b2e8cc974b06cde9c1359c3968eb7ee5aa439bdbce64755104a`  
		Last Modified: Thu, 13 Nov 2025 19:24:31 GMT  
		Size: 45.7 MB (45724240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477939e0570f35a4b3c6751eab88b3262bb2f6ff48c0318d48bc0c5c45675e3`  
		Last Modified: Thu, 13 Nov 2025 19:24:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:23f5618d53a892148332d57d2ede8d2ee3a8732b7c2dc4b4b54fb816d1d02cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16fa0ba1cab63862239e6082e020a6d21cd4c1de30dc575124f8bdddd6888b3`

```dockerfile
```

-	Layers:
	-	`sha256:36e2999ec319d68f804befceb99d7113aa3974a80a46d0dfb07467cd67523ae9`  
		Last Modified: Thu, 13 Nov 2025 22:10:50 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88060a1568c1937b8510e18b59b41987917f281f321d7b1813972ddbe0a4b695`  
		Last Modified: Thu, 13 Nov 2025 22:10:51 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:57684c57a1e49162f19d657da824d7ea22db26d21eec658cd0bbe68831fd751a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21675f9c8f81318c4c9156f56b9396310b1aefab6e32b8c0237f1d6f420c52d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a010ab16ebfec2b479bc3e300311d009b17476cfe9f80b381b98b0889a839b`  
		Last Modified: Thu, 13 Nov 2025 19:14:42 GMT  
		Size: 45.6 MB (45580717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe2eb642ef817cbf966363ea05d39709a4cbc5d6d2cadb14cecf82956987fcf`  
		Last Modified: Thu, 13 Nov 2025 19:14:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:0f2b3c058a353077b5c72a214ba374ed6df3f7ca72b6d693bbcbb2ac22e6907c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d23d4f2dce825ea204e8e7e5e35683a8725152fb93217969af0631c12286063`

```dockerfile
```

-	Layers:
	-	`sha256:8d9063a18078a6f67adffb6db83e0f78ac4edb1938dff287a82188702bd1cbba`  
		Last Modified: Thu, 13 Nov 2025 22:10:56 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7579dd78d953d239f24779388eb6e7c8ab4459d802f30dda62d2b2f3cf784b`  
		Last Modified: Thu, 13 Nov 2025 22:10:57 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5d6ca30e329165e96c56f1fd156f70c5c2577de35d688f876c97f635163a0785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:b9196e194acf30722e1a9dedf988332b2ebb2552efe7a36ff22cf302aff457e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174526254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0578d8bc4ef5c2cfdd7f48f0c7333cb0a0098cff3cc429ff29897f0186d79e0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:15:07 GMT
RUN cmd /S /C #(nop) COPY file:df006074126428890c75ce9f22baebfdec5a264a990fb6ef8bc8a4b313a3e0e2 in \ 
# Thu, 13 Nov 2025 20:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:15:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90be197a6e9f4e660c67d7abdfdc3ba4e85494254c85ee2c65d1d7d124c64e`  
		Last Modified: Thu, 13 Nov 2025 20:16:02 GMT  
		Size: 48.2 MB (48174025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907fdb6b48a6dbb9bab1403d6fccf06dc677b3b3bf0b8e8f38f14dbed63a73ae`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5bd4f08e951abc1038d0efdc2e7b742ddb0b8f372e30cc6725eabbe83d1e2c`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e577efa40922862889ab39b0ac9aef080548ff69bc03d42197b8c1d80f02ad`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:9c67fc3881910b007a12d907b8df88ae83f70c9587e232d5327473052c680ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:724408b3ccca658b88ac1461cc089a271002fb9e2c5131d3ff30312e89043bc0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818795877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1214d81eb3bbd278e5a08de4e240c31c61b750ac1b03562f8725f4448aab341`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:24:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:24:50 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:24:51 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:24:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:25b20ab24b3f2281ff269a84b2b6019053b1dadcb1229fc0dcc0ce962f0ad701`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2d0c7a5b72413426fcd192c7803ae2597b6d6e53797b4d647bf4b03adc456`  
		Last Modified: Thu, 13 Nov 2025 19:25:57 GMT  
		Size: 48.8 MB (48829162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d265d05fa488ae24de5bb4a67509b668a3c411fb2326470ca65ecb85b8cadfb`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9a4faafbd41fe83f32192c4866c1a3ddbcb5f0c83cced89ffba313cc4b727e`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ac1488c6eb1af5018f2b64e40a535357b72ecc8918336d498fdfcad8479e52`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
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
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
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
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.31`

```console
$ docker pull traefik@sha256:91ec852c76c2509984f6c1fddc99322b1a325f26dfdcc85706cb02db06980cb9
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

### `traefik:v2.11.31` - linux; amd64

```console
$ docker pull traefik@sha256:182ecd08da6fc039a7395b8291e2a0b88063e29e5ed57feb15edc84468f3aad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50917369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711a5b11568ec46b618b20fcf76337f12345cf8a4b602db4bf290a2d0dadaff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:58 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6780a15ce59e8be8a6dacf3eaf1a446c64c0ad72649bedb21826be2aa0f2a4`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 456.9 KB (456924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3492de4fd58e7b95fa2b5f1a8210cd13acb007f0ee6c076e9c741fd417f7379`  
		Last Modified: Thu, 13 Nov 2025 19:13:35 GMT  
		Size: 46.7 MB (46657623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ab98f0b9e0f0d235060ac09aef2c0db82930d33f3b7262c6000f858b8e185`  
		Last Modified: Thu, 13 Nov 2025 19:13:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:eb72c387b2444538ab471c2499d43d5c7bc0d37c68a94659c917c71853fa7525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5dff6dd21c7778f9cfee47422ba7549a386355f97c64fd743f90b7196910`

```dockerfile
```

-	Layers:
	-	`sha256:c7181869d789107a7a222236c661f57dfe64d5d3313c860b2409456adb0451a0`  
		Last Modified: Thu, 13 Nov 2025 22:09:36 GMT  
		Size: 855.0 KB (854971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91271f14b96837d1369e724dc99c7283863add2ecb004c881424b9e082b617de`  
		Last Modified: Thu, 13 Nov 2025 22:09:37 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.31` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1b6d13878191cf9e06ce713c6e5f574af43618da370ded6829a806de26d23b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46672214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c204acb814034ef5d4c48c7b3407b8a7014a30fc452a693d587ea45bb483471`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:15:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:15:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:16 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:15:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f57dbce8bd3823f8d2ceb8cb154032396f26d3ccea4796790fe4fb091dce5`  
		Last Modified: Thu, 13 Nov 2025 19:15:36 GMT  
		Size: 42.7 MB (42710029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f6f776dbcfd07716a37f9a653cd5a81e63308ae3d9555e2ab332ee16699f85`  
		Last Modified: Thu, 13 Nov 2025 19:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:609e9acf75cb8006b88e75b41ad909109d03a832e3e650ff42142b57e5d870ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed03220b83789b5805c614bf4ecec537beb20f52fa386146a8d6e184981ac`

```dockerfile
```

-	Layers:
	-	`sha256:486da32aedabcf199093359824ba2e5cc7995d9daa919efb11004810fbf5232a`  
		Last Modified: Thu, 13 Nov 2025 22:09:41 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.31` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ca2127179c52195038fd26e3ed20eb3593065ab17a5ced983ee2f5b9fbebfecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdde9bad6914243557eb7e7cad9275fe7fb038bc38bdb2f76ee8d7999870de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:22 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15000443286858b20e696fde033546f50f103bdd0b551e6f7b5359d918f4da92`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f3da66ca1f547c4943fee8d7540037105c9579ca98fc72aaba14ea0ce238a`  
		Last Modified: Thu, 13 Nov 2025 19:13:57 GMT  
		Size: 42.6 MB (42563442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66962aa545193298720c86cd6662144de4e72f3312270492a140124360f6b61a`  
		Last Modified: Thu, 13 Nov 2025 19:13:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:78ac85b05d37c6052defb15f326c4accc8a8cf9b47b0ebffb8862c4385a0830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939179e68ae34c5fc75b40b4f306957c49528b603ffb5c09ae1df5ad645548`

```dockerfile
```

-	Layers:
	-	`sha256:633c6cc6daf3381d88ba9ef854b85181fb754164a1411c527f90bca700a2dc3e`  
		Last Modified: Thu, 13 Nov 2025 22:09:44 GMT  
		Size: 855.1 KB (855063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5fa48342eaffb4e3d0df5e5a389a28020a92df479376eeb9c6d546c6235bcb`  
		Last Modified: Thu, 13 Nov 2025 22:09:45 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.31` - linux; ppc64le

```console
$ docker pull traefik@sha256:7b2b8416020937e188de930dc89ccd621777c093085b189a6a83388e4700de75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45071308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651687edffb1e79aecb6b0fc6206aa4b1226131abba8f001ac9b821d00ff346`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 20:25:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 20:25:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 20:25:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 20:25:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1377280355c9d2c7db52b1f2c2ebdc779d98db09410d63e989af59a95b278ce8`  
		Last Modified: Thu, 13 Nov 2025 20:26:32 GMT  
		Size: 40.9 MB (40879253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a2616391a252ecffdc2ba7816d3aa88b9fc4b37178da114601edb441216d6`  
		Last Modified: Thu, 13 Nov 2025 20:26:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:4eaaa164ed58388f964ed5c1ba1d3bdc2bda6ccba70350d8ffac90be3a5eadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7468e3da5f0483272bcc5cf6d9d098264c966fdcffdf0c498f50042c0adfe4`

```dockerfile
```

-	Layers:
	-	`sha256:737548a60f754e5b0fe9c410d426f0a9d12105e9ac9218566b28f45657c1ee4b`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 853.1 KB (853072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760b2197bdc4583f9f368ac922f46d0d8d514c00b77a1678151e4bfa02ddbd65`  
		Last Modified: Thu, 13 Nov 2025 22:09:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.31` - linux; riscv64

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

### `traefik:v2.11.31` - unknown; unknown

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

### `traefik:v2.11.31` - linux; s390x

```console
$ docker pull traefik@sha256:693af998ffa7d4d08a097df305fd116b615ce4de743e4c90a2b3e920d6e26ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41153d8b2813de0e38eab4f7b9d8a85856c711afeb512e8bac86b70a6f119f1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b6d308851ca31a26ba927d5391be1aa74107e546f8056bd880cfbbe01b854a`  
		Last Modified: Thu, 13 Nov 2025 19:14:38 GMT  
		Size: 45.2 MB (45193937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81247020778807b820abd22d6d3bdeaadba10fca05e26c596915030801c107e`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.31` - unknown; unknown

```console
$ docker pull traefik@sha256:3f5a0ab9fa98e93eb9a974153acb94b9b703ecbf23736e3dde39e4ed5285c0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68913f934f6323ab1095a1078ff07828777a1148b0215ccf243d00afe4962caa`

```dockerfile
```

-	Layers:
	-	`sha256:26d509148e5fd45361c75ddf1ec2d934173ef989383eb58deff03bb52fb3d510`  
		Last Modified: Thu, 13 Nov 2025 22:09:57 GMT  
		Size: 853.0 KB (853016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc41752be8655c6f9be9eda5e6ab58a661e94fe0134c509da88aae659970c4d`  
		Last Modified: Thu, 13 Nov 2025 22:09:58 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.31-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:aae61788f09632acda1661d4b8f0039f06eaec12a701472695359c7a558d2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11.31-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2425040de232b4cf1e501dc9cdd6d41eba06e8b9b4ed21567e77cabc5af660a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173791425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aade119d4b861c64935ccab38b6f95b9b11902339794dd0efda73b7ee46547b`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:16:12 GMT
RUN cmd /S /C #(nop) COPY file:538c737733185d849e52445ceb96a70617c3af70afe4dbb5098c99241fd9e5ca in \ 
# Thu, 13 Nov 2025 20:16:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:16:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:16:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a21b752eabead63b7e7b00c2f75e92023d4c4bf19e0a0553b4b862fcc08b64`  
		Last Modified: Thu, 13 Nov 2025 20:16:56 GMT  
		Size: 47.4 MB (47439167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db78d6f4429872e31d3bf74c6e476dcd4f000ff0fa7e1c54e9412734616acc38`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e87288450ccf7480a3d43579bac23ad32a78057dae732166ea3f1f7d8843bb`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7f7c5f1bce20ad2fbacf0fb555a564ee4f41af53f6c10b308cf39491cc6e0`  
		Last Modified: Thu, 13 Nov 2025 20:16:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.31-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11.31-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:fd5932c796f7e2db9fd6bff485ef693d53797f0ee8ad03dc68aa424ea6f21958
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
$ docker pull traefik@sha256:2ba9a6e99daf342de4268279e3f90cdfc1f9d33349b04384be145247a1ef3871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2908c092e5b20b852f9891b365aa5ec46cf2691388fc2e0d33e9d9758bdf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:51 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc116d93e45b7dd6b0e202416a0f87f43cf074bcfbb3840135a3af3955ac5d25`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 456.9 KB (456917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a5be716dde6c158836ea784748160c7e3cce4d05b9e87cf4acf2347554549f`  
		Last Modified: Thu, 13 Nov 2025 19:14:27 GMT  
		Size: 47.4 MB (47433229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12cf03b5b74f31ef0947aa472eefd4fce22995a01973c8144abc637c1f2dfd5`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:e1492e6f42f11978c617abd8b4a21fa865da7ccf11d4bc414b2f6f42eeb67f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7465e314b58062e784680b370d540481a673e78fcf4ca5a8aecccac959980f27`

```dockerfile
```

-	Layers:
	-	`sha256:6670fb0d409908f002c851c5511d0789b795e1816e3121ae259510739cd2254f`  
		Last Modified: Thu, 13 Nov 2025 22:10:33 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6397e1ae01371742c023d5b67c10c9bae0091c72d66b61bcef294dfb8b3952dc`  
		Last Modified: Thu, 13 Nov 2025 22:10:34 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a1d1ac9647edbc2ebf71f02fae36dfb0987f723cb75b2cc34af2662370f6456a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67b9222909a6f3f190f23a5b870f4a022ab35a0b91b895e52f4046d2a01e753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:29 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478833cf572b525173b83aac05920d7faa1767c3ed6bbd77da3163b2cae6b4ae`  
		Last Modified: Thu, 13 Nov 2025 19:13:47 GMT  
		Size: 43.0 MB (42954559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f0e437df47d735153b26cdcc66b1480166934e38f869439d841027f4cc35`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:fc0aee6221bc5414887c9dcadbfdd1ba7686dad6dd77cb727c90ed52c68b2d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2e97386835fa649ec5cd112c3daa4840f3aeefcd7869d3bc8e77781d546c4c`

```dockerfile
```

-	Layers:
	-	`sha256:9b41a77347fa9f26071f17808c1bcf672554222d5d3b4858f24c1c9f2a357b1a`  
		Last Modified: Thu, 13 Nov 2025 22:10:37 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:66932e80d0538da2b2bfe95902efb6fb24a4dc8d9023ce126c6c955f3f1b278a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e894f1bea0e7d825598088e385632ba9365e4b3ad19dc744ccc3fae07cfdb90f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:18 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:20 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3ddfe0bafb1dd910204e794eb628e45b2afe738326d376a5d70eb30f71700e`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79149dff62553ad73224fdf1d11e93d2e70271346ce5a640d52318bb16187596`  
		Last Modified: Thu, 13 Nov 2025 19:13:55 GMT  
		Size: 43.1 MB (43147895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c562cf25ba9f3495b524dee77caa4d1a63314ea71d4196f860e1e26110938e50`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:2b781dfc72ea4be899e6dcea154da96b7ab2a1113f2d5bba19505cd763ce6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9db86cb954917ea716d604cd9839ae3bb1a618c8eec0b46a3e5a57f08ff5a13`

```dockerfile
```

-	Layers:
	-	`sha256:f29ef1727b2134afdfaaf9fb8cb788b01c1f38c533e1cf4092ffa33cebe3b0b0`  
		Last Modified: Thu, 13 Nov 2025 22:10:41 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c90bf4d7b399b4f868701dd3105b7460edd45bf27da061130e0f78d2d043ae5`  
		Last Modified: Thu, 13 Nov 2025 22:10:42 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:5516f662db0b5b3a08843cb2cf973c4a96acf8d450b700b90740eaa5b9e6c34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45322769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d853e9906b1afe1b346f887775f021ca14f984ddeceb11018c0dec475a9a781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:34 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:2a3cc0606b72cc9a105fb59921dc520b2e4355ee7288429aac12513223e0c311`  
		Last Modified: Thu, 13 Nov 2025 19:13:49 GMT  
		Size: 41.1 MB (41130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea2c564ccf61d08c50f750859aad773b368d89040a3ccd29460a760f570961d`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:a0db86a66b16086329348f82dd6db984be72f8f63cd3ea987e00b854fe7856c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618c579126c296a23a35616d335fde341f56191af6cb1fbc29365bfd45c8b460`

```dockerfile
```

-	Layers:
	-	`sha256:ef79b9555be7f951cf5bb85482945d7e54b04d827c2bf096422b0894f1f64fbe`  
		Last Modified: Thu, 13 Nov 2025 22:10:46 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b03fdc549077b0aa8f4eaf5155939c7cd8e2aa7702f091044d88ea9cc03aab1`  
		Last Modified: Thu, 13 Nov 2025 22:10:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:0910886c34c7016f6bfa06f64d1a96afae257d413bb907f657dde7321ae18175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49697126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cce600707e0c46bf7c2b43bce29f05a80e06680700bbdd22644278dbae058b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:18:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:18:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:400bcb23c4605b2e8cc974b06cde9c1359c3968eb7ee5aa439bdbce64755104a`  
		Last Modified: Thu, 13 Nov 2025 19:24:31 GMT  
		Size: 45.7 MB (45724240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477939e0570f35a4b3c6751eab88b3262bb2f6ff48c0318d48bc0c5c45675e3`  
		Last Modified: Thu, 13 Nov 2025 19:24:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:23f5618d53a892148332d57d2ede8d2ee3a8732b7c2dc4b4b54fb816d1d02cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16fa0ba1cab63862239e6082e020a6d21cd4c1de30dc575124f8bdddd6888b3`

```dockerfile
```

-	Layers:
	-	`sha256:36e2999ec319d68f804befceb99d7113aa3974a80a46d0dfb07467cd67523ae9`  
		Last Modified: Thu, 13 Nov 2025 22:10:50 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88060a1568c1937b8510e18b59b41987917f281f321d7b1813972ddbe0a4b695`  
		Last Modified: Thu, 13 Nov 2025 22:10:51 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:57684c57a1e49162f19d657da824d7ea22db26d21eec658cd0bbe68831fd751a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21675f9c8f81318c4c9156f56b9396310b1aefab6e32b8c0237f1d6f420c52d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a010ab16ebfec2b479bc3e300311d009b17476cfe9f80b381b98b0889a839b`  
		Last Modified: Thu, 13 Nov 2025 19:14:42 GMT  
		Size: 45.6 MB (45580717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe2eb642ef817cbf966363ea05d39709a4cbc5d6d2cadb14cecf82956987fcf`  
		Last Modified: Thu, 13 Nov 2025 19:14:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:0f2b3c058a353077b5c72a214ba374ed6df3f7ca72b6d693bbcbb2ac22e6907c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d23d4f2dce825ea204e8e7e5e35683a8725152fb93217969af0631c12286063`

```dockerfile
```

-	Layers:
	-	`sha256:8d9063a18078a6f67adffb6db83e0f78ac4edb1938dff287a82188702bd1cbba`  
		Last Modified: Thu, 13 Nov 2025 22:10:56 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7579dd78d953d239f24779388eb6e7c8ab4459d802f30dda62d2b2f3cf784b`  
		Last Modified: Thu, 13 Nov 2025 22:10:57 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5d6ca30e329165e96c56f1fd156f70c5c2577de35d688f876c97f635163a0785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:b9196e194acf30722e1a9dedf988332b2ebb2552efe7a36ff22cf302aff457e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174526254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0578d8bc4ef5c2cfdd7f48f0c7333cb0a0098cff3cc429ff29897f0186d79e0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:15:07 GMT
RUN cmd /S /C #(nop) COPY file:df006074126428890c75ce9f22baebfdec5a264a990fb6ef8bc8a4b313a3e0e2 in \ 
# Thu, 13 Nov 2025 20:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:15:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90be197a6e9f4e660c67d7abdfdc3ba4e85494254c85ee2c65d1d7d124c64e`  
		Last Modified: Thu, 13 Nov 2025 20:16:02 GMT  
		Size: 48.2 MB (48174025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907fdb6b48a6dbb9bab1403d6fccf06dc677b3b3bf0b8e8f38f14dbed63a73ae`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5bd4f08e951abc1038d0efdc2e7b742ddb0b8f372e30cc6725eabbe83d1e2c`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e577efa40922862889ab39b0ac9aef080548ff69bc03d42197b8c1d80f02ad`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:9c67fc3881910b007a12d907b8df88ae83f70c9587e232d5327473052c680ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:724408b3ccca658b88ac1461cc089a271002fb9e2c5131d3ff30312e89043bc0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818795877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1214d81eb3bbd278e5a08de4e240c31c61b750ac1b03562f8725f4448aab341`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:24:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:24:50 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:24:51 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:24:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:25b20ab24b3f2281ff269a84b2b6019053b1dadcb1229fc0dcc0ce962f0ad701`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2d0c7a5b72413426fcd192c7803ae2597b6d6e53797b4d647bf4b03adc456`  
		Last Modified: Thu, 13 Nov 2025 19:25:57 GMT  
		Size: 48.8 MB (48829162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d265d05fa488ae24de5bb4a67509b668a3c411fb2326470ca65ecb85b8cadfb`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9a4faafbd41fe83f32192c4866c1a3ddbcb5f0c83cced89ffba313cc4b727e`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ac1488c6eb1af5018f2b64e40a535357b72ecc8918336d498fdfcad8479e52`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:fd5932c796f7e2db9fd6bff485ef693d53797f0ee8ad03dc68aa424ea6f21958
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
$ docker pull traefik@sha256:2ba9a6e99daf342de4268279e3f90cdfc1f9d33349b04384be145247a1ef3871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2908c092e5b20b852f9891b365aa5ec46cf2691388fc2e0d33e9d9758bdf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:51 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc116d93e45b7dd6b0e202416a0f87f43cf074bcfbb3840135a3af3955ac5d25`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 456.9 KB (456917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a5be716dde6c158836ea784748160c7e3cce4d05b9e87cf4acf2347554549f`  
		Last Modified: Thu, 13 Nov 2025 19:14:27 GMT  
		Size: 47.4 MB (47433229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12cf03b5b74f31ef0947aa472eefd4fce22995a01973c8144abc637c1f2dfd5`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:e1492e6f42f11978c617abd8b4a21fa865da7ccf11d4bc414b2f6f42eeb67f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7465e314b58062e784680b370d540481a673e78fcf4ca5a8aecccac959980f27`

```dockerfile
```

-	Layers:
	-	`sha256:6670fb0d409908f002c851c5511d0789b795e1816e3121ae259510739cd2254f`  
		Last Modified: Thu, 13 Nov 2025 22:10:33 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6397e1ae01371742c023d5b67c10c9bae0091c72d66b61bcef294dfb8b3952dc`  
		Last Modified: Thu, 13 Nov 2025 22:10:34 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a1d1ac9647edbc2ebf71f02fae36dfb0987f723cb75b2cc34af2662370f6456a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67b9222909a6f3f190f23a5b870f4a022ab35a0b91b895e52f4046d2a01e753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:29 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478833cf572b525173b83aac05920d7faa1767c3ed6bbd77da3163b2cae6b4ae`  
		Last Modified: Thu, 13 Nov 2025 19:13:47 GMT  
		Size: 43.0 MB (42954559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f0e437df47d735153b26cdcc66b1480166934e38f869439d841027f4cc35`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:fc0aee6221bc5414887c9dcadbfdd1ba7686dad6dd77cb727c90ed52c68b2d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2e97386835fa649ec5cd112c3daa4840f3aeefcd7869d3bc8e77781d546c4c`

```dockerfile
```

-	Layers:
	-	`sha256:9b41a77347fa9f26071f17808c1bcf672554222d5d3b4858f24c1c9f2a357b1a`  
		Last Modified: Thu, 13 Nov 2025 22:10:37 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:66932e80d0538da2b2bfe95902efb6fb24a4dc8d9023ce126c6c955f3f1b278a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e894f1bea0e7d825598088e385632ba9365e4b3ad19dc744ccc3fae07cfdb90f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:18 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:20 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3ddfe0bafb1dd910204e794eb628e45b2afe738326d376a5d70eb30f71700e`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79149dff62553ad73224fdf1d11e93d2e70271346ce5a640d52318bb16187596`  
		Last Modified: Thu, 13 Nov 2025 19:13:55 GMT  
		Size: 43.1 MB (43147895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c562cf25ba9f3495b524dee77caa4d1a63314ea71d4196f860e1e26110938e50`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:2b781dfc72ea4be899e6dcea154da96b7ab2a1113f2d5bba19505cd763ce6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9db86cb954917ea716d604cd9839ae3bb1a618c8eec0b46a3e5a57f08ff5a13`

```dockerfile
```

-	Layers:
	-	`sha256:f29ef1727b2134afdfaaf9fb8cb788b01c1f38c533e1cf4092ffa33cebe3b0b0`  
		Last Modified: Thu, 13 Nov 2025 22:10:41 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c90bf4d7b399b4f868701dd3105b7460edd45bf27da061130e0f78d2d043ae5`  
		Last Modified: Thu, 13 Nov 2025 22:10:42 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:5516f662db0b5b3a08843cb2cf973c4a96acf8d450b700b90740eaa5b9e6c34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45322769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d853e9906b1afe1b346f887775f021ca14f984ddeceb11018c0dec475a9a781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:34 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:2a3cc0606b72cc9a105fb59921dc520b2e4355ee7288429aac12513223e0c311`  
		Last Modified: Thu, 13 Nov 2025 19:13:49 GMT  
		Size: 41.1 MB (41130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea2c564ccf61d08c50f750859aad773b368d89040a3ccd29460a760f570961d`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:a0db86a66b16086329348f82dd6db984be72f8f63cd3ea987e00b854fe7856c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618c579126c296a23a35616d335fde341f56191af6cb1fbc29365bfd45c8b460`

```dockerfile
```

-	Layers:
	-	`sha256:ef79b9555be7f951cf5bb85482945d7e54b04d827c2bf096422b0894f1f64fbe`  
		Last Modified: Thu, 13 Nov 2025 22:10:46 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b03fdc549077b0aa8f4eaf5155939c7cd8e2aa7702f091044d88ea9cc03aab1`  
		Last Modified: Thu, 13 Nov 2025 22:10:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:0910886c34c7016f6bfa06f64d1a96afae257d413bb907f657dde7321ae18175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49697126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cce600707e0c46bf7c2b43bce29f05a80e06680700bbdd22644278dbae058b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:18:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:18:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:400bcb23c4605b2e8cc974b06cde9c1359c3968eb7ee5aa439bdbce64755104a`  
		Last Modified: Thu, 13 Nov 2025 19:24:31 GMT  
		Size: 45.7 MB (45724240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477939e0570f35a4b3c6751eab88b3262bb2f6ff48c0318d48bc0c5c45675e3`  
		Last Modified: Thu, 13 Nov 2025 19:24:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:23f5618d53a892148332d57d2ede8d2ee3a8732b7c2dc4b4b54fb816d1d02cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16fa0ba1cab63862239e6082e020a6d21cd4c1de30dc575124f8bdddd6888b3`

```dockerfile
```

-	Layers:
	-	`sha256:36e2999ec319d68f804befceb99d7113aa3974a80a46d0dfb07467cd67523ae9`  
		Last Modified: Thu, 13 Nov 2025 22:10:50 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88060a1568c1937b8510e18b59b41987917f281f321d7b1813972ddbe0a4b695`  
		Last Modified: Thu, 13 Nov 2025 22:10:51 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:57684c57a1e49162f19d657da824d7ea22db26d21eec658cd0bbe68831fd751a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21675f9c8f81318c4c9156f56b9396310b1aefab6e32b8c0237f1d6f420c52d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a010ab16ebfec2b479bc3e300311d009b17476cfe9f80b381b98b0889a839b`  
		Last Modified: Thu, 13 Nov 2025 19:14:42 GMT  
		Size: 45.6 MB (45580717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe2eb642ef817cbf966363ea05d39709a4cbc5d6d2cadb14cecf82956987fcf`  
		Last Modified: Thu, 13 Nov 2025 19:14:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0f2b3c058a353077b5c72a214ba374ed6df3f7ca72b6d693bbcbb2ac22e6907c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d23d4f2dce825ea204e8e7e5e35683a8725152fb93217969af0631c12286063`

```dockerfile
```

-	Layers:
	-	`sha256:8d9063a18078a6f67adffb6db83e0f78ac4edb1938dff287a82188702bd1cbba`  
		Last Modified: Thu, 13 Nov 2025 22:10:56 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7579dd78d953d239f24779388eb6e7c8ab4459d802f30dda62d2b2f3cf784b`  
		Last Modified: Thu, 13 Nov 2025 22:10:57 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5d6ca30e329165e96c56f1fd156f70c5c2577de35d688f876c97f635163a0785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:b9196e194acf30722e1a9dedf988332b2ebb2552efe7a36ff22cf302aff457e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174526254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0578d8bc4ef5c2cfdd7f48f0c7333cb0a0098cff3cc429ff29897f0186d79e0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:15:07 GMT
RUN cmd /S /C #(nop) COPY file:df006074126428890c75ce9f22baebfdec5a264a990fb6ef8bc8a4b313a3e0e2 in \ 
# Thu, 13 Nov 2025 20:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:15:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90be197a6e9f4e660c67d7abdfdc3ba4e85494254c85ee2c65d1d7d124c64e`  
		Last Modified: Thu, 13 Nov 2025 20:16:02 GMT  
		Size: 48.2 MB (48174025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907fdb6b48a6dbb9bab1403d6fccf06dc677b3b3bf0b8e8f38f14dbed63a73ae`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5bd4f08e951abc1038d0efdc2e7b742ddb0b8f372e30cc6725eabbe83d1e2c`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e577efa40922862889ab39b0ac9aef080548ff69bc03d42197b8c1d80f02ad`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:9c67fc3881910b007a12d907b8df88ae83f70c9587e232d5327473052c680ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:724408b3ccca658b88ac1461cc089a271002fb9e2c5131d3ff30312e89043bc0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818795877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1214d81eb3bbd278e5a08de4e240c31c61b750ac1b03562f8725f4448aab341`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:24:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:24:50 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:24:51 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:24:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:25b20ab24b3f2281ff269a84b2b6019053b1dadcb1229fc0dcc0ce962f0ad701`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2d0c7a5b72413426fcd192c7803ae2597b6d6e53797b4d647bf4b03adc456`  
		Last Modified: Thu, 13 Nov 2025 19:25:57 GMT  
		Size: 48.8 MB (48829162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d265d05fa488ae24de5bb4a67509b668a3c411fb2326470ca65ecb85b8cadfb`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9a4faafbd41fe83f32192c4866c1a3ddbcb5f0c83cced89ffba313cc4b727e`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ac1488c6eb1af5018f2b64e40a535357b72ecc8918336d498fdfcad8479e52`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.1`

```console
$ docker pull traefik@sha256:fd5932c796f7e2db9fd6bff485ef693d53797f0ee8ad03dc68aa424ea6f21958
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

### `traefik:v3.6.1` - linux; amd64

```console
$ docker pull traefik@sha256:2ba9a6e99daf342de4268279e3f90cdfc1f9d33349b04384be145247a1ef3871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51692967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2908c092e5b20b852f9891b365aa5ec46cf2691388fc2e0d33e9d9758bdf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:51 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc116d93e45b7dd6b0e202416a0f87f43cf074bcfbb3840135a3af3955ac5d25`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 456.9 KB (456917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a5be716dde6c158836ea784748160c7e3cce4d05b9e87cf4acf2347554549f`  
		Last Modified: Thu, 13 Nov 2025 19:14:27 GMT  
		Size: 47.4 MB (47433229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12cf03b5b74f31ef0947aa472eefd4fce22995a01973c8144abc637c1f2dfd5`  
		Last Modified: Thu, 13 Nov 2025 19:14:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:e1492e6f42f11978c617abd8b4a21fa865da7ccf11d4bc414b2f6f42eeb67f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7465e314b58062e784680b370d540481a673e78fcf4ca5a8aecccac959980f27`

```dockerfile
```

-	Layers:
	-	`sha256:6670fb0d409908f002c851c5511d0789b795e1816e3121ae259510739cd2254f`  
		Last Modified: Thu, 13 Nov 2025 22:10:33 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6397e1ae01371742c023d5b67c10c9bae0091c72d66b61bcef294dfb8b3952dc`  
		Last Modified: Thu, 13 Nov 2025 22:10:34 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a1d1ac9647edbc2ebf71f02fae36dfb0987f723cb75b2cc34af2662370f6456a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46916748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67b9222909a6f3f190f23a5b870f4a022ab35a0b91b895e52f4046d2a01e753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:29 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35422b2ee48bb1319ae170207ca3c49bb030ca3fc323663563166df6b2c284d`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478833cf572b525173b83aac05920d7faa1767c3ed6bbd77da3163b2cae6b4ae`  
		Last Modified: Thu, 13 Nov 2025 19:13:47 GMT  
		Size: 43.0 MB (42954559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f0e437df47d735153b26cdcc66b1480166934e38f869439d841027f4cc35`  
		Last Modified: Thu, 13 Nov 2025 19:13:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:fc0aee6221bc5414887c9dcadbfdd1ba7686dad6dd77cb727c90ed52c68b2d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2e97386835fa649ec5cd112c3daa4840f3aeefcd7869d3bc8e77781d546c4c`

```dockerfile
```

-	Layers:
	-	`sha256:9b41a77347fa9f26071f17808c1bcf672554222d5d3b4858f24c1c9f2a357b1a`  
		Last Modified: Thu, 13 Nov 2025 22:10:37 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:66932e80d0538da2b2bfe95902efb6fb24a4dc8d9023ce126c6c955f3f1b278a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47745361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e894f1bea0e7d825598088e385632ba9365e4b3ad19dc744ccc3fae07cfdb90f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:18 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:20 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:20 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3ddfe0bafb1dd910204e794eb628e45b2afe738326d376a5d70eb30f71700e`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 459.0 KB (459028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79149dff62553ad73224fdf1d11e93d2e70271346ce5a640d52318bb16187596`  
		Last Modified: Thu, 13 Nov 2025 19:13:55 GMT  
		Size: 43.1 MB (43147895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c562cf25ba9f3495b524dee77caa4d1a63314ea71d4196f860e1e26110938e50`  
		Last Modified: Thu, 13 Nov 2025 19:13:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:2b781dfc72ea4be899e6dcea154da96b7ab2a1113f2d5bba19505cd763ce6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9db86cb954917ea716d604cd9839ae3bb1a618c8eec0b46a3e5a57f08ff5a13`

```dockerfile
```

-	Layers:
	-	`sha256:f29ef1727b2134afdfaaf9fb8cb788b01c1f38c533e1cf4092ffa33cebe3b0b0`  
		Last Modified: Thu, 13 Nov 2025 22:10:41 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c90bf4d7b399b4f868701dd3105b7460edd45bf27da061130e0f78d2d043ae5`  
		Last Modified: Thu, 13 Nov 2025 22:10:42 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.1` - linux; ppc64le

```console
$ docker pull traefik@sha256:5516f662db0b5b3a08843cb2cf973c4a96acf8d450b700b90740eaa5b9e6c34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45322769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d853e9906b1afe1b346f887775f021ca14f984ddeceb11018c0dec475a9a781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:12:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:12:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:12:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:34 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:12:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:2a3cc0606b72cc9a105fb59921dc520b2e4355ee7288429aac12513223e0c311`  
		Last Modified: Thu, 13 Nov 2025 19:13:49 GMT  
		Size: 41.1 MB (41130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea2c564ccf61d08c50f750859aad773b368d89040a3ccd29460a760f570961d`  
		Last Modified: Thu, 13 Nov 2025 19:13:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:a0db86a66b16086329348f82dd6db984be72f8f63cd3ea987e00b854fe7856c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618c579126c296a23a35616d335fde341f56191af6cb1fbc29365bfd45c8b460`

```dockerfile
```

-	Layers:
	-	`sha256:ef79b9555be7f951cf5bb85482945d7e54b04d827c2bf096422b0894f1f64fbe`  
		Last Modified: Thu, 13 Nov 2025 22:10:46 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b03fdc549077b0aa8f4eaf5155939c7cd8e2aa7702f091044d88ea9cc03aab1`  
		Last Modified: Thu, 13 Nov 2025 22:10:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.1` - linux; riscv64

```console
$ docker pull traefik@sha256:0910886c34c7016f6bfa06f64d1a96afae257d413bb907f657dde7321ae18175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49697126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cce600707e0c46bf7c2b43bce29f05a80e06680700bbdd22644278dbae058b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:18:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:18:18 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:18:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:400bcb23c4605b2e8cc974b06cde9c1359c3968eb7ee5aa439bdbce64755104a`  
		Last Modified: Thu, 13 Nov 2025 19:24:31 GMT  
		Size: 45.7 MB (45724240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477939e0570f35a4b3c6751eab88b3262bb2f6ff48c0318d48bc0c5c45675e3`  
		Last Modified: Thu, 13 Nov 2025 19:24:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:23f5618d53a892148332d57d2ede8d2ee3a8732b7c2dc4b4b54fb816d1d02cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16fa0ba1cab63862239e6082e020a6d21cd4c1de30dc575124f8bdddd6888b3`

```dockerfile
```

-	Layers:
	-	`sha256:36e2999ec319d68f804befceb99d7113aa3974a80a46d0dfb07467cd67523ae9`  
		Last Modified: Thu, 13 Nov 2025 22:10:50 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88060a1568c1937b8510e18b59b41987917f281f321d7b1813972ddbe0a4b695`  
		Last Modified: Thu, 13 Nov 2025 22:10:51 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.1` - linux; s390x

```console
$ docker pull traefik@sha256:57684c57a1e49162f19d657da824d7ea22db26d21eec658cd0bbe68831fd751a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21675f9c8f81318c4c9156f56b9396310b1aefab6e32b8c0237f1d6f420c52d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 19:13:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
COPY entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 19:13:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Nov 2025 19:13:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 19:13:42 GMT
CMD ["traefik"]
# Thu, 13 Nov 2025 19:13:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbf1808932a530beec06dadcfb1194ff78bde6eafe68e2daa3c89a06ccbc96`  
		Last Modified: Thu, 13 Nov 2025 19:14:34 GMT  
		Size: 457.9 KB (457903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a010ab16ebfec2b479bc3e300311d009b17476cfe9f80b381b98b0889a839b`  
		Last Modified: Thu, 13 Nov 2025 19:14:42 GMT  
		Size: 45.6 MB (45580717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe2eb642ef817cbf966363ea05d39709a4cbc5d6d2cadb14cecf82956987fcf`  
		Last Modified: Thu, 13 Nov 2025 19:14:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.1` - unknown; unknown

```console
$ docker pull traefik@sha256:0f2b3c058a353077b5c72a214ba374ed6df3f7ca72b6d693bbcbb2ac22e6907c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d23d4f2dce825ea204e8e7e5e35683a8725152fb93217969af0631c12286063`

```dockerfile
```

-	Layers:
	-	`sha256:8d9063a18078a6f67adffb6db83e0f78ac4edb1938dff287a82188702bd1cbba`  
		Last Modified: Thu, 13 Nov 2025 22:10:56 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7579dd78d953d239f24779388eb6e7c8ab4459d802f30dda62d2b2f3cf784b`  
		Last Modified: Thu, 13 Nov 2025 22:10:57 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6.1-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5d6ca30e329165e96c56f1fd156f70c5c2577de35d688f876c97f635163a0785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6.1-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:b9196e194acf30722e1a9dedf988332b2ebb2552efe7a36ff22cf302aff457e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174526254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0578d8bc4ef5c2cfdd7f48f0c7333cb0a0098cff3cc429ff29897f0186d79e0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Thu, 13 Nov 2025 20:15:07 GMT
RUN cmd /S /C #(nop) COPY file:df006074126428890c75ce9f22baebfdec5a264a990fb6ef8bc8a4b313a3e0e2 in \ 
# Thu, 13 Nov 2025 20:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 13 Nov 2025 20:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 20:15:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90be197a6e9f4e660c67d7abdfdc3ba4e85494254c85ee2c65d1d7d124c64e`  
		Last Modified: Thu, 13 Nov 2025 20:16:02 GMT  
		Size: 48.2 MB (48174025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907fdb6b48a6dbb9bab1403d6fccf06dc677b3b3bf0b8e8f38f14dbed63a73ae`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5bd4f08e951abc1038d0efdc2e7b742ddb0b8f372e30cc6725eabbe83d1e2c`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e577efa40922862889ab39b0ac9aef080548ff69bc03d42197b8c1d80f02ad`  
		Last Modified: Thu, 13 Nov 2025 20:15:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.1-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:9c67fc3881910b007a12d907b8df88ae83f70c9587e232d5327473052c680ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:724408b3ccca658b88ac1461cc089a271002fb9e2c5131d3ff30312e89043bc0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818795877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1214d81eb3bbd278e5a08de4e240c31c61b750ac1b03562f8725f4448aab341`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:24:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:24:50 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:24:51 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:24:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:25b20ab24b3f2281ff269a84b2b6019053b1dadcb1229fc0dcc0ce962f0ad701`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2d0c7a5b72413426fcd192c7803ae2597b6d6e53797b4d647bf4b03adc456`  
		Last Modified: Thu, 13 Nov 2025 19:25:57 GMT  
		Size: 48.8 MB (48829162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d265d05fa488ae24de5bb4a67509b668a3c411fb2326470ca65ecb85b8cadfb`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9a4faafbd41fe83f32192c4866c1a3ddbcb5f0c83cced89ffba313cc4b727e`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ac1488c6eb1af5018f2b64e40a535357b72ecc8918336d498fdfcad8479e52`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:9c67fc3881910b007a12d907b8df88ae83f70c9587e232d5327473052c680ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:724408b3ccca658b88ac1461cc089a271002fb9e2c5131d3ff30312e89043bc0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818795877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1214d81eb3bbd278e5a08de4e240c31c61b750ac1b03562f8725f4448aab341`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:24:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.1/traefik_v3.6.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:24:50 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:24:51 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:24:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:25b20ab24b3f2281ff269a84b2b6019053b1dadcb1229fc0dcc0ce962f0ad701`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac2d0c7a5b72413426fcd192c7803ae2597b6d6e53797b4d647bf4b03adc456`  
		Last Modified: Thu, 13 Nov 2025 19:25:57 GMT  
		Size: 48.8 MB (48829162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d265d05fa488ae24de5bb4a67509b668a3c411fb2326470ca65ecb85b8cadfb`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9a4faafbd41fe83f32192c4866c1a3ddbcb5f0c83cced89ffba313cc4b727e`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ac1488c6eb1af5018f2b64e40a535357b72ecc8918336d498fdfcad8479e52`  
		Last Modified: Thu, 13 Nov 2025 19:25:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
