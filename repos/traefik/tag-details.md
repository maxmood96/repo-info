<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.33`](#traefik21133)
-	[`traefik:2.11.33-nanoserver-ltsc2022`](#traefik21133-nanoserver-ltsc2022)
-	[`traefik:2.11.33-windowsservercore-ltsc2022`](#traefik21133-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.5`](#traefik365)
-	[`traefik:3.6.5-nanoserver-ltsc2022`](#traefik365-nanoserver-ltsc2022)
-	[`traefik:3.6.5-windowsservercore-ltsc2022`](#traefik365-windowsservercore-ltsc2022)
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
-	[`traefik:v2.11.33`](#traefikv21133)
-	[`traefik:v2.11.33-nanoserver-ltsc2022`](#traefikv21133-nanoserver-ltsc2022)
-	[`traefik:v2.11.33-windowsservercore-ltsc2022`](#traefikv21133-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.5`](#traefikv365)
-	[`traefik:v3.6.5-nanoserver-ltsc2022`](#traefikv365-nanoserver-ltsc2022)
-	[`traefik:v3.6.5-windowsservercore-ltsc2022`](#traefikv365-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:b33557ba954d31336f3250919090ef124df0df3f8e7d17363fc251e568b77f9f
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
$ docker pull traefik@sha256:174f1a2c9487667e9cbd7f22236dda09fee74ffa9ccda6103164252ccef31dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc01ef432ddfb18e1ae4ccc7bf86c2c6e983b629812126cf00879938d5ef133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:30 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7373d7ff39c66d31e7e328d22241ad97173ac89003753dda524102cc53107802`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 460.9 KB (460949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aeb2a1ad90f6ffe5f5528580e42014da732e0c0d8312c158e086f70d64dfae`  
		Last Modified: Wed, 17 Dec 2025 18:42:14 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e111053df7c8cadd8dfaeb8490d04dfc93f9d07ed5652b6d640ef7a4c58fc3d8`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:c43ba2a7b61dfd2a423b7bc481f9845385f44395167e8352d996e94008d8ce6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c31e578e41f7186282529a4aad4f109a4f551710f1319062ca985a6da05c1`

```dockerfile
```

-	Layers:
	-	`sha256:2116d94ea9bacc40e0ade3117fa96ddf15e63fa36da8089c273c7e19c571a691`  
		Last Modified: Wed, 17 Dec 2025 19:09:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616c0b95ca69d28108937c887312561431c91b944f1ea54a1b821593e630d3d8`  
		Last Modified: Wed, 17 Dec 2025 19:09:30 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:92441aad8fdae59c61052bfa9a38b055e5e0b43008760f39bf9e3ea3d1216a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd42a450c3eb021d903de7b72452138cb66eb624c3dcaee29499c6fa5632e80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d6b4fdc1185815334dc04ce5cc1add06158e45c57ee901bce7ac29c718bff`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 461.5 KB (461458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd52af12c0cf52ba92b89743e3cfbafd1ffde7319bb061e614aced61f76e2b5`  
		Last Modified: Wed, 17 Dec 2025 18:41:49 GMT  
		Size: 42.8 MB (42793192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacdf7ee72f87469cb1cb594d1db6e02ad7b957c4dc8b7f056628b13ffb30139`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:179008a6edecd9f0bf04d1569f2c94987ee782c4afefb7801105652fb6c74628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58f432c0aa626bd6c3bdeb59724617cd8e3d8f9f4996bf9e16578d562f85dbb`

```dockerfile
```

-	Layers:
	-	`sha256:af59878afd8906fc5a2f9e36d5a677d20b9c81a5c32820fd4d9b41c34e580ef9`  
		Last Modified: Wed, 17 Dec 2025 19:10:23 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:897a5aa39c473ea62abf1f910044f5eeaefad47e12869f4112eea4660f362798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47293996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3057d7d3ee9aa83dad87f39d63216072423a688a68904564f774e54e3f222f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:42 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e904d2dc9111f62005b5dee00d41be23f0e8a19c4a23e54bfdb850682016936`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 463.0 KB (462978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b65b72401107ae382d9d6ab97ba706452bd292a3def06379a6d660470aabc8`  
		Last Modified: Wed, 17 Dec 2025 18:42:36 GMT  
		Size: 42.6 MB (42635448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfad583f79b6f025efef8774b3387f883401b93e51814eee60232141be6ebc2`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:cebe3d5c0ee5748098ae3bf7fbd1a8cbe9f0e7233bd3b5b68e0b09556319d495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987ca039b19e65a128578209c8e90778569093e1e1381decda320a874936e84a`

```dockerfile
```

-	Layers:
	-	`sha256:8f0075057da843c163b2f08e96d4f28d56500fd40eadfe5c26c3a3c5a98f77a3`  
		Last Modified: Wed, 17 Dec 2025 19:10:13 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ddc52028080001ed81b15d3ffdaba3aec997ef0fa669c7f80db66c448d4a88`  
		Last Modified: Wed, 17 Dec 2025 19:10:14 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:cecb7fad0442537204b5a852b39b02a8cfd85dbc9b362cb9cf9c15eeada73be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45245867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86dd3fd2ce35f83b500540009c71516d3e645f6d2f95c114c92bbc6606712f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:40:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:40:43 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:40:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09f86acc20c95b057694bed643875f0fa537cc6c0ba74652b355ad1b13c676`  
		Last Modified: Wed, 17 Dec 2025 18:42:00 GMT  
		Size: 41.0 MB (40954988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808d07d15fd68e5b11573c4e23dcc3fcf45e874102593287eb2e4d88eb5b6ea4`  
		Last Modified: Wed, 17 Dec 2025 18:41:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:10a02d8db0ae1a0efe8d4fe8ebd21133236322a14d263b0e174be1ccbb6b0057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831af4e9709665d4bdce755617fdea77d83235af766377e5885e5294132b04b2`

```dockerfile
```

-	Layers:
	-	`sha256:05f05dd8d7581f226db59ca208c11ca7d2e0c562f8ea4a2b081988a23dc51cae`  
		Last Modified: Wed, 17 Dec 2025 19:09:51 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d892a603513bfc38f1406b7b741a8acf028c5c350784d2d9fbc304b6f460c6`  
		Last Modified: Wed, 17 Dec 2025 19:09:52 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:66453f892822049494eb3c8d4e32f4c6ae5b3fe1a1490faa7ee3f503166170b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034e55d3eb9fd4fc2a6b5641b60d1ad6d02bad4083173401d0141c19b2722d1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:21 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409c0c18fc01012d825955c45a3a5ceee29dee3b8b54fd022ea3ca54b9b3d43`  
		Last Modified: Wed, 17 Dec 2025 18:46:53 GMT  
		Size: 45.3 MB (45324006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:1a66487a7b7719f85e925c7240ca641986f6a1fb0cd09f7382947a174310266e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de290e004466b29a7d0b2bc1ba76d9efcd3023b92c98049f8c1c0ffee7decd44`

```dockerfile
```

-	Layers:
	-	`sha256:9898591f677ff88b24f40976126580788387e360775ce6df02ad2d7c5dece53f`  
		Last Modified: Wed, 17 Dec 2025 19:09:56 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bdef50f6d22cc758b74d773276e97c56fe87f1396f5bfe19523ebb28b8e0ec`  
		Last Modified: Wed, 17 Dec 2025 19:09:57 GMT  
		Size: 12.6 KB (12557 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:788fd58abaaed61e2a36b88c929635c1c6566fe7b439f3eb5a8da1fee71282f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2b7ce4095e57c30dbe3f418349fe0086fb6815c343e8ca4bef82aae35a2248`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:02 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916fa41a772c8e72261f201209754a22b4cf24230aab2c0ad48d8d6849c20cdf`  
		Last Modified: Wed, 17 Dec 2025 18:42:09 GMT  
		Size: 45.3 MB (45254479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7f095d3b68b3257e638e5eb536d404c9dfc4dd1bb5546cba15a608a8fefd5`  
		Last Modified: Wed, 17 Dec 2025 18:42:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:95146c996e59baad3fbc78a82f7a8b2bd88d0d7a08d3355388cebb9fe547e21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93a5f35eecd903207574d988e9525c8bbb059af2fa6d25ccebbfdef1cc0ffb`

```dockerfile
```

-	Layers:
	-	`sha256:88bd86b5901a9b0c186d4cd648c8601559b401d3c4fd407ff806e137b3165394`  
		Last Modified: Wed, 17 Dec 2025 19:10:33 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0338d130ec8acfd06d982e64932bf0c73936bf53d285d57bb1f9fce908043b`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:b33557ba954d31336f3250919090ef124df0df3f8e7d17363fc251e568b77f9f
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
$ docker pull traefik@sha256:174f1a2c9487667e9cbd7f22236dda09fee74ffa9ccda6103164252ccef31dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc01ef432ddfb18e1ae4ccc7bf86c2c6e983b629812126cf00879938d5ef133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:30 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7373d7ff39c66d31e7e328d22241ad97173ac89003753dda524102cc53107802`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 460.9 KB (460949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aeb2a1ad90f6ffe5f5528580e42014da732e0c0d8312c158e086f70d64dfae`  
		Last Modified: Wed, 17 Dec 2025 18:42:14 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e111053df7c8cadd8dfaeb8490d04dfc93f9d07ed5652b6d640ef7a4c58fc3d8`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c43ba2a7b61dfd2a423b7bc481f9845385f44395167e8352d996e94008d8ce6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c31e578e41f7186282529a4aad4f109a4f551710f1319062ca985a6da05c1`

```dockerfile
```

-	Layers:
	-	`sha256:2116d94ea9bacc40e0ade3117fa96ddf15e63fa36da8089c273c7e19c571a691`  
		Last Modified: Wed, 17 Dec 2025 19:09:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616c0b95ca69d28108937c887312561431c91b944f1ea54a1b821593e630d3d8`  
		Last Modified: Wed, 17 Dec 2025 19:09:30 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:92441aad8fdae59c61052bfa9a38b055e5e0b43008760f39bf9e3ea3d1216a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd42a450c3eb021d903de7b72452138cb66eb624c3dcaee29499c6fa5632e80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d6b4fdc1185815334dc04ce5cc1add06158e45c57ee901bce7ac29c718bff`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 461.5 KB (461458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd52af12c0cf52ba92b89743e3cfbafd1ffde7319bb061e614aced61f76e2b5`  
		Last Modified: Wed, 17 Dec 2025 18:41:49 GMT  
		Size: 42.8 MB (42793192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacdf7ee72f87469cb1cb594d1db6e02ad7b957c4dc8b7f056628b13ffb30139`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:179008a6edecd9f0bf04d1569f2c94987ee782c4afefb7801105652fb6c74628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58f432c0aa626bd6c3bdeb59724617cd8e3d8f9f4996bf9e16578d562f85dbb`

```dockerfile
```

-	Layers:
	-	`sha256:af59878afd8906fc5a2f9e36d5a677d20b9c81a5c32820fd4d9b41c34e580ef9`  
		Last Modified: Wed, 17 Dec 2025 19:10:23 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:897a5aa39c473ea62abf1f910044f5eeaefad47e12869f4112eea4660f362798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47293996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3057d7d3ee9aa83dad87f39d63216072423a688a68904564f774e54e3f222f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:42 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e904d2dc9111f62005b5dee00d41be23f0e8a19c4a23e54bfdb850682016936`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 463.0 KB (462978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b65b72401107ae382d9d6ab97ba706452bd292a3def06379a6d660470aabc8`  
		Last Modified: Wed, 17 Dec 2025 18:42:36 GMT  
		Size: 42.6 MB (42635448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfad583f79b6f025efef8774b3387f883401b93e51814eee60232141be6ebc2`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:cebe3d5c0ee5748098ae3bf7fbd1a8cbe9f0e7233bd3b5b68e0b09556319d495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987ca039b19e65a128578209c8e90778569093e1e1381decda320a874936e84a`

```dockerfile
```

-	Layers:
	-	`sha256:8f0075057da843c163b2f08e96d4f28d56500fd40eadfe5c26c3a3c5a98f77a3`  
		Last Modified: Wed, 17 Dec 2025 19:10:13 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ddc52028080001ed81b15d3ffdaba3aec997ef0fa669c7f80db66c448d4a88`  
		Last Modified: Wed, 17 Dec 2025 19:10:14 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:cecb7fad0442537204b5a852b39b02a8cfd85dbc9b362cb9cf9c15eeada73be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45245867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86dd3fd2ce35f83b500540009c71516d3e645f6d2f95c114c92bbc6606712f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:40:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:40:43 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:40:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09f86acc20c95b057694bed643875f0fa537cc6c0ba74652b355ad1b13c676`  
		Last Modified: Wed, 17 Dec 2025 18:42:00 GMT  
		Size: 41.0 MB (40954988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808d07d15fd68e5b11573c4e23dcc3fcf45e874102593287eb2e4d88eb5b6ea4`  
		Last Modified: Wed, 17 Dec 2025 18:41:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:10a02d8db0ae1a0efe8d4fe8ebd21133236322a14d263b0e174be1ccbb6b0057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831af4e9709665d4bdce755617fdea77d83235af766377e5885e5294132b04b2`

```dockerfile
```

-	Layers:
	-	`sha256:05f05dd8d7581f226db59ca208c11ca7d2e0c562f8ea4a2b081988a23dc51cae`  
		Last Modified: Wed, 17 Dec 2025 19:09:51 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d892a603513bfc38f1406b7b741a8acf028c5c350784d2d9fbc304b6f460c6`  
		Last Modified: Wed, 17 Dec 2025 19:09:52 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:66453f892822049494eb3c8d4e32f4c6ae5b3fe1a1490faa7ee3f503166170b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034e55d3eb9fd4fc2a6b5641b60d1ad6d02bad4083173401d0141c19b2722d1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:21 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409c0c18fc01012d825955c45a3a5ceee29dee3b8b54fd022ea3ca54b9b3d43`  
		Last Modified: Wed, 17 Dec 2025 18:46:53 GMT  
		Size: 45.3 MB (45324006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:1a66487a7b7719f85e925c7240ca641986f6a1fb0cd09f7382947a174310266e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de290e004466b29a7d0b2bc1ba76d9efcd3023b92c98049f8c1c0ffee7decd44`

```dockerfile
```

-	Layers:
	-	`sha256:9898591f677ff88b24f40976126580788387e360775ce6df02ad2d7c5dece53f`  
		Last Modified: Wed, 17 Dec 2025 19:09:56 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bdef50f6d22cc758b74d773276e97c56fe87f1396f5bfe19523ebb28b8e0ec`  
		Last Modified: Wed, 17 Dec 2025 19:09:57 GMT  
		Size: 12.6 KB (12557 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:788fd58abaaed61e2a36b88c929635c1c6566fe7b439f3eb5a8da1fee71282f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2b7ce4095e57c30dbe3f418349fe0086fb6815c343e8ca4bef82aae35a2248`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:02 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916fa41a772c8e72261f201209754a22b4cf24230aab2c0ad48d8d6849c20cdf`  
		Last Modified: Wed, 17 Dec 2025 18:42:09 GMT  
		Size: 45.3 MB (45254479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7f095d3b68b3257e638e5eb536d404c9dfc4dd1bb5546cba15a608a8fefd5`  
		Last Modified: Wed, 17 Dec 2025 18:42:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:95146c996e59baad3fbc78a82f7a8b2bd88d0d7a08d3355388cebb9fe547e21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93a5f35eecd903207574d988e9525c8bbb059af2fa6d25ccebbfdef1cc0ffb`

```dockerfile
```

-	Layers:
	-	`sha256:88bd86b5901a9b0c186d4cd648c8601559b401d3c4fd407ff806e137b3165394`  
		Last Modified: Wed, 17 Dec 2025 19:10:33 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0338d130ec8acfd06d982e64932bf0c73936bf53d285d57bb1f9fce908043b`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.33`

```console
$ docker pull traefik@sha256:b33557ba954d31336f3250919090ef124df0df3f8e7d17363fc251e568b77f9f
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

### `traefik:2.11.33` - linux; amd64

```console
$ docker pull traefik@sha256:174f1a2c9487667e9cbd7f22236dda09fee74ffa9ccda6103164252ccef31dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc01ef432ddfb18e1ae4ccc7bf86c2c6e983b629812126cf00879938d5ef133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:30 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7373d7ff39c66d31e7e328d22241ad97173ac89003753dda524102cc53107802`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 460.9 KB (460949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aeb2a1ad90f6ffe5f5528580e42014da732e0c0d8312c158e086f70d64dfae`  
		Last Modified: Wed, 17 Dec 2025 18:42:14 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e111053df7c8cadd8dfaeb8490d04dfc93f9d07ed5652b6d640ef7a4c58fc3d8`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:c43ba2a7b61dfd2a423b7bc481f9845385f44395167e8352d996e94008d8ce6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c31e578e41f7186282529a4aad4f109a4f551710f1319062ca985a6da05c1`

```dockerfile
```

-	Layers:
	-	`sha256:2116d94ea9bacc40e0ade3117fa96ddf15e63fa36da8089c273c7e19c571a691`  
		Last Modified: Wed, 17 Dec 2025 19:09:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616c0b95ca69d28108937c887312561431c91b944f1ea54a1b821593e630d3d8`  
		Last Modified: Wed, 17 Dec 2025 19:09:30 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.33` - linux; arm variant v6

```console
$ docker pull traefik@sha256:92441aad8fdae59c61052bfa9a38b055e5e0b43008760f39bf9e3ea3d1216a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd42a450c3eb021d903de7b72452138cb66eb624c3dcaee29499c6fa5632e80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d6b4fdc1185815334dc04ce5cc1add06158e45c57ee901bce7ac29c718bff`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 461.5 KB (461458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd52af12c0cf52ba92b89743e3cfbafd1ffde7319bb061e614aced61f76e2b5`  
		Last Modified: Wed, 17 Dec 2025 18:41:49 GMT  
		Size: 42.8 MB (42793192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacdf7ee72f87469cb1cb594d1db6e02ad7b957c4dc8b7f056628b13ffb30139`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:179008a6edecd9f0bf04d1569f2c94987ee782c4afefb7801105652fb6c74628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58f432c0aa626bd6c3bdeb59724617cd8e3d8f9f4996bf9e16578d562f85dbb`

```dockerfile
```

-	Layers:
	-	`sha256:af59878afd8906fc5a2f9e36d5a677d20b9c81a5c32820fd4d9b41c34e580ef9`  
		Last Modified: Wed, 17 Dec 2025 19:10:23 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.33` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:897a5aa39c473ea62abf1f910044f5eeaefad47e12869f4112eea4660f362798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47293996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3057d7d3ee9aa83dad87f39d63216072423a688a68904564f774e54e3f222f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:42 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e904d2dc9111f62005b5dee00d41be23f0e8a19c4a23e54bfdb850682016936`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 463.0 KB (462978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b65b72401107ae382d9d6ab97ba706452bd292a3def06379a6d660470aabc8`  
		Last Modified: Wed, 17 Dec 2025 18:42:36 GMT  
		Size: 42.6 MB (42635448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfad583f79b6f025efef8774b3387f883401b93e51814eee60232141be6ebc2`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:cebe3d5c0ee5748098ae3bf7fbd1a8cbe9f0e7233bd3b5b68e0b09556319d495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987ca039b19e65a128578209c8e90778569093e1e1381decda320a874936e84a`

```dockerfile
```

-	Layers:
	-	`sha256:8f0075057da843c163b2f08e96d4f28d56500fd40eadfe5c26c3a3c5a98f77a3`  
		Last Modified: Wed, 17 Dec 2025 19:10:13 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ddc52028080001ed81b15d3ffdaba3aec997ef0fa669c7f80db66c448d4a88`  
		Last Modified: Wed, 17 Dec 2025 19:10:14 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.33` - linux; ppc64le

```console
$ docker pull traefik@sha256:cecb7fad0442537204b5a852b39b02a8cfd85dbc9b362cb9cf9c15eeada73be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45245867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86dd3fd2ce35f83b500540009c71516d3e645f6d2f95c114c92bbc6606712f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:40:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:40:43 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:40:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09f86acc20c95b057694bed643875f0fa537cc6c0ba74652b355ad1b13c676`  
		Last Modified: Wed, 17 Dec 2025 18:42:00 GMT  
		Size: 41.0 MB (40954988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808d07d15fd68e5b11573c4e23dcc3fcf45e874102593287eb2e4d88eb5b6ea4`  
		Last Modified: Wed, 17 Dec 2025 18:41:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:10a02d8db0ae1a0efe8d4fe8ebd21133236322a14d263b0e174be1ccbb6b0057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831af4e9709665d4bdce755617fdea77d83235af766377e5885e5294132b04b2`

```dockerfile
```

-	Layers:
	-	`sha256:05f05dd8d7581f226db59ca208c11ca7d2e0c562f8ea4a2b081988a23dc51cae`  
		Last Modified: Wed, 17 Dec 2025 19:09:51 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d892a603513bfc38f1406b7b741a8acf028c5c350784d2d9fbc304b6f460c6`  
		Last Modified: Wed, 17 Dec 2025 19:09:52 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.33` - linux; riscv64

```console
$ docker pull traefik@sha256:66453f892822049494eb3c8d4e32f4c6ae5b3fe1a1490faa7ee3f503166170b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034e55d3eb9fd4fc2a6b5641b60d1ad6d02bad4083173401d0141c19b2722d1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:21 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409c0c18fc01012d825955c45a3a5ceee29dee3b8b54fd022ea3ca54b9b3d43`  
		Last Modified: Wed, 17 Dec 2025 18:46:53 GMT  
		Size: 45.3 MB (45324006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:1a66487a7b7719f85e925c7240ca641986f6a1fb0cd09f7382947a174310266e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de290e004466b29a7d0b2bc1ba76d9efcd3023b92c98049f8c1c0ffee7decd44`

```dockerfile
```

-	Layers:
	-	`sha256:9898591f677ff88b24f40976126580788387e360775ce6df02ad2d7c5dece53f`  
		Last Modified: Wed, 17 Dec 2025 19:09:56 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bdef50f6d22cc758b74d773276e97c56fe87f1396f5bfe19523ebb28b8e0ec`  
		Last Modified: Wed, 17 Dec 2025 19:09:57 GMT  
		Size: 12.6 KB (12557 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.33` - linux; s390x

```console
$ docker pull traefik@sha256:788fd58abaaed61e2a36b88c929635c1c6566fe7b439f3eb5a8da1fee71282f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2b7ce4095e57c30dbe3f418349fe0086fb6815c343e8ca4bef82aae35a2248`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:02 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916fa41a772c8e72261f201209754a22b4cf24230aab2c0ad48d8d6849c20cdf`  
		Last Modified: Wed, 17 Dec 2025 18:42:09 GMT  
		Size: 45.3 MB (45254479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7f095d3b68b3257e638e5eb536d404c9dfc4dd1bb5546cba15a608a8fefd5`  
		Last Modified: Wed, 17 Dec 2025 18:42:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:95146c996e59baad3fbc78a82f7a8b2bd88d0d7a08d3355388cebb9fe547e21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93a5f35eecd903207574d988e9525c8bbb059af2fa6d25ccebbfdef1cc0ffb`

```dockerfile
```

-	Layers:
	-	`sha256:88bd86b5901a9b0c186d4cd648c8601559b401d3c4fd407ff806e137b3165394`  
		Last Modified: Wed, 17 Dec 2025 19:10:33 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0338d130ec8acfd06d982e64932bf0c73936bf53d285d57bb1f9fce908043b`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.33-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11.33-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.33-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11.33-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:2979bff651c98e70345dd886186a7a15ee3ce18b636af208d4ccbf2d56dbdddd
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
$ docker pull traefik@sha256:a6e6ffb23b620d5f8c7019a50c46875adc672389262758d239ed4fd602a1f86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebe7d161d0ca503ad8ebff362c34495b143e950a43016bbeefb68ceeade7ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:43 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c123c4b79203ea3d8aeadc78f39dcf4880551dbbce0f8c9265118147744290`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 460.9 KB (460941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae3961098f3b7eb90636311c62458e9d162d07d0c97984a4b8b9b2822b1e51c`  
		Last Modified: Tue, 16 Dec 2025 21:54:37 GMT  
		Size: 47.5 MB (47508411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6566b26c730bcb23fa154e162a73cd9362242dff8ab5551c3dcc7013ea377a2`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:59679a79dfb910f3d0ca1eed402b2516e2cd3de1fff2eb71b541a9848bf92696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a47fae0c266934036c870c1b0a29f10280547bb5920be2bcf68db607c5eab5`

```dockerfile
```

-	Layers:
	-	`sha256:252a04653ea612c30195020406ee86a653199e286a9d9dba847d5d5c1d61a0a8`  
		Last Modified: Tue, 16 Dec 2025 22:10:19 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888a3101a685aed38696caf472987774b89d4dd16cfcadb8e51aaf71ce405acc`  
		Last Modified: Tue, 16 Dec 2025 22:10:20 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:b2675b52948b6c87913d2cec95c10274afa28211ebef9a6c4895ee9a25f95287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47124574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa3558b9f3cf74070782f7ff953938a92a26c3be26529a9d183470df21ef3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:40 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d02c5a62d4136e3d9a27874e3f90d268a1e2bd21b5d014e8f6efa096ac62f5b`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dc4feddb18b5bb5fd6db4e1e934f32ed25a0cfd8f55eb790dedb4b2af53195`  
		Last Modified: Tue, 16 Dec 2025 21:55:02 GMT  
		Size: 43.1 MB (43094851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e5e96f6a45288ea41808ef79469b328b5d40aad67cb25840a96bd395f513e`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:86db7813d8e8062a04e0fae95fdd1ee2e894f27121a08be871062c2390a19469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bf7b6e0dd92b132c7c91beba5500bf6992408142614fedd73e33f222b00c7f`

```dockerfile
```

-	Layers:
	-	`sha256:d8b3daf4d00d15dcb2f24da0bf9762294c6695421572ef747fc9997ad708e727`  
		Last Modified: Tue, 16 Dec 2025 22:09:41 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6cbc266ff2aaaebc1d6f466eb6b2ed19aabb948ed34509a70aa2b3de9d8642d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4283f5af9f565dd6e90ec8f89b5ccb1dc6a7948e5a8ad04821c6f3aa1ee16101`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:47 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566766f1cca2628996b2c76f70f9307c33565b0771e3986efe943c6caece91b3`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 463.0 KB (462956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8988b5fa3857eee98f77c575d62ffbd99dd6bc84d22e78f092d7b1fcde42ea38`  
		Last Modified: Tue, 16 Dec 2025 21:54:34 GMT  
		Size: 43.2 MB (43235887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4cdd0a069b276d39beffe344ab2bf995b83295c1244374d4e53d40bcd704ef`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:d73b94160a95ad415b4bf47d621eb3675f1f2bc87eb920184e034473298c80b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3960dad2ec0b64a3e7a952fcf3d253bf2852fd358d9308bd56d302b7c29528`

```dockerfile
```

-	Layers:
	-	`sha256:5c321edc2a81a2b4ed1eb48497cff6f1c233b04dedf9609b7a168747c1c2af6b`  
		Last Modified: Tue, 16 Dec 2025 22:09:44 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6333a5f55afb6f36c7506e8de0334052764cca5a7b9edcdb5ab07c6d9d19fe9`  
		Last Modified: Tue, 16 Dec 2025 22:09:45 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:980934ddda50fdf87c97a0122b6b28c0d6c36c4586d3556acc3c4a908d1b6633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3fddc5c561077ded3f490c7c200156c27f4c1108ba69e4a7f751fb91825c0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:20 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f441f4d99a26e179d2526a42bd1c9175f545e1ca3a33506d0b8ab30a9f0881b`  
		Last Modified: Tue, 16 Dec 2025 21:57:38 GMT  
		Size: 41.3 MB (41258568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82fc7573a1347d7a1eb3426038d4dcde7881ae070f85d4ab234dacb3071486`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:b11123b48f2acf071838ad624aa6d0caa56b93881696a7619e80ee518f5c21c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b894a327d59478ddf84e916ff7554fbf7afdd9e81cc9ef6ed629cef57fb159`

```dockerfile
```

-	Layers:
	-	`sha256:0a11c3bd010dd789e90eac3656a409676311194977d78fc371cbb39684d28106`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d1a0c5edd23a7fd793a6418a6d658b1fb7ea379487c7a75627e6e3d16329c7`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:6897a7373e41d2ba27f918cc77f0972388239b2efbc2d7cf10cf931f5e1aa24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d76a1013a54de99b0a6821e2307209961bb10ab500b24620e6894b42659fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:59 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfc3a02968c43f57b5da703c6894a5a55b6c98d5bc1492e74821a9093241d2`  
		Last Modified: Tue, 16 Dec 2025 22:02:30 GMT  
		Size: 45.8 MB (45795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:c1d691e3b689732157509f1e2c8eaf47253beb2aa45bcb5c932fdd83e1ac2503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f4e2dffe5bcfb172995e23308a0fcf0c8db556fb0f8d4503d2e14b2d2447b`

```dockerfile
```

-	Layers:
	-	`sha256:e53f0a3aa459b728963b618c65bc1d895aec698979e52617f4c2e9315d4f0530`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a279bfeb8713cb9d08bb3bf4232d9b69754e2495fa6ad7942e151a570de0dda9`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:b2f780a63f69029bf3b14e4051401ae9a98664b55bedb527931d7fafcea326c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49844511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf3004c5d3013f840161103038ab6ee14b0b084427e63bbfbd9eb14537d51bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:33 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2fbf42c48fff38dea98dc46f2c9bb22a8f4a630e67201e376421193c12f9e5`  
		Last Modified: Tue, 16 Dec 2025 21:55:49 GMT  
		Size: 45.7 MB (45658595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01674c2b8a9c731b10dae5670fc27a9a56409aab9564a25318e2995fd83af5b5`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:fd6432a961346ffdaa69077bccf74461ab8a255f76fb246fb76bab6e95b6d572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01564b41d37955505edeb640e08f411681e8d84a25369ca8b1f6ac4d115440c2`

```dockerfile
```

-	Layers:
	-	`sha256:2769263b7d8448b1201ab044140a4890824b1f952022c55611b782fa4314c92d`  
		Last Modified: Tue, 16 Dec 2025 22:09:54 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f67737957a7c8409ffb2b142341664e9e08c910d8ad74b501da46e6d0a3af4`  
		Last Modified: Tue, 16 Dec 2025 22:09:55 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:2979bff651c98e70345dd886186a7a15ee3ce18b636af208d4ccbf2d56dbdddd
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
$ docker pull traefik@sha256:a6e6ffb23b620d5f8c7019a50c46875adc672389262758d239ed4fd602a1f86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebe7d161d0ca503ad8ebff362c34495b143e950a43016bbeefb68ceeade7ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:43 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c123c4b79203ea3d8aeadc78f39dcf4880551dbbce0f8c9265118147744290`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 460.9 KB (460941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae3961098f3b7eb90636311c62458e9d162d07d0c97984a4b8b9b2822b1e51c`  
		Last Modified: Tue, 16 Dec 2025 21:54:37 GMT  
		Size: 47.5 MB (47508411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6566b26c730bcb23fa154e162a73cd9362242dff8ab5551c3dcc7013ea377a2`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:59679a79dfb910f3d0ca1eed402b2516e2cd3de1fff2eb71b541a9848bf92696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a47fae0c266934036c870c1b0a29f10280547bb5920be2bcf68db607c5eab5`

```dockerfile
```

-	Layers:
	-	`sha256:252a04653ea612c30195020406ee86a653199e286a9d9dba847d5d5c1d61a0a8`  
		Last Modified: Tue, 16 Dec 2025 22:10:19 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888a3101a685aed38696caf472987774b89d4dd16cfcadb8e51aaf71ce405acc`  
		Last Modified: Tue, 16 Dec 2025 22:10:20 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:b2675b52948b6c87913d2cec95c10274afa28211ebef9a6c4895ee9a25f95287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47124574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa3558b9f3cf74070782f7ff953938a92a26c3be26529a9d183470df21ef3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:40 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d02c5a62d4136e3d9a27874e3f90d268a1e2bd21b5d014e8f6efa096ac62f5b`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dc4feddb18b5bb5fd6db4e1e934f32ed25a0cfd8f55eb790dedb4b2af53195`  
		Last Modified: Tue, 16 Dec 2025 21:55:02 GMT  
		Size: 43.1 MB (43094851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e5e96f6a45288ea41808ef79469b328b5d40aad67cb25840a96bd395f513e`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:86db7813d8e8062a04e0fae95fdd1ee2e894f27121a08be871062c2390a19469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bf7b6e0dd92b132c7c91beba5500bf6992408142614fedd73e33f222b00c7f`

```dockerfile
```

-	Layers:
	-	`sha256:d8b3daf4d00d15dcb2f24da0bf9762294c6695421572ef747fc9997ad708e727`  
		Last Modified: Tue, 16 Dec 2025 22:09:41 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6cbc266ff2aaaebc1d6f466eb6b2ed19aabb948ed34509a70aa2b3de9d8642d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4283f5af9f565dd6e90ec8f89b5ccb1dc6a7948e5a8ad04821c6f3aa1ee16101`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:47 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566766f1cca2628996b2c76f70f9307c33565b0771e3986efe943c6caece91b3`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 463.0 KB (462956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8988b5fa3857eee98f77c575d62ffbd99dd6bc84d22e78f092d7b1fcde42ea38`  
		Last Modified: Tue, 16 Dec 2025 21:54:34 GMT  
		Size: 43.2 MB (43235887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4cdd0a069b276d39beffe344ab2bf995b83295c1244374d4e53d40bcd704ef`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:d73b94160a95ad415b4bf47d621eb3675f1f2bc87eb920184e034473298c80b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3960dad2ec0b64a3e7a952fcf3d253bf2852fd358d9308bd56d302b7c29528`

```dockerfile
```

-	Layers:
	-	`sha256:5c321edc2a81a2b4ed1eb48497cff6f1c233b04dedf9609b7a168747c1c2af6b`  
		Last Modified: Tue, 16 Dec 2025 22:09:44 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6333a5f55afb6f36c7506e8de0334052764cca5a7b9edcdb5ab07c6d9d19fe9`  
		Last Modified: Tue, 16 Dec 2025 22:09:45 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:980934ddda50fdf87c97a0122b6b28c0d6c36c4586d3556acc3c4a908d1b6633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3fddc5c561077ded3f490c7c200156c27f4c1108ba69e4a7f751fb91825c0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:20 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f441f4d99a26e179d2526a42bd1c9175f545e1ca3a33506d0b8ab30a9f0881b`  
		Last Modified: Tue, 16 Dec 2025 21:57:38 GMT  
		Size: 41.3 MB (41258568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82fc7573a1347d7a1eb3426038d4dcde7881ae070f85d4ab234dacb3071486`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:b11123b48f2acf071838ad624aa6d0caa56b93881696a7619e80ee518f5c21c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b894a327d59478ddf84e916ff7554fbf7afdd9e81cc9ef6ed629cef57fb159`

```dockerfile
```

-	Layers:
	-	`sha256:0a11c3bd010dd789e90eac3656a409676311194977d78fc371cbb39684d28106`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d1a0c5edd23a7fd793a6418a6d658b1fb7ea379487c7a75627e6e3d16329c7`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:6897a7373e41d2ba27f918cc77f0972388239b2efbc2d7cf10cf931f5e1aa24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d76a1013a54de99b0a6821e2307209961bb10ab500b24620e6894b42659fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:59 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfc3a02968c43f57b5da703c6894a5a55b6c98d5bc1492e74821a9093241d2`  
		Last Modified: Tue, 16 Dec 2025 22:02:30 GMT  
		Size: 45.8 MB (45795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:c1d691e3b689732157509f1e2c8eaf47253beb2aa45bcb5c932fdd83e1ac2503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f4e2dffe5bcfb172995e23308a0fcf0c8db556fb0f8d4503d2e14b2d2447b`

```dockerfile
```

-	Layers:
	-	`sha256:e53f0a3aa459b728963b618c65bc1d895aec698979e52617f4c2e9315d4f0530`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a279bfeb8713cb9d08bb3bf4232d9b69754e2495fa6ad7942e151a570de0dda9`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:b2f780a63f69029bf3b14e4051401ae9a98664b55bedb527931d7fafcea326c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49844511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf3004c5d3013f840161103038ab6ee14b0b084427e63bbfbd9eb14537d51bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:33 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2fbf42c48fff38dea98dc46f2c9bb22a8f4a630e67201e376421193c12f9e5`  
		Last Modified: Tue, 16 Dec 2025 21:55:49 GMT  
		Size: 45.7 MB (45658595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01674c2b8a9c731b10dae5670fc27a9a56409aab9564a25318e2995fd83af5b5`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:fd6432a961346ffdaa69077bccf74461ab8a255f76fb246fb76bab6e95b6d572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01564b41d37955505edeb640e08f411681e8d84a25369ca8b1f6ac4d115440c2`

```dockerfile
```

-	Layers:
	-	`sha256:2769263b7d8448b1201ab044140a4890824b1f952022c55611b782fa4314c92d`  
		Last Modified: Tue, 16 Dec 2025 22:09:54 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f67737957a7c8409ffb2b142341664e9e08c910d8ad74b501da46e6d0a3af4`  
		Last Modified: Tue, 16 Dec 2025 22:09:55 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.5`

```console
$ docker pull traefik@sha256:2979bff651c98e70345dd886186a7a15ee3ce18b636af208d4ccbf2d56dbdddd
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

### `traefik:3.6.5` - linux; amd64

```console
$ docker pull traefik@sha256:a6e6ffb23b620d5f8c7019a50c46875adc672389262758d239ed4fd602a1f86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebe7d161d0ca503ad8ebff362c34495b143e950a43016bbeefb68ceeade7ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:43 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c123c4b79203ea3d8aeadc78f39dcf4880551dbbce0f8c9265118147744290`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 460.9 KB (460941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae3961098f3b7eb90636311c62458e9d162d07d0c97984a4b8b9b2822b1e51c`  
		Last Modified: Tue, 16 Dec 2025 21:54:37 GMT  
		Size: 47.5 MB (47508411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6566b26c730bcb23fa154e162a73cd9362242dff8ab5551c3dcc7013ea377a2`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:59679a79dfb910f3d0ca1eed402b2516e2cd3de1fff2eb71b541a9848bf92696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a47fae0c266934036c870c1b0a29f10280547bb5920be2bcf68db607c5eab5`

```dockerfile
```

-	Layers:
	-	`sha256:252a04653ea612c30195020406ee86a653199e286a9d9dba847d5d5c1d61a0a8`  
		Last Modified: Tue, 16 Dec 2025 22:10:19 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888a3101a685aed38696caf472987774b89d4dd16cfcadb8e51aaf71ce405acc`  
		Last Modified: Tue, 16 Dec 2025 22:10:20 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:b2675b52948b6c87913d2cec95c10274afa28211ebef9a6c4895ee9a25f95287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47124574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa3558b9f3cf74070782f7ff953938a92a26c3be26529a9d183470df21ef3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:40 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d02c5a62d4136e3d9a27874e3f90d268a1e2bd21b5d014e8f6efa096ac62f5b`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dc4feddb18b5bb5fd6db4e1e934f32ed25a0cfd8f55eb790dedb4b2af53195`  
		Last Modified: Tue, 16 Dec 2025 21:55:02 GMT  
		Size: 43.1 MB (43094851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e5e96f6a45288ea41808ef79469b328b5d40aad67cb25840a96bd395f513e`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:86db7813d8e8062a04e0fae95fdd1ee2e894f27121a08be871062c2390a19469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bf7b6e0dd92b132c7c91beba5500bf6992408142614fedd73e33f222b00c7f`

```dockerfile
```

-	Layers:
	-	`sha256:d8b3daf4d00d15dcb2f24da0bf9762294c6695421572ef747fc9997ad708e727`  
		Last Modified: Tue, 16 Dec 2025 22:09:41 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6cbc266ff2aaaebc1d6f466eb6b2ed19aabb948ed34509a70aa2b3de9d8642d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4283f5af9f565dd6e90ec8f89b5ccb1dc6a7948e5a8ad04821c6f3aa1ee16101`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:47 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566766f1cca2628996b2c76f70f9307c33565b0771e3986efe943c6caece91b3`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 463.0 KB (462956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8988b5fa3857eee98f77c575d62ffbd99dd6bc84d22e78f092d7b1fcde42ea38`  
		Last Modified: Tue, 16 Dec 2025 21:54:34 GMT  
		Size: 43.2 MB (43235887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4cdd0a069b276d39beffe344ab2bf995b83295c1244374d4e53d40bcd704ef`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:d73b94160a95ad415b4bf47d621eb3675f1f2bc87eb920184e034473298c80b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3960dad2ec0b64a3e7a952fcf3d253bf2852fd358d9308bd56d302b7c29528`

```dockerfile
```

-	Layers:
	-	`sha256:5c321edc2a81a2b4ed1eb48497cff6f1c233b04dedf9609b7a168747c1c2af6b`  
		Last Modified: Tue, 16 Dec 2025 22:09:44 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6333a5f55afb6f36c7506e8de0334052764cca5a7b9edcdb5ab07c6d9d19fe9`  
		Last Modified: Tue, 16 Dec 2025 22:09:45 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:980934ddda50fdf87c97a0122b6b28c0d6c36c4586d3556acc3c4a908d1b6633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3fddc5c561077ded3f490c7c200156c27f4c1108ba69e4a7f751fb91825c0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:20 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f441f4d99a26e179d2526a42bd1c9175f545e1ca3a33506d0b8ab30a9f0881b`  
		Last Modified: Tue, 16 Dec 2025 21:57:38 GMT  
		Size: 41.3 MB (41258568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82fc7573a1347d7a1eb3426038d4dcde7881ae070f85d4ab234dacb3071486`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:b11123b48f2acf071838ad624aa6d0caa56b93881696a7619e80ee518f5c21c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b894a327d59478ddf84e916ff7554fbf7afdd9e81cc9ef6ed629cef57fb159`

```dockerfile
```

-	Layers:
	-	`sha256:0a11c3bd010dd789e90eac3656a409676311194977d78fc371cbb39684d28106`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d1a0c5edd23a7fd793a6418a6d658b1fb7ea379487c7a75627e6e3d16329c7`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.5` - linux; riscv64

```console
$ docker pull traefik@sha256:6897a7373e41d2ba27f918cc77f0972388239b2efbc2d7cf10cf931f5e1aa24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d76a1013a54de99b0a6821e2307209961bb10ab500b24620e6894b42659fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:59 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfc3a02968c43f57b5da703c6894a5a55b6c98d5bc1492e74821a9093241d2`  
		Last Modified: Tue, 16 Dec 2025 22:02:30 GMT  
		Size: 45.8 MB (45795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:c1d691e3b689732157509f1e2c8eaf47253beb2aa45bcb5c932fdd83e1ac2503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f4e2dffe5bcfb172995e23308a0fcf0c8db556fb0f8d4503d2e14b2d2447b`

```dockerfile
```

-	Layers:
	-	`sha256:e53f0a3aa459b728963b618c65bc1d895aec698979e52617f4c2e9315d4f0530`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a279bfeb8713cb9d08bb3bf4232d9b69754e2495fa6ad7942e151a570de0dda9`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.5` - linux; s390x

```console
$ docker pull traefik@sha256:b2f780a63f69029bf3b14e4051401ae9a98664b55bedb527931d7fafcea326c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49844511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf3004c5d3013f840161103038ab6ee14b0b084427e63bbfbd9eb14537d51bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:33 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2fbf42c48fff38dea98dc46f2c9bb22a8f4a630e67201e376421193c12f9e5`  
		Last Modified: Tue, 16 Dec 2025 21:55:49 GMT  
		Size: 45.7 MB (45658595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01674c2b8a9c731b10dae5670fc27a9a56409aab9564a25318e2995fd83af5b5`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:fd6432a961346ffdaa69077bccf74461ab8a255f76fb246fb76bab6e95b6d572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01564b41d37955505edeb640e08f411681e8d84a25369ca8b1f6ac4d115440c2`

```dockerfile
```

-	Layers:
	-	`sha256:2769263b7d8448b1201ab044140a4890824b1f952022c55611b782fa4314c92d`  
		Last Modified: Tue, 16 Dec 2025 22:09:54 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f67737957a7c8409ffb2b142341664e9e08c910d8ad74b501da46e6d0a3af4`  
		Last Modified: Tue, 16 Dec 2025 22:09:55 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6.5-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:2979bff651c98e70345dd886186a7a15ee3ce18b636af208d4ccbf2d56dbdddd
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
$ docker pull traefik@sha256:a6e6ffb23b620d5f8c7019a50c46875adc672389262758d239ed4fd602a1f86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebe7d161d0ca503ad8ebff362c34495b143e950a43016bbeefb68ceeade7ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:43 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c123c4b79203ea3d8aeadc78f39dcf4880551dbbce0f8c9265118147744290`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 460.9 KB (460941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae3961098f3b7eb90636311c62458e9d162d07d0c97984a4b8b9b2822b1e51c`  
		Last Modified: Tue, 16 Dec 2025 21:54:37 GMT  
		Size: 47.5 MB (47508411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6566b26c730bcb23fa154e162a73cd9362242dff8ab5551c3dcc7013ea377a2`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:59679a79dfb910f3d0ca1eed402b2516e2cd3de1fff2eb71b541a9848bf92696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a47fae0c266934036c870c1b0a29f10280547bb5920be2bcf68db607c5eab5`

```dockerfile
```

-	Layers:
	-	`sha256:252a04653ea612c30195020406ee86a653199e286a9d9dba847d5d5c1d61a0a8`  
		Last Modified: Tue, 16 Dec 2025 22:10:19 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888a3101a685aed38696caf472987774b89d4dd16cfcadb8e51aaf71ce405acc`  
		Last Modified: Tue, 16 Dec 2025 22:10:20 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:b2675b52948b6c87913d2cec95c10274afa28211ebef9a6c4895ee9a25f95287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47124574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa3558b9f3cf74070782f7ff953938a92a26c3be26529a9d183470df21ef3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:40 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d02c5a62d4136e3d9a27874e3f90d268a1e2bd21b5d014e8f6efa096ac62f5b`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dc4feddb18b5bb5fd6db4e1e934f32ed25a0cfd8f55eb790dedb4b2af53195`  
		Last Modified: Tue, 16 Dec 2025 21:55:02 GMT  
		Size: 43.1 MB (43094851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e5e96f6a45288ea41808ef79469b328b5d40aad67cb25840a96bd395f513e`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:86db7813d8e8062a04e0fae95fdd1ee2e894f27121a08be871062c2390a19469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bf7b6e0dd92b132c7c91beba5500bf6992408142614fedd73e33f222b00c7f`

```dockerfile
```

-	Layers:
	-	`sha256:d8b3daf4d00d15dcb2f24da0bf9762294c6695421572ef747fc9997ad708e727`  
		Last Modified: Tue, 16 Dec 2025 22:09:41 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6cbc266ff2aaaebc1d6f466eb6b2ed19aabb948ed34509a70aa2b3de9d8642d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4283f5af9f565dd6e90ec8f89b5ccb1dc6a7948e5a8ad04821c6f3aa1ee16101`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:47 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566766f1cca2628996b2c76f70f9307c33565b0771e3986efe943c6caece91b3`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 463.0 KB (462956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8988b5fa3857eee98f77c575d62ffbd99dd6bc84d22e78f092d7b1fcde42ea38`  
		Last Modified: Tue, 16 Dec 2025 21:54:34 GMT  
		Size: 43.2 MB (43235887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4cdd0a069b276d39beffe344ab2bf995b83295c1244374d4e53d40bcd704ef`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:d73b94160a95ad415b4bf47d621eb3675f1f2bc87eb920184e034473298c80b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3960dad2ec0b64a3e7a952fcf3d253bf2852fd358d9308bd56d302b7c29528`

```dockerfile
```

-	Layers:
	-	`sha256:5c321edc2a81a2b4ed1eb48497cff6f1c233b04dedf9609b7a168747c1c2af6b`  
		Last Modified: Tue, 16 Dec 2025 22:09:44 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6333a5f55afb6f36c7506e8de0334052764cca5a7b9edcdb5ab07c6d9d19fe9`  
		Last Modified: Tue, 16 Dec 2025 22:09:45 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:980934ddda50fdf87c97a0122b6b28c0d6c36c4586d3556acc3c4a908d1b6633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3fddc5c561077ded3f490c7c200156c27f4c1108ba69e4a7f751fb91825c0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:20 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f441f4d99a26e179d2526a42bd1c9175f545e1ca3a33506d0b8ab30a9f0881b`  
		Last Modified: Tue, 16 Dec 2025 21:57:38 GMT  
		Size: 41.3 MB (41258568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82fc7573a1347d7a1eb3426038d4dcde7881ae070f85d4ab234dacb3071486`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:b11123b48f2acf071838ad624aa6d0caa56b93881696a7619e80ee518f5c21c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b894a327d59478ddf84e916ff7554fbf7afdd9e81cc9ef6ed629cef57fb159`

```dockerfile
```

-	Layers:
	-	`sha256:0a11c3bd010dd789e90eac3656a409676311194977d78fc371cbb39684d28106`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d1a0c5edd23a7fd793a6418a6d658b1fb7ea379487c7a75627e6e3d16329c7`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:6897a7373e41d2ba27f918cc77f0972388239b2efbc2d7cf10cf931f5e1aa24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d76a1013a54de99b0a6821e2307209961bb10ab500b24620e6894b42659fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:59 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfc3a02968c43f57b5da703c6894a5a55b6c98d5bc1492e74821a9093241d2`  
		Last Modified: Tue, 16 Dec 2025 22:02:30 GMT  
		Size: 45.8 MB (45795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:c1d691e3b689732157509f1e2c8eaf47253beb2aa45bcb5c932fdd83e1ac2503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f4e2dffe5bcfb172995e23308a0fcf0c8db556fb0f8d4503d2e14b2d2447b`

```dockerfile
```

-	Layers:
	-	`sha256:e53f0a3aa459b728963b618c65bc1d895aec698979e52617f4c2e9315d4f0530`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a279bfeb8713cb9d08bb3bf4232d9b69754e2495fa6ad7942e151a570de0dda9`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:b2f780a63f69029bf3b14e4051401ae9a98664b55bedb527931d7fafcea326c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49844511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf3004c5d3013f840161103038ab6ee14b0b084427e63bbfbd9eb14537d51bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:33 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2fbf42c48fff38dea98dc46f2c9bb22a8f4a630e67201e376421193c12f9e5`  
		Last Modified: Tue, 16 Dec 2025 21:55:49 GMT  
		Size: 45.7 MB (45658595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01674c2b8a9c731b10dae5670fc27a9a56409aab9564a25318e2995fd83af5b5`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:fd6432a961346ffdaa69077bccf74461ab8a255f76fb246fb76bab6e95b6d572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01564b41d37955505edeb640e08f411681e8d84a25369ca8b1f6ac4d115440c2`

```dockerfile
```

-	Layers:
	-	`sha256:2769263b7d8448b1201ab044140a4890824b1f952022c55611b782fa4314c92d`  
		Last Modified: Tue, 16 Dec 2025 22:09:54 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f67737957a7c8409ffb2b142341664e9e08c910d8ad74b501da46e6d0a3af4`  
		Last Modified: Tue, 16 Dec 2025 22:09:55 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:b33557ba954d31336f3250919090ef124df0df3f8e7d17363fc251e568b77f9f
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
$ docker pull traefik@sha256:174f1a2c9487667e9cbd7f22236dda09fee74ffa9ccda6103164252ccef31dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc01ef432ddfb18e1ae4ccc7bf86c2c6e983b629812126cf00879938d5ef133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:30 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7373d7ff39c66d31e7e328d22241ad97173ac89003753dda524102cc53107802`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 460.9 KB (460949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aeb2a1ad90f6ffe5f5528580e42014da732e0c0d8312c158e086f70d64dfae`  
		Last Modified: Wed, 17 Dec 2025 18:42:14 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e111053df7c8cadd8dfaeb8490d04dfc93f9d07ed5652b6d640ef7a4c58fc3d8`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:c43ba2a7b61dfd2a423b7bc481f9845385f44395167e8352d996e94008d8ce6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c31e578e41f7186282529a4aad4f109a4f551710f1319062ca985a6da05c1`

```dockerfile
```

-	Layers:
	-	`sha256:2116d94ea9bacc40e0ade3117fa96ddf15e63fa36da8089c273c7e19c571a691`  
		Last Modified: Wed, 17 Dec 2025 19:09:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616c0b95ca69d28108937c887312561431c91b944f1ea54a1b821593e630d3d8`  
		Last Modified: Wed, 17 Dec 2025 19:09:30 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:92441aad8fdae59c61052bfa9a38b055e5e0b43008760f39bf9e3ea3d1216a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd42a450c3eb021d903de7b72452138cb66eb624c3dcaee29499c6fa5632e80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d6b4fdc1185815334dc04ce5cc1add06158e45c57ee901bce7ac29c718bff`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 461.5 KB (461458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd52af12c0cf52ba92b89743e3cfbafd1ffde7319bb061e614aced61f76e2b5`  
		Last Modified: Wed, 17 Dec 2025 18:41:49 GMT  
		Size: 42.8 MB (42793192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacdf7ee72f87469cb1cb594d1db6e02ad7b957c4dc8b7f056628b13ffb30139`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:179008a6edecd9f0bf04d1569f2c94987ee782c4afefb7801105652fb6c74628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58f432c0aa626bd6c3bdeb59724617cd8e3d8f9f4996bf9e16578d562f85dbb`

```dockerfile
```

-	Layers:
	-	`sha256:af59878afd8906fc5a2f9e36d5a677d20b9c81a5c32820fd4d9b41c34e580ef9`  
		Last Modified: Wed, 17 Dec 2025 19:10:23 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:897a5aa39c473ea62abf1f910044f5eeaefad47e12869f4112eea4660f362798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47293996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3057d7d3ee9aa83dad87f39d63216072423a688a68904564f774e54e3f222f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:42 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e904d2dc9111f62005b5dee00d41be23f0e8a19c4a23e54bfdb850682016936`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 463.0 KB (462978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b65b72401107ae382d9d6ab97ba706452bd292a3def06379a6d660470aabc8`  
		Last Modified: Wed, 17 Dec 2025 18:42:36 GMT  
		Size: 42.6 MB (42635448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfad583f79b6f025efef8774b3387f883401b93e51814eee60232141be6ebc2`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:cebe3d5c0ee5748098ae3bf7fbd1a8cbe9f0e7233bd3b5b68e0b09556319d495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987ca039b19e65a128578209c8e90778569093e1e1381decda320a874936e84a`

```dockerfile
```

-	Layers:
	-	`sha256:8f0075057da843c163b2f08e96d4f28d56500fd40eadfe5c26c3a3c5a98f77a3`  
		Last Modified: Wed, 17 Dec 2025 19:10:13 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ddc52028080001ed81b15d3ffdaba3aec997ef0fa669c7f80db66c448d4a88`  
		Last Modified: Wed, 17 Dec 2025 19:10:14 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:cecb7fad0442537204b5a852b39b02a8cfd85dbc9b362cb9cf9c15eeada73be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45245867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86dd3fd2ce35f83b500540009c71516d3e645f6d2f95c114c92bbc6606712f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:40:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:40:43 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:40:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09f86acc20c95b057694bed643875f0fa537cc6c0ba74652b355ad1b13c676`  
		Last Modified: Wed, 17 Dec 2025 18:42:00 GMT  
		Size: 41.0 MB (40954988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808d07d15fd68e5b11573c4e23dcc3fcf45e874102593287eb2e4d88eb5b6ea4`  
		Last Modified: Wed, 17 Dec 2025 18:41:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:10a02d8db0ae1a0efe8d4fe8ebd21133236322a14d263b0e174be1ccbb6b0057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831af4e9709665d4bdce755617fdea77d83235af766377e5885e5294132b04b2`

```dockerfile
```

-	Layers:
	-	`sha256:05f05dd8d7581f226db59ca208c11ca7d2e0c562f8ea4a2b081988a23dc51cae`  
		Last Modified: Wed, 17 Dec 2025 19:09:51 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d892a603513bfc38f1406b7b741a8acf028c5c350784d2d9fbc304b6f460c6`  
		Last Modified: Wed, 17 Dec 2025 19:09:52 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:66453f892822049494eb3c8d4e32f4c6ae5b3fe1a1490faa7ee3f503166170b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034e55d3eb9fd4fc2a6b5641b60d1ad6d02bad4083173401d0141c19b2722d1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:21 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409c0c18fc01012d825955c45a3a5ceee29dee3b8b54fd022ea3ca54b9b3d43`  
		Last Modified: Wed, 17 Dec 2025 18:46:53 GMT  
		Size: 45.3 MB (45324006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:1a66487a7b7719f85e925c7240ca641986f6a1fb0cd09f7382947a174310266e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de290e004466b29a7d0b2bc1ba76d9efcd3023b92c98049f8c1c0ffee7decd44`

```dockerfile
```

-	Layers:
	-	`sha256:9898591f677ff88b24f40976126580788387e360775ce6df02ad2d7c5dece53f`  
		Last Modified: Wed, 17 Dec 2025 19:09:56 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bdef50f6d22cc758b74d773276e97c56fe87f1396f5bfe19523ebb28b8e0ec`  
		Last Modified: Wed, 17 Dec 2025 19:09:57 GMT  
		Size: 12.6 KB (12557 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:788fd58abaaed61e2a36b88c929635c1c6566fe7b439f3eb5a8da1fee71282f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2b7ce4095e57c30dbe3f418349fe0086fb6815c343e8ca4bef82aae35a2248`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:02 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916fa41a772c8e72261f201209754a22b4cf24230aab2c0ad48d8d6849c20cdf`  
		Last Modified: Wed, 17 Dec 2025 18:42:09 GMT  
		Size: 45.3 MB (45254479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7f095d3b68b3257e638e5eb536d404c9dfc4dd1bb5546cba15a608a8fefd5`  
		Last Modified: Wed, 17 Dec 2025 18:42:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:95146c996e59baad3fbc78a82f7a8b2bd88d0d7a08d3355388cebb9fe547e21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93a5f35eecd903207574d988e9525c8bbb059af2fa6d25ccebbfdef1cc0ffb`

```dockerfile
```

-	Layers:
	-	`sha256:88bd86b5901a9b0c186d4cd648c8601559b401d3c4fd407ff806e137b3165394`  
		Last Modified: Wed, 17 Dec 2025 19:10:33 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0338d130ec8acfd06d982e64932bf0c73936bf53d285d57bb1f9fce908043b`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:2979bff651c98e70345dd886186a7a15ee3ce18b636af208d4ccbf2d56dbdddd
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
$ docker pull traefik@sha256:a6e6ffb23b620d5f8c7019a50c46875adc672389262758d239ed4fd602a1f86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebe7d161d0ca503ad8ebff362c34495b143e950a43016bbeefb68ceeade7ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:43 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c123c4b79203ea3d8aeadc78f39dcf4880551dbbce0f8c9265118147744290`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 460.9 KB (460941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae3961098f3b7eb90636311c62458e9d162d07d0c97984a4b8b9b2822b1e51c`  
		Last Modified: Tue, 16 Dec 2025 21:54:37 GMT  
		Size: 47.5 MB (47508411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6566b26c730bcb23fa154e162a73cd9362242dff8ab5551c3dcc7013ea377a2`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:59679a79dfb910f3d0ca1eed402b2516e2cd3de1fff2eb71b541a9848bf92696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a47fae0c266934036c870c1b0a29f10280547bb5920be2bcf68db607c5eab5`

```dockerfile
```

-	Layers:
	-	`sha256:252a04653ea612c30195020406ee86a653199e286a9d9dba847d5d5c1d61a0a8`  
		Last Modified: Tue, 16 Dec 2025 22:10:19 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888a3101a685aed38696caf472987774b89d4dd16cfcadb8e51aaf71ce405acc`  
		Last Modified: Tue, 16 Dec 2025 22:10:20 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:b2675b52948b6c87913d2cec95c10274afa28211ebef9a6c4895ee9a25f95287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47124574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa3558b9f3cf74070782f7ff953938a92a26c3be26529a9d183470df21ef3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:40 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d02c5a62d4136e3d9a27874e3f90d268a1e2bd21b5d014e8f6efa096ac62f5b`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dc4feddb18b5bb5fd6db4e1e934f32ed25a0cfd8f55eb790dedb4b2af53195`  
		Last Modified: Tue, 16 Dec 2025 21:55:02 GMT  
		Size: 43.1 MB (43094851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e5e96f6a45288ea41808ef79469b328b5d40aad67cb25840a96bd395f513e`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:86db7813d8e8062a04e0fae95fdd1ee2e894f27121a08be871062c2390a19469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bf7b6e0dd92b132c7c91beba5500bf6992408142614fedd73e33f222b00c7f`

```dockerfile
```

-	Layers:
	-	`sha256:d8b3daf4d00d15dcb2f24da0bf9762294c6695421572ef747fc9997ad708e727`  
		Last Modified: Tue, 16 Dec 2025 22:09:41 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6cbc266ff2aaaebc1d6f466eb6b2ed19aabb948ed34509a70aa2b3de9d8642d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4283f5af9f565dd6e90ec8f89b5ccb1dc6a7948e5a8ad04821c6f3aa1ee16101`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:47 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566766f1cca2628996b2c76f70f9307c33565b0771e3986efe943c6caece91b3`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 463.0 KB (462956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8988b5fa3857eee98f77c575d62ffbd99dd6bc84d22e78f092d7b1fcde42ea38`  
		Last Modified: Tue, 16 Dec 2025 21:54:34 GMT  
		Size: 43.2 MB (43235887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4cdd0a069b276d39beffe344ab2bf995b83295c1244374d4e53d40bcd704ef`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:d73b94160a95ad415b4bf47d621eb3675f1f2bc87eb920184e034473298c80b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3960dad2ec0b64a3e7a952fcf3d253bf2852fd358d9308bd56d302b7c29528`

```dockerfile
```

-	Layers:
	-	`sha256:5c321edc2a81a2b4ed1eb48497cff6f1c233b04dedf9609b7a168747c1c2af6b`  
		Last Modified: Tue, 16 Dec 2025 22:09:44 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6333a5f55afb6f36c7506e8de0334052764cca5a7b9edcdb5ab07c6d9d19fe9`  
		Last Modified: Tue, 16 Dec 2025 22:09:45 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:980934ddda50fdf87c97a0122b6b28c0d6c36c4586d3556acc3c4a908d1b6633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3fddc5c561077ded3f490c7c200156c27f4c1108ba69e4a7f751fb91825c0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:20 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f441f4d99a26e179d2526a42bd1c9175f545e1ca3a33506d0b8ab30a9f0881b`  
		Last Modified: Tue, 16 Dec 2025 21:57:38 GMT  
		Size: 41.3 MB (41258568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82fc7573a1347d7a1eb3426038d4dcde7881ae070f85d4ab234dacb3071486`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:b11123b48f2acf071838ad624aa6d0caa56b93881696a7619e80ee518f5c21c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b894a327d59478ddf84e916ff7554fbf7afdd9e81cc9ef6ed629cef57fb159`

```dockerfile
```

-	Layers:
	-	`sha256:0a11c3bd010dd789e90eac3656a409676311194977d78fc371cbb39684d28106`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d1a0c5edd23a7fd793a6418a6d658b1fb7ea379487c7a75627e6e3d16329c7`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:6897a7373e41d2ba27f918cc77f0972388239b2efbc2d7cf10cf931f5e1aa24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d76a1013a54de99b0a6821e2307209961bb10ab500b24620e6894b42659fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:59 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfc3a02968c43f57b5da703c6894a5a55b6c98d5bc1492e74821a9093241d2`  
		Last Modified: Tue, 16 Dec 2025 22:02:30 GMT  
		Size: 45.8 MB (45795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:c1d691e3b689732157509f1e2c8eaf47253beb2aa45bcb5c932fdd83e1ac2503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f4e2dffe5bcfb172995e23308a0fcf0c8db556fb0f8d4503d2e14b2d2447b`

```dockerfile
```

-	Layers:
	-	`sha256:e53f0a3aa459b728963b618c65bc1d895aec698979e52617f4c2e9315d4f0530`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a279bfeb8713cb9d08bb3bf4232d9b69754e2495fa6ad7942e151a570de0dda9`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:b2f780a63f69029bf3b14e4051401ae9a98664b55bedb527931d7fafcea326c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49844511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf3004c5d3013f840161103038ab6ee14b0b084427e63bbfbd9eb14537d51bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:33 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2fbf42c48fff38dea98dc46f2c9bb22a8f4a630e67201e376421193c12f9e5`  
		Last Modified: Tue, 16 Dec 2025 21:55:49 GMT  
		Size: 45.7 MB (45658595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01674c2b8a9c731b10dae5670fc27a9a56409aab9564a25318e2995fd83af5b5`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:fd6432a961346ffdaa69077bccf74461ab8a255f76fb246fb76bab6e95b6d572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01564b41d37955505edeb640e08f411681e8d84a25369ca8b1f6ac4d115440c2`

```dockerfile
```

-	Layers:
	-	`sha256:2769263b7d8448b1201ab044140a4890824b1f952022c55611b782fa4314c92d`  
		Last Modified: Tue, 16 Dec 2025 22:09:54 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f67737957a7c8409ffb2b142341664e9e08c910d8ad74b501da46e6d0a3af4`  
		Last Modified: Tue, 16 Dec 2025 22:09:55 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:b33557ba954d31336f3250919090ef124df0df3f8e7d17363fc251e568b77f9f
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
$ docker pull traefik@sha256:174f1a2c9487667e9cbd7f22236dda09fee74ffa9ccda6103164252ccef31dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc01ef432ddfb18e1ae4ccc7bf86c2c6e983b629812126cf00879938d5ef133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:30 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7373d7ff39c66d31e7e328d22241ad97173ac89003753dda524102cc53107802`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 460.9 KB (460949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aeb2a1ad90f6ffe5f5528580e42014da732e0c0d8312c158e086f70d64dfae`  
		Last Modified: Wed, 17 Dec 2025 18:42:14 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e111053df7c8cadd8dfaeb8490d04dfc93f9d07ed5652b6d640ef7a4c58fc3d8`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:c43ba2a7b61dfd2a423b7bc481f9845385f44395167e8352d996e94008d8ce6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c31e578e41f7186282529a4aad4f109a4f551710f1319062ca985a6da05c1`

```dockerfile
```

-	Layers:
	-	`sha256:2116d94ea9bacc40e0ade3117fa96ddf15e63fa36da8089c273c7e19c571a691`  
		Last Modified: Wed, 17 Dec 2025 19:09:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616c0b95ca69d28108937c887312561431c91b944f1ea54a1b821593e630d3d8`  
		Last Modified: Wed, 17 Dec 2025 19:09:30 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:92441aad8fdae59c61052bfa9a38b055e5e0b43008760f39bf9e3ea3d1216a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd42a450c3eb021d903de7b72452138cb66eb624c3dcaee29499c6fa5632e80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d6b4fdc1185815334dc04ce5cc1add06158e45c57ee901bce7ac29c718bff`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 461.5 KB (461458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd52af12c0cf52ba92b89743e3cfbafd1ffde7319bb061e614aced61f76e2b5`  
		Last Modified: Wed, 17 Dec 2025 18:41:49 GMT  
		Size: 42.8 MB (42793192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacdf7ee72f87469cb1cb594d1db6e02ad7b957c4dc8b7f056628b13ffb30139`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:179008a6edecd9f0bf04d1569f2c94987ee782c4afefb7801105652fb6c74628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58f432c0aa626bd6c3bdeb59724617cd8e3d8f9f4996bf9e16578d562f85dbb`

```dockerfile
```

-	Layers:
	-	`sha256:af59878afd8906fc5a2f9e36d5a677d20b9c81a5c32820fd4d9b41c34e580ef9`  
		Last Modified: Wed, 17 Dec 2025 19:10:23 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:897a5aa39c473ea62abf1f910044f5eeaefad47e12869f4112eea4660f362798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47293996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3057d7d3ee9aa83dad87f39d63216072423a688a68904564f774e54e3f222f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:42 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e904d2dc9111f62005b5dee00d41be23f0e8a19c4a23e54bfdb850682016936`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 463.0 KB (462978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b65b72401107ae382d9d6ab97ba706452bd292a3def06379a6d660470aabc8`  
		Last Modified: Wed, 17 Dec 2025 18:42:36 GMT  
		Size: 42.6 MB (42635448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfad583f79b6f025efef8774b3387f883401b93e51814eee60232141be6ebc2`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:cebe3d5c0ee5748098ae3bf7fbd1a8cbe9f0e7233bd3b5b68e0b09556319d495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987ca039b19e65a128578209c8e90778569093e1e1381decda320a874936e84a`

```dockerfile
```

-	Layers:
	-	`sha256:8f0075057da843c163b2f08e96d4f28d56500fd40eadfe5c26c3a3c5a98f77a3`  
		Last Modified: Wed, 17 Dec 2025 19:10:13 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ddc52028080001ed81b15d3ffdaba3aec997ef0fa669c7f80db66c448d4a88`  
		Last Modified: Wed, 17 Dec 2025 19:10:14 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:cecb7fad0442537204b5a852b39b02a8cfd85dbc9b362cb9cf9c15eeada73be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45245867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86dd3fd2ce35f83b500540009c71516d3e645f6d2f95c114c92bbc6606712f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:40:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:40:43 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:40:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09f86acc20c95b057694bed643875f0fa537cc6c0ba74652b355ad1b13c676`  
		Last Modified: Wed, 17 Dec 2025 18:42:00 GMT  
		Size: 41.0 MB (40954988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808d07d15fd68e5b11573c4e23dcc3fcf45e874102593287eb2e4d88eb5b6ea4`  
		Last Modified: Wed, 17 Dec 2025 18:41:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:10a02d8db0ae1a0efe8d4fe8ebd21133236322a14d263b0e174be1ccbb6b0057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831af4e9709665d4bdce755617fdea77d83235af766377e5885e5294132b04b2`

```dockerfile
```

-	Layers:
	-	`sha256:05f05dd8d7581f226db59ca208c11ca7d2e0c562f8ea4a2b081988a23dc51cae`  
		Last Modified: Wed, 17 Dec 2025 19:09:51 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d892a603513bfc38f1406b7b741a8acf028c5c350784d2d9fbc304b6f460c6`  
		Last Modified: Wed, 17 Dec 2025 19:09:52 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:66453f892822049494eb3c8d4e32f4c6ae5b3fe1a1490faa7ee3f503166170b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034e55d3eb9fd4fc2a6b5641b60d1ad6d02bad4083173401d0141c19b2722d1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:21 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409c0c18fc01012d825955c45a3a5ceee29dee3b8b54fd022ea3ca54b9b3d43`  
		Last Modified: Wed, 17 Dec 2025 18:46:53 GMT  
		Size: 45.3 MB (45324006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:1a66487a7b7719f85e925c7240ca641986f6a1fb0cd09f7382947a174310266e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de290e004466b29a7d0b2bc1ba76d9efcd3023b92c98049f8c1c0ffee7decd44`

```dockerfile
```

-	Layers:
	-	`sha256:9898591f677ff88b24f40976126580788387e360775ce6df02ad2d7c5dece53f`  
		Last Modified: Wed, 17 Dec 2025 19:09:56 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bdef50f6d22cc758b74d773276e97c56fe87f1396f5bfe19523ebb28b8e0ec`  
		Last Modified: Wed, 17 Dec 2025 19:09:57 GMT  
		Size: 12.6 KB (12557 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:788fd58abaaed61e2a36b88c929635c1c6566fe7b439f3eb5a8da1fee71282f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2b7ce4095e57c30dbe3f418349fe0086fb6815c343e8ca4bef82aae35a2248`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:02 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916fa41a772c8e72261f201209754a22b4cf24230aab2c0ad48d8d6849c20cdf`  
		Last Modified: Wed, 17 Dec 2025 18:42:09 GMT  
		Size: 45.3 MB (45254479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7f095d3b68b3257e638e5eb536d404c9dfc4dd1bb5546cba15a608a8fefd5`  
		Last Modified: Wed, 17 Dec 2025 18:42:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:95146c996e59baad3fbc78a82f7a8b2bd88d0d7a08d3355388cebb9fe547e21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93a5f35eecd903207574d988e9525c8bbb059af2fa6d25ccebbfdef1cc0ffb`

```dockerfile
```

-	Layers:
	-	`sha256:88bd86b5901a9b0c186d4cd648c8601559b401d3c4fd407ff806e137b3165394`  
		Last Modified: Wed, 17 Dec 2025 19:10:33 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0338d130ec8acfd06d982e64932bf0c73936bf53d285d57bb1f9fce908043b`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:b33557ba954d31336f3250919090ef124df0df3f8e7d17363fc251e568b77f9f
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
$ docker pull traefik@sha256:174f1a2c9487667e9cbd7f22236dda09fee74ffa9ccda6103164252ccef31dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc01ef432ddfb18e1ae4ccc7bf86c2c6e983b629812126cf00879938d5ef133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:30 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7373d7ff39c66d31e7e328d22241ad97173ac89003753dda524102cc53107802`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 460.9 KB (460949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aeb2a1ad90f6ffe5f5528580e42014da732e0c0d8312c158e086f70d64dfae`  
		Last Modified: Wed, 17 Dec 2025 18:42:14 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e111053df7c8cadd8dfaeb8490d04dfc93f9d07ed5652b6d640ef7a4c58fc3d8`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c43ba2a7b61dfd2a423b7bc481f9845385f44395167e8352d996e94008d8ce6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c31e578e41f7186282529a4aad4f109a4f551710f1319062ca985a6da05c1`

```dockerfile
```

-	Layers:
	-	`sha256:2116d94ea9bacc40e0ade3117fa96ddf15e63fa36da8089c273c7e19c571a691`  
		Last Modified: Wed, 17 Dec 2025 19:09:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616c0b95ca69d28108937c887312561431c91b944f1ea54a1b821593e630d3d8`  
		Last Modified: Wed, 17 Dec 2025 19:09:30 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:92441aad8fdae59c61052bfa9a38b055e5e0b43008760f39bf9e3ea3d1216a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd42a450c3eb021d903de7b72452138cb66eb624c3dcaee29499c6fa5632e80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d6b4fdc1185815334dc04ce5cc1add06158e45c57ee901bce7ac29c718bff`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 461.5 KB (461458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd52af12c0cf52ba92b89743e3cfbafd1ffde7319bb061e614aced61f76e2b5`  
		Last Modified: Wed, 17 Dec 2025 18:41:49 GMT  
		Size: 42.8 MB (42793192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacdf7ee72f87469cb1cb594d1db6e02ad7b957c4dc8b7f056628b13ffb30139`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:179008a6edecd9f0bf04d1569f2c94987ee782c4afefb7801105652fb6c74628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58f432c0aa626bd6c3bdeb59724617cd8e3d8f9f4996bf9e16578d562f85dbb`

```dockerfile
```

-	Layers:
	-	`sha256:af59878afd8906fc5a2f9e36d5a677d20b9c81a5c32820fd4d9b41c34e580ef9`  
		Last Modified: Wed, 17 Dec 2025 19:10:23 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:897a5aa39c473ea62abf1f910044f5eeaefad47e12869f4112eea4660f362798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47293996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3057d7d3ee9aa83dad87f39d63216072423a688a68904564f774e54e3f222f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:42 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e904d2dc9111f62005b5dee00d41be23f0e8a19c4a23e54bfdb850682016936`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 463.0 KB (462978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b65b72401107ae382d9d6ab97ba706452bd292a3def06379a6d660470aabc8`  
		Last Modified: Wed, 17 Dec 2025 18:42:36 GMT  
		Size: 42.6 MB (42635448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfad583f79b6f025efef8774b3387f883401b93e51814eee60232141be6ebc2`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:cebe3d5c0ee5748098ae3bf7fbd1a8cbe9f0e7233bd3b5b68e0b09556319d495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987ca039b19e65a128578209c8e90778569093e1e1381decda320a874936e84a`

```dockerfile
```

-	Layers:
	-	`sha256:8f0075057da843c163b2f08e96d4f28d56500fd40eadfe5c26c3a3c5a98f77a3`  
		Last Modified: Wed, 17 Dec 2025 19:10:13 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ddc52028080001ed81b15d3ffdaba3aec997ef0fa669c7f80db66c448d4a88`  
		Last Modified: Wed, 17 Dec 2025 19:10:14 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:cecb7fad0442537204b5a852b39b02a8cfd85dbc9b362cb9cf9c15eeada73be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45245867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86dd3fd2ce35f83b500540009c71516d3e645f6d2f95c114c92bbc6606712f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:40:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:40:43 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:40:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09f86acc20c95b057694bed643875f0fa537cc6c0ba74652b355ad1b13c676`  
		Last Modified: Wed, 17 Dec 2025 18:42:00 GMT  
		Size: 41.0 MB (40954988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808d07d15fd68e5b11573c4e23dcc3fcf45e874102593287eb2e4d88eb5b6ea4`  
		Last Modified: Wed, 17 Dec 2025 18:41:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:10a02d8db0ae1a0efe8d4fe8ebd21133236322a14d263b0e174be1ccbb6b0057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831af4e9709665d4bdce755617fdea77d83235af766377e5885e5294132b04b2`

```dockerfile
```

-	Layers:
	-	`sha256:05f05dd8d7581f226db59ca208c11ca7d2e0c562f8ea4a2b081988a23dc51cae`  
		Last Modified: Wed, 17 Dec 2025 19:09:51 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d892a603513bfc38f1406b7b741a8acf028c5c350784d2d9fbc304b6f460c6`  
		Last Modified: Wed, 17 Dec 2025 19:09:52 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:66453f892822049494eb3c8d4e32f4c6ae5b3fe1a1490faa7ee3f503166170b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034e55d3eb9fd4fc2a6b5641b60d1ad6d02bad4083173401d0141c19b2722d1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:21 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409c0c18fc01012d825955c45a3a5ceee29dee3b8b54fd022ea3ca54b9b3d43`  
		Last Modified: Wed, 17 Dec 2025 18:46:53 GMT  
		Size: 45.3 MB (45324006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:1a66487a7b7719f85e925c7240ca641986f6a1fb0cd09f7382947a174310266e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de290e004466b29a7d0b2bc1ba76d9efcd3023b92c98049f8c1c0ffee7decd44`

```dockerfile
```

-	Layers:
	-	`sha256:9898591f677ff88b24f40976126580788387e360775ce6df02ad2d7c5dece53f`  
		Last Modified: Wed, 17 Dec 2025 19:09:56 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bdef50f6d22cc758b74d773276e97c56fe87f1396f5bfe19523ebb28b8e0ec`  
		Last Modified: Wed, 17 Dec 2025 19:09:57 GMT  
		Size: 12.6 KB (12557 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:788fd58abaaed61e2a36b88c929635c1c6566fe7b439f3eb5a8da1fee71282f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2b7ce4095e57c30dbe3f418349fe0086fb6815c343e8ca4bef82aae35a2248`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:02 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916fa41a772c8e72261f201209754a22b4cf24230aab2c0ad48d8d6849c20cdf`  
		Last Modified: Wed, 17 Dec 2025 18:42:09 GMT  
		Size: 45.3 MB (45254479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7f095d3b68b3257e638e5eb536d404c9dfc4dd1bb5546cba15a608a8fefd5`  
		Last Modified: Wed, 17 Dec 2025 18:42:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:95146c996e59baad3fbc78a82f7a8b2bd88d0d7a08d3355388cebb9fe547e21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93a5f35eecd903207574d988e9525c8bbb059af2fa6d25ccebbfdef1cc0ffb`

```dockerfile
```

-	Layers:
	-	`sha256:88bd86b5901a9b0c186d4cd648c8601559b401d3c4fd407ff806e137b3165394`  
		Last Modified: Wed, 17 Dec 2025 19:10:33 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0338d130ec8acfd06d982e64932bf0c73936bf53d285d57bb1f9fce908043b`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.33`

```console
$ docker pull traefik@sha256:b33557ba954d31336f3250919090ef124df0df3f8e7d17363fc251e568b77f9f
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

### `traefik:v2.11.33` - linux; amd64

```console
$ docker pull traefik@sha256:174f1a2c9487667e9cbd7f22236dda09fee74ffa9ccda6103164252ccef31dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc01ef432ddfb18e1ae4ccc7bf86c2c6e983b629812126cf00879938d5ef133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:30 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7373d7ff39c66d31e7e328d22241ad97173ac89003753dda524102cc53107802`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 460.9 KB (460949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aeb2a1ad90f6ffe5f5528580e42014da732e0c0d8312c158e086f70d64dfae`  
		Last Modified: Wed, 17 Dec 2025 18:42:14 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e111053df7c8cadd8dfaeb8490d04dfc93f9d07ed5652b6d640ef7a4c58fc3d8`  
		Last Modified: Wed, 17 Dec 2025 18:42:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:c43ba2a7b61dfd2a423b7bc481f9845385f44395167e8352d996e94008d8ce6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c31e578e41f7186282529a4aad4f109a4f551710f1319062ca985a6da05c1`

```dockerfile
```

-	Layers:
	-	`sha256:2116d94ea9bacc40e0ade3117fa96ddf15e63fa36da8089c273c7e19c571a691`  
		Last Modified: Wed, 17 Dec 2025 19:09:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616c0b95ca69d28108937c887312561431c91b944f1ea54a1b821593e630d3d8`  
		Last Modified: Wed, 17 Dec 2025 19:09:30 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.33` - linux; arm variant v6

```console
$ docker pull traefik@sha256:92441aad8fdae59c61052bfa9a38b055e5e0b43008760f39bf9e3ea3d1216a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd42a450c3eb021d903de7b72452138cb66eb624c3dcaee29499c6fa5632e80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:28 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:28 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d6b4fdc1185815334dc04ce5cc1add06158e45c57ee901bce7ac29c718bff`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 461.5 KB (461458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd52af12c0cf52ba92b89743e3cfbafd1ffde7319bb061e614aced61f76e2b5`  
		Last Modified: Wed, 17 Dec 2025 18:41:49 GMT  
		Size: 42.8 MB (42793192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacdf7ee72f87469cb1cb594d1db6e02ad7b957c4dc8b7f056628b13ffb30139`  
		Last Modified: Wed, 17 Dec 2025 18:41:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:179008a6edecd9f0bf04d1569f2c94987ee782c4afefb7801105652fb6c74628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58f432c0aa626bd6c3bdeb59724617cd8e3d8f9f4996bf9e16578d562f85dbb`

```dockerfile
```

-	Layers:
	-	`sha256:af59878afd8906fc5a2f9e36d5a677d20b9c81a5c32820fd4d9b41c34e580ef9`  
		Last Modified: Wed, 17 Dec 2025 19:10:23 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.33` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:897a5aa39c473ea62abf1f910044f5eeaefad47e12869f4112eea4660f362798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47293996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3057d7d3ee9aa83dad87f39d63216072423a688a68904564f774e54e3f222f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 18:41:39 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:42 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:42 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e904d2dc9111f62005b5dee00d41be23f0e8a19c4a23e54bfdb850682016936`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 463.0 KB (462978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b65b72401107ae382d9d6ab97ba706452bd292a3def06379a6d660470aabc8`  
		Last Modified: Wed, 17 Dec 2025 18:42:36 GMT  
		Size: 42.6 MB (42635448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfad583f79b6f025efef8774b3387f883401b93e51814eee60232141be6ebc2`  
		Last Modified: Wed, 17 Dec 2025 18:42:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:cebe3d5c0ee5748098ae3bf7fbd1a8cbe9f0e7233bd3b5b68e0b09556319d495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987ca039b19e65a128578209c8e90778569093e1e1381decda320a874936e84a`

```dockerfile
```

-	Layers:
	-	`sha256:8f0075057da843c163b2f08e96d4f28d56500fd40eadfe5c26c3a3c5a98f77a3`  
		Last Modified: Wed, 17 Dec 2025 19:10:13 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ddc52028080001ed81b15d3ffdaba3aec997ef0fa669c7f80db66c448d4a88`  
		Last Modified: Wed, 17 Dec 2025 19:10:14 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.33` - linux; ppc64le

```console
$ docker pull traefik@sha256:cecb7fad0442537204b5a852b39b02a8cfd85dbc9b362cb9cf9c15eeada73be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45245867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86dd3fd2ce35f83b500540009c71516d3e645f6d2f95c114c92bbc6606712f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:40:43 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:40:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:40:43 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:40:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09f86acc20c95b057694bed643875f0fa537cc6c0ba74652b355ad1b13c676`  
		Last Modified: Wed, 17 Dec 2025 18:42:00 GMT  
		Size: 41.0 MB (40954988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808d07d15fd68e5b11573c4e23dcc3fcf45e874102593287eb2e4d88eb5b6ea4`  
		Last Modified: Wed, 17 Dec 2025 18:41:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:10a02d8db0ae1a0efe8d4fe8ebd21133236322a14d263b0e174be1ccbb6b0057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831af4e9709665d4bdce755617fdea77d83235af766377e5885e5294132b04b2`

```dockerfile
```

-	Layers:
	-	`sha256:05f05dd8d7581f226db59ca208c11ca7d2e0c562f8ea4a2b081988a23dc51cae`  
		Last Modified: Wed, 17 Dec 2025 19:09:51 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d892a603513bfc38f1406b7b741a8acf028c5c350784d2d9fbc304b6f460c6`  
		Last Modified: Wed, 17 Dec 2025 19:09:52 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.33` - linux; riscv64

```console
$ docker pull traefik@sha256:66453f892822049494eb3c8d4e32f4c6ae5b3fe1a1490faa7ee3f503166170b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034e55d3eb9fd4fc2a6b5641b60d1ad6d02bad4083173401d0141c19b2722d1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:21 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409c0c18fc01012d825955c45a3a5ceee29dee3b8b54fd022ea3ca54b9b3d43`  
		Last Modified: Wed, 17 Dec 2025 18:46:53 GMT  
		Size: 45.3 MB (45324006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:1a66487a7b7719f85e925c7240ca641986f6a1fb0cd09f7382947a174310266e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de290e004466b29a7d0b2bc1ba76d9efcd3023b92c98049f8c1c0ffee7decd44`

```dockerfile
```

-	Layers:
	-	`sha256:9898591f677ff88b24f40976126580788387e360775ce6df02ad2d7c5dece53f`  
		Last Modified: Wed, 17 Dec 2025 19:09:56 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bdef50f6d22cc758b74d773276e97c56fe87f1396f5bfe19523ebb28b8e0ec`  
		Last Modified: Wed, 17 Dec 2025 19:09:57 GMT  
		Size: 12.6 KB (12557 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.33` - linux; s390x

```console
$ docker pull traefik@sha256:788fd58abaaed61e2a36b88c929635c1c6566fe7b439f3eb5a8da1fee71282f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2b7ce4095e57c30dbe3f418349fe0086fb6815c343e8ca4bef82aae35a2248`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
COPY entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 18:41:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Dec 2025 18:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Dec 2025 18:41:02 GMT
CMD ["traefik"]
# Wed, 17 Dec 2025 18:41:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916fa41a772c8e72261f201209754a22b4cf24230aab2c0ad48d8d6849c20cdf`  
		Last Modified: Wed, 17 Dec 2025 18:42:09 GMT  
		Size: 45.3 MB (45254479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c7f095d3b68b3257e638e5eb536d404c9dfc4dd1bb5546cba15a608a8fefd5`  
		Last Modified: Wed, 17 Dec 2025 18:42:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:95146c996e59baad3fbc78a82f7a8b2bd88d0d7a08d3355388cebb9fe547e21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93a5f35eecd903207574d988e9525c8bbb059af2fa6d25ccebbfdef1cc0ffb`

```dockerfile
```

-	Layers:
	-	`sha256:88bd86b5901a9b0c186d4cd648c8601559b401d3c4fd407ff806e137b3165394`  
		Last Modified: Wed, 17 Dec 2025 19:10:33 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0338d130ec8acfd06d982e64932bf0c73936bf53d285d57bb1f9fce908043b`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.33-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11.33-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.33-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11.33-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:2979bff651c98e70345dd886186a7a15ee3ce18b636af208d4ccbf2d56dbdddd
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
$ docker pull traefik@sha256:a6e6ffb23b620d5f8c7019a50c46875adc672389262758d239ed4fd602a1f86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebe7d161d0ca503ad8ebff362c34495b143e950a43016bbeefb68ceeade7ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:43 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c123c4b79203ea3d8aeadc78f39dcf4880551dbbce0f8c9265118147744290`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 460.9 KB (460941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae3961098f3b7eb90636311c62458e9d162d07d0c97984a4b8b9b2822b1e51c`  
		Last Modified: Tue, 16 Dec 2025 21:54:37 GMT  
		Size: 47.5 MB (47508411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6566b26c730bcb23fa154e162a73cd9362242dff8ab5551c3dcc7013ea377a2`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:59679a79dfb910f3d0ca1eed402b2516e2cd3de1fff2eb71b541a9848bf92696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a47fae0c266934036c870c1b0a29f10280547bb5920be2bcf68db607c5eab5`

```dockerfile
```

-	Layers:
	-	`sha256:252a04653ea612c30195020406ee86a653199e286a9d9dba847d5d5c1d61a0a8`  
		Last Modified: Tue, 16 Dec 2025 22:10:19 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888a3101a685aed38696caf472987774b89d4dd16cfcadb8e51aaf71ce405acc`  
		Last Modified: Tue, 16 Dec 2025 22:10:20 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:b2675b52948b6c87913d2cec95c10274afa28211ebef9a6c4895ee9a25f95287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47124574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa3558b9f3cf74070782f7ff953938a92a26c3be26529a9d183470df21ef3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:40 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d02c5a62d4136e3d9a27874e3f90d268a1e2bd21b5d014e8f6efa096ac62f5b`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dc4feddb18b5bb5fd6db4e1e934f32ed25a0cfd8f55eb790dedb4b2af53195`  
		Last Modified: Tue, 16 Dec 2025 21:55:02 GMT  
		Size: 43.1 MB (43094851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e5e96f6a45288ea41808ef79469b328b5d40aad67cb25840a96bd395f513e`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:86db7813d8e8062a04e0fae95fdd1ee2e894f27121a08be871062c2390a19469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bf7b6e0dd92b132c7c91beba5500bf6992408142614fedd73e33f222b00c7f`

```dockerfile
```

-	Layers:
	-	`sha256:d8b3daf4d00d15dcb2f24da0bf9762294c6695421572ef747fc9997ad708e727`  
		Last Modified: Tue, 16 Dec 2025 22:09:41 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6cbc266ff2aaaebc1d6f466eb6b2ed19aabb948ed34509a70aa2b3de9d8642d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4283f5af9f565dd6e90ec8f89b5ccb1dc6a7948e5a8ad04821c6f3aa1ee16101`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:47 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566766f1cca2628996b2c76f70f9307c33565b0771e3986efe943c6caece91b3`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 463.0 KB (462956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8988b5fa3857eee98f77c575d62ffbd99dd6bc84d22e78f092d7b1fcde42ea38`  
		Last Modified: Tue, 16 Dec 2025 21:54:34 GMT  
		Size: 43.2 MB (43235887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4cdd0a069b276d39beffe344ab2bf995b83295c1244374d4e53d40bcd704ef`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:d73b94160a95ad415b4bf47d621eb3675f1f2bc87eb920184e034473298c80b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3960dad2ec0b64a3e7a952fcf3d253bf2852fd358d9308bd56d302b7c29528`

```dockerfile
```

-	Layers:
	-	`sha256:5c321edc2a81a2b4ed1eb48497cff6f1c233b04dedf9609b7a168747c1c2af6b`  
		Last Modified: Tue, 16 Dec 2025 22:09:44 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6333a5f55afb6f36c7506e8de0334052764cca5a7b9edcdb5ab07c6d9d19fe9`  
		Last Modified: Tue, 16 Dec 2025 22:09:45 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:980934ddda50fdf87c97a0122b6b28c0d6c36c4586d3556acc3c4a908d1b6633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3fddc5c561077ded3f490c7c200156c27f4c1108ba69e4a7f751fb91825c0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:20 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f441f4d99a26e179d2526a42bd1c9175f545e1ca3a33506d0b8ab30a9f0881b`  
		Last Modified: Tue, 16 Dec 2025 21:57:38 GMT  
		Size: 41.3 MB (41258568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82fc7573a1347d7a1eb3426038d4dcde7881ae070f85d4ab234dacb3071486`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:b11123b48f2acf071838ad624aa6d0caa56b93881696a7619e80ee518f5c21c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b894a327d59478ddf84e916ff7554fbf7afdd9e81cc9ef6ed629cef57fb159`

```dockerfile
```

-	Layers:
	-	`sha256:0a11c3bd010dd789e90eac3656a409676311194977d78fc371cbb39684d28106`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d1a0c5edd23a7fd793a6418a6d658b1fb7ea379487c7a75627e6e3d16329c7`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:6897a7373e41d2ba27f918cc77f0972388239b2efbc2d7cf10cf931f5e1aa24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d76a1013a54de99b0a6821e2307209961bb10ab500b24620e6894b42659fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:59 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfc3a02968c43f57b5da703c6894a5a55b6c98d5bc1492e74821a9093241d2`  
		Last Modified: Tue, 16 Dec 2025 22:02:30 GMT  
		Size: 45.8 MB (45795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:c1d691e3b689732157509f1e2c8eaf47253beb2aa45bcb5c932fdd83e1ac2503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f4e2dffe5bcfb172995e23308a0fcf0c8db556fb0f8d4503d2e14b2d2447b`

```dockerfile
```

-	Layers:
	-	`sha256:e53f0a3aa459b728963b618c65bc1d895aec698979e52617f4c2e9315d4f0530`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a279bfeb8713cb9d08bb3bf4232d9b69754e2495fa6ad7942e151a570de0dda9`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:b2f780a63f69029bf3b14e4051401ae9a98664b55bedb527931d7fafcea326c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49844511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf3004c5d3013f840161103038ab6ee14b0b084427e63bbfbd9eb14537d51bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:33 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2fbf42c48fff38dea98dc46f2c9bb22a8f4a630e67201e376421193c12f9e5`  
		Last Modified: Tue, 16 Dec 2025 21:55:49 GMT  
		Size: 45.7 MB (45658595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01674c2b8a9c731b10dae5670fc27a9a56409aab9564a25318e2995fd83af5b5`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:fd6432a961346ffdaa69077bccf74461ab8a255f76fb246fb76bab6e95b6d572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01564b41d37955505edeb640e08f411681e8d84a25369ca8b1f6ac4d115440c2`

```dockerfile
```

-	Layers:
	-	`sha256:2769263b7d8448b1201ab044140a4890824b1f952022c55611b782fa4314c92d`  
		Last Modified: Tue, 16 Dec 2025 22:09:54 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f67737957a7c8409ffb2b142341664e9e08c910d8ad74b501da46e6d0a3af4`  
		Last Modified: Tue, 16 Dec 2025 22:09:55 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:2979bff651c98e70345dd886186a7a15ee3ce18b636af208d4ccbf2d56dbdddd
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
$ docker pull traefik@sha256:a6e6ffb23b620d5f8c7019a50c46875adc672389262758d239ed4fd602a1f86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebe7d161d0ca503ad8ebff362c34495b143e950a43016bbeefb68ceeade7ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:43 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c123c4b79203ea3d8aeadc78f39dcf4880551dbbce0f8c9265118147744290`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 460.9 KB (460941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae3961098f3b7eb90636311c62458e9d162d07d0c97984a4b8b9b2822b1e51c`  
		Last Modified: Tue, 16 Dec 2025 21:54:37 GMT  
		Size: 47.5 MB (47508411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6566b26c730bcb23fa154e162a73cd9362242dff8ab5551c3dcc7013ea377a2`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:59679a79dfb910f3d0ca1eed402b2516e2cd3de1fff2eb71b541a9848bf92696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a47fae0c266934036c870c1b0a29f10280547bb5920be2bcf68db607c5eab5`

```dockerfile
```

-	Layers:
	-	`sha256:252a04653ea612c30195020406ee86a653199e286a9d9dba847d5d5c1d61a0a8`  
		Last Modified: Tue, 16 Dec 2025 22:10:19 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888a3101a685aed38696caf472987774b89d4dd16cfcadb8e51aaf71ce405acc`  
		Last Modified: Tue, 16 Dec 2025 22:10:20 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:b2675b52948b6c87913d2cec95c10274afa28211ebef9a6c4895ee9a25f95287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47124574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa3558b9f3cf74070782f7ff953938a92a26c3be26529a9d183470df21ef3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:40 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d02c5a62d4136e3d9a27874e3f90d268a1e2bd21b5d014e8f6efa096ac62f5b`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dc4feddb18b5bb5fd6db4e1e934f32ed25a0cfd8f55eb790dedb4b2af53195`  
		Last Modified: Tue, 16 Dec 2025 21:55:02 GMT  
		Size: 43.1 MB (43094851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e5e96f6a45288ea41808ef79469b328b5d40aad67cb25840a96bd395f513e`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:86db7813d8e8062a04e0fae95fdd1ee2e894f27121a08be871062c2390a19469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bf7b6e0dd92b132c7c91beba5500bf6992408142614fedd73e33f222b00c7f`

```dockerfile
```

-	Layers:
	-	`sha256:d8b3daf4d00d15dcb2f24da0bf9762294c6695421572ef747fc9997ad708e727`  
		Last Modified: Tue, 16 Dec 2025 22:09:41 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6cbc266ff2aaaebc1d6f466eb6b2ed19aabb948ed34509a70aa2b3de9d8642d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4283f5af9f565dd6e90ec8f89b5ccb1dc6a7948e5a8ad04821c6f3aa1ee16101`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:47 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566766f1cca2628996b2c76f70f9307c33565b0771e3986efe943c6caece91b3`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 463.0 KB (462956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8988b5fa3857eee98f77c575d62ffbd99dd6bc84d22e78f092d7b1fcde42ea38`  
		Last Modified: Tue, 16 Dec 2025 21:54:34 GMT  
		Size: 43.2 MB (43235887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4cdd0a069b276d39beffe344ab2bf995b83295c1244374d4e53d40bcd704ef`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:d73b94160a95ad415b4bf47d621eb3675f1f2bc87eb920184e034473298c80b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3960dad2ec0b64a3e7a952fcf3d253bf2852fd358d9308bd56d302b7c29528`

```dockerfile
```

-	Layers:
	-	`sha256:5c321edc2a81a2b4ed1eb48497cff6f1c233b04dedf9609b7a168747c1c2af6b`  
		Last Modified: Tue, 16 Dec 2025 22:09:44 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6333a5f55afb6f36c7506e8de0334052764cca5a7b9edcdb5ab07c6d9d19fe9`  
		Last Modified: Tue, 16 Dec 2025 22:09:45 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:980934ddda50fdf87c97a0122b6b28c0d6c36c4586d3556acc3c4a908d1b6633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3fddc5c561077ded3f490c7c200156c27f4c1108ba69e4a7f751fb91825c0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:20 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f441f4d99a26e179d2526a42bd1c9175f545e1ca3a33506d0b8ab30a9f0881b`  
		Last Modified: Tue, 16 Dec 2025 21:57:38 GMT  
		Size: 41.3 MB (41258568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82fc7573a1347d7a1eb3426038d4dcde7881ae070f85d4ab234dacb3071486`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:b11123b48f2acf071838ad624aa6d0caa56b93881696a7619e80ee518f5c21c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b894a327d59478ddf84e916ff7554fbf7afdd9e81cc9ef6ed629cef57fb159`

```dockerfile
```

-	Layers:
	-	`sha256:0a11c3bd010dd789e90eac3656a409676311194977d78fc371cbb39684d28106`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d1a0c5edd23a7fd793a6418a6d658b1fb7ea379487c7a75627e6e3d16329c7`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:6897a7373e41d2ba27f918cc77f0972388239b2efbc2d7cf10cf931f5e1aa24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d76a1013a54de99b0a6821e2307209961bb10ab500b24620e6894b42659fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:59 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfc3a02968c43f57b5da703c6894a5a55b6c98d5bc1492e74821a9093241d2`  
		Last Modified: Tue, 16 Dec 2025 22:02:30 GMT  
		Size: 45.8 MB (45795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:c1d691e3b689732157509f1e2c8eaf47253beb2aa45bcb5c932fdd83e1ac2503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f4e2dffe5bcfb172995e23308a0fcf0c8db556fb0f8d4503d2e14b2d2447b`

```dockerfile
```

-	Layers:
	-	`sha256:e53f0a3aa459b728963b618c65bc1d895aec698979e52617f4c2e9315d4f0530`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a279bfeb8713cb9d08bb3bf4232d9b69754e2495fa6ad7942e151a570de0dda9`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:b2f780a63f69029bf3b14e4051401ae9a98664b55bedb527931d7fafcea326c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49844511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf3004c5d3013f840161103038ab6ee14b0b084427e63bbfbd9eb14537d51bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:33 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2fbf42c48fff38dea98dc46f2c9bb22a8f4a630e67201e376421193c12f9e5`  
		Last Modified: Tue, 16 Dec 2025 21:55:49 GMT  
		Size: 45.7 MB (45658595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01674c2b8a9c731b10dae5670fc27a9a56409aab9564a25318e2995fd83af5b5`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:fd6432a961346ffdaa69077bccf74461ab8a255f76fb246fb76bab6e95b6d572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01564b41d37955505edeb640e08f411681e8d84a25369ca8b1f6ac4d115440c2`

```dockerfile
```

-	Layers:
	-	`sha256:2769263b7d8448b1201ab044140a4890824b1f952022c55611b782fa4314c92d`  
		Last Modified: Tue, 16 Dec 2025 22:09:54 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f67737957a7c8409ffb2b142341664e9e08c910d8ad74b501da46e6d0a3af4`  
		Last Modified: Tue, 16 Dec 2025 22:09:55 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.5`

```console
$ docker pull traefik@sha256:2979bff651c98e70345dd886186a7a15ee3ce18b636af208d4ccbf2d56dbdddd
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

### `traefik:v3.6.5` - linux; amd64

```console
$ docker pull traefik@sha256:a6e6ffb23b620d5f8c7019a50c46875adc672389262758d239ed4fd602a1f86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebe7d161d0ca503ad8ebff362c34495b143e950a43016bbeefb68ceeade7ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:43 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c123c4b79203ea3d8aeadc78f39dcf4880551dbbce0f8c9265118147744290`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 460.9 KB (460941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae3961098f3b7eb90636311c62458e9d162d07d0c97984a4b8b9b2822b1e51c`  
		Last Modified: Tue, 16 Dec 2025 21:54:37 GMT  
		Size: 47.5 MB (47508411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6566b26c730bcb23fa154e162a73cd9362242dff8ab5551c3dcc7013ea377a2`  
		Last Modified: Tue, 16 Dec 2025 21:54:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:59679a79dfb910f3d0ca1eed402b2516e2cd3de1fff2eb71b541a9848bf92696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a47fae0c266934036c870c1b0a29f10280547bb5920be2bcf68db607c5eab5`

```dockerfile
```

-	Layers:
	-	`sha256:252a04653ea612c30195020406ee86a653199e286a9d9dba847d5d5c1d61a0a8`  
		Last Modified: Tue, 16 Dec 2025 22:10:19 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888a3101a685aed38696caf472987774b89d4dd16cfcadb8e51aaf71ce405acc`  
		Last Modified: Tue, 16 Dec 2025 22:10:20 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:b2675b52948b6c87913d2cec95c10274afa28211ebef9a6c4895ee9a25f95287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47124574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa3558b9f3cf74070782f7ff953938a92a26c3be26529a9d183470df21ef3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:37 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:40 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:40 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d02c5a62d4136e3d9a27874e3f90d268a1e2bd21b5d014e8f6efa096ac62f5b`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dc4feddb18b5bb5fd6db4e1e934f32ed25a0cfd8f55eb790dedb4b2af53195`  
		Last Modified: Tue, 16 Dec 2025 21:55:02 GMT  
		Size: 43.1 MB (43094851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e5e96f6a45288ea41808ef79469b328b5d40aad67cb25840a96bd395f513e`  
		Last Modified: Tue, 16 Dec 2025 21:54:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:86db7813d8e8062a04e0fae95fdd1ee2e894f27121a08be871062c2390a19469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bf7b6e0dd92b132c7c91beba5500bf6992408142614fedd73e33f222b00c7f`

```dockerfile
```

-	Layers:
	-	`sha256:d8b3daf4d00d15dcb2f24da0bf9762294c6695421572ef747fc9997ad708e727`  
		Last Modified: Tue, 16 Dec 2025 22:09:41 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:6cbc266ff2aaaebc1d6f466eb6b2ed19aabb948ed34509a70aa2b3de9d8642d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4283f5af9f565dd6e90ec8f89b5ccb1dc6a7948e5a8ad04821c6f3aa1ee16101`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:53:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:53:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:53:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:53:47 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:53:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566766f1cca2628996b2c76f70f9307c33565b0771e3986efe943c6caece91b3`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 463.0 KB (462956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8988b5fa3857eee98f77c575d62ffbd99dd6bc84d22e78f092d7b1fcde42ea38`  
		Last Modified: Tue, 16 Dec 2025 21:54:34 GMT  
		Size: 43.2 MB (43235887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4cdd0a069b276d39beffe344ab2bf995b83295c1244374d4e53d40bcd704ef`  
		Last Modified: Tue, 16 Dec 2025 21:54:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:d73b94160a95ad415b4bf47d621eb3675f1f2bc87eb920184e034473298c80b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3960dad2ec0b64a3e7a952fcf3d253bf2852fd358d9308bd56d302b7c29528`

```dockerfile
```

-	Layers:
	-	`sha256:5c321edc2a81a2b4ed1eb48497cff6f1c233b04dedf9609b7a168747c1c2af6b`  
		Last Modified: Tue, 16 Dec 2025 22:09:44 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6333a5f55afb6f36c7506e8de0334052764cca5a7b9edcdb5ab07c6d9d19fe9`  
		Last Modified: Tue, 16 Dec 2025 22:09:45 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:980934ddda50fdf87c97a0122b6b28c0d6c36c4586d3556acc3c4a908d1b6633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3fddc5c561077ded3f490c7c200156c27f4c1108ba69e4a7f751fb91825c0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:20 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dce07fefb48158c8c0fbe3f9571afdd22754b309db77aa1dc8517a24fff5b7`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 463.5 KB (463493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f441f4d99a26e179d2526a42bd1c9175f545e1ca3a33506d0b8ab30a9f0881b`  
		Last Modified: Tue, 16 Dec 2025 21:57:38 GMT  
		Size: 41.3 MB (41258568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82fc7573a1347d7a1eb3426038d4dcde7881ae070f85d4ab234dacb3071486`  
		Last Modified: Tue, 16 Dec 2025 21:57:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:b11123b48f2acf071838ad624aa6d0caa56b93881696a7619e80ee518f5c21c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b894a327d59478ddf84e916ff7554fbf7afdd9e81cc9ef6ed629cef57fb159`

```dockerfile
```

-	Layers:
	-	`sha256:0a11c3bd010dd789e90eac3656a409676311194977d78fc371cbb39684d28106`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d1a0c5edd23a7fd793a6418a6d658b1fb7ea379487c7a75627e6e3d16329c7`  
		Last Modified: Tue, 16 Dec 2025 22:09:56 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.5` - linux; riscv64

```console
$ docker pull traefik@sha256:6897a7373e41d2ba27f918cc77f0972388239b2efbc2d7cf10cf931f5e1aa24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d76a1013a54de99b0a6821e2307209961bb10ab500b24620e6894b42659fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:56:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:56:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:56:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:56:59 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:56:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d282c71eb69604d39dfbc532e09bf3b28312e3995dcf5364692c8abdf47de4d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfc3a02968c43f57b5da703c6894a5a55b6c98d5bc1492e74821a9093241d2`  
		Last Modified: Tue, 16 Dec 2025 22:02:30 GMT  
		Size: 45.8 MB (45795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:c1d691e3b689732157509f1e2c8eaf47253beb2aa45bcb5c932fdd83e1ac2503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f4e2dffe5bcfb172995e23308a0fcf0c8db556fb0f8d4503d2e14b2d2447b`

```dockerfile
```

-	Layers:
	-	`sha256:e53f0a3aa459b728963b618c65bc1d895aec698979e52617f4c2e9315d4f0530`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a279bfeb8713cb9d08bb3bf4232d9b69754e2495fa6ad7942e151a570de0dda9`  
		Last Modified: Tue, 16 Dec 2025 22:10:05 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.5` - linux; s390x

```console
$ docker pull traefik@sha256:b2f780a63f69029bf3b14e4051401ae9a98664b55bedb527931d7fafcea326c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49844511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf3004c5d3013f840161103038ab6ee14b0b084427e63bbfbd9eb14537d51bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Dec 2025 21:54:28 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 16 Dec 2025 21:54:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
COPY entrypoint.sh / # buildkit
# Tue, 16 Dec 2025 21:54:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Dec 2025 21:54:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Dec 2025 21:54:33 GMT
CMD ["traefik"]
# Tue, 16 Dec 2025 21:54:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff6bcd7f51fb2c4f9e173371f06b5b4c2f2db246e2c7dd410e8128099c0717`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2fbf42c48fff38dea98dc46f2c9bb22a8f4a630e67201e376421193c12f9e5`  
		Last Modified: Tue, 16 Dec 2025 21:55:49 GMT  
		Size: 45.7 MB (45658595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01674c2b8a9c731b10dae5670fc27a9a56409aab9564a25318e2995fd83af5b5`  
		Last Modified: Tue, 16 Dec 2025 21:55:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:fd6432a961346ffdaa69077bccf74461ab8a255f76fb246fb76bab6e95b6d572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01564b41d37955505edeb640e08f411681e8d84a25369ca8b1f6ac4d115440c2`

```dockerfile
```

-	Layers:
	-	`sha256:2769263b7d8448b1201ab044140a4890824b1f952022c55611b782fa4314c92d`  
		Last Modified: Tue, 16 Dec 2025 22:09:54 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f67737957a7c8409ffb2b142341664e9e08c910d8ad74b501da46e6d0a3af4`  
		Last Modified: Tue, 16 Dec 2025 22:09:55 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6.5-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
