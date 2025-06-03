<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.25`](#traefik21125)
-	[`traefik:2.11.25-nanoserver-ltsc2022`](#traefik21125-nanoserver-ltsc2022)
-	[`traefik:2.11.25-windowsservercore-ltsc2022`](#traefik21125-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.4`](#traefik34)
-	[`traefik:3.4-nanoserver-ltsc2022`](#traefik34-nanoserver-ltsc2022)
-	[`traefik:3.4-windowsservercore-ltsc2022`](#traefik34-windowsservercore-ltsc2022)
-	[`traefik:3.4.1`](#traefik341)
-	[`traefik:3.4.1-nanoserver-ltsc2022`](#traefik341-nanoserver-ltsc2022)
-	[`traefik:3.4.1-windowsservercore-ltsc2022`](#traefik341-windowsservercore-ltsc2022)
-	[`traefik:chaource`](#traefikchaource)
-	[`traefik:chaource-nanoserver-ltsc2022`](#traefikchaource-nanoserver-ltsc2022)
-	[`traefik:chaource-windowsservercore-ltsc2022`](#traefikchaource-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-nanoserver-ltsc2022`](#traefikmimolette-nanoserver-ltsc2022)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:nanoserver-ltsc2022`](#traefiknanoserver-ltsc2022)
-	[`traefik:v2`](#traefikv2)
-	[`traefik:v2-nanoserver-ltsc2022`](#traefikv2-nanoserver-ltsc2022)
-	[`traefik:v2-windowsservercore-ltsc2022`](#traefikv2-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-nanoserver-ltsc2022`](#traefikv211-nanoserver-ltsc2022)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.25`](#traefikv21125)
-	[`traefik:v2.11.25-nanoserver-ltsc2022`](#traefikv21125-nanoserver-ltsc2022)
-	[`traefik:v2.11.25-windowsservercore-ltsc2022`](#traefikv21125-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.4`](#traefikv34)
-	[`traefik:v3.4-nanoserver-ltsc2022`](#traefikv34-nanoserver-ltsc2022)
-	[`traefik:v3.4-windowsservercore-ltsc2022`](#traefikv34-windowsservercore-ltsc2022)
-	[`traefik:v3.4.1`](#traefikv341)
-	[`traefik:v3.4.1-nanoserver-ltsc2022`](#traefikv341-nanoserver-ltsc2022)
-	[`traefik:v3.4.1-windowsservercore-ltsc2022`](#traefikv341-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:6b0e06781a8c7ecfc0171b86ef4239567913f025d054f829b93836484c08d4de
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
$ docker pull traefik@sha256:7a3e93790acb9cc76a1671d60edac91f2b44a660c542a129f7b60ec2051f5935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56552512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51ba6b3748820dfa2350e62162dc7b6923bce1d439d7590dfe7b5b06fd7a43d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47353acdc55d84d8eab52dc12ed5a0544a15baeaaf7f841ac086cebb50b82d5f`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 52.4 MB (52449696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:306abeba90dd204cc7e01407add4fff90b5c5a9edf4c8aca9919bd795665ccf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.2 KB (853200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90af661a720bad4fc40519980c3e6448ce6246bde83edb130c438936f7345d8f`

```dockerfile
```

-	Layers:
	-	`sha256:6a24cac55bba047916faf531a3af8614f532036041648fc1eb0745bcfbea3b18`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 840.7 KB (840662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc7f0bf9995aaadc937e4bd1a4035f31cd89dff5ca1ef50562db74686283f15`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9394e41a11e186e65d61d6b214efaf23a6df92f739bed50b27cf7d54b5de99bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52318031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d7b2f69920da843f662e3a66d609b3d54978c34e6a1a3e313f1e51ae77229`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2366ec9e01d41af275db660969c094e2c585439262f2f12cc2a5e5b6ce53464`  
		Last Modified: Tue, 27 May 2025 14:49:39 GMT  
		Size: 48.5 MB (48493507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab654d05db06d563d37378656367863bf7956cfffe339a7f3d02e668dbb4744c`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:cb2ed2f99573807413124377f2dac2912f2fb9efa7a46ffe8fe108f34c519e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c2276f0758ed20a2cdafbd17e771bafe65925182dc94eb10f8d5937905387`

```dockerfile
```

-	Layers:
	-	`sha256:d213ff87ba5e5f2b4267754c42ecd52932a688283e3aae2a395d8ce09530f8c0`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:87d941b6f55eaf4cdb35a94803f120d1c4167ebeaaaa43e6b46c5ac2d0f4e99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52858264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12c6c93b980e31b195991ec6609863b02a4c28a32584413c48d18bc364abe8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3870bcc7664fbf79c85068a58c49eadda5b3d3e83b3a261eb0687c8f382cba`  
		Last Modified: Tue, 03 Jun 2025 13:36:16 GMT  
		Size: 48.4 MB (48402796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955359e8bfcdc4fb80c3199996d51984fb401ed62747abf90d51c961f03ace5`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:c55567b804aad0b14a0467ceec3987a7d82ffaefb10fa549f77866f9e0c1b9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.4 KB (853445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb10668fadc74f6751e3b60cbd6f4c38843f45a6a9be6fbb22532ba802de1db`

```dockerfile
```

-	Layers:
	-	`sha256:30c42da66f61218a3020f7f694222b6575250a771d2bcb1b7fdc0e6faeaad8b4`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 840.8 KB (840754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392d505427c83a6e8915f94fb1287d21d09271fc51f8ddb46f01a299c650ec5e`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 12.7 KB (12691 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:ffa941c3a39cf8070066f8e642d043b3bbb93382b65ab191cb4f59a70c6af732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50485530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a848a8c9fbb90595a5bc10de6eb825d5b3eca316940e9f1f8f2f089a9cd7877`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be76b49bda3c8fd09b1fc1bb633224dd0871739cf51c1e96256322e662eb9ecc`  
		Last Modified: Tue, 27 May 2025 14:51:02 GMT  
		Size: 46.4 MB (46448254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729c14791b9df9fc72e478fa8d5c6bc0247b943a8520f7c10212326ae2273676`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:d12369f44494221de3c8b33bade1adfdcbbe7c11ac178c4bec540f4011d4aa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cf941cdda74702c092277fefff62640a0061d956f3961e5ebd1f020c55db3e`

```dockerfile
```

-	Layers:
	-	`sha256:ab995543f597da5ad856301f199da00314c3433240b338a4d72dfd57eda69543`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 838.8 KB (838763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c506f180b2e644e256354fcf1d9c72b834e9b34b994f54e4f66289491fef8f7`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:cbdceda31ee00c7b062c990ec0fde6ff734a6165dabd0f30f0a9e46f8a2bb997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55066625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7cd47da7429fb932128830b734060a66d1f54770ef47cea34d873da4c00c33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3115a6a25b258b9e6ace1b0865be4dfe817364e04295415d9f7ad8891c7510f`  
		Last Modified: Tue, 27 May 2025 15:04:50 GMT  
		Size: 51.3 MB (51254269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd870e16b4065f50d4818a3eca6af18cfa6eb0dea46fa7c17cada837663f7e`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:faa9e0a8c1162ef514b66cd1e71b134fcbbe8a0d253913101ae6fb89938f6cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886aeabd3fa90dcd67373554d829bb0a831a59a49f9398d35fd890adcabf15bc`

```dockerfile
```

-	Layers:
	-	`sha256:0ec7f3ca118232f7217ec7ee6748d5200b961fee4a7411cb303d10a9fa8bbf77`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 838.8 KB (838759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561720d19e2229fdca25d242ad66237315e65bd8ea379e98ef85ac55e6a345d6`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:2ec88e66f394380bb32f77301b4b815951439772b7e0952eccb1b1697b743ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54971569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ca5336c889b89509ed8f18fe24f502d2bdcc6a3a7f7247eaa4ebd7ed221f14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282b95ed82cbc6b46c6b7a1e316612d0d546c3ba7b5bc14c45f4774a7b2f4383`  
		Last Modified: Tue, 27 May 2025 14:51:43 GMT  
		Size: 51.0 MB (51042479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad521e963e06e44e8503bcbd40a4ae5b06971d6ef38534bba2c7b182a10178fc`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:45a983d5c03ffc11478ad3e7ed3efe5c236040aad3ae901397bc8e313fecbb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.2 KB (851245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a3e5232222151bd241ed48416b76c90efea06ceb139558b3e41e189772cbfa`

```dockerfile
```

-	Layers:
	-	`sha256:ec9c14d451d826a78857066f28d415d3aae40af15f49f6ff59771669432f95e0`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 838.7 KB (838707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b64020f713b42ea7e3b8e70e22d16c4399e5816c8bb219d241adb75fed50cca`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:20482a378759deedd7166b16e815327d2bcd992496a6fd8d9619da0a6197b393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:c9c636486ff1dc545be9b180e9d5b9fc0082f67215e6da7a799fb302615059a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176211547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e99f842b929588a924ce2fbf5aff655ad7ff59b30cfb596498e8223f687c16`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:17:58 GMT
RUN cmd /S /C #(nop) COPY file:924b82a6802fb4e8cf126ab6f07a4372c6070c83b784fcb0de9440d142a32bb4 in \ 
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:18:02 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d009a39cfa2ec096f4b9305fb6c88444ba99b07f9f00274d8e7c43eb87885`  
		Last Modified: Tue, 27 May 2025 15:18:12 GMT  
		Size: 53.6 MB (53631658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349971c9ecaeaae66d83dbd41ecb0e9e356bfaf4411d7aa31e935e81b78f476`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47b4c43feba126f6c436b6c0417e0ec7aea01f5fe47138de39bd5c47d3fe30`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be31ab4f88c09d2ebb9fcef11f5dd558c7cce9d42119d5eef5b1fa6715d32402`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:61d9531a333b7a67629c5957fdd3161b7bfa41c973683b63b7fde027580bbaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:2f1a679895bd4307016c14937aee829274dc7df9709a4f1fde49da3c2a586d34
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327756329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15230a7fcee8b248275d9d9271a3a5c0b588befeb73ba8a4e12f6656e17902`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:53:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:53:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:53:41 GMT
EXPOSE 80
# Tue, 27 May 2025 14:53:42 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:53:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf9f26e233b48aef33777758e8142e80d0faf761f8c9352a42a28c0b6c6019f`  
		Last Modified: Tue, 03 Jun 2025 18:50:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b85f1ce181168083824e21da848aed2bfe1c23377c4f835638696681f76671`  
		Last Modified: Tue, 03 Jun 2025 18:50:21 GMT  
		Size: 54.1 MB (54123071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb90aba608fef62a9f38114c8ce945705eb4fa07bf5ed9bf5aac4ec7b4e694fd`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdfd4a5bca5f6de55f055723fc209e78476d296219e4c93d15f15d45801e92b`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5ea15123c3852202f1aff4d7f6878ec3c50b8ac785ecc2a71e638d8ba9810f`  
		Last Modified: Tue, 03 Jun 2025 18:50:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:6b0e06781a8c7ecfc0171b86ef4239567913f025d054f829b93836484c08d4de
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
$ docker pull traefik@sha256:7a3e93790acb9cc76a1671d60edac91f2b44a660c542a129f7b60ec2051f5935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56552512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51ba6b3748820dfa2350e62162dc7b6923bce1d439d7590dfe7b5b06fd7a43d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47353acdc55d84d8eab52dc12ed5a0544a15baeaaf7f841ac086cebb50b82d5f`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 52.4 MB (52449696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:306abeba90dd204cc7e01407add4fff90b5c5a9edf4c8aca9919bd795665ccf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.2 KB (853200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90af661a720bad4fc40519980c3e6448ce6246bde83edb130c438936f7345d8f`

```dockerfile
```

-	Layers:
	-	`sha256:6a24cac55bba047916faf531a3af8614f532036041648fc1eb0745bcfbea3b18`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 840.7 KB (840662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc7f0bf9995aaadc937e4bd1a4035f31cd89dff5ca1ef50562db74686283f15`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9394e41a11e186e65d61d6b214efaf23a6df92f739bed50b27cf7d54b5de99bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52318031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d7b2f69920da843f662e3a66d609b3d54978c34e6a1a3e313f1e51ae77229`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2366ec9e01d41af275db660969c094e2c585439262f2f12cc2a5e5b6ce53464`  
		Last Modified: Tue, 27 May 2025 14:49:39 GMT  
		Size: 48.5 MB (48493507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab654d05db06d563d37378656367863bf7956cfffe339a7f3d02e668dbb4744c`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:cb2ed2f99573807413124377f2dac2912f2fb9efa7a46ffe8fe108f34c519e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c2276f0758ed20a2cdafbd17e771bafe65925182dc94eb10f8d5937905387`

```dockerfile
```

-	Layers:
	-	`sha256:d213ff87ba5e5f2b4267754c42ecd52932a688283e3aae2a395d8ce09530f8c0`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:87d941b6f55eaf4cdb35a94803f120d1c4167ebeaaaa43e6b46c5ac2d0f4e99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52858264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12c6c93b980e31b195991ec6609863b02a4c28a32584413c48d18bc364abe8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3870bcc7664fbf79c85068a58c49eadda5b3d3e83b3a261eb0687c8f382cba`  
		Last Modified: Tue, 03 Jun 2025 13:36:16 GMT  
		Size: 48.4 MB (48402796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955359e8bfcdc4fb80c3199996d51984fb401ed62747abf90d51c961f03ace5`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c55567b804aad0b14a0467ceec3987a7d82ffaefb10fa549f77866f9e0c1b9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.4 KB (853445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb10668fadc74f6751e3b60cbd6f4c38843f45a6a9be6fbb22532ba802de1db`

```dockerfile
```

-	Layers:
	-	`sha256:30c42da66f61218a3020f7f694222b6575250a771d2bcb1b7fdc0e6faeaad8b4`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 840.8 KB (840754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392d505427c83a6e8915f94fb1287d21d09271fc51f8ddb46f01a299c650ec5e`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 12.7 KB (12691 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:ffa941c3a39cf8070066f8e642d043b3bbb93382b65ab191cb4f59a70c6af732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50485530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a848a8c9fbb90595a5bc10de6eb825d5b3eca316940e9f1f8f2f089a9cd7877`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be76b49bda3c8fd09b1fc1bb633224dd0871739cf51c1e96256322e662eb9ecc`  
		Last Modified: Tue, 27 May 2025 14:51:02 GMT  
		Size: 46.4 MB (46448254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729c14791b9df9fc72e478fa8d5c6bc0247b943a8520f7c10212326ae2273676`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:d12369f44494221de3c8b33bade1adfdcbbe7c11ac178c4bec540f4011d4aa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cf941cdda74702c092277fefff62640a0061d956f3961e5ebd1f020c55db3e`

```dockerfile
```

-	Layers:
	-	`sha256:ab995543f597da5ad856301f199da00314c3433240b338a4d72dfd57eda69543`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 838.8 KB (838763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c506f180b2e644e256354fcf1d9c72b834e9b34b994f54e4f66289491fef8f7`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:cbdceda31ee00c7b062c990ec0fde6ff734a6165dabd0f30f0a9e46f8a2bb997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55066625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7cd47da7429fb932128830b734060a66d1f54770ef47cea34d873da4c00c33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3115a6a25b258b9e6ace1b0865be4dfe817364e04295415d9f7ad8891c7510f`  
		Last Modified: Tue, 27 May 2025 15:04:50 GMT  
		Size: 51.3 MB (51254269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd870e16b4065f50d4818a3eca6af18cfa6eb0dea46fa7c17cada837663f7e`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:faa9e0a8c1162ef514b66cd1e71b134fcbbe8a0d253913101ae6fb89938f6cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886aeabd3fa90dcd67373554d829bb0a831a59a49f9398d35fd890adcabf15bc`

```dockerfile
```

-	Layers:
	-	`sha256:0ec7f3ca118232f7217ec7ee6748d5200b961fee4a7411cb303d10a9fa8bbf77`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 838.8 KB (838759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561720d19e2229fdca25d242ad66237315e65bd8ea379e98ef85ac55e6a345d6`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:2ec88e66f394380bb32f77301b4b815951439772b7e0952eccb1b1697b743ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54971569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ca5336c889b89509ed8f18fe24f502d2bdcc6a3a7f7247eaa4ebd7ed221f14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282b95ed82cbc6b46c6b7a1e316612d0d546c3ba7b5bc14c45f4774a7b2f4383`  
		Last Modified: Tue, 27 May 2025 14:51:43 GMT  
		Size: 51.0 MB (51042479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad521e963e06e44e8503bcbd40a4ae5b06971d6ef38534bba2c7b182a10178fc`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:45a983d5c03ffc11478ad3e7ed3efe5c236040aad3ae901397bc8e313fecbb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.2 KB (851245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a3e5232222151bd241ed48416b76c90efea06ceb139558b3e41e189772cbfa`

```dockerfile
```

-	Layers:
	-	`sha256:ec9c14d451d826a78857066f28d415d3aae40af15f49f6ff59771669432f95e0`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 838.7 KB (838707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b64020f713b42ea7e3b8e70e22d16c4399e5816c8bb219d241adb75fed50cca`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:20482a378759deedd7166b16e815327d2bcd992496a6fd8d9619da0a6197b393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:c9c636486ff1dc545be9b180e9d5b9fc0082f67215e6da7a799fb302615059a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176211547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e99f842b929588a924ce2fbf5aff655ad7ff59b30cfb596498e8223f687c16`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:17:58 GMT
RUN cmd /S /C #(nop) COPY file:924b82a6802fb4e8cf126ab6f07a4372c6070c83b784fcb0de9440d142a32bb4 in \ 
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:18:02 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d009a39cfa2ec096f4b9305fb6c88444ba99b07f9f00274d8e7c43eb87885`  
		Last Modified: Tue, 27 May 2025 15:18:12 GMT  
		Size: 53.6 MB (53631658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349971c9ecaeaae66d83dbd41ecb0e9e356bfaf4411d7aa31e935e81b78f476`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47b4c43feba126f6c436b6c0417e0ec7aea01f5fe47138de39bd5c47d3fe30`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be31ab4f88c09d2ebb9fcef11f5dd558c7cce9d42119d5eef5b1fa6715d32402`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:61d9531a333b7a67629c5957fdd3161b7bfa41c973683b63b7fde027580bbaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:2f1a679895bd4307016c14937aee829274dc7df9709a4f1fde49da3c2a586d34
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327756329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15230a7fcee8b248275d9d9271a3a5c0b588befeb73ba8a4e12f6656e17902`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:53:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:53:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:53:41 GMT
EXPOSE 80
# Tue, 27 May 2025 14:53:42 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:53:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf9f26e233b48aef33777758e8142e80d0faf761f8c9352a42a28c0b6c6019f`  
		Last Modified: Tue, 03 Jun 2025 18:50:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b85f1ce181168083824e21da848aed2bfe1c23377c4f835638696681f76671`  
		Last Modified: Tue, 03 Jun 2025 18:50:21 GMT  
		Size: 54.1 MB (54123071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb90aba608fef62a9f38114c8ce945705eb4fa07bf5ed9bf5aac4ec7b4e694fd`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdfd4a5bca5f6de55f055723fc209e78476d296219e4c93d15f15d45801e92b`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5ea15123c3852202f1aff4d7f6878ec3c50b8ac785ecc2a71e638d8ba9810f`  
		Last Modified: Tue, 03 Jun 2025 18:50:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.25`

```console
$ docker pull traefik@sha256:6b0e06781a8c7ecfc0171b86ef4239567913f025d054f829b93836484c08d4de
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

### `traefik:2.11.25` - linux; amd64

```console
$ docker pull traefik@sha256:7a3e93790acb9cc76a1671d60edac91f2b44a660c542a129f7b60ec2051f5935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56552512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51ba6b3748820dfa2350e62162dc7b6923bce1d439d7590dfe7b5b06fd7a43d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47353acdc55d84d8eab52dc12ed5a0544a15baeaaf7f841ac086cebb50b82d5f`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 52.4 MB (52449696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:306abeba90dd204cc7e01407add4fff90b5c5a9edf4c8aca9919bd795665ccf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.2 KB (853200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90af661a720bad4fc40519980c3e6448ce6246bde83edb130c438936f7345d8f`

```dockerfile
```

-	Layers:
	-	`sha256:6a24cac55bba047916faf531a3af8614f532036041648fc1eb0745bcfbea3b18`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 840.7 KB (840662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc7f0bf9995aaadc937e4bd1a4035f31cd89dff5ca1ef50562db74686283f15`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.25` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9394e41a11e186e65d61d6b214efaf23a6df92f739bed50b27cf7d54b5de99bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52318031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d7b2f69920da843f662e3a66d609b3d54978c34e6a1a3e313f1e51ae77229`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2366ec9e01d41af275db660969c094e2c585439262f2f12cc2a5e5b6ce53464`  
		Last Modified: Tue, 27 May 2025 14:49:39 GMT  
		Size: 48.5 MB (48493507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab654d05db06d563d37378656367863bf7956cfffe339a7f3d02e668dbb4744c`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:cb2ed2f99573807413124377f2dac2912f2fb9efa7a46ffe8fe108f34c519e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c2276f0758ed20a2cdafbd17e771bafe65925182dc94eb10f8d5937905387`

```dockerfile
```

-	Layers:
	-	`sha256:d213ff87ba5e5f2b4267754c42ecd52932a688283e3aae2a395d8ce09530f8c0`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.25` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:87d941b6f55eaf4cdb35a94803f120d1c4167ebeaaaa43e6b46c5ac2d0f4e99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52858264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12c6c93b980e31b195991ec6609863b02a4c28a32584413c48d18bc364abe8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3870bcc7664fbf79c85068a58c49eadda5b3d3e83b3a261eb0687c8f382cba`  
		Last Modified: Tue, 03 Jun 2025 13:36:16 GMT  
		Size: 48.4 MB (48402796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955359e8bfcdc4fb80c3199996d51984fb401ed62747abf90d51c961f03ace5`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:c55567b804aad0b14a0467ceec3987a7d82ffaefb10fa549f77866f9e0c1b9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.4 KB (853445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb10668fadc74f6751e3b60cbd6f4c38843f45a6a9be6fbb22532ba802de1db`

```dockerfile
```

-	Layers:
	-	`sha256:30c42da66f61218a3020f7f694222b6575250a771d2bcb1b7fdc0e6faeaad8b4`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 840.8 KB (840754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392d505427c83a6e8915f94fb1287d21d09271fc51f8ddb46f01a299c650ec5e`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 12.7 KB (12691 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.25` - linux; ppc64le

```console
$ docker pull traefik@sha256:ffa941c3a39cf8070066f8e642d043b3bbb93382b65ab191cb4f59a70c6af732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50485530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a848a8c9fbb90595a5bc10de6eb825d5b3eca316940e9f1f8f2f089a9cd7877`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be76b49bda3c8fd09b1fc1bb633224dd0871739cf51c1e96256322e662eb9ecc`  
		Last Modified: Tue, 27 May 2025 14:51:02 GMT  
		Size: 46.4 MB (46448254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729c14791b9df9fc72e478fa8d5c6bc0247b943a8520f7c10212326ae2273676`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:d12369f44494221de3c8b33bade1adfdcbbe7c11ac178c4bec540f4011d4aa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cf941cdda74702c092277fefff62640a0061d956f3961e5ebd1f020c55db3e`

```dockerfile
```

-	Layers:
	-	`sha256:ab995543f597da5ad856301f199da00314c3433240b338a4d72dfd57eda69543`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 838.8 KB (838763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c506f180b2e644e256354fcf1d9c72b834e9b34b994f54e4f66289491fef8f7`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.25` - linux; riscv64

```console
$ docker pull traefik@sha256:cbdceda31ee00c7b062c990ec0fde6ff734a6165dabd0f30f0a9e46f8a2bb997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55066625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7cd47da7429fb932128830b734060a66d1f54770ef47cea34d873da4c00c33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3115a6a25b258b9e6ace1b0865be4dfe817364e04295415d9f7ad8891c7510f`  
		Last Modified: Tue, 27 May 2025 15:04:50 GMT  
		Size: 51.3 MB (51254269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd870e16b4065f50d4818a3eca6af18cfa6eb0dea46fa7c17cada837663f7e`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:faa9e0a8c1162ef514b66cd1e71b134fcbbe8a0d253913101ae6fb89938f6cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886aeabd3fa90dcd67373554d829bb0a831a59a49f9398d35fd890adcabf15bc`

```dockerfile
```

-	Layers:
	-	`sha256:0ec7f3ca118232f7217ec7ee6748d5200b961fee4a7411cb303d10a9fa8bbf77`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 838.8 KB (838759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561720d19e2229fdca25d242ad66237315e65bd8ea379e98ef85ac55e6a345d6`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.25` - linux; s390x

```console
$ docker pull traefik@sha256:2ec88e66f394380bb32f77301b4b815951439772b7e0952eccb1b1697b743ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54971569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ca5336c889b89509ed8f18fe24f502d2bdcc6a3a7f7247eaa4ebd7ed221f14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282b95ed82cbc6b46c6b7a1e316612d0d546c3ba7b5bc14c45f4774a7b2f4383`  
		Last Modified: Tue, 27 May 2025 14:51:43 GMT  
		Size: 51.0 MB (51042479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad521e963e06e44e8503bcbd40a4ae5b06971d6ef38534bba2c7b182a10178fc`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:45a983d5c03ffc11478ad3e7ed3efe5c236040aad3ae901397bc8e313fecbb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.2 KB (851245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a3e5232222151bd241ed48416b76c90efea06ceb139558b3e41e189772cbfa`

```dockerfile
```

-	Layers:
	-	`sha256:ec9c14d451d826a78857066f28d415d3aae40af15f49f6ff59771669432f95e0`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 838.7 KB (838707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b64020f713b42ea7e3b8e70e22d16c4399e5816c8bb219d241adb75fed50cca`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.25-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:20482a378759deedd7166b16e815327d2bcd992496a6fd8d9619da0a6197b393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:2.11.25-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:c9c636486ff1dc545be9b180e9d5b9fc0082f67215e6da7a799fb302615059a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176211547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e99f842b929588a924ce2fbf5aff655ad7ff59b30cfb596498e8223f687c16`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:17:58 GMT
RUN cmd /S /C #(nop) COPY file:924b82a6802fb4e8cf126ab6f07a4372c6070c83b784fcb0de9440d142a32bb4 in \ 
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:18:02 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d009a39cfa2ec096f4b9305fb6c88444ba99b07f9f00274d8e7c43eb87885`  
		Last Modified: Tue, 27 May 2025 15:18:12 GMT  
		Size: 53.6 MB (53631658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349971c9ecaeaae66d83dbd41ecb0e9e356bfaf4411d7aa31e935e81b78f476`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47b4c43feba126f6c436b6c0417e0ec7aea01f5fe47138de39bd5c47d3fe30`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be31ab4f88c09d2ebb9fcef11f5dd558c7cce9d42119d5eef5b1fa6715d32402`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.25-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:61d9531a333b7a67629c5957fdd3161b7bfa41c973683b63b7fde027580bbaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:2.11.25-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:2f1a679895bd4307016c14937aee829274dc7df9709a4f1fde49da3c2a586d34
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327756329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15230a7fcee8b248275d9d9271a3a5c0b588befeb73ba8a4e12f6656e17902`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:53:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:53:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:53:41 GMT
EXPOSE 80
# Tue, 27 May 2025 14:53:42 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:53:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf9f26e233b48aef33777758e8142e80d0faf761f8c9352a42a28c0b6c6019f`  
		Last Modified: Tue, 03 Jun 2025 18:50:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b85f1ce181168083824e21da848aed2bfe1c23377c4f835638696681f76671`  
		Last Modified: Tue, 03 Jun 2025 18:50:21 GMT  
		Size: 54.1 MB (54123071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb90aba608fef62a9f38114c8ce945705eb4fa07bf5ed9bf5aac4ec7b4e694fd`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdfd4a5bca5f6de55f055723fc209e78476d296219e4c93d15f15d45801e92b`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5ea15123c3852202f1aff4d7f6878ec3c50b8ac785ecc2a71e638d8ba9810f`  
		Last Modified: Tue, 03 Jun 2025 18:50:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:cd40ab7bc1f047731d5b22595203812343efcb6538014c4e93221cfc3a77217a
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
$ docker pull traefik@sha256:06b2f92ba6cb9fdc2de99d41c22b862f196871ad55c26269083eaef39dd4fa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58293647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0a241c8a0a140b0d2142f3f481b2fa847a7f42a1356dc39a8eac9b27df4cf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb594ddbc1285eb9bc5e21f89125fbcf7f370d3f7078638c155337257de4ca5`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 54.2 MB (54190831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:bd3775e8dc18f0eaff57543193acf32e1c3747e67e6e71364e6276636ba61f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 KB (840081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65c49c68a9e64602c396234e259172a812df05f95ca284a971af5fcb285cf3d`

```dockerfile
```

-	Layers:
	-	`sha256:cf9c8d147592b2181fc4bd2d7dfdebe237ee30fb30121650d63e2e2a70d609bf`  
		Last Modified: Tue, 03 Jun 2025 15:14:44 GMT  
		Size: 827.3 KB (827272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfa0a085791bfb75f2bde4f6dbcdad91138333a1752fa36ccb2ca805fa44a20`  
		Last Modified: Tue, 03 Jun 2025 15:14:46 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ac48f2ae151717fe49a90e38c92a0a3630f82abdb3e10c8f216b3d2b2e5e18db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53692448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a28e18eb719fd329d0779f8e0da2e3f4a9f569d81ea005a40242d251f3c2a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376947144f2af43212730e00e809e580baa70c1564a7f1c05ce0b5c89a39bfae`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 49.9 MB (49867924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe19f27e5039137d87ded7aa47f3234bf196b95e6a7636f951be0f303fc62b9`  
		Last Modified: Tue, 03 Jun 2025 15:14:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:bde6cb15b218a8146019f1ade9fa1859819d1eb177dc082c3b97c7b0d3445df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75447718047d59fefcc7894e79fc559894fefb231835c5ad7c1f3dd1bf1c79a0`

```dockerfile
```

-	Layers:
	-	`sha256:2514c0d20a1024e7c7d77fb6fa139f6f49f2b85376220c1c74e5ee15fa765ab2`  
		Last Modified: Tue, 03 Jun 2025 15:14:45 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5ed09f5b4d7df3bb186ba5360e7dca8dc73067ecc5278b4a26f60587db908958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7206871bb3451f03c8939c466c0e63a9e69fa944f4aae62b4be7fe3f74725543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30408b989b42117e933e49a16a00bde8712c625b561afa4e231ba172f5a2c8f4`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 50.1 MB (50051133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:ced2a2408769ffb3560fa21b6854287b03e852458a074b5f65df89147a01509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 KB (840352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16424a5a76aa8af2207a2dbecb3a9791c93454915b99af606460d4fd0fcd4f7c`

```dockerfile
```

-	Layers:
	-	`sha256:ea2259fa8cf34c77b492a8fac036ee83b33d37593f00ae9474a90deae0137fdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:47 GMT  
		Size: 827.4 KB (827376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77668edfb6bddc597a120d1abc4d2d3bd49079937ead823127afe0093ee3642e`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 13.0 KB (12976 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:904d00b37a12fd670c6fc8c2e56f5d1cf927d068e75f362e01bfc2ab787a87a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51802197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76af70530829836acad936bfd80b95121bd6e2e670b3dd45485a91e7879f2093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c884f5e61b441d4901cdb9a4f6b55d488910ad927aa3abe32cbb8b4963b6c2b`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 47.8 MB (47764922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:3804f216242a434a58038d23818cff62a773c51847bda7f75b16c226d6f8b384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f4ced2f8947770e3e135a78555b37d42eb37c4354a957ab285e0df1943e837`

```dockerfile
```

-	Layers:
	-	`sha256:2b234a140882f2b7b712d1397de8b3c99819e10801f47893570e9ce96e63b8dc`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 825.4 KB (825379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f87d532e77998b2a01c1ef79f32e030be1542b903fa47b6eac46cb2150dbcb8`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:10503d09555de721b57d72e21c8147b353ae7e55a09e3d0d36409da7b61d79da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56455485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec54b9cdac031e36fb2fbb8d07099b21706b9405d9730b85495c8519e5be09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e436610aeaf1067679abbafd70788026b845bb9421f3b7ce99130207145bdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:59 GMT  
		Size: 52.6 MB (52643130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4a395f47a23ab42cfa059fdf6a35b3a11c21ee95d3d30a868cb8855901fd38`  
		Last Modified: Tue, 03 Jun 2025 15:15:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:5c006f458ac1cd3e4e4932bf5dec8705de18a88005c8e14efd9dcab0f13ba340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe933e0dc2b408ea91505a7d76c47f35f707371115e064c091bbb57e59cbedd`

```dockerfile
```

-	Layers:
	-	`sha256:6063ec4f68a493b6767b158b205cd1ef8193689de05f6363a8955aa456101000`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 825.4 KB (825375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a92db796c6c7cb6425d882b8f55c8abee2389f7409954a5e7ca909c1f9c048`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:07942bc395eb18e2ccdff76a5db6ec430330b4f6e9e21de93abc22d38dd7a6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56269856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ae8c552f603f116570604fac0d866bd7ea998a35a072390398bb2769bbe45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042c8a716a75e292fa5080b404a4f60081032cafe22d09079bf3f891e9ee2b9`  
		Last Modified: Tue, 03 Jun 2025 15:15:00 GMT  
		Size: 52.3 MB (52340765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c51a73e866e22cc50e4088a69f1cad9336fa407fb7a875dff86ce82ea4c6c8b`  
		Last Modified: Tue, 03 Jun 2025 15:15:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:8b7777d29fef01c7e3e582eab03eb0d2f4d619fba29fd92baf84c3ca4cad17f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.1 KB (838130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3bcbcce76b9d2874c369b9d7cfc548d91aa722a5266d5ab4cc461d68129044`

```dockerfile
```

-	Layers:
	-	`sha256:13b584c594ba870e6372ee32d863a9d72a542a1dc4c5178717435d6f79b78e6c`  
		Last Modified: Tue, 03 Jun 2025 15:14:56 GMT  
		Size: 825.3 KB (825321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178dcee5ee28bb14fd9e2d73d78bcc55398b12e68063bfff1bb3f757490c05c4`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e9dfb85bed73e0e8031b9c9a81bb272b8550e8e2e66a0b59ab77970e7095c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:d55b32d19c53ca332f1e0b093a8437b01ba7b841708ffe5c952cf9034c9cd8a4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177905809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ab1def000e52df8a233af9697e9ccbaa4079612aefcc706f08415c78d8e6e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:14:10 GMT
RUN cmd /S /C #(nop) COPY file:9febf6616005a41118af930de9dceb58bbb7c0dfadaddb7bfab3e211ac5bbe26 in \ 
# Tue, 27 May 2025 15:14:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48db22b9277c3bfe0e95c57c3b195f8f1fdd135aacdd2915ef435467e41f961`  
		Last Modified: Tue, 03 Jun 2025 20:17:45 GMT  
		Size: 55.3 MB (55326045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96bdc498b3e64f5942bcf57617b822f6368eae86c524f3d78887cd816ce8667`  
		Last Modified: Tue, 03 Jun 2025 20:17:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25735e6caa059b5973e065e6b9a2f2f6746cbdfbaba54aaadf8703b5b06ee81f`  
		Last Modified: Tue, 03 Jun 2025 20:17:41 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df498a2287fb011505c6829716e35ed011d1d071e7471f2904a6bf81753a5c1a`  
		Last Modified: Tue, 03 Jun 2025 20:17:42 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4cbc0ec3d96e7458f61766b6a7f20184db198cdd5d3e843990d4ffd5d4776f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:6afe066e8b2138da8f232a83e5323bedc06eb2748b3b14bb426fcc0b02a7ab94
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329464370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878537d0f6cf4c3bc01385bf3b93e83db668959f2390c6853b2f6e829e091238`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:54:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:54:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:54:49 GMT
EXPOSE 80
# Tue, 27 May 2025 14:54:50 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:54:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37ab80d65d0f531dd0dda220ec269bb8d3a64ae4733859bf5cceb7cca8083c4`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c9a42230c171b5f3397c7ed80a1f29f0cdea2a1ac9fd6362a379d3fdd0cb7`  
		Last Modified: Tue, 03 Jun 2025 14:12:47 GMT  
		Size: 55.8 MB (55831084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539ecf95a4c553f7630e2dfc0724182acdc077b42454246064b1e81328be8308`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f437896dd6a4e91f5f8d7f28116f518690a54ca59232a2ebe4f5a11fb48f54`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b93db94dc05cad592e9d27e6cf3ec8bb10a35393168f1c7ea7ec866969a171`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.4`

```console
$ docker pull traefik@sha256:cd40ab7bc1f047731d5b22595203812343efcb6538014c4e93221cfc3a77217a
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

### `traefik:3.4` - linux; amd64

```console
$ docker pull traefik@sha256:06b2f92ba6cb9fdc2de99d41c22b862f196871ad55c26269083eaef39dd4fa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58293647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0a241c8a0a140b0d2142f3f481b2fa847a7f42a1356dc39a8eac9b27df4cf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb594ddbc1285eb9bc5e21f89125fbcf7f370d3f7078638c155337257de4ca5`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 54.2 MB (54190831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:bd3775e8dc18f0eaff57543193acf32e1c3747e67e6e71364e6276636ba61f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 KB (840081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65c49c68a9e64602c396234e259172a812df05f95ca284a971af5fcb285cf3d`

```dockerfile
```

-	Layers:
	-	`sha256:cf9c8d147592b2181fc4bd2d7dfdebe237ee30fb30121650d63e2e2a70d609bf`  
		Last Modified: Tue, 03 Jun 2025 15:14:44 GMT  
		Size: 827.3 KB (827272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfa0a085791bfb75f2bde4f6dbcdad91138333a1752fa36ccb2ca805fa44a20`  
		Last Modified: Tue, 03 Jun 2025 15:14:46 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ac48f2ae151717fe49a90e38c92a0a3630f82abdb3e10c8f216b3d2b2e5e18db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53692448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a28e18eb719fd329d0779f8e0da2e3f4a9f569d81ea005a40242d251f3c2a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376947144f2af43212730e00e809e580baa70c1564a7f1c05ce0b5c89a39bfae`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 49.9 MB (49867924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe19f27e5039137d87ded7aa47f3234bf196b95e6a7636f951be0f303fc62b9`  
		Last Modified: Tue, 03 Jun 2025 15:14:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:bde6cb15b218a8146019f1ade9fa1859819d1eb177dc082c3b97c7b0d3445df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75447718047d59fefcc7894e79fc559894fefb231835c5ad7c1f3dd1bf1c79a0`

```dockerfile
```

-	Layers:
	-	`sha256:2514c0d20a1024e7c7d77fb6fa139f6f49f2b85376220c1c74e5ee15fa765ab2`  
		Last Modified: Tue, 03 Jun 2025 15:14:45 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5ed09f5b4d7df3bb186ba5360e7dca8dc73067ecc5278b4a26f60587db908958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7206871bb3451f03c8939c466c0e63a9e69fa944f4aae62b4be7fe3f74725543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30408b989b42117e933e49a16a00bde8712c625b561afa4e231ba172f5a2c8f4`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 50.1 MB (50051133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:ced2a2408769ffb3560fa21b6854287b03e852458a074b5f65df89147a01509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 KB (840352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16424a5a76aa8af2207a2dbecb3a9791c93454915b99af606460d4fd0fcd4f7c`

```dockerfile
```

-	Layers:
	-	`sha256:ea2259fa8cf34c77b492a8fac036ee83b33d37593f00ae9474a90deae0137fdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:47 GMT  
		Size: 827.4 KB (827376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77668edfb6bddc597a120d1abc4d2d3bd49079937ead823127afe0093ee3642e`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 13.0 KB (12976 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.4` - linux; ppc64le

```console
$ docker pull traefik@sha256:904d00b37a12fd670c6fc8c2e56f5d1cf927d068e75f362e01bfc2ab787a87a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51802197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76af70530829836acad936bfd80b95121bd6e2e670b3dd45485a91e7879f2093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c884f5e61b441d4901cdb9a4f6b55d488910ad927aa3abe32cbb8b4963b6c2b`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 47.8 MB (47764922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:3804f216242a434a58038d23818cff62a773c51847bda7f75b16c226d6f8b384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f4ced2f8947770e3e135a78555b37d42eb37c4354a957ab285e0df1943e837`

```dockerfile
```

-	Layers:
	-	`sha256:2b234a140882f2b7b712d1397de8b3c99819e10801f47893570e9ce96e63b8dc`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 825.4 KB (825379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f87d532e77998b2a01c1ef79f32e030be1542b903fa47b6eac46cb2150dbcb8`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.4` - linux; riscv64

```console
$ docker pull traefik@sha256:10503d09555de721b57d72e21c8147b353ae7e55a09e3d0d36409da7b61d79da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56455485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec54b9cdac031e36fb2fbb8d07099b21706b9405d9730b85495c8519e5be09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e436610aeaf1067679abbafd70788026b845bb9421f3b7ce99130207145bdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:59 GMT  
		Size: 52.6 MB (52643130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4a395f47a23ab42cfa059fdf6a35b3a11c21ee95d3d30a868cb8855901fd38`  
		Last Modified: Tue, 03 Jun 2025 15:15:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:5c006f458ac1cd3e4e4932bf5dec8705de18a88005c8e14efd9dcab0f13ba340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe933e0dc2b408ea91505a7d76c47f35f707371115e064c091bbb57e59cbedd`

```dockerfile
```

-	Layers:
	-	`sha256:6063ec4f68a493b6767b158b205cd1ef8193689de05f6363a8955aa456101000`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 825.4 KB (825375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a92db796c6c7cb6425d882b8f55c8abee2389f7409954a5e7ca909c1f9c048`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.4` - linux; s390x

```console
$ docker pull traefik@sha256:07942bc395eb18e2ccdff76a5db6ec430330b4f6e9e21de93abc22d38dd7a6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56269856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ae8c552f603f116570604fac0d866bd7ea998a35a072390398bb2769bbe45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042c8a716a75e292fa5080b404a4f60081032cafe22d09079bf3f891e9ee2b9`  
		Last Modified: Tue, 03 Jun 2025 15:15:00 GMT  
		Size: 52.3 MB (52340765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c51a73e866e22cc50e4088a69f1cad9336fa407fb7a875dff86ce82ea4c6c8b`  
		Last Modified: Tue, 03 Jun 2025 15:15:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:8b7777d29fef01c7e3e582eab03eb0d2f4d619fba29fd92baf84c3ca4cad17f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.1 KB (838130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3bcbcce76b9d2874c369b9d7cfc548d91aa722a5266d5ab4cc461d68129044`

```dockerfile
```

-	Layers:
	-	`sha256:13b584c594ba870e6372ee32d863a9d72a542a1dc4c5178717435d6f79b78e6c`  
		Last Modified: Tue, 03 Jun 2025 15:14:56 GMT  
		Size: 825.3 KB (825321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178dcee5ee28bb14fd9e2d73d78bcc55398b12e68063bfff1bb3f757490c05c4`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.4-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e9dfb85bed73e0e8031b9c9a81bb272b8550e8e2e66a0b59ab77970e7095c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:3.4-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:d55b32d19c53ca332f1e0b093a8437b01ba7b841708ffe5c952cf9034c9cd8a4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177905809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ab1def000e52df8a233af9697e9ccbaa4079612aefcc706f08415c78d8e6e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:14:10 GMT
RUN cmd /S /C #(nop) COPY file:9febf6616005a41118af930de9dceb58bbb7c0dfadaddb7bfab3e211ac5bbe26 in \ 
# Tue, 27 May 2025 15:14:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48db22b9277c3bfe0e95c57c3b195f8f1fdd135aacdd2915ef435467e41f961`  
		Last Modified: Tue, 03 Jun 2025 20:17:45 GMT  
		Size: 55.3 MB (55326045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96bdc498b3e64f5942bcf57617b822f6368eae86c524f3d78887cd816ce8667`  
		Last Modified: Tue, 03 Jun 2025 20:17:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25735e6caa059b5973e065e6b9a2f2f6746cbdfbaba54aaadf8703b5b06ee81f`  
		Last Modified: Tue, 03 Jun 2025 20:17:41 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df498a2287fb011505c6829716e35ed011d1d071e7471f2904a6bf81753a5c1a`  
		Last Modified: Tue, 03 Jun 2025 20:17:42 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.4-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4cbc0ec3d96e7458f61766b6a7f20184db198cdd5d3e843990d4ffd5d4776f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:3.4-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:6afe066e8b2138da8f232a83e5323bedc06eb2748b3b14bb426fcc0b02a7ab94
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329464370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878537d0f6cf4c3bc01385bf3b93e83db668959f2390c6853b2f6e829e091238`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:54:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:54:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:54:49 GMT
EXPOSE 80
# Tue, 27 May 2025 14:54:50 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:54:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37ab80d65d0f531dd0dda220ec269bb8d3a64ae4733859bf5cceb7cca8083c4`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c9a42230c171b5f3397c7ed80a1f29f0cdea2a1ac9fd6362a379d3fdd0cb7`  
		Last Modified: Tue, 03 Jun 2025 14:12:47 GMT  
		Size: 55.8 MB (55831084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539ecf95a4c553f7630e2dfc0724182acdc077b42454246064b1e81328be8308`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f437896dd6a4e91f5f8d7f28116f518690a54ca59232a2ebe4f5a11fb48f54`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b93db94dc05cad592e9d27e6cf3ec8bb10a35393168f1c7ea7ec866969a171`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.4.1`

```console
$ docker pull traefik@sha256:cd40ab7bc1f047731d5b22595203812343efcb6538014c4e93221cfc3a77217a
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

### `traefik:3.4.1` - linux; amd64

```console
$ docker pull traefik@sha256:06b2f92ba6cb9fdc2de99d41c22b862f196871ad55c26269083eaef39dd4fa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58293647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0a241c8a0a140b0d2142f3f481b2fa847a7f42a1356dc39a8eac9b27df4cf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb594ddbc1285eb9bc5e21f89125fbcf7f370d3f7078638c155337257de4ca5`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 54.2 MB (54190831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:bd3775e8dc18f0eaff57543193acf32e1c3747e67e6e71364e6276636ba61f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 KB (840081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65c49c68a9e64602c396234e259172a812df05f95ca284a971af5fcb285cf3d`

```dockerfile
```

-	Layers:
	-	`sha256:cf9c8d147592b2181fc4bd2d7dfdebe237ee30fb30121650d63e2e2a70d609bf`  
		Last Modified: Tue, 03 Jun 2025 15:14:44 GMT  
		Size: 827.3 KB (827272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfa0a085791bfb75f2bde4f6dbcdad91138333a1752fa36ccb2ca805fa44a20`  
		Last Modified: Tue, 03 Jun 2025 15:14:46 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.4.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ac48f2ae151717fe49a90e38c92a0a3630f82abdb3e10c8f216b3d2b2e5e18db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53692448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a28e18eb719fd329d0779f8e0da2e3f4a9f569d81ea005a40242d251f3c2a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376947144f2af43212730e00e809e580baa70c1564a7f1c05ce0b5c89a39bfae`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 49.9 MB (49867924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe19f27e5039137d87ded7aa47f3234bf196b95e6a7636f951be0f303fc62b9`  
		Last Modified: Tue, 03 Jun 2025 15:14:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:bde6cb15b218a8146019f1ade9fa1859819d1eb177dc082c3b97c7b0d3445df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75447718047d59fefcc7894e79fc559894fefb231835c5ad7c1f3dd1bf1c79a0`

```dockerfile
```

-	Layers:
	-	`sha256:2514c0d20a1024e7c7d77fb6fa139f6f49f2b85376220c1c74e5ee15fa765ab2`  
		Last Modified: Tue, 03 Jun 2025 15:14:45 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.4.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5ed09f5b4d7df3bb186ba5360e7dca8dc73067ecc5278b4a26f60587db908958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7206871bb3451f03c8939c466c0e63a9e69fa944f4aae62b4be7fe3f74725543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30408b989b42117e933e49a16a00bde8712c625b561afa4e231ba172f5a2c8f4`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 50.1 MB (50051133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:ced2a2408769ffb3560fa21b6854287b03e852458a074b5f65df89147a01509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 KB (840352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16424a5a76aa8af2207a2dbecb3a9791c93454915b99af606460d4fd0fcd4f7c`

```dockerfile
```

-	Layers:
	-	`sha256:ea2259fa8cf34c77b492a8fac036ee83b33d37593f00ae9474a90deae0137fdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:47 GMT  
		Size: 827.4 KB (827376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77668edfb6bddc597a120d1abc4d2d3bd49079937ead823127afe0093ee3642e`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 13.0 KB (12976 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.4.1` - linux; ppc64le

```console
$ docker pull traefik@sha256:904d00b37a12fd670c6fc8c2e56f5d1cf927d068e75f362e01bfc2ab787a87a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51802197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76af70530829836acad936bfd80b95121bd6e2e670b3dd45485a91e7879f2093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c884f5e61b441d4901cdb9a4f6b55d488910ad927aa3abe32cbb8b4963b6c2b`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 47.8 MB (47764922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:3804f216242a434a58038d23818cff62a773c51847bda7f75b16c226d6f8b384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f4ced2f8947770e3e135a78555b37d42eb37c4354a957ab285e0df1943e837`

```dockerfile
```

-	Layers:
	-	`sha256:2b234a140882f2b7b712d1397de8b3c99819e10801f47893570e9ce96e63b8dc`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 825.4 KB (825379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f87d532e77998b2a01c1ef79f32e030be1542b903fa47b6eac46cb2150dbcb8`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.4.1` - linux; riscv64

```console
$ docker pull traefik@sha256:10503d09555de721b57d72e21c8147b353ae7e55a09e3d0d36409da7b61d79da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56455485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec54b9cdac031e36fb2fbb8d07099b21706b9405d9730b85495c8519e5be09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e436610aeaf1067679abbafd70788026b845bb9421f3b7ce99130207145bdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:59 GMT  
		Size: 52.6 MB (52643130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4a395f47a23ab42cfa059fdf6a35b3a11c21ee95d3d30a868cb8855901fd38`  
		Last Modified: Tue, 03 Jun 2025 15:15:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:5c006f458ac1cd3e4e4932bf5dec8705de18a88005c8e14efd9dcab0f13ba340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe933e0dc2b408ea91505a7d76c47f35f707371115e064c091bbb57e59cbedd`

```dockerfile
```

-	Layers:
	-	`sha256:6063ec4f68a493b6767b158b205cd1ef8193689de05f6363a8955aa456101000`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 825.4 KB (825375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a92db796c6c7cb6425d882b8f55c8abee2389f7409954a5e7ca909c1f9c048`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.4.1` - linux; s390x

```console
$ docker pull traefik@sha256:07942bc395eb18e2ccdff76a5db6ec430330b4f6e9e21de93abc22d38dd7a6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56269856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ae8c552f603f116570604fac0d866bd7ea998a35a072390398bb2769bbe45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042c8a716a75e292fa5080b404a4f60081032cafe22d09079bf3f891e9ee2b9`  
		Last Modified: Tue, 03 Jun 2025 15:15:00 GMT  
		Size: 52.3 MB (52340765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c51a73e866e22cc50e4088a69f1cad9336fa407fb7a875dff86ce82ea4c6c8b`  
		Last Modified: Tue, 03 Jun 2025 15:15:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:8b7777d29fef01c7e3e582eab03eb0d2f4d619fba29fd92baf84c3ca4cad17f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.1 KB (838130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3bcbcce76b9d2874c369b9d7cfc548d91aa722a5266d5ab4cc461d68129044`

```dockerfile
```

-	Layers:
	-	`sha256:13b584c594ba870e6372ee32d863a9d72a542a1dc4c5178717435d6f79b78e6c`  
		Last Modified: Tue, 03 Jun 2025 15:14:56 GMT  
		Size: 825.3 KB (825321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178dcee5ee28bb14fd9e2d73d78bcc55398b12e68063bfff1bb3f757490c05c4`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.4.1-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e9dfb85bed73e0e8031b9c9a81bb272b8550e8e2e66a0b59ab77970e7095c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:3.4.1-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:d55b32d19c53ca332f1e0b093a8437b01ba7b841708ffe5c952cf9034c9cd8a4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177905809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ab1def000e52df8a233af9697e9ccbaa4079612aefcc706f08415c78d8e6e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:14:10 GMT
RUN cmd /S /C #(nop) COPY file:9febf6616005a41118af930de9dceb58bbb7c0dfadaddb7bfab3e211ac5bbe26 in \ 
# Tue, 27 May 2025 15:14:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48db22b9277c3bfe0e95c57c3b195f8f1fdd135aacdd2915ef435467e41f961`  
		Last Modified: Tue, 03 Jun 2025 20:17:45 GMT  
		Size: 55.3 MB (55326045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96bdc498b3e64f5942bcf57617b822f6368eae86c524f3d78887cd816ce8667`  
		Last Modified: Tue, 03 Jun 2025 20:17:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25735e6caa059b5973e065e6b9a2f2f6746cbdfbaba54aaadf8703b5b06ee81f`  
		Last Modified: Tue, 03 Jun 2025 20:17:41 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df498a2287fb011505c6829716e35ed011d1d071e7471f2904a6bf81753a5c1a`  
		Last Modified: Tue, 03 Jun 2025 20:17:42 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.4.1-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4cbc0ec3d96e7458f61766b6a7f20184db198cdd5d3e843990d4ffd5d4776f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:3.4.1-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:6afe066e8b2138da8f232a83e5323bedc06eb2748b3b14bb426fcc0b02a7ab94
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329464370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878537d0f6cf4c3bc01385bf3b93e83db668959f2390c6853b2f6e829e091238`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:54:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:54:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:54:49 GMT
EXPOSE 80
# Tue, 27 May 2025 14:54:50 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:54:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37ab80d65d0f531dd0dda220ec269bb8d3a64ae4733859bf5cceb7cca8083c4`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c9a42230c171b5f3397c7ed80a1f29f0cdea2a1ac9fd6362a379d3fdd0cb7`  
		Last Modified: Tue, 03 Jun 2025 14:12:47 GMT  
		Size: 55.8 MB (55831084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539ecf95a4c553f7630e2dfc0724182acdc077b42454246064b1e81328be8308`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f437896dd6a4e91f5f8d7f28116f518690a54ca59232a2ebe4f5a11fb48f54`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b93db94dc05cad592e9d27e6cf3ec8bb10a35393168f1c7ea7ec866969a171`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chaource`

```console
$ docker pull traefik@sha256:cd40ab7bc1f047731d5b22595203812343efcb6538014c4e93221cfc3a77217a
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

### `traefik:chaource` - linux; amd64

```console
$ docker pull traefik@sha256:06b2f92ba6cb9fdc2de99d41c22b862f196871ad55c26269083eaef39dd4fa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58293647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0a241c8a0a140b0d2142f3f481b2fa847a7f42a1356dc39a8eac9b27df4cf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb594ddbc1285eb9bc5e21f89125fbcf7f370d3f7078638c155337257de4ca5`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 54.2 MB (54190831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:bd3775e8dc18f0eaff57543193acf32e1c3747e67e6e71364e6276636ba61f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 KB (840081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65c49c68a9e64602c396234e259172a812df05f95ca284a971af5fcb285cf3d`

```dockerfile
```

-	Layers:
	-	`sha256:cf9c8d147592b2181fc4bd2d7dfdebe237ee30fb30121650d63e2e2a70d609bf`  
		Last Modified: Tue, 03 Jun 2025 15:14:44 GMT  
		Size: 827.3 KB (827272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfa0a085791bfb75f2bde4f6dbcdad91138333a1752fa36ccb2ca805fa44a20`  
		Last Modified: Tue, 03 Jun 2025 15:14:46 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chaource` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ac48f2ae151717fe49a90e38c92a0a3630f82abdb3e10c8f216b3d2b2e5e18db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53692448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a28e18eb719fd329d0779f8e0da2e3f4a9f569d81ea005a40242d251f3c2a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376947144f2af43212730e00e809e580baa70c1564a7f1c05ce0b5c89a39bfae`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 49.9 MB (49867924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe19f27e5039137d87ded7aa47f3234bf196b95e6a7636f951be0f303fc62b9`  
		Last Modified: Tue, 03 Jun 2025 15:14:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:bde6cb15b218a8146019f1ade9fa1859819d1eb177dc082c3b97c7b0d3445df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75447718047d59fefcc7894e79fc559894fefb231835c5ad7c1f3dd1bf1c79a0`

```dockerfile
```

-	Layers:
	-	`sha256:2514c0d20a1024e7c7d77fb6fa139f6f49f2b85376220c1c74e5ee15fa765ab2`  
		Last Modified: Tue, 03 Jun 2025 15:14:45 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chaource` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5ed09f5b4d7df3bb186ba5360e7dca8dc73067ecc5278b4a26f60587db908958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7206871bb3451f03c8939c466c0e63a9e69fa944f4aae62b4be7fe3f74725543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30408b989b42117e933e49a16a00bde8712c625b561afa4e231ba172f5a2c8f4`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 50.1 MB (50051133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:ced2a2408769ffb3560fa21b6854287b03e852458a074b5f65df89147a01509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 KB (840352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16424a5a76aa8af2207a2dbecb3a9791c93454915b99af606460d4fd0fcd4f7c`

```dockerfile
```

-	Layers:
	-	`sha256:ea2259fa8cf34c77b492a8fac036ee83b33d37593f00ae9474a90deae0137fdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:47 GMT  
		Size: 827.4 KB (827376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77668edfb6bddc597a120d1abc4d2d3bd49079937ead823127afe0093ee3642e`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 13.0 KB (12976 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chaource` - linux; ppc64le

```console
$ docker pull traefik@sha256:904d00b37a12fd670c6fc8c2e56f5d1cf927d068e75f362e01bfc2ab787a87a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51802197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76af70530829836acad936bfd80b95121bd6e2e670b3dd45485a91e7879f2093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c884f5e61b441d4901cdb9a4f6b55d488910ad927aa3abe32cbb8b4963b6c2b`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 47.8 MB (47764922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:3804f216242a434a58038d23818cff62a773c51847bda7f75b16c226d6f8b384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f4ced2f8947770e3e135a78555b37d42eb37c4354a957ab285e0df1943e837`

```dockerfile
```

-	Layers:
	-	`sha256:2b234a140882f2b7b712d1397de8b3c99819e10801f47893570e9ce96e63b8dc`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 825.4 KB (825379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f87d532e77998b2a01c1ef79f32e030be1542b903fa47b6eac46cb2150dbcb8`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chaource` - linux; riscv64

```console
$ docker pull traefik@sha256:10503d09555de721b57d72e21c8147b353ae7e55a09e3d0d36409da7b61d79da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56455485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec54b9cdac031e36fb2fbb8d07099b21706b9405d9730b85495c8519e5be09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e436610aeaf1067679abbafd70788026b845bb9421f3b7ce99130207145bdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:59 GMT  
		Size: 52.6 MB (52643130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4a395f47a23ab42cfa059fdf6a35b3a11c21ee95d3d30a868cb8855901fd38`  
		Last Modified: Tue, 03 Jun 2025 15:15:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:5c006f458ac1cd3e4e4932bf5dec8705de18a88005c8e14efd9dcab0f13ba340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe933e0dc2b408ea91505a7d76c47f35f707371115e064c091bbb57e59cbedd`

```dockerfile
```

-	Layers:
	-	`sha256:6063ec4f68a493b6767b158b205cd1ef8193689de05f6363a8955aa456101000`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 825.4 KB (825375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a92db796c6c7cb6425d882b8f55c8abee2389f7409954a5e7ca909c1f9c048`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chaource` - linux; s390x

```console
$ docker pull traefik@sha256:07942bc395eb18e2ccdff76a5db6ec430330b4f6e9e21de93abc22d38dd7a6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56269856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ae8c552f603f116570604fac0d866bd7ea998a35a072390398bb2769bbe45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042c8a716a75e292fa5080b404a4f60081032cafe22d09079bf3f891e9ee2b9`  
		Last Modified: Tue, 03 Jun 2025 15:15:00 GMT  
		Size: 52.3 MB (52340765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c51a73e866e22cc50e4088a69f1cad9336fa407fb7a875dff86ce82ea4c6c8b`  
		Last Modified: Tue, 03 Jun 2025 15:15:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:8b7777d29fef01c7e3e582eab03eb0d2f4d619fba29fd92baf84c3ca4cad17f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.1 KB (838130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3bcbcce76b9d2874c369b9d7cfc548d91aa722a5266d5ab4cc461d68129044`

```dockerfile
```

-	Layers:
	-	`sha256:13b584c594ba870e6372ee32d863a9d72a542a1dc4c5178717435d6f79b78e6c`  
		Last Modified: Tue, 03 Jun 2025 15:14:56 GMT  
		Size: 825.3 KB (825321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178dcee5ee28bb14fd9e2d73d78bcc55398b12e68063bfff1bb3f757490c05c4`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:chaource-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e9dfb85bed73e0e8031b9c9a81bb272b8550e8e2e66a0b59ab77970e7095c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:chaource-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:d55b32d19c53ca332f1e0b093a8437b01ba7b841708ffe5c952cf9034c9cd8a4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177905809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ab1def000e52df8a233af9697e9ccbaa4079612aefcc706f08415c78d8e6e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:14:10 GMT
RUN cmd /S /C #(nop) COPY file:9febf6616005a41118af930de9dceb58bbb7c0dfadaddb7bfab3e211ac5bbe26 in \ 
# Tue, 27 May 2025 15:14:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48db22b9277c3bfe0e95c57c3b195f8f1fdd135aacdd2915ef435467e41f961`  
		Last Modified: Tue, 03 Jun 2025 20:17:45 GMT  
		Size: 55.3 MB (55326045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96bdc498b3e64f5942bcf57617b822f6368eae86c524f3d78887cd816ce8667`  
		Last Modified: Tue, 03 Jun 2025 20:17:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25735e6caa059b5973e065e6b9a2f2f6746cbdfbaba54aaadf8703b5b06ee81f`  
		Last Modified: Tue, 03 Jun 2025 20:17:41 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df498a2287fb011505c6829716e35ed011d1d071e7471f2904a6bf81753a5c1a`  
		Last Modified: Tue, 03 Jun 2025 20:17:42 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chaource-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4cbc0ec3d96e7458f61766b6a7f20184db198cdd5d3e843990d4ffd5d4776f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:chaource-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:6afe066e8b2138da8f232a83e5323bedc06eb2748b3b14bb426fcc0b02a7ab94
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329464370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878537d0f6cf4c3bc01385bf3b93e83db668959f2390c6853b2f6e829e091238`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:54:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:54:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:54:49 GMT
EXPOSE 80
# Tue, 27 May 2025 14:54:50 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:54:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37ab80d65d0f531dd0dda220ec269bb8d3a64ae4733859bf5cceb7cca8083c4`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c9a42230c171b5f3397c7ed80a1f29f0cdea2a1ac9fd6362a379d3fdd0cb7`  
		Last Modified: Tue, 03 Jun 2025 14:12:47 GMT  
		Size: 55.8 MB (55831084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539ecf95a4c553f7630e2dfc0724182acdc077b42454246064b1e81328be8308`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f437896dd6a4e91f5f8d7f28116f518690a54ca59232a2ebe4f5a11fb48f54`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b93db94dc05cad592e9d27e6cf3ec8bb10a35393168f1c7ea7ec866969a171`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:cd40ab7bc1f047731d5b22595203812343efcb6538014c4e93221cfc3a77217a
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
$ docker pull traefik@sha256:06b2f92ba6cb9fdc2de99d41c22b862f196871ad55c26269083eaef39dd4fa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58293647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0a241c8a0a140b0d2142f3f481b2fa847a7f42a1356dc39a8eac9b27df4cf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb594ddbc1285eb9bc5e21f89125fbcf7f370d3f7078638c155337257de4ca5`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 54.2 MB (54190831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:bd3775e8dc18f0eaff57543193acf32e1c3747e67e6e71364e6276636ba61f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 KB (840081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65c49c68a9e64602c396234e259172a812df05f95ca284a971af5fcb285cf3d`

```dockerfile
```

-	Layers:
	-	`sha256:cf9c8d147592b2181fc4bd2d7dfdebe237ee30fb30121650d63e2e2a70d609bf`  
		Last Modified: Tue, 03 Jun 2025 15:14:44 GMT  
		Size: 827.3 KB (827272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfa0a085791bfb75f2bde4f6dbcdad91138333a1752fa36ccb2ca805fa44a20`  
		Last Modified: Tue, 03 Jun 2025 15:14:46 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ac48f2ae151717fe49a90e38c92a0a3630f82abdb3e10c8f216b3d2b2e5e18db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53692448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a28e18eb719fd329d0779f8e0da2e3f4a9f569d81ea005a40242d251f3c2a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376947144f2af43212730e00e809e580baa70c1564a7f1c05ce0b5c89a39bfae`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 49.9 MB (49867924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe19f27e5039137d87ded7aa47f3234bf196b95e6a7636f951be0f303fc62b9`  
		Last Modified: Tue, 03 Jun 2025 15:14:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:bde6cb15b218a8146019f1ade9fa1859819d1eb177dc082c3b97c7b0d3445df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75447718047d59fefcc7894e79fc559894fefb231835c5ad7c1f3dd1bf1c79a0`

```dockerfile
```

-	Layers:
	-	`sha256:2514c0d20a1024e7c7d77fb6fa139f6f49f2b85376220c1c74e5ee15fa765ab2`  
		Last Modified: Tue, 03 Jun 2025 15:14:45 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5ed09f5b4d7df3bb186ba5360e7dca8dc73067ecc5278b4a26f60587db908958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7206871bb3451f03c8939c466c0e63a9e69fa944f4aae62b4be7fe3f74725543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30408b989b42117e933e49a16a00bde8712c625b561afa4e231ba172f5a2c8f4`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 50.1 MB (50051133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:ced2a2408769ffb3560fa21b6854287b03e852458a074b5f65df89147a01509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 KB (840352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16424a5a76aa8af2207a2dbecb3a9791c93454915b99af606460d4fd0fcd4f7c`

```dockerfile
```

-	Layers:
	-	`sha256:ea2259fa8cf34c77b492a8fac036ee83b33d37593f00ae9474a90deae0137fdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:47 GMT  
		Size: 827.4 KB (827376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77668edfb6bddc597a120d1abc4d2d3bd49079937ead823127afe0093ee3642e`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 13.0 KB (12976 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:904d00b37a12fd670c6fc8c2e56f5d1cf927d068e75f362e01bfc2ab787a87a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51802197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76af70530829836acad936bfd80b95121bd6e2e670b3dd45485a91e7879f2093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c884f5e61b441d4901cdb9a4f6b55d488910ad927aa3abe32cbb8b4963b6c2b`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 47.8 MB (47764922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:3804f216242a434a58038d23818cff62a773c51847bda7f75b16c226d6f8b384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f4ced2f8947770e3e135a78555b37d42eb37c4354a957ab285e0df1943e837`

```dockerfile
```

-	Layers:
	-	`sha256:2b234a140882f2b7b712d1397de8b3c99819e10801f47893570e9ce96e63b8dc`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 825.4 KB (825379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f87d532e77998b2a01c1ef79f32e030be1542b903fa47b6eac46cb2150dbcb8`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:10503d09555de721b57d72e21c8147b353ae7e55a09e3d0d36409da7b61d79da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56455485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec54b9cdac031e36fb2fbb8d07099b21706b9405d9730b85495c8519e5be09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e436610aeaf1067679abbafd70788026b845bb9421f3b7ce99130207145bdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:59 GMT  
		Size: 52.6 MB (52643130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4a395f47a23ab42cfa059fdf6a35b3a11c21ee95d3d30a868cb8855901fd38`  
		Last Modified: Tue, 03 Jun 2025 15:15:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:5c006f458ac1cd3e4e4932bf5dec8705de18a88005c8e14efd9dcab0f13ba340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe933e0dc2b408ea91505a7d76c47f35f707371115e064c091bbb57e59cbedd`

```dockerfile
```

-	Layers:
	-	`sha256:6063ec4f68a493b6767b158b205cd1ef8193689de05f6363a8955aa456101000`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 825.4 KB (825375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a92db796c6c7cb6425d882b8f55c8abee2389f7409954a5e7ca909c1f9c048`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:07942bc395eb18e2ccdff76a5db6ec430330b4f6e9e21de93abc22d38dd7a6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56269856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ae8c552f603f116570604fac0d866bd7ea998a35a072390398bb2769bbe45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042c8a716a75e292fa5080b404a4f60081032cafe22d09079bf3f891e9ee2b9`  
		Last Modified: Tue, 03 Jun 2025 15:15:00 GMT  
		Size: 52.3 MB (52340765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c51a73e866e22cc50e4088a69f1cad9336fa407fb7a875dff86ce82ea4c6c8b`  
		Last Modified: Tue, 03 Jun 2025 15:15:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:8b7777d29fef01c7e3e582eab03eb0d2f4d619fba29fd92baf84c3ca4cad17f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.1 KB (838130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3bcbcce76b9d2874c369b9d7cfc548d91aa722a5266d5ab4cc461d68129044`

```dockerfile
```

-	Layers:
	-	`sha256:13b584c594ba870e6372ee32d863a9d72a542a1dc4c5178717435d6f79b78e6c`  
		Last Modified: Tue, 03 Jun 2025 15:14:56 GMT  
		Size: 825.3 KB (825321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178dcee5ee28bb14fd9e2d73d78bcc55398b12e68063bfff1bb3f757490c05c4`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:6b0e06781a8c7ecfc0171b86ef4239567913f025d054f829b93836484c08d4de
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
$ docker pull traefik@sha256:7a3e93790acb9cc76a1671d60edac91f2b44a660c542a129f7b60ec2051f5935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56552512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51ba6b3748820dfa2350e62162dc7b6923bce1d439d7590dfe7b5b06fd7a43d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47353acdc55d84d8eab52dc12ed5a0544a15baeaaf7f841ac086cebb50b82d5f`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 52.4 MB (52449696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:306abeba90dd204cc7e01407add4fff90b5c5a9edf4c8aca9919bd795665ccf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.2 KB (853200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90af661a720bad4fc40519980c3e6448ce6246bde83edb130c438936f7345d8f`

```dockerfile
```

-	Layers:
	-	`sha256:6a24cac55bba047916faf531a3af8614f532036041648fc1eb0745bcfbea3b18`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 840.7 KB (840662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc7f0bf9995aaadc937e4bd1a4035f31cd89dff5ca1ef50562db74686283f15`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9394e41a11e186e65d61d6b214efaf23a6df92f739bed50b27cf7d54b5de99bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52318031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d7b2f69920da843f662e3a66d609b3d54978c34e6a1a3e313f1e51ae77229`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2366ec9e01d41af275db660969c094e2c585439262f2f12cc2a5e5b6ce53464`  
		Last Modified: Tue, 27 May 2025 14:49:39 GMT  
		Size: 48.5 MB (48493507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab654d05db06d563d37378656367863bf7956cfffe339a7f3d02e668dbb4744c`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:cb2ed2f99573807413124377f2dac2912f2fb9efa7a46ffe8fe108f34c519e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c2276f0758ed20a2cdafbd17e771bafe65925182dc94eb10f8d5937905387`

```dockerfile
```

-	Layers:
	-	`sha256:d213ff87ba5e5f2b4267754c42ecd52932a688283e3aae2a395d8ce09530f8c0`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:87d941b6f55eaf4cdb35a94803f120d1c4167ebeaaaa43e6b46c5ac2d0f4e99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52858264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12c6c93b980e31b195991ec6609863b02a4c28a32584413c48d18bc364abe8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3870bcc7664fbf79c85068a58c49eadda5b3d3e83b3a261eb0687c8f382cba`  
		Last Modified: Tue, 03 Jun 2025 13:36:16 GMT  
		Size: 48.4 MB (48402796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955359e8bfcdc4fb80c3199996d51984fb401ed62747abf90d51c961f03ace5`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:c55567b804aad0b14a0467ceec3987a7d82ffaefb10fa549f77866f9e0c1b9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.4 KB (853445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb10668fadc74f6751e3b60cbd6f4c38843f45a6a9be6fbb22532ba802de1db`

```dockerfile
```

-	Layers:
	-	`sha256:30c42da66f61218a3020f7f694222b6575250a771d2bcb1b7fdc0e6faeaad8b4`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 840.8 KB (840754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392d505427c83a6e8915f94fb1287d21d09271fc51f8ddb46f01a299c650ec5e`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 12.7 KB (12691 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:ffa941c3a39cf8070066f8e642d043b3bbb93382b65ab191cb4f59a70c6af732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50485530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a848a8c9fbb90595a5bc10de6eb825d5b3eca316940e9f1f8f2f089a9cd7877`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be76b49bda3c8fd09b1fc1bb633224dd0871739cf51c1e96256322e662eb9ecc`  
		Last Modified: Tue, 27 May 2025 14:51:02 GMT  
		Size: 46.4 MB (46448254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729c14791b9df9fc72e478fa8d5c6bc0247b943a8520f7c10212326ae2273676`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:d12369f44494221de3c8b33bade1adfdcbbe7c11ac178c4bec540f4011d4aa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cf941cdda74702c092277fefff62640a0061d956f3961e5ebd1f020c55db3e`

```dockerfile
```

-	Layers:
	-	`sha256:ab995543f597da5ad856301f199da00314c3433240b338a4d72dfd57eda69543`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 838.8 KB (838763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c506f180b2e644e256354fcf1d9c72b834e9b34b994f54e4f66289491fef8f7`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:cbdceda31ee00c7b062c990ec0fde6ff734a6165dabd0f30f0a9e46f8a2bb997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55066625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7cd47da7429fb932128830b734060a66d1f54770ef47cea34d873da4c00c33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3115a6a25b258b9e6ace1b0865be4dfe817364e04295415d9f7ad8891c7510f`  
		Last Modified: Tue, 27 May 2025 15:04:50 GMT  
		Size: 51.3 MB (51254269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd870e16b4065f50d4818a3eca6af18cfa6eb0dea46fa7c17cada837663f7e`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:faa9e0a8c1162ef514b66cd1e71b134fcbbe8a0d253913101ae6fb89938f6cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886aeabd3fa90dcd67373554d829bb0a831a59a49f9398d35fd890adcabf15bc`

```dockerfile
```

-	Layers:
	-	`sha256:0ec7f3ca118232f7217ec7ee6748d5200b961fee4a7411cb303d10a9fa8bbf77`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 838.8 KB (838759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561720d19e2229fdca25d242ad66237315e65bd8ea379e98ef85ac55e6a345d6`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:2ec88e66f394380bb32f77301b4b815951439772b7e0952eccb1b1697b743ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54971569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ca5336c889b89509ed8f18fe24f502d2bdcc6a3a7f7247eaa4ebd7ed221f14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282b95ed82cbc6b46c6b7a1e316612d0d546c3ba7b5bc14c45f4774a7b2f4383`  
		Last Modified: Tue, 27 May 2025 14:51:43 GMT  
		Size: 51.0 MB (51042479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad521e963e06e44e8503bcbd40a4ae5b06971d6ef38534bba2c7b182a10178fc`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:45a983d5c03ffc11478ad3e7ed3efe5c236040aad3ae901397bc8e313fecbb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.2 KB (851245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a3e5232222151bd241ed48416b76c90efea06ceb139558b3e41e189772cbfa`

```dockerfile
```

-	Layers:
	-	`sha256:ec9c14d451d826a78857066f28d415d3aae40af15f49f6ff59771669432f95e0`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 838.7 KB (838707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b64020f713b42ea7e3b8e70e22d16c4399e5816c8bb219d241adb75fed50cca`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:20482a378759deedd7166b16e815327d2bcd992496a6fd8d9619da0a6197b393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:c9c636486ff1dc545be9b180e9d5b9fc0082f67215e6da7a799fb302615059a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176211547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e99f842b929588a924ce2fbf5aff655ad7ff59b30cfb596498e8223f687c16`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:17:58 GMT
RUN cmd /S /C #(nop) COPY file:924b82a6802fb4e8cf126ab6f07a4372c6070c83b784fcb0de9440d142a32bb4 in \ 
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:18:02 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d009a39cfa2ec096f4b9305fb6c88444ba99b07f9f00274d8e7c43eb87885`  
		Last Modified: Tue, 27 May 2025 15:18:12 GMT  
		Size: 53.6 MB (53631658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349971c9ecaeaae66d83dbd41ecb0e9e356bfaf4411d7aa31e935e81b78f476`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47b4c43feba126f6c436b6c0417e0ec7aea01f5fe47138de39bd5c47d3fe30`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be31ab4f88c09d2ebb9fcef11f5dd558c7cce9d42119d5eef5b1fa6715d32402`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:61d9531a333b7a67629c5957fdd3161b7bfa41c973683b63b7fde027580bbaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:2f1a679895bd4307016c14937aee829274dc7df9709a4f1fde49da3c2a586d34
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327756329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15230a7fcee8b248275d9d9271a3a5c0b588befeb73ba8a4e12f6656e17902`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:53:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:53:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:53:41 GMT
EXPOSE 80
# Tue, 27 May 2025 14:53:42 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:53:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf9f26e233b48aef33777758e8142e80d0faf761f8c9352a42a28c0b6c6019f`  
		Last Modified: Tue, 03 Jun 2025 18:50:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b85f1ce181168083824e21da848aed2bfe1c23377c4f835638696681f76671`  
		Last Modified: Tue, 03 Jun 2025 18:50:21 GMT  
		Size: 54.1 MB (54123071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb90aba608fef62a9f38114c8ce945705eb4fa07bf5ed9bf5aac4ec7b4e694fd`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdfd4a5bca5f6de55f055723fc209e78476d296219e4c93d15f15d45801e92b`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5ea15123c3852202f1aff4d7f6878ec3c50b8ac785ecc2a71e638d8ba9810f`  
		Last Modified: Tue, 03 Jun 2025 18:50:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e9dfb85bed73e0e8031b9c9a81bb272b8550e8e2e66a0b59ab77970e7095c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:d55b32d19c53ca332f1e0b093a8437b01ba7b841708ffe5c952cf9034c9cd8a4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177905809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ab1def000e52df8a233af9697e9ccbaa4079612aefcc706f08415c78d8e6e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:14:10 GMT
RUN cmd /S /C #(nop) COPY file:9febf6616005a41118af930de9dceb58bbb7c0dfadaddb7bfab3e211ac5bbe26 in \ 
# Tue, 27 May 2025 15:14:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48db22b9277c3bfe0e95c57c3b195f8f1fdd135aacdd2915ef435467e41f961`  
		Last Modified: Tue, 03 Jun 2025 20:17:45 GMT  
		Size: 55.3 MB (55326045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96bdc498b3e64f5942bcf57617b822f6368eae86c524f3d78887cd816ce8667`  
		Last Modified: Tue, 03 Jun 2025 20:17:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25735e6caa059b5973e065e6b9a2f2f6746cbdfbaba54aaadf8703b5b06ee81f`  
		Last Modified: Tue, 03 Jun 2025 20:17:41 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df498a2287fb011505c6829716e35ed011d1d071e7471f2904a6bf81753a5c1a`  
		Last Modified: Tue, 03 Jun 2025 20:17:42 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:6b0e06781a8c7ecfc0171b86ef4239567913f025d054f829b93836484c08d4de
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
$ docker pull traefik@sha256:7a3e93790acb9cc76a1671d60edac91f2b44a660c542a129f7b60ec2051f5935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56552512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51ba6b3748820dfa2350e62162dc7b6923bce1d439d7590dfe7b5b06fd7a43d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47353acdc55d84d8eab52dc12ed5a0544a15baeaaf7f841ac086cebb50b82d5f`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 52.4 MB (52449696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:306abeba90dd204cc7e01407add4fff90b5c5a9edf4c8aca9919bd795665ccf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.2 KB (853200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90af661a720bad4fc40519980c3e6448ce6246bde83edb130c438936f7345d8f`

```dockerfile
```

-	Layers:
	-	`sha256:6a24cac55bba047916faf531a3af8614f532036041648fc1eb0745bcfbea3b18`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 840.7 KB (840662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc7f0bf9995aaadc937e4bd1a4035f31cd89dff5ca1ef50562db74686283f15`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9394e41a11e186e65d61d6b214efaf23a6df92f739bed50b27cf7d54b5de99bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52318031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d7b2f69920da843f662e3a66d609b3d54978c34e6a1a3e313f1e51ae77229`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2366ec9e01d41af275db660969c094e2c585439262f2f12cc2a5e5b6ce53464`  
		Last Modified: Tue, 27 May 2025 14:49:39 GMT  
		Size: 48.5 MB (48493507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab654d05db06d563d37378656367863bf7956cfffe339a7f3d02e668dbb4744c`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:cb2ed2f99573807413124377f2dac2912f2fb9efa7a46ffe8fe108f34c519e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c2276f0758ed20a2cdafbd17e771bafe65925182dc94eb10f8d5937905387`

```dockerfile
```

-	Layers:
	-	`sha256:d213ff87ba5e5f2b4267754c42ecd52932a688283e3aae2a395d8ce09530f8c0`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:87d941b6f55eaf4cdb35a94803f120d1c4167ebeaaaa43e6b46c5ac2d0f4e99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52858264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12c6c93b980e31b195991ec6609863b02a4c28a32584413c48d18bc364abe8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3870bcc7664fbf79c85068a58c49eadda5b3d3e83b3a261eb0687c8f382cba`  
		Last Modified: Tue, 03 Jun 2025 13:36:16 GMT  
		Size: 48.4 MB (48402796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955359e8bfcdc4fb80c3199996d51984fb401ed62747abf90d51c961f03ace5`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:c55567b804aad0b14a0467ceec3987a7d82ffaefb10fa549f77866f9e0c1b9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.4 KB (853445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb10668fadc74f6751e3b60cbd6f4c38843f45a6a9be6fbb22532ba802de1db`

```dockerfile
```

-	Layers:
	-	`sha256:30c42da66f61218a3020f7f694222b6575250a771d2bcb1b7fdc0e6faeaad8b4`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 840.8 KB (840754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392d505427c83a6e8915f94fb1287d21d09271fc51f8ddb46f01a299c650ec5e`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 12.7 KB (12691 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:ffa941c3a39cf8070066f8e642d043b3bbb93382b65ab191cb4f59a70c6af732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50485530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a848a8c9fbb90595a5bc10de6eb825d5b3eca316940e9f1f8f2f089a9cd7877`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be76b49bda3c8fd09b1fc1bb633224dd0871739cf51c1e96256322e662eb9ecc`  
		Last Modified: Tue, 27 May 2025 14:51:02 GMT  
		Size: 46.4 MB (46448254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729c14791b9df9fc72e478fa8d5c6bc0247b943a8520f7c10212326ae2273676`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:d12369f44494221de3c8b33bade1adfdcbbe7c11ac178c4bec540f4011d4aa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cf941cdda74702c092277fefff62640a0061d956f3961e5ebd1f020c55db3e`

```dockerfile
```

-	Layers:
	-	`sha256:ab995543f597da5ad856301f199da00314c3433240b338a4d72dfd57eda69543`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 838.8 KB (838763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c506f180b2e644e256354fcf1d9c72b834e9b34b994f54e4f66289491fef8f7`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:cbdceda31ee00c7b062c990ec0fde6ff734a6165dabd0f30f0a9e46f8a2bb997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55066625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7cd47da7429fb932128830b734060a66d1f54770ef47cea34d873da4c00c33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3115a6a25b258b9e6ace1b0865be4dfe817364e04295415d9f7ad8891c7510f`  
		Last Modified: Tue, 27 May 2025 15:04:50 GMT  
		Size: 51.3 MB (51254269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd870e16b4065f50d4818a3eca6af18cfa6eb0dea46fa7c17cada837663f7e`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:faa9e0a8c1162ef514b66cd1e71b134fcbbe8a0d253913101ae6fb89938f6cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886aeabd3fa90dcd67373554d829bb0a831a59a49f9398d35fd890adcabf15bc`

```dockerfile
```

-	Layers:
	-	`sha256:0ec7f3ca118232f7217ec7ee6748d5200b961fee4a7411cb303d10a9fa8bbf77`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 838.8 KB (838759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561720d19e2229fdca25d242ad66237315e65bd8ea379e98ef85ac55e6a345d6`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:2ec88e66f394380bb32f77301b4b815951439772b7e0952eccb1b1697b743ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54971569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ca5336c889b89509ed8f18fe24f502d2bdcc6a3a7f7247eaa4ebd7ed221f14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282b95ed82cbc6b46c6b7a1e316612d0d546c3ba7b5bc14c45f4774a7b2f4383`  
		Last Modified: Tue, 27 May 2025 14:51:43 GMT  
		Size: 51.0 MB (51042479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad521e963e06e44e8503bcbd40a4ae5b06971d6ef38534bba2c7b182a10178fc`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:45a983d5c03ffc11478ad3e7ed3efe5c236040aad3ae901397bc8e313fecbb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.2 KB (851245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a3e5232222151bd241ed48416b76c90efea06ceb139558b3e41e189772cbfa`

```dockerfile
```

-	Layers:
	-	`sha256:ec9c14d451d826a78857066f28d415d3aae40af15f49f6ff59771669432f95e0`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 838.7 KB (838707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b64020f713b42ea7e3b8e70e22d16c4399e5816c8bb219d241adb75fed50cca`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:20482a378759deedd7166b16e815327d2bcd992496a6fd8d9619da0a6197b393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:c9c636486ff1dc545be9b180e9d5b9fc0082f67215e6da7a799fb302615059a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176211547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e99f842b929588a924ce2fbf5aff655ad7ff59b30cfb596498e8223f687c16`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:17:58 GMT
RUN cmd /S /C #(nop) COPY file:924b82a6802fb4e8cf126ab6f07a4372c6070c83b784fcb0de9440d142a32bb4 in \ 
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:18:02 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d009a39cfa2ec096f4b9305fb6c88444ba99b07f9f00274d8e7c43eb87885`  
		Last Modified: Tue, 27 May 2025 15:18:12 GMT  
		Size: 53.6 MB (53631658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349971c9ecaeaae66d83dbd41ecb0e9e356bfaf4411d7aa31e935e81b78f476`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47b4c43feba126f6c436b6c0417e0ec7aea01f5fe47138de39bd5c47d3fe30`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be31ab4f88c09d2ebb9fcef11f5dd558c7cce9d42119d5eef5b1fa6715d32402`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:61d9531a333b7a67629c5957fdd3161b7bfa41c973683b63b7fde027580bbaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:2f1a679895bd4307016c14937aee829274dc7df9709a4f1fde49da3c2a586d34
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327756329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15230a7fcee8b248275d9d9271a3a5c0b588befeb73ba8a4e12f6656e17902`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:53:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:53:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:53:41 GMT
EXPOSE 80
# Tue, 27 May 2025 14:53:42 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:53:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf9f26e233b48aef33777758e8142e80d0faf761f8c9352a42a28c0b6c6019f`  
		Last Modified: Tue, 03 Jun 2025 18:50:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b85f1ce181168083824e21da848aed2bfe1c23377c4f835638696681f76671`  
		Last Modified: Tue, 03 Jun 2025 18:50:21 GMT  
		Size: 54.1 MB (54123071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb90aba608fef62a9f38114c8ce945705eb4fa07bf5ed9bf5aac4ec7b4e694fd`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdfd4a5bca5f6de55f055723fc209e78476d296219e4c93d15f15d45801e92b`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5ea15123c3852202f1aff4d7f6878ec3c50b8ac785ecc2a71e638d8ba9810f`  
		Last Modified: Tue, 03 Jun 2025 18:50:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:6b0e06781a8c7ecfc0171b86ef4239567913f025d054f829b93836484c08d4de
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
$ docker pull traefik@sha256:7a3e93790acb9cc76a1671d60edac91f2b44a660c542a129f7b60ec2051f5935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56552512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51ba6b3748820dfa2350e62162dc7b6923bce1d439d7590dfe7b5b06fd7a43d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47353acdc55d84d8eab52dc12ed5a0544a15baeaaf7f841ac086cebb50b82d5f`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 52.4 MB (52449696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:306abeba90dd204cc7e01407add4fff90b5c5a9edf4c8aca9919bd795665ccf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.2 KB (853200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90af661a720bad4fc40519980c3e6448ce6246bde83edb130c438936f7345d8f`

```dockerfile
```

-	Layers:
	-	`sha256:6a24cac55bba047916faf531a3af8614f532036041648fc1eb0745bcfbea3b18`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 840.7 KB (840662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc7f0bf9995aaadc937e4bd1a4035f31cd89dff5ca1ef50562db74686283f15`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9394e41a11e186e65d61d6b214efaf23a6df92f739bed50b27cf7d54b5de99bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52318031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d7b2f69920da843f662e3a66d609b3d54978c34e6a1a3e313f1e51ae77229`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2366ec9e01d41af275db660969c094e2c585439262f2f12cc2a5e5b6ce53464`  
		Last Modified: Tue, 27 May 2025 14:49:39 GMT  
		Size: 48.5 MB (48493507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab654d05db06d563d37378656367863bf7956cfffe339a7f3d02e668dbb4744c`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:cb2ed2f99573807413124377f2dac2912f2fb9efa7a46ffe8fe108f34c519e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c2276f0758ed20a2cdafbd17e771bafe65925182dc94eb10f8d5937905387`

```dockerfile
```

-	Layers:
	-	`sha256:d213ff87ba5e5f2b4267754c42ecd52932a688283e3aae2a395d8ce09530f8c0`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:87d941b6f55eaf4cdb35a94803f120d1c4167ebeaaaa43e6b46c5ac2d0f4e99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52858264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12c6c93b980e31b195991ec6609863b02a4c28a32584413c48d18bc364abe8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3870bcc7664fbf79c85068a58c49eadda5b3d3e83b3a261eb0687c8f382cba`  
		Last Modified: Tue, 03 Jun 2025 13:36:16 GMT  
		Size: 48.4 MB (48402796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955359e8bfcdc4fb80c3199996d51984fb401ed62747abf90d51c961f03ace5`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c55567b804aad0b14a0467ceec3987a7d82ffaefb10fa549f77866f9e0c1b9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.4 KB (853445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb10668fadc74f6751e3b60cbd6f4c38843f45a6a9be6fbb22532ba802de1db`

```dockerfile
```

-	Layers:
	-	`sha256:30c42da66f61218a3020f7f694222b6575250a771d2bcb1b7fdc0e6faeaad8b4`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 840.8 KB (840754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392d505427c83a6e8915f94fb1287d21d09271fc51f8ddb46f01a299c650ec5e`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 12.7 KB (12691 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:ffa941c3a39cf8070066f8e642d043b3bbb93382b65ab191cb4f59a70c6af732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50485530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a848a8c9fbb90595a5bc10de6eb825d5b3eca316940e9f1f8f2f089a9cd7877`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be76b49bda3c8fd09b1fc1bb633224dd0871739cf51c1e96256322e662eb9ecc`  
		Last Modified: Tue, 27 May 2025 14:51:02 GMT  
		Size: 46.4 MB (46448254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729c14791b9df9fc72e478fa8d5c6bc0247b943a8520f7c10212326ae2273676`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:d12369f44494221de3c8b33bade1adfdcbbe7c11ac178c4bec540f4011d4aa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cf941cdda74702c092277fefff62640a0061d956f3961e5ebd1f020c55db3e`

```dockerfile
```

-	Layers:
	-	`sha256:ab995543f597da5ad856301f199da00314c3433240b338a4d72dfd57eda69543`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 838.8 KB (838763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c506f180b2e644e256354fcf1d9c72b834e9b34b994f54e4f66289491fef8f7`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:cbdceda31ee00c7b062c990ec0fde6ff734a6165dabd0f30f0a9e46f8a2bb997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55066625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7cd47da7429fb932128830b734060a66d1f54770ef47cea34d873da4c00c33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3115a6a25b258b9e6ace1b0865be4dfe817364e04295415d9f7ad8891c7510f`  
		Last Modified: Tue, 27 May 2025 15:04:50 GMT  
		Size: 51.3 MB (51254269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd870e16b4065f50d4818a3eca6af18cfa6eb0dea46fa7c17cada837663f7e`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:faa9e0a8c1162ef514b66cd1e71b134fcbbe8a0d253913101ae6fb89938f6cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886aeabd3fa90dcd67373554d829bb0a831a59a49f9398d35fd890adcabf15bc`

```dockerfile
```

-	Layers:
	-	`sha256:0ec7f3ca118232f7217ec7ee6748d5200b961fee4a7411cb303d10a9fa8bbf77`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 838.8 KB (838759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561720d19e2229fdca25d242ad66237315e65bd8ea379e98ef85ac55e6a345d6`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:2ec88e66f394380bb32f77301b4b815951439772b7e0952eccb1b1697b743ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54971569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ca5336c889b89509ed8f18fe24f502d2bdcc6a3a7f7247eaa4ebd7ed221f14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282b95ed82cbc6b46c6b7a1e316612d0d546c3ba7b5bc14c45f4774a7b2f4383`  
		Last Modified: Tue, 27 May 2025 14:51:43 GMT  
		Size: 51.0 MB (51042479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad521e963e06e44e8503bcbd40a4ae5b06971d6ef38534bba2c7b182a10178fc`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:45a983d5c03ffc11478ad3e7ed3efe5c236040aad3ae901397bc8e313fecbb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.2 KB (851245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a3e5232222151bd241ed48416b76c90efea06ceb139558b3e41e189772cbfa`

```dockerfile
```

-	Layers:
	-	`sha256:ec9c14d451d826a78857066f28d415d3aae40af15f49f6ff59771669432f95e0`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 838.7 KB (838707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b64020f713b42ea7e3b8e70e22d16c4399e5816c8bb219d241adb75fed50cca`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:20482a378759deedd7166b16e815327d2bcd992496a6fd8d9619da0a6197b393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:c9c636486ff1dc545be9b180e9d5b9fc0082f67215e6da7a799fb302615059a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176211547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e99f842b929588a924ce2fbf5aff655ad7ff59b30cfb596498e8223f687c16`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:17:58 GMT
RUN cmd /S /C #(nop) COPY file:924b82a6802fb4e8cf126ab6f07a4372c6070c83b784fcb0de9440d142a32bb4 in \ 
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:18:02 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d009a39cfa2ec096f4b9305fb6c88444ba99b07f9f00274d8e7c43eb87885`  
		Last Modified: Tue, 27 May 2025 15:18:12 GMT  
		Size: 53.6 MB (53631658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349971c9ecaeaae66d83dbd41ecb0e9e356bfaf4411d7aa31e935e81b78f476`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47b4c43feba126f6c436b6c0417e0ec7aea01f5fe47138de39bd5c47d3fe30`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be31ab4f88c09d2ebb9fcef11f5dd558c7cce9d42119d5eef5b1fa6715d32402`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:61d9531a333b7a67629c5957fdd3161b7bfa41c973683b63b7fde027580bbaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:2f1a679895bd4307016c14937aee829274dc7df9709a4f1fde49da3c2a586d34
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327756329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15230a7fcee8b248275d9d9271a3a5c0b588befeb73ba8a4e12f6656e17902`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:53:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:53:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:53:41 GMT
EXPOSE 80
# Tue, 27 May 2025 14:53:42 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:53:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf9f26e233b48aef33777758e8142e80d0faf761f8c9352a42a28c0b6c6019f`  
		Last Modified: Tue, 03 Jun 2025 18:50:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b85f1ce181168083824e21da848aed2bfe1c23377c4f835638696681f76671`  
		Last Modified: Tue, 03 Jun 2025 18:50:21 GMT  
		Size: 54.1 MB (54123071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb90aba608fef62a9f38114c8ce945705eb4fa07bf5ed9bf5aac4ec7b4e694fd`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdfd4a5bca5f6de55f055723fc209e78476d296219e4c93d15f15d45801e92b`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5ea15123c3852202f1aff4d7f6878ec3c50b8ac785ecc2a71e638d8ba9810f`  
		Last Modified: Tue, 03 Jun 2025 18:50:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.25`

```console
$ docker pull traefik@sha256:6b0e06781a8c7ecfc0171b86ef4239567913f025d054f829b93836484c08d4de
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

### `traefik:v2.11.25` - linux; amd64

```console
$ docker pull traefik@sha256:7a3e93790acb9cc76a1671d60edac91f2b44a660c542a129f7b60ec2051f5935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56552512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51ba6b3748820dfa2350e62162dc7b6923bce1d439d7590dfe7b5b06fd7a43d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47353acdc55d84d8eab52dc12ed5a0544a15baeaaf7f841ac086cebb50b82d5f`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 52.4 MB (52449696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:306abeba90dd204cc7e01407add4fff90b5c5a9edf4c8aca9919bd795665ccf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.2 KB (853200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90af661a720bad4fc40519980c3e6448ce6246bde83edb130c438936f7345d8f`

```dockerfile
```

-	Layers:
	-	`sha256:6a24cac55bba047916faf531a3af8614f532036041648fc1eb0745bcfbea3b18`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 840.7 KB (840662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc7f0bf9995aaadc937e4bd1a4035f31cd89dff5ca1ef50562db74686283f15`  
		Last Modified: Tue, 27 May 2025 14:49:46 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.25` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9394e41a11e186e65d61d6b214efaf23a6df92f739bed50b27cf7d54b5de99bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52318031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d7b2f69920da843f662e3a66d609b3d54978c34e6a1a3e313f1e51ae77229`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2366ec9e01d41af275db660969c094e2c585439262f2f12cc2a5e5b6ce53464`  
		Last Modified: Tue, 27 May 2025 14:49:39 GMT  
		Size: 48.5 MB (48493507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab654d05db06d563d37378656367863bf7956cfffe339a7f3d02e668dbb4744c`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:cb2ed2f99573807413124377f2dac2912f2fb9efa7a46ffe8fe108f34c519e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c2276f0758ed20a2cdafbd17e771bafe65925182dc94eb10f8d5937905387`

```dockerfile
```

-	Layers:
	-	`sha256:d213ff87ba5e5f2b4267754c42ecd52932a688283e3aae2a395d8ce09530f8c0`  
		Last Modified: Tue, 27 May 2025 14:49:37 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.25` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:87d941b6f55eaf4cdb35a94803f120d1c4167ebeaaaa43e6b46c5ac2d0f4e99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52858264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12c6c93b980e31b195991ec6609863b02a4c28a32584413c48d18bc364abe8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3870bcc7664fbf79c85068a58c49eadda5b3d3e83b3a261eb0687c8f382cba`  
		Last Modified: Tue, 03 Jun 2025 13:36:16 GMT  
		Size: 48.4 MB (48402796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955359e8bfcdc4fb80c3199996d51984fb401ed62747abf90d51c961f03ace5`  
		Last Modified: Tue, 03 Jun 2025 13:36:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:c55567b804aad0b14a0467ceec3987a7d82ffaefb10fa549f77866f9e0c1b9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.4 KB (853445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb10668fadc74f6751e3b60cbd6f4c38843f45a6a9be6fbb22532ba802de1db`

```dockerfile
```

-	Layers:
	-	`sha256:30c42da66f61218a3020f7f694222b6575250a771d2bcb1b7fdc0e6faeaad8b4`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 840.8 KB (840754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392d505427c83a6e8915f94fb1287d21d09271fc51f8ddb46f01a299c650ec5e`  
		Last Modified: Tue, 27 May 2025 14:50:08 GMT  
		Size: 12.7 KB (12691 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.25` - linux; ppc64le

```console
$ docker pull traefik@sha256:ffa941c3a39cf8070066f8e642d043b3bbb93382b65ab191cb4f59a70c6af732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50485530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a848a8c9fbb90595a5bc10de6eb825d5b3eca316940e9f1f8f2f089a9cd7877`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be76b49bda3c8fd09b1fc1bb633224dd0871739cf51c1e96256322e662eb9ecc`  
		Last Modified: Tue, 27 May 2025 14:51:02 GMT  
		Size: 46.4 MB (46448254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729c14791b9df9fc72e478fa8d5c6bc0247b943a8520f7c10212326ae2273676`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:d12369f44494221de3c8b33bade1adfdcbbe7c11ac178c4bec540f4011d4aa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cf941cdda74702c092277fefff62640a0061d956f3961e5ebd1f020c55db3e`

```dockerfile
```

-	Layers:
	-	`sha256:ab995543f597da5ad856301f199da00314c3433240b338a4d72dfd57eda69543`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 838.8 KB (838763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c506f180b2e644e256354fcf1d9c72b834e9b34b994f54e4f66289491fef8f7`  
		Last Modified: Tue, 27 May 2025 14:51:00 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.25` - linux; riscv64

```console
$ docker pull traefik@sha256:cbdceda31ee00c7b062c990ec0fde6ff734a6165dabd0f30f0a9e46f8a2bb997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55066625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7cd47da7429fb932128830b734060a66d1f54770ef47cea34d873da4c00c33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3115a6a25b258b9e6ace1b0865be4dfe817364e04295415d9f7ad8891c7510f`  
		Last Modified: Tue, 27 May 2025 15:04:50 GMT  
		Size: 51.3 MB (51254269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd870e16b4065f50d4818a3eca6af18cfa6eb0dea46fa7c17cada837663f7e`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:faa9e0a8c1162ef514b66cd1e71b134fcbbe8a0d253913101ae6fb89938f6cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886aeabd3fa90dcd67373554d829bb0a831a59a49f9398d35fd890adcabf15bc`

```dockerfile
```

-	Layers:
	-	`sha256:0ec7f3ca118232f7217ec7ee6748d5200b961fee4a7411cb303d10a9fa8bbf77`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 838.8 KB (838759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561720d19e2229fdca25d242ad66237315e65bd8ea379e98ef85ac55e6a345d6`  
		Last Modified: Tue, 27 May 2025 15:04:42 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.25` - linux; s390x

```console
$ docker pull traefik@sha256:2ec88e66f394380bb32f77301b4b815951439772b7e0952eccb1b1697b743ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54971569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ca5336c889b89509ed8f18fe24f502d2bdcc6a3a7f7247eaa4ebd7ed221f14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 10:25:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 10:25:30 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 10:25:30 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 10:25:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 10:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 10:25:30 GMT
CMD ["traefik"]
# Tue, 27 May 2025 10:25:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282b95ed82cbc6b46c6b7a1e316612d0d546c3ba7b5bc14c45f4774a7b2f4383`  
		Last Modified: Tue, 27 May 2025 14:51:43 GMT  
		Size: 51.0 MB (51042479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad521e963e06e44e8503bcbd40a4ae5b06971d6ef38534bba2c7b182a10178fc`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.25` - unknown; unknown

```console
$ docker pull traefik@sha256:45a983d5c03ffc11478ad3e7ed3efe5c236040aad3ae901397bc8e313fecbb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.2 KB (851245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a3e5232222151bd241ed48416b76c90efea06ceb139558b3e41e189772cbfa`

```dockerfile
```

-	Layers:
	-	`sha256:ec9c14d451d826a78857066f28d415d3aae40af15f49f6ff59771669432f95e0`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 838.7 KB (838707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b64020f713b42ea7e3b8e70e22d16c4399e5816c8bb219d241adb75fed50cca`  
		Last Modified: Tue, 27 May 2025 14:51:42 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.25-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:20482a378759deedd7166b16e815327d2bcd992496a6fd8d9619da0a6197b393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v2.11.25-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:c9c636486ff1dc545be9b180e9d5b9fc0082f67215e6da7a799fb302615059a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176211547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e99f842b929588a924ce2fbf5aff655ad7ff59b30cfb596498e8223f687c16`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:17:58 GMT
RUN cmd /S /C #(nop) COPY file:924b82a6802fb4e8cf126ab6f07a4372c6070c83b784fcb0de9440d142a32bb4 in \ 
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:18:02 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d009a39cfa2ec096f4b9305fb6c88444ba99b07f9f00274d8e7c43eb87885`  
		Last Modified: Tue, 27 May 2025 15:18:12 GMT  
		Size: 53.6 MB (53631658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349971c9ecaeaae66d83dbd41ecb0e9e356bfaf4411d7aa31e935e81b78f476`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47b4c43feba126f6c436b6c0417e0ec7aea01f5fe47138de39bd5c47d3fe30`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be31ab4f88c09d2ebb9fcef11f5dd558c7cce9d42119d5eef5b1fa6715d32402`  
		Last Modified: Tue, 27 May 2025 15:18:05 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.25-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:61d9531a333b7a67629c5957fdd3161b7bfa41c973683b63b7fde027580bbaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v2.11.25-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:2f1a679895bd4307016c14937aee829274dc7df9709a4f1fde49da3c2a586d34
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327756329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15230a7fcee8b248275d9d9271a3a5c0b588befeb73ba8a4e12f6656e17902`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:53:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:53:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.25/traefik_v2.11.25_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:53:41 GMT
EXPOSE 80
# Tue, 27 May 2025 14:53:42 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:53:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf9f26e233b48aef33777758e8142e80d0faf761f8c9352a42a28c0b6c6019f`  
		Last Modified: Tue, 03 Jun 2025 18:50:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b85f1ce181168083824e21da848aed2bfe1c23377c4f835638696681f76671`  
		Last Modified: Tue, 03 Jun 2025 18:50:21 GMT  
		Size: 54.1 MB (54123071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb90aba608fef62a9f38114c8ce945705eb4fa07bf5ed9bf5aac4ec7b4e694fd`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdfd4a5bca5f6de55f055723fc209e78476d296219e4c93d15f15d45801e92b`  
		Last Modified: Tue, 03 Jun 2025 18:50:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5ea15123c3852202f1aff4d7f6878ec3c50b8ac785ecc2a71e638d8ba9810f`  
		Last Modified: Tue, 03 Jun 2025 18:50:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:cd40ab7bc1f047731d5b22595203812343efcb6538014c4e93221cfc3a77217a
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
$ docker pull traefik@sha256:06b2f92ba6cb9fdc2de99d41c22b862f196871ad55c26269083eaef39dd4fa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58293647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0a241c8a0a140b0d2142f3f481b2fa847a7f42a1356dc39a8eac9b27df4cf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb594ddbc1285eb9bc5e21f89125fbcf7f370d3f7078638c155337257de4ca5`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 54.2 MB (54190831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:bd3775e8dc18f0eaff57543193acf32e1c3747e67e6e71364e6276636ba61f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 KB (840081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65c49c68a9e64602c396234e259172a812df05f95ca284a971af5fcb285cf3d`

```dockerfile
```

-	Layers:
	-	`sha256:cf9c8d147592b2181fc4bd2d7dfdebe237ee30fb30121650d63e2e2a70d609bf`  
		Last Modified: Tue, 03 Jun 2025 15:14:44 GMT  
		Size: 827.3 KB (827272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfa0a085791bfb75f2bde4f6dbcdad91138333a1752fa36ccb2ca805fa44a20`  
		Last Modified: Tue, 03 Jun 2025 15:14:46 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ac48f2ae151717fe49a90e38c92a0a3630f82abdb3e10c8f216b3d2b2e5e18db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53692448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a28e18eb719fd329d0779f8e0da2e3f4a9f569d81ea005a40242d251f3c2a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376947144f2af43212730e00e809e580baa70c1564a7f1c05ce0b5c89a39bfae`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 49.9 MB (49867924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe19f27e5039137d87ded7aa47f3234bf196b95e6a7636f951be0f303fc62b9`  
		Last Modified: Tue, 03 Jun 2025 15:14:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:bde6cb15b218a8146019f1ade9fa1859819d1eb177dc082c3b97c7b0d3445df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75447718047d59fefcc7894e79fc559894fefb231835c5ad7c1f3dd1bf1c79a0`

```dockerfile
```

-	Layers:
	-	`sha256:2514c0d20a1024e7c7d77fb6fa139f6f49f2b85376220c1c74e5ee15fa765ab2`  
		Last Modified: Tue, 03 Jun 2025 15:14:45 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5ed09f5b4d7df3bb186ba5360e7dca8dc73067ecc5278b4a26f60587db908958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7206871bb3451f03c8939c466c0e63a9e69fa944f4aae62b4be7fe3f74725543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30408b989b42117e933e49a16a00bde8712c625b561afa4e231ba172f5a2c8f4`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 50.1 MB (50051133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:ced2a2408769ffb3560fa21b6854287b03e852458a074b5f65df89147a01509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 KB (840352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16424a5a76aa8af2207a2dbecb3a9791c93454915b99af606460d4fd0fcd4f7c`

```dockerfile
```

-	Layers:
	-	`sha256:ea2259fa8cf34c77b492a8fac036ee83b33d37593f00ae9474a90deae0137fdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:47 GMT  
		Size: 827.4 KB (827376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77668edfb6bddc597a120d1abc4d2d3bd49079937ead823127afe0093ee3642e`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 13.0 KB (12976 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:904d00b37a12fd670c6fc8c2e56f5d1cf927d068e75f362e01bfc2ab787a87a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51802197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76af70530829836acad936bfd80b95121bd6e2e670b3dd45485a91e7879f2093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c884f5e61b441d4901cdb9a4f6b55d488910ad927aa3abe32cbb8b4963b6c2b`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 47.8 MB (47764922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:3804f216242a434a58038d23818cff62a773c51847bda7f75b16c226d6f8b384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f4ced2f8947770e3e135a78555b37d42eb37c4354a957ab285e0df1943e837`

```dockerfile
```

-	Layers:
	-	`sha256:2b234a140882f2b7b712d1397de8b3c99819e10801f47893570e9ce96e63b8dc`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 825.4 KB (825379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f87d532e77998b2a01c1ef79f32e030be1542b903fa47b6eac46cb2150dbcb8`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:10503d09555de721b57d72e21c8147b353ae7e55a09e3d0d36409da7b61d79da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56455485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec54b9cdac031e36fb2fbb8d07099b21706b9405d9730b85495c8519e5be09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e436610aeaf1067679abbafd70788026b845bb9421f3b7ce99130207145bdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:59 GMT  
		Size: 52.6 MB (52643130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4a395f47a23ab42cfa059fdf6a35b3a11c21ee95d3d30a868cb8855901fd38`  
		Last Modified: Tue, 03 Jun 2025 15:15:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:5c006f458ac1cd3e4e4932bf5dec8705de18a88005c8e14efd9dcab0f13ba340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe933e0dc2b408ea91505a7d76c47f35f707371115e064c091bbb57e59cbedd`

```dockerfile
```

-	Layers:
	-	`sha256:6063ec4f68a493b6767b158b205cd1ef8193689de05f6363a8955aa456101000`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 825.4 KB (825375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a92db796c6c7cb6425d882b8f55c8abee2389f7409954a5e7ca909c1f9c048`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:07942bc395eb18e2ccdff76a5db6ec430330b4f6e9e21de93abc22d38dd7a6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56269856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ae8c552f603f116570604fac0d866bd7ea998a35a072390398bb2769bbe45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042c8a716a75e292fa5080b404a4f60081032cafe22d09079bf3f891e9ee2b9`  
		Last Modified: Tue, 03 Jun 2025 15:15:00 GMT  
		Size: 52.3 MB (52340765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c51a73e866e22cc50e4088a69f1cad9336fa407fb7a875dff86ce82ea4c6c8b`  
		Last Modified: Tue, 03 Jun 2025 15:15:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:8b7777d29fef01c7e3e582eab03eb0d2f4d619fba29fd92baf84c3ca4cad17f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.1 KB (838130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3bcbcce76b9d2874c369b9d7cfc548d91aa722a5266d5ab4cc461d68129044`

```dockerfile
```

-	Layers:
	-	`sha256:13b584c594ba870e6372ee32d863a9d72a542a1dc4c5178717435d6f79b78e6c`  
		Last Modified: Tue, 03 Jun 2025 15:14:56 GMT  
		Size: 825.3 KB (825321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178dcee5ee28bb14fd9e2d73d78bcc55398b12e68063bfff1bb3f757490c05c4`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e9dfb85bed73e0e8031b9c9a81bb272b8550e8e2e66a0b59ab77970e7095c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:d55b32d19c53ca332f1e0b093a8437b01ba7b841708ffe5c952cf9034c9cd8a4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177905809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ab1def000e52df8a233af9697e9ccbaa4079612aefcc706f08415c78d8e6e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:14:10 GMT
RUN cmd /S /C #(nop) COPY file:9febf6616005a41118af930de9dceb58bbb7c0dfadaddb7bfab3e211ac5bbe26 in \ 
# Tue, 27 May 2025 15:14:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48db22b9277c3bfe0e95c57c3b195f8f1fdd135aacdd2915ef435467e41f961`  
		Last Modified: Tue, 03 Jun 2025 20:17:45 GMT  
		Size: 55.3 MB (55326045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96bdc498b3e64f5942bcf57617b822f6368eae86c524f3d78887cd816ce8667`  
		Last Modified: Tue, 03 Jun 2025 20:17:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25735e6caa059b5973e065e6b9a2f2f6746cbdfbaba54aaadf8703b5b06ee81f`  
		Last Modified: Tue, 03 Jun 2025 20:17:41 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df498a2287fb011505c6829716e35ed011d1d071e7471f2904a6bf81753a5c1a`  
		Last Modified: Tue, 03 Jun 2025 20:17:42 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4cbc0ec3d96e7458f61766b6a7f20184db198cdd5d3e843990d4ffd5d4776f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:6afe066e8b2138da8f232a83e5323bedc06eb2748b3b14bb426fcc0b02a7ab94
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329464370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878537d0f6cf4c3bc01385bf3b93e83db668959f2390c6853b2f6e829e091238`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:54:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:54:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:54:49 GMT
EXPOSE 80
# Tue, 27 May 2025 14:54:50 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:54:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37ab80d65d0f531dd0dda220ec269bb8d3a64ae4733859bf5cceb7cca8083c4`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c9a42230c171b5f3397c7ed80a1f29f0cdea2a1ac9fd6362a379d3fdd0cb7`  
		Last Modified: Tue, 03 Jun 2025 14:12:47 GMT  
		Size: 55.8 MB (55831084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539ecf95a4c553f7630e2dfc0724182acdc077b42454246064b1e81328be8308`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f437896dd6a4e91f5f8d7f28116f518690a54ca59232a2ebe4f5a11fb48f54`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b93db94dc05cad592e9d27e6cf3ec8bb10a35393168f1c7ea7ec866969a171`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.4`

```console
$ docker pull traefik@sha256:cd40ab7bc1f047731d5b22595203812343efcb6538014c4e93221cfc3a77217a
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

### `traefik:v3.4` - linux; amd64

```console
$ docker pull traefik@sha256:06b2f92ba6cb9fdc2de99d41c22b862f196871ad55c26269083eaef39dd4fa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58293647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0a241c8a0a140b0d2142f3f481b2fa847a7f42a1356dc39a8eac9b27df4cf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb594ddbc1285eb9bc5e21f89125fbcf7f370d3f7078638c155337257de4ca5`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 54.2 MB (54190831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:bd3775e8dc18f0eaff57543193acf32e1c3747e67e6e71364e6276636ba61f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 KB (840081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65c49c68a9e64602c396234e259172a812df05f95ca284a971af5fcb285cf3d`

```dockerfile
```

-	Layers:
	-	`sha256:cf9c8d147592b2181fc4bd2d7dfdebe237ee30fb30121650d63e2e2a70d609bf`  
		Last Modified: Tue, 03 Jun 2025 15:14:44 GMT  
		Size: 827.3 KB (827272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfa0a085791bfb75f2bde4f6dbcdad91138333a1752fa36ccb2ca805fa44a20`  
		Last Modified: Tue, 03 Jun 2025 15:14:46 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ac48f2ae151717fe49a90e38c92a0a3630f82abdb3e10c8f216b3d2b2e5e18db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53692448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a28e18eb719fd329d0779f8e0da2e3f4a9f569d81ea005a40242d251f3c2a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376947144f2af43212730e00e809e580baa70c1564a7f1c05ce0b5c89a39bfae`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 49.9 MB (49867924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe19f27e5039137d87ded7aa47f3234bf196b95e6a7636f951be0f303fc62b9`  
		Last Modified: Tue, 03 Jun 2025 15:14:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:bde6cb15b218a8146019f1ade9fa1859819d1eb177dc082c3b97c7b0d3445df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75447718047d59fefcc7894e79fc559894fefb231835c5ad7c1f3dd1bf1c79a0`

```dockerfile
```

-	Layers:
	-	`sha256:2514c0d20a1024e7c7d77fb6fa139f6f49f2b85376220c1c74e5ee15fa765ab2`  
		Last Modified: Tue, 03 Jun 2025 15:14:45 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5ed09f5b4d7df3bb186ba5360e7dca8dc73067ecc5278b4a26f60587db908958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7206871bb3451f03c8939c466c0e63a9e69fa944f4aae62b4be7fe3f74725543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30408b989b42117e933e49a16a00bde8712c625b561afa4e231ba172f5a2c8f4`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 50.1 MB (50051133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:ced2a2408769ffb3560fa21b6854287b03e852458a074b5f65df89147a01509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 KB (840352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16424a5a76aa8af2207a2dbecb3a9791c93454915b99af606460d4fd0fcd4f7c`

```dockerfile
```

-	Layers:
	-	`sha256:ea2259fa8cf34c77b492a8fac036ee83b33d37593f00ae9474a90deae0137fdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:47 GMT  
		Size: 827.4 KB (827376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77668edfb6bddc597a120d1abc4d2d3bd49079937ead823127afe0093ee3642e`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 13.0 KB (12976 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.4` - linux; ppc64le

```console
$ docker pull traefik@sha256:904d00b37a12fd670c6fc8c2e56f5d1cf927d068e75f362e01bfc2ab787a87a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51802197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76af70530829836acad936bfd80b95121bd6e2e670b3dd45485a91e7879f2093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c884f5e61b441d4901cdb9a4f6b55d488910ad927aa3abe32cbb8b4963b6c2b`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 47.8 MB (47764922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:3804f216242a434a58038d23818cff62a773c51847bda7f75b16c226d6f8b384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f4ced2f8947770e3e135a78555b37d42eb37c4354a957ab285e0df1943e837`

```dockerfile
```

-	Layers:
	-	`sha256:2b234a140882f2b7b712d1397de8b3c99819e10801f47893570e9ce96e63b8dc`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 825.4 KB (825379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f87d532e77998b2a01c1ef79f32e030be1542b903fa47b6eac46cb2150dbcb8`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.4` - linux; riscv64

```console
$ docker pull traefik@sha256:10503d09555de721b57d72e21c8147b353ae7e55a09e3d0d36409da7b61d79da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56455485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec54b9cdac031e36fb2fbb8d07099b21706b9405d9730b85495c8519e5be09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e436610aeaf1067679abbafd70788026b845bb9421f3b7ce99130207145bdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:59 GMT  
		Size: 52.6 MB (52643130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4a395f47a23ab42cfa059fdf6a35b3a11c21ee95d3d30a868cb8855901fd38`  
		Last Modified: Tue, 03 Jun 2025 15:15:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:5c006f458ac1cd3e4e4932bf5dec8705de18a88005c8e14efd9dcab0f13ba340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe933e0dc2b408ea91505a7d76c47f35f707371115e064c091bbb57e59cbedd`

```dockerfile
```

-	Layers:
	-	`sha256:6063ec4f68a493b6767b158b205cd1ef8193689de05f6363a8955aa456101000`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 825.4 KB (825375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a92db796c6c7cb6425d882b8f55c8abee2389f7409954a5e7ca909c1f9c048`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.4` - linux; s390x

```console
$ docker pull traefik@sha256:07942bc395eb18e2ccdff76a5db6ec430330b4f6e9e21de93abc22d38dd7a6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56269856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ae8c552f603f116570604fac0d866bd7ea998a35a072390398bb2769bbe45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042c8a716a75e292fa5080b404a4f60081032cafe22d09079bf3f891e9ee2b9`  
		Last Modified: Tue, 03 Jun 2025 15:15:00 GMT  
		Size: 52.3 MB (52340765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c51a73e866e22cc50e4088a69f1cad9336fa407fb7a875dff86ce82ea4c6c8b`  
		Last Modified: Tue, 03 Jun 2025 15:15:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4` - unknown; unknown

```console
$ docker pull traefik@sha256:8b7777d29fef01c7e3e582eab03eb0d2f4d619fba29fd92baf84c3ca4cad17f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.1 KB (838130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3bcbcce76b9d2874c369b9d7cfc548d91aa722a5266d5ab4cc461d68129044`

```dockerfile
```

-	Layers:
	-	`sha256:13b584c594ba870e6372ee32d863a9d72a542a1dc4c5178717435d6f79b78e6c`  
		Last Modified: Tue, 03 Jun 2025 15:14:56 GMT  
		Size: 825.3 KB (825321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178dcee5ee28bb14fd9e2d73d78bcc55398b12e68063bfff1bb3f757490c05c4`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.4-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e9dfb85bed73e0e8031b9c9a81bb272b8550e8e2e66a0b59ab77970e7095c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v3.4-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:d55b32d19c53ca332f1e0b093a8437b01ba7b841708ffe5c952cf9034c9cd8a4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177905809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ab1def000e52df8a233af9697e9ccbaa4079612aefcc706f08415c78d8e6e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:14:10 GMT
RUN cmd /S /C #(nop) COPY file:9febf6616005a41118af930de9dceb58bbb7c0dfadaddb7bfab3e211ac5bbe26 in \ 
# Tue, 27 May 2025 15:14:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48db22b9277c3bfe0e95c57c3b195f8f1fdd135aacdd2915ef435467e41f961`  
		Last Modified: Tue, 03 Jun 2025 20:17:45 GMT  
		Size: 55.3 MB (55326045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96bdc498b3e64f5942bcf57617b822f6368eae86c524f3d78887cd816ce8667`  
		Last Modified: Tue, 03 Jun 2025 20:17:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25735e6caa059b5973e065e6b9a2f2f6746cbdfbaba54aaadf8703b5b06ee81f`  
		Last Modified: Tue, 03 Jun 2025 20:17:41 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df498a2287fb011505c6829716e35ed011d1d071e7471f2904a6bf81753a5c1a`  
		Last Modified: Tue, 03 Jun 2025 20:17:42 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.4-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4cbc0ec3d96e7458f61766b6a7f20184db198cdd5d3e843990d4ffd5d4776f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v3.4-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:6afe066e8b2138da8f232a83e5323bedc06eb2748b3b14bb426fcc0b02a7ab94
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329464370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878537d0f6cf4c3bc01385bf3b93e83db668959f2390c6853b2f6e829e091238`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:54:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:54:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:54:49 GMT
EXPOSE 80
# Tue, 27 May 2025 14:54:50 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:54:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37ab80d65d0f531dd0dda220ec269bb8d3a64ae4733859bf5cceb7cca8083c4`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c9a42230c171b5f3397c7ed80a1f29f0cdea2a1ac9fd6362a379d3fdd0cb7`  
		Last Modified: Tue, 03 Jun 2025 14:12:47 GMT  
		Size: 55.8 MB (55831084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539ecf95a4c553f7630e2dfc0724182acdc077b42454246064b1e81328be8308`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f437896dd6a4e91f5f8d7f28116f518690a54ca59232a2ebe4f5a11fb48f54`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b93db94dc05cad592e9d27e6cf3ec8bb10a35393168f1c7ea7ec866969a171`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.4.1`

```console
$ docker pull traefik@sha256:cd40ab7bc1f047731d5b22595203812343efcb6538014c4e93221cfc3a77217a
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

### `traefik:v3.4.1` - linux; amd64

```console
$ docker pull traefik@sha256:06b2f92ba6cb9fdc2de99d41c22b862f196871ad55c26269083eaef39dd4fa99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58293647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0a241c8a0a140b0d2142f3f481b2fa847a7f42a1356dc39a8eac9b27df4cf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff649176b021e9351562a500f04ed9750d0e7d04eaa6022c1c6178100e3c78`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 460.2 KB (460201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb594ddbc1285eb9bc5e21f89125fbcf7f370d3f7078638c155337257de4ca5`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 54.2 MB (54190831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c9803dbe740295ae4bc2c7a9257cec09353a41ee212e69bfc8df610e0fe366`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:bd3775e8dc18f0eaff57543193acf32e1c3747e67e6e71364e6276636ba61f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 KB (840081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65c49c68a9e64602c396234e259172a812df05f95ca284a971af5fcb285cf3d`

```dockerfile
```

-	Layers:
	-	`sha256:cf9c8d147592b2181fc4bd2d7dfdebe237ee30fb30121650d63e2e2a70d609bf`  
		Last Modified: Tue, 03 Jun 2025 15:14:44 GMT  
		Size: 827.3 KB (827272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfa0a085791bfb75f2bde4f6dbcdad91138333a1752fa36ccb2ca805fa44a20`  
		Last Modified: Tue, 03 Jun 2025 15:14:46 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.4.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ac48f2ae151717fe49a90e38c92a0a3630f82abdb3e10c8f216b3d2b2e5e18db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53692448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a28e18eb719fd329d0779f8e0da2e3f4a9f569d81ea005a40242d251f3c2a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376947144f2af43212730e00e809e580baa70c1564a7f1c05ce0b5c89a39bfae`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 49.9 MB (49867924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe19f27e5039137d87ded7aa47f3234bf196b95e6a7636f951be0f303fc62b9`  
		Last Modified: Tue, 03 Jun 2025 15:14:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:bde6cb15b218a8146019f1ade9fa1859819d1eb177dc082c3b97c7b0d3445df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75447718047d59fefcc7894e79fc559894fefb231835c5ad7c1f3dd1bf1c79a0`

```dockerfile
```

-	Layers:
	-	`sha256:2514c0d20a1024e7c7d77fb6fa139f6f49f2b85376220c1c74e5ee15fa765ab2`  
		Last Modified: Tue, 03 Jun 2025 15:14:45 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.4.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5ed09f5b4d7df3bb186ba5360e7dca8dc73067ecc5278b4a26f60587db908958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7206871bb3451f03c8939c466c0e63a9e69fa944f4aae62b4be7fe3f74725543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6a72f7e5fd93302d79a7c71fe8a3b655da4a58c354de2a055696206bbe75c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 462.1 KB (462070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30408b989b42117e933e49a16a00bde8712c625b561afa4e231ba172f5a2c8f4`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 50.1 MB (50051133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:ced2a2408769ffb3560fa21b6854287b03e852458a074b5f65df89147a01509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 KB (840352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16424a5a76aa8af2207a2dbecb3a9791c93454915b99af606460d4fd0fcd4f7c`

```dockerfile
```

-	Layers:
	-	`sha256:ea2259fa8cf34c77b492a8fac036ee83b33d37593f00ae9474a90deae0137fdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:47 GMT  
		Size: 827.4 KB (827376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77668edfb6bddc597a120d1abc4d2d3bd49079937ead823127afe0093ee3642e`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 13.0 KB (12976 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.4.1` - linux; ppc64le

```console
$ docker pull traefik@sha256:904d00b37a12fd670c6fc8c2e56f5d1cf927d068e75f362e01bfc2ab787a87a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51802197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76af70530829836acad936bfd80b95121bd6e2e670b3dd45485a91e7879f2093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d6251428fe1da9f0b75bb525a1700f9568411da5e1ca63660f271dcfb93`  
		Last Modified: Tue, 03 Jun 2025 15:14:51 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c884f5e61b441d4901cdb9a4f6b55d488910ad927aa3abe32cbb8b4963b6c2b`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 47.8 MB (47764922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e8b6b347fc61f9555c1fd33ced0681b92103b6d81a1c9931174ba908cbbdc`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:3804f216242a434a58038d23818cff62a773c51847bda7f75b16c226d6f8b384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f4ced2f8947770e3e135a78555b37d42eb37c4354a957ab285e0df1943e837`

```dockerfile
```

-	Layers:
	-	`sha256:2b234a140882f2b7b712d1397de8b3c99819e10801f47893570e9ce96e63b8dc`  
		Last Modified: Tue, 03 Jun 2025 15:14:50 GMT  
		Size: 825.4 KB (825379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f87d532e77998b2a01c1ef79f32e030be1542b903fa47b6eac46cb2150dbcb8`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.4.1` - linux; riscv64

```console
$ docker pull traefik@sha256:10503d09555de721b57d72e21c8147b353ae7e55a09e3d0d36409da7b61d79da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56455485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec54b9cdac031e36fb2fbb8d07099b21706b9405d9730b85495c8519e5be09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 09 May 2025 00:30:57 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e436610aeaf1067679abbafd70788026b845bb9421f3b7ce99130207145bdb`  
		Last Modified: Tue, 03 Jun 2025 15:14:59 GMT  
		Size: 52.6 MB (52643130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4a395f47a23ab42cfa059fdf6a35b3a11c21ee95d3d30a868cb8855901fd38`  
		Last Modified: Tue, 03 Jun 2025 15:15:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:5c006f458ac1cd3e4e4932bf5dec8705de18a88005c8e14efd9dcab0f13ba340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.3 KB (838254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe933e0dc2b408ea91505a7d76c47f35f707371115e064c091bbb57e59cbedd`

```dockerfile
```

-	Layers:
	-	`sha256:6063ec4f68a493b6767b158b205cd1ef8193689de05f6363a8955aa456101000`  
		Last Modified: Tue, 03 Jun 2025 15:14:52 GMT  
		Size: 825.4 KB (825375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a92db796c6c7cb6425d882b8f55c8abee2389f7409954a5e7ca909c1f9c048`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.4.1` - linux; s390x

```console
$ docker pull traefik@sha256:07942bc395eb18e2ccdff76a5db6ec430330b4f6e9e21de93abc22d38dd7a6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56269856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ae8c552f603f116570604fac0d866bd7ea998a35a072390398bb2769bbe45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 27 May 2025 12:53:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 27 May 2025 12:53:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 27 May 2025 12:53:59 GMT
COPY entrypoint.sh / # buildkit
# Tue, 27 May 2025 12:53:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 May 2025 12:53:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 May 2025 12:53:59 GMT
CMD ["traefik"]
# Tue, 27 May 2025 12:53:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c36ada1f7f62c015816565ca88f00a59a6dc0f47c3b03fab0df051cbd6720`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 461.2 KB (461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042c8a716a75e292fa5080b404a4f60081032cafe22d09079bf3f891e9ee2b9`  
		Last Modified: Tue, 03 Jun 2025 15:15:00 GMT  
		Size: 52.3 MB (52340765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c51a73e866e22cc50e4088a69f1cad9336fa407fb7a875dff86ce82ea4c6c8b`  
		Last Modified: Tue, 03 Jun 2025 15:15:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.4.1` - unknown; unknown

```console
$ docker pull traefik@sha256:8b7777d29fef01c7e3e582eab03eb0d2f4d619fba29fd92baf84c3ca4cad17f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.1 KB (838130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3bcbcce76b9d2874c369b9d7cfc548d91aa722a5266d5ab4cc461d68129044`

```dockerfile
```

-	Layers:
	-	`sha256:13b584c594ba870e6372ee32d863a9d72a542a1dc4c5178717435d6f79b78e6c`  
		Last Modified: Tue, 03 Jun 2025 15:14:56 GMT  
		Size: 825.3 KB (825321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178dcee5ee28bb14fd9e2d73d78bcc55398b12e68063bfff1bb3f757490c05c4`  
		Last Modified: Tue, 03 Jun 2025 15:14:58 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.4.1-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5e9dfb85bed73e0e8031b9c9a81bb272b8550e8e2e66a0b59ab77970e7095c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v3.4.1-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:d55b32d19c53ca332f1e0b093a8437b01ba7b841708ffe5c952cf9034c9cd8a4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177905809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556ab1def000e52df8a233af9697e9ccbaa4079612aefcc706f08415c78d8e6e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 27 May 2025 15:14:10 GMT
RUN cmd /S /C #(nop) COPY file:9febf6616005a41118af930de9dceb58bbb7c0dfadaddb7bfab3e211ac5bbe26 in \ 
# Tue, 27 May 2025 15:14:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 15:14:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48db22b9277c3bfe0e95c57c3b195f8f1fdd135aacdd2915ef435467e41f961`  
		Last Modified: Tue, 03 Jun 2025 20:17:45 GMT  
		Size: 55.3 MB (55326045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96bdc498b3e64f5942bcf57617b822f6368eae86c524f3d78887cd816ce8667`  
		Last Modified: Tue, 03 Jun 2025 20:17:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25735e6caa059b5973e065e6b9a2f2f6746cbdfbaba54aaadf8703b5b06ee81f`  
		Last Modified: Tue, 03 Jun 2025 20:17:41 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df498a2287fb011505c6829716e35ed011d1d071e7471f2904a6bf81753a5c1a`  
		Last Modified: Tue, 03 Jun 2025 20:17:42 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.4.1-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4cbc0ec3d96e7458f61766b6a7f20184db198cdd5d3e843990d4ffd5d4776f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:v3.4.1-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:6afe066e8b2138da8f232a83e5323bedc06eb2748b3b14bb426fcc0b02a7ab94
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329464370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878537d0f6cf4c3bc01385bf3b93e83db668959f2390c6853b2f6e829e091238`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:54:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:54:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:54:49 GMT
EXPOSE 80
# Tue, 27 May 2025 14:54:50 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:54:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37ab80d65d0f531dd0dda220ec269bb8d3a64ae4733859bf5cceb7cca8083c4`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c9a42230c171b5f3397c7ed80a1f29f0cdea2a1ac9fd6362a379d3fdd0cb7`  
		Last Modified: Tue, 03 Jun 2025 14:12:47 GMT  
		Size: 55.8 MB (55831084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539ecf95a4c553f7630e2dfc0724182acdc077b42454246064b1e81328be8308`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f437896dd6a4e91f5f8d7f28116f518690a54ca59232a2ebe4f5a11fb48f54`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b93db94dc05cad592e9d27e6cf3ec8bb10a35393168f1c7ea7ec866969a171`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4cbc0ec3d96e7458f61766b6a7f20184db198cdd5d3e843990d4ffd5d4776f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:6afe066e8b2138da8f232a83e5323bedc06eb2748b3b14bb426fcc0b02a7ab94
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329464370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878537d0f6cf4c3bc01385bf3b93e83db668959f2390c6853b2f6e829e091238`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 14:54:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 14:54:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.1/traefik_v3.4.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 27 May 2025 14:54:49 GMT
EXPOSE 80
# Tue, 27 May 2025 14:54:50 GMT
ENTRYPOINT ["/traefik"]
# Tue, 27 May 2025 14:54:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37ab80d65d0f531dd0dda220ec269bb8d3a64ae4733859bf5cceb7cca8083c4`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c9a42230c171b5f3397c7ed80a1f29f0cdea2a1ac9fd6362a379d3fdd0cb7`  
		Last Modified: Tue, 03 Jun 2025 14:12:47 GMT  
		Size: 55.8 MB (55831084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539ecf95a4c553f7630e2dfc0724182acdc077b42454246064b1e81328be8308`  
		Last Modified: Tue, 03 Jun 2025 14:12:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f437896dd6a4e91f5f8d7f28116f518690a54ca59232a2ebe4f5a11fb48f54`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b93db94dc05cad592e9d27e6cf3ec8bb10a35393168f1c7ea7ec866969a171`  
		Last Modified: Tue, 03 Jun 2025 14:12:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
