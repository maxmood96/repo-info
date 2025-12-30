<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.34`](#traefik21134)
-	[`traefik:2.11.34-nanoserver-ltsc2022`](#traefik21134-nanoserver-ltsc2022)
-	[`traefik:2.11.34-windowsservercore-ltsc2022`](#traefik21134-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.6`](#traefik366)
-	[`traefik:3.6.6-nanoserver-ltsc2022`](#traefik366-nanoserver-ltsc2022)
-	[`traefik:3.6.6-windowsservercore-ltsc2022`](#traefik366-windowsservercore-ltsc2022)
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
-	[`traefik:v2.11.34`](#traefikv21134)
-	[`traefik:v2.11.34-nanoserver-ltsc2022`](#traefikv21134-nanoserver-ltsc2022)
-	[`traefik:v2.11.34-windowsservercore-ltsc2022`](#traefikv21134-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.6`](#traefikv366)
-	[`traefik:v3.6.6-nanoserver-ltsc2022`](#traefikv366-nanoserver-ltsc2022)
-	[`traefik:v3.6.6-windowsservercore-ltsc2022`](#traefikv366-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:ec06628f2693a846bdf0d84a20e1c2d13026963370c422ef3c301a0ec95122f8
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
$ docker pull traefik@sha256:dde8db8bf8a8c2b68181a5bf51bad71b145427f8f42d85543c063a2878c5430c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51045034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c73645b5a95f5868c73795f8be36f1b016096ba044ca898ec4ec6bdf67f49a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:32 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460d3ed754bcad38468a7e39c71a8ae0bd2a6e3f0fe243a6b06bf93fdc341ac`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf71e0662417ca9e09cdcb8dbe1ceaab2d24ca270364186656c3989fde4dd89f`  
		Last Modified: Mon, 29 Dec 2025 22:15:09 GMT  
		Size: 46.7 MB (46723619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccabf121282a73971c74c565541d08d7858279fd78860d4f539d7e055925dae`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:7b80c6aa4cb2a906161bb1363e3bab6e372c4fdfeb8e0905a5678b98b674a487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea0349cca0e8260efbb16808875c70ddb72cbe8efa0543b79bad57767ebdf79`

```dockerfile
```

-	Layers:
	-	`sha256:6fe270a0fa6590e1551a1ee4f6efd31418369e213caa83e16a1ca434588b3387`  
		Last Modified: Tue, 30 Dec 2025 01:10:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63df6effd3e9e12b969fcfa50ab1e9b2acaff2e83f72f2446a4d786944098fd`  
		Last Modified: Tue, 30 Dec 2025 01:10:33 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7a6812ddc9c24690d7a5a499003dc945857a175e7f5dda6981d1f7274749a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6243483a0b396d4fe7d53eaaf3249de044c8dc788057696eb33a805148646fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:05 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9a25acc457736a96b93a0281b7736208e4dc00987f78b5a473bb17e3487d70`  
		Last Modified: Mon, 29 Dec 2025 22:12:24 GMT  
		Size: 42.8 MB (42792487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2555957720388bf7fad85128cde658f26ed9c0878ea5e3587e5d61b776b17b`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:386b9114b5a54555c4beb1d339812a25a03b2a79342fc9c0a77f4a12689188c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0bdf4205aa969b25895232ca1c8c3366ef418998b9cad892302307b58a1d05`

```dockerfile
```

-	Layers:
	-	`sha256:9d9d0e6ec35917ebf98a85505427f212b0def2618d49faab2a9e6b98a4d12f1f`  
		Last Modified: Tue, 30 Dec 2025 01:10:36 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:068c114909900cf35accd4cb1e661d47fb16d4a9fc14cba2c991c5ec82143804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47288453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf94b991a93fcc4f35ceaa5860a12210bb8a3773a114e6dfbee0c00b361f1c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:27 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeadd60e258df383b0cc98606207bf109ef121df1971f4462b45ec54ee9f318`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 463.0 KB (462969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf7d2a33fd20248262d1c4cf1a1e70d0443286f144ff431455a223caa65601`  
		Last Modified: Mon, 29 Dec 2025 22:15:03 GMT  
		Size: 42.6 MB (42629375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c517dbb8d79767704a0d7fa570e4c08d418574401c1f3ed2aa365160213329d`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:c388de6c2b71abf77689d398e067a6bd8c9e90557af9ce13025e1e6a1766f53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb04cbf1de6bf71b2a625f6ccd7c33fdd963d4f1afd226100807e0e105080a7`

```dockerfile
```

-	Layers:
	-	`sha256:dbe071740321aed9566e9a7ce2de44c21da3fd82adef85df41ec2e1569447ddc`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4510a9494ca18bef567409f7d6cd142fde24682356b6be783ebb1f81b6a01b`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:3c36c86703831acb8abb0a22a2841be45264d32be03ee0076c136c81b12a1079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ef1b95ee8ae6ee6556e92f98edc54ea617c1925464e45e91d54911209e5e6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bedccbda7f6c026594b1bac44b809089174355a4e044e6ebfdc6286c9588756`  
		Last Modified: Mon, 29 Dec 2025 22:12:28 GMT  
		Size: 41.0 MB (40951452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a3d0d79b5160993f0c0a41639ed185b7a0f0bd4f4f8237368605fa4674ee2`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:4b586213bdae7d3e4ee91a8608d35500d306e36a06bc41c7f240ff60b6a15681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6810ccb80adb216f5b638e0a0253b8f04ebf89e679860c97482dde9e9bcb0c26`

```dockerfile
```

-	Layers:
	-	`sha256:595c3b71af7b44b03435988a57a0d7a6107af8e394fe81f30537110e5049411f`  
		Last Modified: Tue, 30 Dec 2025 01:10:44 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a33507a6c12c57f9d79818ef6f55e323f54095506204186caeef90c1cfea6f4`  
		Last Modified: Tue, 30 Dec 2025 01:10:45 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:d885398c11e1e2255f530086a8a38dd5703151f3d01ac65f37fa0ed677b3790d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49371197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423faff905cf66d01d4b68a15665db0f1efae634854bab7c395d35c3be94f799`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:17:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:17:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:17:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11e3a76c0fe809fef053b28f4223652f383a7155827cca3f996e6b5ad99347b`  
		Last Modified: Mon, 29 Dec 2025 22:22:50 GMT  
		Size: 45.3 MB (45325697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cded5f8ab82a089eef5c39ab4214eda5d15f737ee5865b41892a6b2a62423c`  
		Last Modified: Mon, 29 Dec 2025 22:22:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:cfd66037b02e24fbc4bf4e26ae9279b6f9cfd9034c24a39f5e34d0c15ae0bce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2d62009ccbbbac92862f457a0144b820e0544d6763726310a66361b80fbf9e`

```dockerfile
```

-	Layers:
	-	`sha256:745a3f8aa84f981044005ec6c920f6bb1dad5840785ce877c136dd5e098ed262`  
		Last Modified: Tue, 30 Dec 2025 01:10:48 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86df83cb3765bdd568c1f258f62e4e5a4b1fdaa5bebcdd69e11e5f9eba1d7ac9`  
		Last Modified: Tue, 30 Dec 2025 01:10:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:c8e0bcf5d966979dc1c7e217f9e49c4c4d37693e18a2e2521d82884dbf0b6f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49441303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2846fbc72078df664092ad73630af388378efe6d44006852635652c5f704974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:52 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa895b2e41ff3a43aa2644cdbbbf2b91678301e65d1804cc3ddd31bad02b85b`  
		Last Modified: Mon, 29 Dec 2025 22:12:55 GMT  
		Size: 45.3 MB (45254880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87e0c0d53b7263e6598aa3669471a57768b8f4f67198215ff65e4269eacf11`  
		Last Modified: Mon, 29 Dec 2025 22:12:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:9e2e342705e2de6737da28772b5f86362dd121c687d450ba873ca82d90f04e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282a7969c762c223edcd680164bca446cfe6172b44fdb559d211302bf1fcf083`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cf47226e83925db8f301df6f56d2a03543e2e5a7cf6b034bc1765b4e65e58`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a52bfeb8caa44a23436add6d2771844b859fa3c5503f91b4648602975bd3845`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e412515e710521fa7986c58e5d1c6760081b86409fbd7ada71c280008f6a7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:583653b643ac3f1f46003cb5420a6020ebbab38b4223e42dedccb73bdfb5a58c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173878068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3deb70fa9dfc3d168fd0f74db8842e94f92d1a34c9d1603651c6e4f2ae7206`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:26:01 GMT
RUN cmd /S /C #(nop) COPY file:bb401afdd9d3934a7a4f9b92a64ab967d454bd5889893f3e6bb99650a87af92c in \ 
# Mon, 29 Dec 2025 22:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282ed5ab3ad2747524afcc687c7af1981fee639f80841907ec190c541a8225a`  
		Last Modified: Mon, 29 Dec 2025 22:26:27 GMT  
		Size: 47.5 MB (47516598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c830cf11eb297146e37f3dc86b7d3eb61623f5ed17b3ad2c799157b35e1e24a9`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf10c5e839cb5e9a0e4e608989f75e46e276c01b90f16cf02628c3317ffe07e`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c62f03aa8b4ff4fbb3e842cb32d489adc9b7ff1cd733fbfdd369a333f7ca74`  
		Last Modified: Mon, 29 Dec 2025 22:26:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:89357a7b41ff2c571cfe33f4102c7933b0f7fb1c53a41bae1a30ddb83e7d7dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:9047cfdfe358271d4a6760faf9809787c81e8a906b0e5a3b341a0abbfdf9cb4a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828029861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76acbfb4dc298a43b62470fe1dd8b0b4093ce9938b3d3a328ef1143141a61c6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:20:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:20:12 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:20:13 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:20:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d4f4c744a59ac227520b5e733ac7e2c3bb8792ebea040dedecf0dd290fbb44`  
		Last Modified: Mon, 29 Dec 2025 22:20:47 GMT  
		Size: 48.1 MB (48145327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c42cd93e2c4a2994963205e46b4ec55d2b2f4c4d5d38f34f8f4d10e4d0625`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a558267a225392878a35ac6136c8729fe970c469f2d9bacd35f04d21568a2`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b61952c0488abc61e0aa13adc437b892be0123d5a2807c46192869a8e19f42`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:ec06628f2693a846bdf0d84a20e1c2d13026963370c422ef3c301a0ec95122f8
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
$ docker pull traefik@sha256:dde8db8bf8a8c2b68181a5bf51bad71b145427f8f42d85543c063a2878c5430c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51045034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c73645b5a95f5868c73795f8be36f1b016096ba044ca898ec4ec6bdf67f49a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:32 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460d3ed754bcad38468a7e39c71a8ae0bd2a6e3f0fe243a6b06bf93fdc341ac`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf71e0662417ca9e09cdcb8dbe1ceaab2d24ca270364186656c3989fde4dd89f`  
		Last Modified: Mon, 29 Dec 2025 22:15:09 GMT  
		Size: 46.7 MB (46723619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccabf121282a73971c74c565541d08d7858279fd78860d4f539d7e055925dae`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:7b80c6aa4cb2a906161bb1363e3bab6e372c4fdfeb8e0905a5678b98b674a487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea0349cca0e8260efbb16808875c70ddb72cbe8efa0543b79bad57767ebdf79`

```dockerfile
```

-	Layers:
	-	`sha256:6fe270a0fa6590e1551a1ee4f6efd31418369e213caa83e16a1ca434588b3387`  
		Last Modified: Tue, 30 Dec 2025 01:10:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63df6effd3e9e12b969fcfa50ab1e9b2acaff2e83f72f2446a4d786944098fd`  
		Last Modified: Tue, 30 Dec 2025 01:10:33 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7a6812ddc9c24690d7a5a499003dc945857a175e7f5dda6981d1f7274749a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6243483a0b396d4fe7d53eaaf3249de044c8dc788057696eb33a805148646fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:05 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9a25acc457736a96b93a0281b7736208e4dc00987f78b5a473bb17e3487d70`  
		Last Modified: Mon, 29 Dec 2025 22:12:24 GMT  
		Size: 42.8 MB (42792487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2555957720388bf7fad85128cde658f26ed9c0878ea5e3587e5d61b776b17b`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:386b9114b5a54555c4beb1d339812a25a03b2a79342fc9c0a77f4a12689188c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0bdf4205aa969b25895232ca1c8c3366ef418998b9cad892302307b58a1d05`

```dockerfile
```

-	Layers:
	-	`sha256:9d9d0e6ec35917ebf98a85505427f212b0def2618d49faab2a9e6b98a4d12f1f`  
		Last Modified: Tue, 30 Dec 2025 01:10:36 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:068c114909900cf35accd4cb1e661d47fb16d4a9fc14cba2c991c5ec82143804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47288453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf94b991a93fcc4f35ceaa5860a12210bb8a3773a114e6dfbee0c00b361f1c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:27 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeadd60e258df383b0cc98606207bf109ef121df1971f4462b45ec54ee9f318`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 463.0 KB (462969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf7d2a33fd20248262d1c4cf1a1e70d0443286f144ff431455a223caa65601`  
		Last Modified: Mon, 29 Dec 2025 22:15:03 GMT  
		Size: 42.6 MB (42629375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c517dbb8d79767704a0d7fa570e4c08d418574401c1f3ed2aa365160213329d`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c388de6c2b71abf77689d398e067a6bd8c9e90557af9ce13025e1e6a1766f53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb04cbf1de6bf71b2a625f6ccd7c33fdd963d4f1afd226100807e0e105080a7`

```dockerfile
```

-	Layers:
	-	`sha256:dbe071740321aed9566e9a7ce2de44c21da3fd82adef85df41ec2e1569447ddc`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4510a9494ca18bef567409f7d6cd142fde24682356b6be783ebb1f81b6a01b`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:3c36c86703831acb8abb0a22a2841be45264d32be03ee0076c136c81b12a1079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ef1b95ee8ae6ee6556e92f98edc54ea617c1925464e45e91d54911209e5e6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bedccbda7f6c026594b1bac44b809089174355a4e044e6ebfdc6286c9588756`  
		Last Modified: Mon, 29 Dec 2025 22:12:28 GMT  
		Size: 41.0 MB (40951452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a3d0d79b5160993f0c0a41639ed185b7a0f0bd4f4f8237368605fa4674ee2`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:4b586213bdae7d3e4ee91a8608d35500d306e36a06bc41c7f240ff60b6a15681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6810ccb80adb216f5b638e0a0253b8f04ebf89e679860c97482dde9e9bcb0c26`

```dockerfile
```

-	Layers:
	-	`sha256:595c3b71af7b44b03435988a57a0d7a6107af8e394fe81f30537110e5049411f`  
		Last Modified: Tue, 30 Dec 2025 01:10:44 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a33507a6c12c57f9d79818ef6f55e323f54095506204186caeef90c1cfea6f4`  
		Last Modified: Tue, 30 Dec 2025 01:10:45 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:d885398c11e1e2255f530086a8a38dd5703151f3d01ac65f37fa0ed677b3790d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49371197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423faff905cf66d01d4b68a15665db0f1efae634854bab7c395d35c3be94f799`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:17:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:17:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:17:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11e3a76c0fe809fef053b28f4223652f383a7155827cca3f996e6b5ad99347b`  
		Last Modified: Mon, 29 Dec 2025 22:22:50 GMT  
		Size: 45.3 MB (45325697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cded5f8ab82a089eef5c39ab4214eda5d15f737ee5865b41892a6b2a62423c`  
		Last Modified: Mon, 29 Dec 2025 22:22:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:cfd66037b02e24fbc4bf4e26ae9279b6f9cfd9034c24a39f5e34d0c15ae0bce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2d62009ccbbbac92862f457a0144b820e0544d6763726310a66361b80fbf9e`

```dockerfile
```

-	Layers:
	-	`sha256:745a3f8aa84f981044005ec6c920f6bb1dad5840785ce877c136dd5e098ed262`  
		Last Modified: Tue, 30 Dec 2025 01:10:48 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86df83cb3765bdd568c1f258f62e4e5a4b1fdaa5bebcdd69e11e5f9eba1d7ac9`  
		Last Modified: Tue, 30 Dec 2025 01:10:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:c8e0bcf5d966979dc1c7e217f9e49c4c4d37693e18a2e2521d82884dbf0b6f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49441303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2846fbc72078df664092ad73630af388378efe6d44006852635652c5f704974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:52 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa895b2e41ff3a43aa2644cdbbbf2b91678301e65d1804cc3ddd31bad02b85b`  
		Last Modified: Mon, 29 Dec 2025 22:12:55 GMT  
		Size: 45.3 MB (45254880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87e0c0d53b7263e6598aa3669471a57768b8f4f67198215ff65e4269eacf11`  
		Last Modified: Mon, 29 Dec 2025 22:12:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:9e2e342705e2de6737da28772b5f86362dd121c687d450ba873ca82d90f04e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282a7969c762c223edcd680164bca446cfe6172b44fdb559d211302bf1fcf083`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cf47226e83925db8f301df6f56d2a03543e2e5a7cf6b034bc1765b4e65e58`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a52bfeb8caa44a23436add6d2771844b859fa3c5503f91b4648602975bd3845`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e412515e710521fa7986c58e5d1c6760081b86409fbd7ada71c280008f6a7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:583653b643ac3f1f46003cb5420a6020ebbab38b4223e42dedccb73bdfb5a58c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173878068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3deb70fa9dfc3d168fd0f74db8842e94f92d1a34c9d1603651c6e4f2ae7206`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:26:01 GMT
RUN cmd /S /C #(nop) COPY file:bb401afdd9d3934a7a4f9b92a64ab967d454bd5889893f3e6bb99650a87af92c in \ 
# Mon, 29 Dec 2025 22:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282ed5ab3ad2747524afcc687c7af1981fee639f80841907ec190c541a8225a`  
		Last Modified: Mon, 29 Dec 2025 22:26:27 GMT  
		Size: 47.5 MB (47516598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c830cf11eb297146e37f3dc86b7d3eb61623f5ed17b3ad2c799157b35e1e24a9`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf10c5e839cb5e9a0e4e608989f75e46e276c01b90f16cf02628c3317ffe07e`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c62f03aa8b4ff4fbb3e842cb32d489adc9b7ff1cd733fbfdd369a333f7ca74`  
		Last Modified: Mon, 29 Dec 2025 22:26:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:89357a7b41ff2c571cfe33f4102c7933b0f7fb1c53a41bae1a30ddb83e7d7dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:9047cfdfe358271d4a6760faf9809787c81e8a906b0e5a3b341a0abbfdf9cb4a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828029861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76acbfb4dc298a43b62470fe1dd8b0b4093ce9938b3d3a328ef1143141a61c6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:20:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:20:12 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:20:13 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:20:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d4f4c744a59ac227520b5e733ac7e2c3bb8792ebea040dedecf0dd290fbb44`  
		Last Modified: Mon, 29 Dec 2025 22:20:47 GMT  
		Size: 48.1 MB (48145327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c42cd93e2c4a2994963205e46b4ec55d2b2f4c4d5d38f34f8f4d10e4d0625`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a558267a225392878a35ac6136c8729fe970c469f2d9bacd35f04d21568a2`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b61952c0488abc61e0aa13adc437b892be0123d5a2807c46192869a8e19f42`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.34`

```console
$ docker pull traefik@sha256:ec06628f2693a846bdf0d84a20e1c2d13026963370c422ef3c301a0ec95122f8
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

### `traefik:2.11.34` - linux; amd64

```console
$ docker pull traefik@sha256:dde8db8bf8a8c2b68181a5bf51bad71b145427f8f42d85543c063a2878c5430c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51045034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c73645b5a95f5868c73795f8be36f1b016096ba044ca898ec4ec6bdf67f49a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:32 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460d3ed754bcad38468a7e39c71a8ae0bd2a6e3f0fe243a6b06bf93fdc341ac`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf71e0662417ca9e09cdcb8dbe1ceaab2d24ca270364186656c3989fde4dd89f`  
		Last Modified: Mon, 29 Dec 2025 22:15:09 GMT  
		Size: 46.7 MB (46723619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccabf121282a73971c74c565541d08d7858279fd78860d4f539d7e055925dae`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:7b80c6aa4cb2a906161bb1363e3bab6e372c4fdfeb8e0905a5678b98b674a487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea0349cca0e8260efbb16808875c70ddb72cbe8efa0543b79bad57767ebdf79`

```dockerfile
```

-	Layers:
	-	`sha256:6fe270a0fa6590e1551a1ee4f6efd31418369e213caa83e16a1ca434588b3387`  
		Last Modified: Tue, 30 Dec 2025 01:10:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63df6effd3e9e12b969fcfa50ab1e9b2acaff2e83f72f2446a4d786944098fd`  
		Last Modified: Tue, 30 Dec 2025 01:10:33 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7a6812ddc9c24690d7a5a499003dc945857a175e7f5dda6981d1f7274749a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6243483a0b396d4fe7d53eaaf3249de044c8dc788057696eb33a805148646fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:05 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9a25acc457736a96b93a0281b7736208e4dc00987f78b5a473bb17e3487d70`  
		Last Modified: Mon, 29 Dec 2025 22:12:24 GMT  
		Size: 42.8 MB (42792487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2555957720388bf7fad85128cde658f26ed9c0878ea5e3587e5d61b776b17b`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:386b9114b5a54555c4beb1d339812a25a03b2a79342fc9c0a77f4a12689188c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0bdf4205aa969b25895232ca1c8c3366ef418998b9cad892302307b58a1d05`

```dockerfile
```

-	Layers:
	-	`sha256:9d9d0e6ec35917ebf98a85505427f212b0def2618d49faab2a9e6b98a4d12f1f`  
		Last Modified: Tue, 30 Dec 2025 01:10:36 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:068c114909900cf35accd4cb1e661d47fb16d4a9fc14cba2c991c5ec82143804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47288453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf94b991a93fcc4f35ceaa5860a12210bb8a3773a114e6dfbee0c00b361f1c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:27 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeadd60e258df383b0cc98606207bf109ef121df1971f4462b45ec54ee9f318`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 463.0 KB (462969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf7d2a33fd20248262d1c4cf1a1e70d0443286f144ff431455a223caa65601`  
		Last Modified: Mon, 29 Dec 2025 22:15:03 GMT  
		Size: 42.6 MB (42629375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c517dbb8d79767704a0d7fa570e4c08d418574401c1f3ed2aa365160213329d`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:c388de6c2b71abf77689d398e067a6bd8c9e90557af9ce13025e1e6a1766f53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb04cbf1de6bf71b2a625f6ccd7c33fdd963d4f1afd226100807e0e105080a7`

```dockerfile
```

-	Layers:
	-	`sha256:dbe071740321aed9566e9a7ce2de44c21da3fd82adef85df41ec2e1569447ddc`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4510a9494ca18bef567409f7d6cd142fde24682356b6be783ebb1f81b6a01b`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.34` - linux; ppc64le

```console
$ docker pull traefik@sha256:3c36c86703831acb8abb0a22a2841be45264d32be03ee0076c136c81b12a1079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ef1b95ee8ae6ee6556e92f98edc54ea617c1925464e45e91d54911209e5e6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bedccbda7f6c026594b1bac44b809089174355a4e044e6ebfdc6286c9588756`  
		Last Modified: Mon, 29 Dec 2025 22:12:28 GMT  
		Size: 41.0 MB (40951452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a3d0d79b5160993f0c0a41639ed185b7a0f0bd4f4f8237368605fa4674ee2`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:4b586213bdae7d3e4ee91a8608d35500d306e36a06bc41c7f240ff60b6a15681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6810ccb80adb216f5b638e0a0253b8f04ebf89e679860c97482dde9e9bcb0c26`

```dockerfile
```

-	Layers:
	-	`sha256:595c3b71af7b44b03435988a57a0d7a6107af8e394fe81f30537110e5049411f`  
		Last Modified: Tue, 30 Dec 2025 01:10:44 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a33507a6c12c57f9d79818ef6f55e323f54095506204186caeef90c1cfea6f4`  
		Last Modified: Tue, 30 Dec 2025 01:10:45 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.34` - linux; riscv64

```console
$ docker pull traefik@sha256:d885398c11e1e2255f530086a8a38dd5703151f3d01ac65f37fa0ed677b3790d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49371197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423faff905cf66d01d4b68a15665db0f1efae634854bab7c395d35c3be94f799`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:17:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:17:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:17:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11e3a76c0fe809fef053b28f4223652f383a7155827cca3f996e6b5ad99347b`  
		Last Modified: Mon, 29 Dec 2025 22:22:50 GMT  
		Size: 45.3 MB (45325697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cded5f8ab82a089eef5c39ab4214eda5d15f737ee5865b41892a6b2a62423c`  
		Last Modified: Mon, 29 Dec 2025 22:22:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:cfd66037b02e24fbc4bf4e26ae9279b6f9cfd9034c24a39f5e34d0c15ae0bce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2d62009ccbbbac92862f457a0144b820e0544d6763726310a66361b80fbf9e`

```dockerfile
```

-	Layers:
	-	`sha256:745a3f8aa84f981044005ec6c920f6bb1dad5840785ce877c136dd5e098ed262`  
		Last Modified: Tue, 30 Dec 2025 01:10:48 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86df83cb3765bdd568c1f258f62e4e5a4b1fdaa5bebcdd69e11e5f9eba1d7ac9`  
		Last Modified: Tue, 30 Dec 2025 01:10:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.34` - linux; s390x

```console
$ docker pull traefik@sha256:c8e0bcf5d966979dc1c7e217f9e49c4c4d37693e18a2e2521d82884dbf0b6f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49441303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2846fbc72078df664092ad73630af388378efe6d44006852635652c5f704974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:52 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa895b2e41ff3a43aa2644cdbbbf2b91678301e65d1804cc3ddd31bad02b85b`  
		Last Modified: Mon, 29 Dec 2025 22:12:55 GMT  
		Size: 45.3 MB (45254880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87e0c0d53b7263e6598aa3669471a57768b8f4f67198215ff65e4269eacf11`  
		Last Modified: Mon, 29 Dec 2025 22:12:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:9e2e342705e2de6737da28772b5f86362dd121c687d450ba873ca82d90f04e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282a7969c762c223edcd680164bca446cfe6172b44fdb559d211302bf1fcf083`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cf47226e83925db8f301df6f56d2a03543e2e5a7cf6b034bc1765b4e65e58`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a52bfeb8caa44a23436add6d2771844b859fa3c5503f91b4648602975bd3845`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.34-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e412515e710521fa7986c58e5d1c6760081b86409fbd7ada71c280008f6a7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11.34-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:583653b643ac3f1f46003cb5420a6020ebbab38b4223e42dedccb73bdfb5a58c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173878068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3deb70fa9dfc3d168fd0f74db8842e94f92d1a34c9d1603651c6e4f2ae7206`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:26:01 GMT
RUN cmd /S /C #(nop) COPY file:bb401afdd9d3934a7a4f9b92a64ab967d454bd5889893f3e6bb99650a87af92c in \ 
# Mon, 29 Dec 2025 22:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282ed5ab3ad2747524afcc687c7af1981fee639f80841907ec190c541a8225a`  
		Last Modified: Mon, 29 Dec 2025 22:26:27 GMT  
		Size: 47.5 MB (47516598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c830cf11eb297146e37f3dc86b7d3eb61623f5ed17b3ad2c799157b35e1e24a9`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf10c5e839cb5e9a0e4e608989f75e46e276c01b90f16cf02628c3317ffe07e`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c62f03aa8b4ff4fbb3e842cb32d489adc9b7ff1cd733fbfdd369a333f7ca74`  
		Last Modified: Mon, 29 Dec 2025 22:26:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.34-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:89357a7b41ff2c571cfe33f4102c7933b0f7fb1c53a41bae1a30ddb83e7d7dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11.34-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:9047cfdfe358271d4a6760faf9809787c81e8a906b0e5a3b341a0abbfdf9cb4a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828029861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76acbfb4dc298a43b62470fe1dd8b0b4093ce9938b3d3a328ef1143141a61c6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:20:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:20:12 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:20:13 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:20:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d4f4c744a59ac227520b5e733ac7e2c3bb8792ebea040dedecf0dd290fbb44`  
		Last Modified: Mon, 29 Dec 2025 22:20:47 GMT  
		Size: 48.1 MB (48145327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c42cd93e2c4a2994963205e46b4ec55d2b2f4c4d5d38f34f8f4d10e4d0625`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a558267a225392878a35ac6136c8729fe970c469f2d9bacd35f04d21568a2`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b61952c0488abc61e0aa13adc437b892be0123d5a2807c46192869a8e19f42`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:82d3d16dde0474a51fef00b28de143d48b67f7a27453224d5e7b5aaefff26a97
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
$ docker pull traefik@sha256:13e903c820dfeab5cb464ca6cc9f3b276317f768e324402f440cd3472f3612b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51976248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f174a52e1993a764172bba2c07106a766f2895b2b069a19c7d3bb6f69a18d222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:25 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a471ba94e701f551e79684073e592976607816526d57a987948bff6526c5b`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0802690440f2ca58ae524161b78276377a7a1b65b3f8f6c5053ffabb41708d54`  
		Last Modified: Mon, 29 Dec 2025 22:14:59 GMT  
		Size: 47.7 MB (47654821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e800de571d9f8e3e1570b7ab6ffa6cf7518881c2467f3b4ed474c5332aee3`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:00a627efcd6fc72b53d3bdd7a4ccfa21a4b6ed7f733c3388ed4cc08255f2309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.2 KB (854240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64e165bdaee378a18e512759d5d70d3c7a5dd930282041a764309dcfce32bac`

```dockerfile
```

-	Layers:
	-	`sha256:ff45197c317b2ca934a8cc34ddb376986be02b75920b99d313d539e6e7c911fa`  
		Last Modified: Tue, 30 Dec 2025 01:11:08 GMT  
		Size: 841.5 KB (841474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86fb8844e05b2481883284fb064a496d50c1a26502d834595358d8626eb4947`  
		Last Modified: Tue, 30 Dec 2025 01:11:09 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5457c0a157f7ed95be8253228daf32bba1a12ae1db68ba0337fee123623c347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47249818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c44ed4360eecfed4fbcbfa09e59c09eeea8e674776865aa3fc1af12df3ad9e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:26 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f336e0c0ee4704e0d01821f3ad4ea570e26819a11a2b63dbb387cf34084e4`  
		Last Modified: Mon, 29 Dec 2025 22:12:42 GMT  
		Size: 43.2 MB (43219572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b178f7eca0fa59dd94e45d3d21766dca74576e55362c4962bf9b8ceec0d72572`  
		Last Modified: Mon, 29 Dec 2025 22:12:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:a80f6381e2f7d4ad95451ebe1f7f4bc0d17ec0a8abf35d2a042d68ac291db1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5061d5772660ee643e094c24fd496931f45d553812861885b99cf369df7de503`

```dockerfile
```

-	Layers:
	-	`sha256:ab584a1e249e5e6a4f4a0ceb6f89a8dff471278819ca51a8c8936df3072f5f25`  
		Last Modified: Tue, 30 Dec 2025 01:11:12 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f3e50962d4a55032f1bcb106d9d9e00a62f9500f07d48beea58ea88ef29cd819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47929090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b8b96e4b90391bedf7bc092fbac775f0e8a1507cda4550480b89b7db5693b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a276118be49d5475e0a06948e16fc8cd4b0bda3c3898430f6114e63b13f8fe23`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253096b3edd30e4dea19f06bf189e516335ef1a629a1b1dc6af7a813331a3042`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 43.3 MB (43269978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeccce14e96312025b4be6b969ea3e7729ba121e7a62ac30994e6b3b55ddcc6f`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:f9c8baaf32db379ef5af0c9f077cbfb6adf222c4b83c8b02aca2bd01b15fd10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.9 KB (853859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bbcfb9b4da509161f176758b2d50a6611cc531e0d8cd2de3c4d3558d94b8d1`

```dockerfile
```

-	Layers:
	-	`sha256:202977780cf1f2517394823fc0ad01200ee0e7fe1d684742af45433eaa725bfd`  
		Last Modified: Tue, 30 Dec 2025 01:11:15 GMT  
		Size: 840.9 KB (840928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cddd80706ffbef64d8b4e4108248b1dd6574a0c4daa989ae65199763cb7fda8`  
		Last Modified: Tue, 30 Dec 2025 01:11:16 GMT  
		Size: 12.9 KB (12931 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:f370bfaf055906751a40aa2602862664385167c1ed4702e7b2845646e09f1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45411891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4c43778d8848986aa9c6e57346998df3e0553b9f60f37cf46b1af9dd9cadad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a14a5a8b1e9f321ce7c2ee0dd494572157283dabd4908919bd42a2624bd9b7f`  
		Last Modified: Mon, 29 Dec 2025 22:12:33 GMT  
		Size: 41.1 MB (41120256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1c0ce4e6e90bd62ef1527e0b929814a30b66ab9dfa97b1fdfa5a10ca69246`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:14d63ad02ff72713a77bb9d2cd51f1a84807cca32f7a143e9be43ab2b7a8a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff23458bfec55077a9171f2ab6f84ee6b4504aafaec9d5448595db669dd79e7b`

```dockerfile
```

-	Layers:
	-	`sha256:92030776799ba4b7a5539a6f4eda6cc21d035b4bc63610bf72660d504c54ce84`  
		Last Modified: Tue, 30 Dec 2025 01:11:19 GMT  
		Size: 840.9 KB (840881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d937595ae2d0850f52fec601c1bf72a17b3a606174ad9de0fd4e98b024f34d`  
		Last Modified: Tue, 30 Dec 2025 01:11:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:fcad624b6c038a6ce9f23947bc913569ac3a582a361649bcec01cf7685fe1ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50131261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62d8c5216f1f866d94da4ac4114ab659a566122b37241eabbd2e9c0cb1e3e48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0941ee3a780b0edc04da4dbe59ee4854382951b9d7b3c7f0723617225bf179`  
		Last Modified: Mon, 29 Dec 2025 22:17:07 GMT  
		Size: 46.1 MB (46085759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0836a9f82df338c90828978f066ff4179a3786145f1409a81c9b0fda098ca079`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:4ee810a821586c1b7dfad2678e680c29cf91f9e5c939cb906f2836f399c58e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13baea432a1fff2eefd00a15970a4bb94d49230e48791f0ab1ad5f2ec56cdf35`

```dockerfile
```

-	Layers:
	-	`sha256:9dcc67bee13becd6a3dd7f1a1f4f19d3f8938adbf98359ce2bda9686e95c7543`  
		Last Modified: Tue, 30 Dec 2025 01:11:23 GMT  
		Size: 840.9 KB (840877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f6ac844190990794ea1badab8f0eb9008a988dae526b34259838d9c435ade8`  
		Last Modified: Tue, 30 Dec 2025 01:11:24 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:c90fb8eaf4f198acfcdc5ac5ee91d5017d85d7f1ee5ab34254e3e7413f75e7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50138784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b8c7e2ec2cce85fccc6ded5f989bcb54d35802064a883422107c8cec37788`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:48 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570fee54adbbcbd48c3264b6c1c48307759a232a8e62577915b34419d6908823`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2778402c6a2b9b0e23db64c01d948de928390074f3217c880d2e23fbad16d7c`  
		Last Modified: Mon, 29 Dec 2025 22:12:56 GMT  
		Size: 46.0 MB (45952359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82d9b41c12793837adea9cf222b43b978adf330a79cfe2facb415ae098f56f`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:f74a2a2e3a3fe763f6f53a84573d360bef963db9f78da5033b74dde5b86ed411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.6 KB (853589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d5912b64f161d66a4a5eecba009f5e5140eef5534c786abb8c0e7b13f74dd`

```dockerfile
```

-	Layers:
	-	`sha256:bc7b6070213f81954f2b800d7cec8f31869934919b88ebe831fad467713d455b`  
		Last Modified: Tue, 30 Dec 2025 01:11:27 GMT  
		Size: 840.8 KB (840823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb35d8c89e649d99bbb968932c09b39061aa837608b6d87face316071d01b18`  
		Last Modified: Tue, 30 Dec 2025 01:11:28 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5a06c29fbab874cee300291b95fe0afc4c24577dfeb4e52b91e87b8bb4a0b6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:89e7f45b4d36afe825781bf842c1b2ad594dda583c304e016a0696b90fda9cdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174773190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4167b1c56d9d49dc5d7a01b75d801b66a4580bd14a318da164f777eb9d9edeb8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:25:15 GMT
RUN cmd /S /C #(nop) COPY file:66315e29abc155939f3aa5baae45983776d9ac6f972112c785969c7332675bc4 in \ 
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:25:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe3710db5e56686dc75936e84ccb581a06c42485c91cc068ecf53aaa4d44d03`  
		Last Modified: Mon, 29 Dec 2025 22:25:55 GMT  
		Size: 48.4 MB (48411694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393668b98eb25293e345abf4ea21e1330bfe707727dfcbb662b255a1023a5c0d`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098625c20c4915bce3bf639faae72ec50f5979f0862783f4328a18015219137`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90d470c03edd3b2ad3f78d40bcf1c32d676318db21ce688e573e024160fa6e4`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:6a1d4363048b9caf4dde75474ab67fe10e742efd309cba4aecbfb6e6bdd80b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:e61041560509b551768ffe5ecf742e7f2668f06dcfdd0893fd284872dc853874
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828952089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f55d9baaf252e02a884479dc6a115e3d0dc82c3041f60a18031e485d203ab9b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:14:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:14:22 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:14:23 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493bb1b1e2906612559b21c8266db58d2befb0eef85e8f7c4ef50bb6a9b4e00b`  
		Last Modified: Mon, 29 Dec 2025 22:19:46 GMT  
		Size: 49.1 MB (49067574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a82646025bc5e6b27acd5447841931e26ddf6dedd74b01d003a9af276d112f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d4458d8a58188be1cc63f52855d2005c8db1495bbc7758a9c3b84c4bb898fb`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19bb40fd6917864ac17900b45224f4420bad7e7a17d608b05941a83b174282f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:82d3d16dde0474a51fef00b28de143d48b67f7a27453224d5e7b5aaefff26a97
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
$ docker pull traefik@sha256:13e903c820dfeab5cb464ca6cc9f3b276317f768e324402f440cd3472f3612b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51976248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f174a52e1993a764172bba2c07106a766f2895b2b069a19c7d3bb6f69a18d222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:25 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a471ba94e701f551e79684073e592976607816526d57a987948bff6526c5b`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0802690440f2ca58ae524161b78276377a7a1b65b3f8f6c5053ffabb41708d54`  
		Last Modified: Mon, 29 Dec 2025 22:14:59 GMT  
		Size: 47.7 MB (47654821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e800de571d9f8e3e1570b7ab6ffa6cf7518881c2467f3b4ed474c5332aee3`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:00a627efcd6fc72b53d3bdd7a4ccfa21a4b6ed7f733c3388ed4cc08255f2309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.2 KB (854240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64e165bdaee378a18e512759d5d70d3c7a5dd930282041a764309dcfce32bac`

```dockerfile
```

-	Layers:
	-	`sha256:ff45197c317b2ca934a8cc34ddb376986be02b75920b99d313d539e6e7c911fa`  
		Last Modified: Tue, 30 Dec 2025 01:11:08 GMT  
		Size: 841.5 KB (841474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86fb8844e05b2481883284fb064a496d50c1a26502d834595358d8626eb4947`  
		Last Modified: Tue, 30 Dec 2025 01:11:09 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5457c0a157f7ed95be8253228daf32bba1a12ae1db68ba0337fee123623c347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47249818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c44ed4360eecfed4fbcbfa09e59c09eeea8e674776865aa3fc1af12df3ad9e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:26 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f336e0c0ee4704e0d01821f3ad4ea570e26819a11a2b63dbb387cf34084e4`  
		Last Modified: Mon, 29 Dec 2025 22:12:42 GMT  
		Size: 43.2 MB (43219572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b178f7eca0fa59dd94e45d3d21766dca74576e55362c4962bf9b8ceec0d72572`  
		Last Modified: Mon, 29 Dec 2025 22:12:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:a80f6381e2f7d4ad95451ebe1f7f4bc0d17ec0a8abf35d2a042d68ac291db1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5061d5772660ee643e094c24fd496931f45d553812861885b99cf369df7de503`

```dockerfile
```

-	Layers:
	-	`sha256:ab584a1e249e5e6a4f4a0ceb6f89a8dff471278819ca51a8c8936df3072f5f25`  
		Last Modified: Tue, 30 Dec 2025 01:11:12 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f3e50962d4a55032f1bcb106d9d9e00a62f9500f07d48beea58ea88ef29cd819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47929090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b8b96e4b90391bedf7bc092fbac775f0e8a1507cda4550480b89b7db5693b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a276118be49d5475e0a06948e16fc8cd4b0bda3c3898430f6114e63b13f8fe23`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253096b3edd30e4dea19f06bf189e516335ef1a629a1b1dc6af7a813331a3042`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 43.3 MB (43269978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeccce14e96312025b4be6b969ea3e7729ba121e7a62ac30994e6b3b55ddcc6f`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:f9c8baaf32db379ef5af0c9f077cbfb6adf222c4b83c8b02aca2bd01b15fd10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.9 KB (853859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bbcfb9b4da509161f176758b2d50a6611cc531e0d8cd2de3c4d3558d94b8d1`

```dockerfile
```

-	Layers:
	-	`sha256:202977780cf1f2517394823fc0ad01200ee0e7fe1d684742af45433eaa725bfd`  
		Last Modified: Tue, 30 Dec 2025 01:11:15 GMT  
		Size: 840.9 KB (840928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cddd80706ffbef64d8b4e4108248b1dd6574a0c4daa989ae65199763cb7fda8`  
		Last Modified: Tue, 30 Dec 2025 01:11:16 GMT  
		Size: 12.9 KB (12931 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:f370bfaf055906751a40aa2602862664385167c1ed4702e7b2845646e09f1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45411891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4c43778d8848986aa9c6e57346998df3e0553b9f60f37cf46b1af9dd9cadad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a14a5a8b1e9f321ce7c2ee0dd494572157283dabd4908919bd42a2624bd9b7f`  
		Last Modified: Mon, 29 Dec 2025 22:12:33 GMT  
		Size: 41.1 MB (41120256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1c0ce4e6e90bd62ef1527e0b929814a30b66ab9dfa97b1fdfa5a10ca69246`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:14d63ad02ff72713a77bb9d2cd51f1a84807cca32f7a143e9be43ab2b7a8a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff23458bfec55077a9171f2ab6f84ee6b4504aafaec9d5448595db669dd79e7b`

```dockerfile
```

-	Layers:
	-	`sha256:92030776799ba4b7a5539a6f4eda6cc21d035b4bc63610bf72660d504c54ce84`  
		Last Modified: Tue, 30 Dec 2025 01:11:19 GMT  
		Size: 840.9 KB (840881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d937595ae2d0850f52fec601c1bf72a17b3a606174ad9de0fd4e98b024f34d`  
		Last Modified: Tue, 30 Dec 2025 01:11:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:fcad624b6c038a6ce9f23947bc913569ac3a582a361649bcec01cf7685fe1ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50131261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62d8c5216f1f866d94da4ac4114ab659a566122b37241eabbd2e9c0cb1e3e48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0941ee3a780b0edc04da4dbe59ee4854382951b9d7b3c7f0723617225bf179`  
		Last Modified: Mon, 29 Dec 2025 22:17:07 GMT  
		Size: 46.1 MB (46085759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0836a9f82df338c90828978f066ff4179a3786145f1409a81c9b0fda098ca079`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4ee810a821586c1b7dfad2678e680c29cf91f9e5c939cb906f2836f399c58e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13baea432a1fff2eefd00a15970a4bb94d49230e48791f0ab1ad5f2ec56cdf35`

```dockerfile
```

-	Layers:
	-	`sha256:9dcc67bee13becd6a3dd7f1a1f4f19d3f8938adbf98359ce2bda9686e95c7543`  
		Last Modified: Tue, 30 Dec 2025 01:11:23 GMT  
		Size: 840.9 KB (840877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f6ac844190990794ea1badab8f0eb9008a988dae526b34259838d9c435ade8`  
		Last Modified: Tue, 30 Dec 2025 01:11:24 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:c90fb8eaf4f198acfcdc5ac5ee91d5017d85d7f1ee5ab34254e3e7413f75e7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50138784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b8c7e2ec2cce85fccc6ded5f989bcb54d35802064a883422107c8cec37788`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:48 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570fee54adbbcbd48c3264b6c1c48307759a232a8e62577915b34419d6908823`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2778402c6a2b9b0e23db64c01d948de928390074f3217c880d2e23fbad16d7c`  
		Last Modified: Mon, 29 Dec 2025 22:12:56 GMT  
		Size: 46.0 MB (45952359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82d9b41c12793837adea9cf222b43b978adf330a79cfe2facb415ae098f56f`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:f74a2a2e3a3fe763f6f53a84573d360bef963db9f78da5033b74dde5b86ed411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.6 KB (853589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d5912b64f161d66a4a5eecba009f5e5140eef5534c786abb8c0e7b13f74dd`

```dockerfile
```

-	Layers:
	-	`sha256:bc7b6070213f81954f2b800d7cec8f31869934919b88ebe831fad467713d455b`  
		Last Modified: Tue, 30 Dec 2025 01:11:27 GMT  
		Size: 840.8 KB (840823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb35d8c89e649d99bbb968932c09b39061aa837608b6d87face316071d01b18`  
		Last Modified: Tue, 30 Dec 2025 01:11:28 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5a06c29fbab874cee300291b95fe0afc4c24577dfeb4e52b91e87b8bb4a0b6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:89e7f45b4d36afe825781bf842c1b2ad594dda583c304e016a0696b90fda9cdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174773190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4167b1c56d9d49dc5d7a01b75d801b66a4580bd14a318da164f777eb9d9edeb8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:25:15 GMT
RUN cmd /S /C #(nop) COPY file:66315e29abc155939f3aa5baae45983776d9ac6f972112c785969c7332675bc4 in \ 
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:25:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe3710db5e56686dc75936e84ccb581a06c42485c91cc068ecf53aaa4d44d03`  
		Last Modified: Mon, 29 Dec 2025 22:25:55 GMT  
		Size: 48.4 MB (48411694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393668b98eb25293e345abf4ea21e1330bfe707727dfcbb662b255a1023a5c0d`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098625c20c4915bce3bf639faae72ec50f5979f0862783f4328a18015219137`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90d470c03edd3b2ad3f78d40bcf1c32d676318db21ce688e573e024160fa6e4`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:6a1d4363048b9caf4dde75474ab67fe10e742efd309cba4aecbfb6e6bdd80b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:e61041560509b551768ffe5ecf742e7f2668f06dcfdd0893fd284872dc853874
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828952089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f55d9baaf252e02a884479dc6a115e3d0dc82c3041f60a18031e485d203ab9b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:14:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:14:22 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:14:23 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493bb1b1e2906612559b21c8266db58d2befb0eef85e8f7c4ef50bb6a9b4e00b`  
		Last Modified: Mon, 29 Dec 2025 22:19:46 GMT  
		Size: 49.1 MB (49067574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a82646025bc5e6b27acd5447841931e26ddf6dedd74b01d003a9af276d112f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d4458d8a58188be1cc63f52855d2005c8db1495bbc7758a9c3b84c4bb898fb`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19bb40fd6917864ac17900b45224f4420bad7e7a17d608b05941a83b174282f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.6`

```console
$ docker pull traefik@sha256:82d3d16dde0474a51fef00b28de143d48b67f7a27453224d5e7b5aaefff26a97
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

### `traefik:3.6.6` - linux; amd64

```console
$ docker pull traefik@sha256:13e903c820dfeab5cb464ca6cc9f3b276317f768e324402f440cd3472f3612b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51976248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f174a52e1993a764172bba2c07106a766f2895b2b069a19c7d3bb6f69a18d222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:25 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a471ba94e701f551e79684073e592976607816526d57a987948bff6526c5b`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0802690440f2ca58ae524161b78276377a7a1b65b3f8f6c5053ffabb41708d54`  
		Last Modified: Mon, 29 Dec 2025 22:14:59 GMT  
		Size: 47.7 MB (47654821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e800de571d9f8e3e1570b7ab6ffa6cf7518881c2467f3b4ed474c5332aee3`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:00a627efcd6fc72b53d3bdd7a4ccfa21a4b6ed7f733c3388ed4cc08255f2309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.2 KB (854240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64e165bdaee378a18e512759d5d70d3c7a5dd930282041a764309dcfce32bac`

```dockerfile
```

-	Layers:
	-	`sha256:ff45197c317b2ca934a8cc34ddb376986be02b75920b99d313d539e6e7c911fa`  
		Last Modified: Tue, 30 Dec 2025 01:11:08 GMT  
		Size: 841.5 KB (841474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86fb8844e05b2481883284fb064a496d50c1a26502d834595358d8626eb4947`  
		Last Modified: Tue, 30 Dec 2025 01:11:09 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5457c0a157f7ed95be8253228daf32bba1a12ae1db68ba0337fee123623c347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47249818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c44ed4360eecfed4fbcbfa09e59c09eeea8e674776865aa3fc1af12df3ad9e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:26 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f336e0c0ee4704e0d01821f3ad4ea570e26819a11a2b63dbb387cf34084e4`  
		Last Modified: Mon, 29 Dec 2025 22:12:42 GMT  
		Size: 43.2 MB (43219572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b178f7eca0fa59dd94e45d3d21766dca74576e55362c4962bf9b8ceec0d72572`  
		Last Modified: Mon, 29 Dec 2025 22:12:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:a80f6381e2f7d4ad95451ebe1f7f4bc0d17ec0a8abf35d2a042d68ac291db1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5061d5772660ee643e094c24fd496931f45d553812861885b99cf369df7de503`

```dockerfile
```

-	Layers:
	-	`sha256:ab584a1e249e5e6a4f4a0ceb6f89a8dff471278819ca51a8c8936df3072f5f25`  
		Last Modified: Tue, 30 Dec 2025 01:11:12 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f3e50962d4a55032f1bcb106d9d9e00a62f9500f07d48beea58ea88ef29cd819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47929090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b8b96e4b90391bedf7bc092fbac775f0e8a1507cda4550480b89b7db5693b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a276118be49d5475e0a06948e16fc8cd4b0bda3c3898430f6114e63b13f8fe23`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253096b3edd30e4dea19f06bf189e516335ef1a629a1b1dc6af7a813331a3042`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 43.3 MB (43269978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeccce14e96312025b4be6b969ea3e7729ba121e7a62ac30994e6b3b55ddcc6f`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:f9c8baaf32db379ef5af0c9f077cbfb6adf222c4b83c8b02aca2bd01b15fd10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.9 KB (853859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bbcfb9b4da509161f176758b2d50a6611cc531e0d8cd2de3c4d3558d94b8d1`

```dockerfile
```

-	Layers:
	-	`sha256:202977780cf1f2517394823fc0ad01200ee0e7fe1d684742af45433eaa725bfd`  
		Last Modified: Tue, 30 Dec 2025 01:11:15 GMT  
		Size: 840.9 KB (840928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cddd80706ffbef64d8b4e4108248b1dd6574a0c4daa989ae65199763cb7fda8`  
		Last Modified: Tue, 30 Dec 2025 01:11:16 GMT  
		Size: 12.9 KB (12931 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:f370bfaf055906751a40aa2602862664385167c1ed4702e7b2845646e09f1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45411891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4c43778d8848986aa9c6e57346998df3e0553b9f60f37cf46b1af9dd9cadad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a14a5a8b1e9f321ce7c2ee0dd494572157283dabd4908919bd42a2624bd9b7f`  
		Last Modified: Mon, 29 Dec 2025 22:12:33 GMT  
		Size: 41.1 MB (41120256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1c0ce4e6e90bd62ef1527e0b929814a30b66ab9dfa97b1fdfa5a10ca69246`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:14d63ad02ff72713a77bb9d2cd51f1a84807cca32f7a143e9be43ab2b7a8a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff23458bfec55077a9171f2ab6f84ee6b4504aafaec9d5448595db669dd79e7b`

```dockerfile
```

-	Layers:
	-	`sha256:92030776799ba4b7a5539a6f4eda6cc21d035b4bc63610bf72660d504c54ce84`  
		Last Modified: Tue, 30 Dec 2025 01:11:19 GMT  
		Size: 840.9 KB (840881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d937595ae2d0850f52fec601c1bf72a17b3a606174ad9de0fd4e98b024f34d`  
		Last Modified: Tue, 30 Dec 2025 01:11:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.6` - linux; riscv64

```console
$ docker pull traefik@sha256:fcad624b6c038a6ce9f23947bc913569ac3a582a361649bcec01cf7685fe1ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50131261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62d8c5216f1f866d94da4ac4114ab659a566122b37241eabbd2e9c0cb1e3e48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0941ee3a780b0edc04da4dbe59ee4854382951b9d7b3c7f0723617225bf179`  
		Last Modified: Mon, 29 Dec 2025 22:17:07 GMT  
		Size: 46.1 MB (46085759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0836a9f82df338c90828978f066ff4179a3786145f1409a81c9b0fda098ca079`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4ee810a821586c1b7dfad2678e680c29cf91f9e5c939cb906f2836f399c58e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13baea432a1fff2eefd00a15970a4bb94d49230e48791f0ab1ad5f2ec56cdf35`

```dockerfile
```

-	Layers:
	-	`sha256:9dcc67bee13becd6a3dd7f1a1f4f19d3f8938adbf98359ce2bda9686e95c7543`  
		Last Modified: Tue, 30 Dec 2025 01:11:23 GMT  
		Size: 840.9 KB (840877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f6ac844190990794ea1badab8f0eb9008a988dae526b34259838d9c435ade8`  
		Last Modified: Tue, 30 Dec 2025 01:11:24 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.6` - linux; s390x

```console
$ docker pull traefik@sha256:c90fb8eaf4f198acfcdc5ac5ee91d5017d85d7f1ee5ab34254e3e7413f75e7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50138784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b8c7e2ec2cce85fccc6ded5f989bcb54d35802064a883422107c8cec37788`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:48 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570fee54adbbcbd48c3264b6c1c48307759a232a8e62577915b34419d6908823`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2778402c6a2b9b0e23db64c01d948de928390074f3217c880d2e23fbad16d7c`  
		Last Modified: Mon, 29 Dec 2025 22:12:56 GMT  
		Size: 46.0 MB (45952359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82d9b41c12793837adea9cf222b43b978adf330a79cfe2facb415ae098f56f`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:f74a2a2e3a3fe763f6f53a84573d360bef963db9f78da5033b74dde5b86ed411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.6 KB (853589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d5912b64f161d66a4a5eecba009f5e5140eef5534c786abb8c0e7b13f74dd`

```dockerfile
```

-	Layers:
	-	`sha256:bc7b6070213f81954f2b800d7cec8f31869934919b88ebe831fad467713d455b`  
		Last Modified: Tue, 30 Dec 2025 01:11:27 GMT  
		Size: 840.8 KB (840823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb35d8c89e649d99bbb968932c09b39061aa837608b6d87face316071d01b18`  
		Last Modified: Tue, 30 Dec 2025 01:11:28 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5a06c29fbab874cee300291b95fe0afc4c24577dfeb4e52b91e87b8bb4a0b6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6.6-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:89e7f45b4d36afe825781bf842c1b2ad594dda583c304e016a0696b90fda9cdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174773190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4167b1c56d9d49dc5d7a01b75d801b66a4580bd14a318da164f777eb9d9edeb8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:25:15 GMT
RUN cmd /S /C #(nop) COPY file:66315e29abc155939f3aa5baae45983776d9ac6f972112c785969c7332675bc4 in \ 
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:25:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe3710db5e56686dc75936e84ccb581a06c42485c91cc068ecf53aaa4d44d03`  
		Last Modified: Mon, 29 Dec 2025 22:25:55 GMT  
		Size: 48.4 MB (48411694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393668b98eb25293e345abf4ea21e1330bfe707727dfcbb662b255a1023a5c0d`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098625c20c4915bce3bf639faae72ec50f5979f0862783f4328a18015219137`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90d470c03edd3b2ad3f78d40bcf1c32d676318db21ce688e573e024160fa6e4`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:6a1d4363048b9caf4dde75474ab67fe10e742efd309cba4aecbfb6e6bdd80b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:e61041560509b551768ffe5ecf742e7f2668f06dcfdd0893fd284872dc853874
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828952089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f55d9baaf252e02a884479dc6a115e3d0dc82c3041f60a18031e485d203ab9b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:14:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:14:22 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:14:23 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493bb1b1e2906612559b21c8266db58d2befb0eef85e8f7c4ef50bb6a9b4e00b`  
		Last Modified: Mon, 29 Dec 2025 22:19:46 GMT  
		Size: 49.1 MB (49067574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a82646025bc5e6b27acd5447841931e26ddf6dedd74b01d003a9af276d112f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d4458d8a58188be1cc63f52855d2005c8db1495bbc7758a9c3b84c4bb898fb`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19bb40fd6917864ac17900b45224f4420bad7e7a17d608b05941a83b174282f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:82d3d16dde0474a51fef00b28de143d48b67f7a27453224d5e7b5aaefff26a97
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
$ docker pull traefik@sha256:13e903c820dfeab5cb464ca6cc9f3b276317f768e324402f440cd3472f3612b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51976248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f174a52e1993a764172bba2c07106a766f2895b2b069a19c7d3bb6f69a18d222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:25 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a471ba94e701f551e79684073e592976607816526d57a987948bff6526c5b`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0802690440f2ca58ae524161b78276377a7a1b65b3f8f6c5053ffabb41708d54`  
		Last Modified: Mon, 29 Dec 2025 22:14:59 GMT  
		Size: 47.7 MB (47654821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e800de571d9f8e3e1570b7ab6ffa6cf7518881c2467f3b4ed474c5332aee3`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:00a627efcd6fc72b53d3bdd7a4ccfa21a4b6ed7f733c3388ed4cc08255f2309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.2 KB (854240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64e165bdaee378a18e512759d5d70d3c7a5dd930282041a764309dcfce32bac`

```dockerfile
```

-	Layers:
	-	`sha256:ff45197c317b2ca934a8cc34ddb376986be02b75920b99d313d539e6e7c911fa`  
		Last Modified: Tue, 30 Dec 2025 01:11:08 GMT  
		Size: 841.5 KB (841474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86fb8844e05b2481883284fb064a496d50c1a26502d834595358d8626eb4947`  
		Last Modified: Tue, 30 Dec 2025 01:11:09 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5457c0a157f7ed95be8253228daf32bba1a12ae1db68ba0337fee123623c347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47249818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c44ed4360eecfed4fbcbfa09e59c09eeea8e674776865aa3fc1af12df3ad9e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:26 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f336e0c0ee4704e0d01821f3ad4ea570e26819a11a2b63dbb387cf34084e4`  
		Last Modified: Mon, 29 Dec 2025 22:12:42 GMT  
		Size: 43.2 MB (43219572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b178f7eca0fa59dd94e45d3d21766dca74576e55362c4962bf9b8ceec0d72572`  
		Last Modified: Mon, 29 Dec 2025 22:12:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:a80f6381e2f7d4ad95451ebe1f7f4bc0d17ec0a8abf35d2a042d68ac291db1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5061d5772660ee643e094c24fd496931f45d553812861885b99cf369df7de503`

```dockerfile
```

-	Layers:
	-	`sha256:ab584a1e249e5e6a4f4a0ceb6f89a8dff471278819ca51a8c8936df3072f5f25`  
		Last Modified: Tue, 30 Dec 2025 01:11:12 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f3e50962d4a55032f1bcb106d9d9e00a62f9500f07d48beea58ea88ef29cd819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47929090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b8b96e4b90391bedf7bc092fbac775f0e8a1507cda4550480b89b7db5693b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a276118be49d5475e0a06948e16fc8cd4b0bda3c3898430f6114e63b13f8fe23`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253096b3edd30e4dea19f06bf189e516335ef1a629a1b1dc6af7a813331a3042`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 43.3 MB (43269978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeccce14e96312025b4be6b969ea3e7729ba121e7a62ac30994e6b3b55ddcc6f`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:f9c8baaf32db379ef5af0c9f077cbfb6adf222c4b83c8b02aca2bd01b15fd10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.9 KB (853859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bbcfb9b4da509161f176758b2d50a6611cc531e0d8cd2de3c4d3558d94b8d1`

```dockerfile
```

-	Layers:
	-	`sha256:202977780cf1f2517394823fc0ad01200ee0e7fe1d684742af45433eaa725bfd`  
		Last Modified: Tue, 30 Dec 2025 01:11:15 GMT  
		Size: 840.9 KB (840928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cddd80706ffbef64d8b4e4108248b1dd6574a0c4daa989ae65199763cb7fda8`  
		Last Modified: Tue, 30 Dec 2025 01:11:16 GMT  
		Size: 12.9 KB (12931 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:f370bfaf055906751a40aa2602862664385167c1ed4702e7b2845646e09f1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45411891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4c43778d8848986aa9c6e57346998df3e0553b9f60f37cf46b1af9dd9cadad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a14a5a8b1e9f321ce7c2ee0dd494572157283dabd4908919bd42a2624bd9b7f`  
		Last Modified: Mon, 29 Dec 2025 22:12:33 GMT  
		Size: 41.1 MB (41120256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1c0ce4e6e90bd62ef1527e0b929814a30b66ab9dfa97b1fdfa5a10ca69246`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:14d63ad02ff72713a77bb9d2cd51f1a84807cca32f7a143e9be43ab2b7a8a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff23458bfec55077a9171f2ab6f84ee6b4504aafaec9d5448595db669dd79e7b`

```dockerfile
```

-	Layers:
	-	`sha256:92030776799ba4b7a5539a6f4eda6cc21d035b4bc63610bf72660d504c54ce84`  
		Last Modified: Tue, 30 Dec 2025 01:11:19 GMT  
		Size: 840.9 KB (840881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d937595ae2d0850f52fec601c1bf72a17b3a606174ad9de0fd4e98b024f34d`  
		Last Modified: Tue, 30 Dec 2025 01:11:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:fcad624b6c038a6ce9f23947bc913569ac3a582a361649bcec01cf7685fe1ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50131261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62d8c5216f1f866d94da4ac4114ab659a566122b37241eabbd2e9c0cb1e3e48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0941ee3a780b0edc04da4dbe59ee4854382951b9d7b3c7f0723617225bf179`  
		Last Modified: Mon, 29 Dec 2025 22:17:07 GMT  
		Size: 46.1 MB (46085759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0836a9f82df338c90828978f066ff4179a3786145f1409a81c9b0fda098ca079`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:4ee810a821586c1b7dfad2678e680c29cf91f9e5c939cb906f2836f399c58e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13baea432a1fff2eefd00a15970a4bb94d49230e48791f0ab1ad5f2ec56cdf35`

```dockerfile
```

-	Layers:
	-	`sha256:9dcc67bee13becd6a3dd7f1a1f4f19d3f8938adbf98359ce2bda9686e95c7543`  
		Last Modified: Tue, 30 Dec 2025 01:11:23 GMT  
		Size: 840.9 KB (840877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f6ac844190990794ea1badab8f0eb9008a988dae526b34259838d9c435ade8`  
		Last Modified: Tue, 30 Dec 2025 01:11:24 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:c90fb8eaf4f198acfcdc5ac5ee91d5017d85d7f1ee5ab34254e3e7413f75e7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50138784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b8c7e2ec2cce85fccc6ded5f989bcb54d35802064a883422107c8cec37788`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:48 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570fee54adbbcbd48c3264b6c1c48307759a232a8e62577915b34419d6908823`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2778402c6a2b9b0e23db64c01d948de928390074f3217c880d2e23fbad16d7c`  
		Last Modified: Mon, 29 Dec 2025 22:12:56 GMT  
		Size: 46.0 MB (45952359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82d9b41c12793837adea9cf222b43b978adf330a79cfe2facb415ae098f56f`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:f74a2a2e3a3fe763f6f53a84573d360bef963db9f78da5033b74dde5b86ed411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.6 KB (853589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d5912b64f161d66a4a5eecba009f5e5140eef5534c786abb8c0e7b13f74dd`

```dockerfile
```

-	Layers:
	-	`sha256:bc7b6070213f81954f2b800d7cec8f31869934919b88ebe831fad467713d455b`  
		Last Modified: Tue, 30 Dec 2025 01:11:27 GMT  
		Size: 840.8 KB (840823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb35d8c89e649d99bbb968932c09b39061aa837608b6d87face316071d01b18`  
		Last Modified: Tue, 30 Dec 2025 01:11:28 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:ec06628f2693a846bdf0d84a20e1c2d13026963370c422ef3c301a0ec95122f8
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
$ docker pull traefik@sha256:dde8db8bf8a8c2b68181a5bf51bad71b145427f8f42d85543c063a2878c5430c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51045034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c73645b5a95f5868c73795f8be36f1b016096ba044ca898ec4ec6bdf67f49a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:32 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460d3ed754bcad38468a7e39c71a8ae0bd2a6e3f0fe243a6b06bf93fdc341ac`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf71e0662417ca9e09cdcb8dbe1ceaab2d24ca270364186656c3989fde4dd89f`  
		Last Modified: Mon, 29 Dec 2025 22:15:09 GMT  
		Size: 46.7 MB (46723619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccabf121282a73971c74c565541d08d7858279fd78860d4f539d7e055925dae`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:7b80c6aa4cb2a906161bb1363e3bab6e372c4fdfeb8e0905a5678b98b674a487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea0349cca0e8260efbb16808875c70ddb72cbe8efa0543b79bad57767ebdf79`

```dockerfile
```

-	Layers:
	-	`sha256:6fe270a0fa6590e1551a1ee4f6efd31418369e213caa83e16a1ca434588b3387`  
		Last Modified: Tue, 30 Dec 2025 01:10:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63df6effd3e9e12b969fcfa50ab1e9b2acaff2e83f72f2446a4d786944098fd`  
		Last Modified: Tue, 30 Dec 2025 01:10:33 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7a6812ddc9c24690d7a5a499003dc945857a175e7f5dda6981d1f7274749a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6243483a0b396d4fe7d53eaaf3249de044c8dc788057696eb33a805148646fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:05 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9a25acc457736a96b93a0281b7736208e4dc00987f78b5a473bb17e3487d70`  
		Last Modified: Mon, 29 Dec 2025 22:12:24 GMT  
		Size: 42.8 MB (42792487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2555957720388bf7fad85128cde658f26ed9c0878ea5e3587e5d61b776b17b`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:386b9114b5a54555c4beb1d339812a25a03b2a79342fc9c0a77f4a12689188c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0bdf4205aa969b25895232ca1c8c3366ef418998b9cad892302307b58a1d05`

```dockerfile
```

-	Layers:
	-	`sha256:9d9d0e6ec35917ebf98a85505427f212b0def2618d49faab2a9e6b98a4d12f1f`  
		Last Modified: Tue, 30 Dec 2025 01:10:36 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:068c114909900cf35accd4cb1e661d47fb16d4a9fc14cba2c991c5ec82143804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47288453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf94b991a93fcc4f35ceaa5860a12210bb8a3773a114e6dfbee0c00b361f1c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:27 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeadd60e258df383b0cc98606207bf109ef121df1971f4462b45ec54ee9f318`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 463.0 KB (462969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf7d2a33fd20248262d1c4cf1a1e70d0443286f144ff431455a223caa65601`  
		Last Modified: Mon, 29 Dec 2025 22:15:03 GMT  
		Size: 42.6 MB (42629375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c517dbb8d79767704a0d7fa570e4c08d418574401c1f3ed2aa365160213329d`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:c388de6c2b71abf77689d398e067a6bd8c9e90557af9ce13025e1e6a1766f53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb04cbf1de6bf71b2a625f6ccd7c33fdd963d4f1afd226100807e0e105080a7`

```dockerfile
```

-	Layers:
	-	`sha256:dbe071740321aed9566e9a7ce2de44c21da3fd82adef85df41ec2e1569447ddc`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4510a9494ca18bef567409f7d6cd142fde24682356b6be783ebb1f81b6a01b`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:3c36c86703831acb8abb0a22a2841be45264d32be03ee0076c136c81b12a1079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ef1b95ee8ae6ee6556e92f98edc54ea617c1925464e45e91d54911209e5e6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bedccbda7f6c026594b1bac44b809089174355a4e044e6ebfdc6286c9588756`  
		Last Modified: Mon, 29 Dec 2025 22:12:28 GMT  
		Size: 41.0 MB (40951452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a3d0d79b5160993f0c0a41639ed185b7a0f0bd4f4f8237368605fa4674ee2`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:4b586213bdae7d3e4ee91a8608d35500d306e36a06bc41c7f240ff60b6a15681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6810ccb80adb216f5b638e0a0253b8f04ebf89e679860c97482dde9e9bcb0c26`

```dockerfile
```

-	Layers:
	-	`sha256:595c3b71af7b44b03435988a57a0d7a6107af8e394fe81f30537110e5049411f`  
		Last Modified: Tue, 30 Dec 2025 01:10:44 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a33507a6c12c57f9d79818ef6f55e323f54095506204186caeef90c1cfea6f4`  
		Last Modified: Tue, 30 Dec 2025 01:10:45 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:d885398c11e1e2255f530086a8a38dd5703151f3d01ac65f37fa0ed677b3790d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49371197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423faff905cf66d01d4b68a15665db0f1efae634854bab7c395d35c3be94f799`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:17:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:17:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:17:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11e3a76c0fe809fef053b28f4223652f383a7155827cca3f996e6b5ad99347b`  
		Last Modified: Mon, 29 Dec 2025 22:22:50 GMT  
		Size: 45.3 MB (45325697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cded5f8ab82a089eef5c39ab4214eda5d15f737ee5865b41892a6b2a62423c`  
		Last Modified: Mon, 29 Dec 2025 22:22:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:cfd66037b02e24fbc4bf4e26ae9279b6f9cfd9034c24a39f5e34d0c15ae0bce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2d62009ccbbbac92862f457a0144b820e0544d6763726310a66361b80fbf9e`

```dockerfile
```

-	Layers:
	-	`sha256:745a3f8aa84f981044005ec6c920f6bb1dad5840785ce877c136dd5e098ed262`  
		Last Modified: Tue, 30 Dec 2025 01:10:48 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86df83cb3765bdd568c1f258f62e4e5a4b1fdaa5bebcdd69e11e5f9eba1d7ac9`  
		Last Modified: Tue, 30 Dec 2025 01:10:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:c8e0bcf5d966979dc1c7e217f9e49c4c4d37693e18a2e2521d82884dbf0b6f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49441303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2846fbc72078df664092ad73630af388378efe6d44006852635652c5f704974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:52 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa895b2e41ff3a43aa2644cdbbbf2b91678301e65d1804cc3ddd31bad02b85b`  
		Last Modified: Mon, 29 Dec 2025 22:12:55 GMT  
		Size: 45.3 MB (45254880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87e0c0d53b7263e6598aa3669471a57768b8f4f67198215ff65e4269eacf11`  
		Last Modified: Mon, 29 Dec 2025 22:12:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:9e2e342705e2de6737da28772b5f86362dd121c687d450ba873ca82d90f04e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282a7969c762c223edcd680164bca446cfe6172b44fdb559d211302bf1fcf083`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cf47226e83925db8f301df6f56d2a03543e2e5a7cf6b034bc1765b4e65e58`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a52bfeb8caa44a23436add6d2771844b859fa3c5503f91b4648602975bd3845`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e412515e710521fa7986c58e5d1c6760081b86409fbd7ada71c280008f6a7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:583653b643ac3f1f46003cb5420a6020ebbab38b4223e42dedccb73bdfb5a58c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173878068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3deb70fa9dfc3d168fd0f74db8842e94f92d1a34c9d1603651c6e4f2ae7206`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:26:01 GMT
RUN cmd /S /C #(nop) COPY file:bb401afdd9d3934a7a4f9b92a64ab967d454bd5889893f3e6bb99650a87af92c in \ 
# Mon, 29 Dec 2025 22:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282ed5ab3ad2747524afcc687c7af1981fee639f80841907ec190c541a8225a`  
		Last Modified: Mon, 29 Dec 2025 22:26:27 GMT  
		Size: 47.5 MB (47516598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c830cf11eb297146e37f3dc86b7d3eb61623f5ed17b3ad2c799157b35e1e24a9`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf10c5e839cb5e9a0e4e608989f75e46e276c01b90f16cf02628c3317ffe07e`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c62f03aa8b4ff4fbb3e842cb32d489adc9b7ff1cd733fbfdd369a333f7ca74`  
		Last Modified: Mon, 29 Dec 2025 22:26:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:89357a7b41ff2c571cfe33f4102c7933b0f7fb1c53a41bae1a30ddb83e7d7dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:9047cfdfe358271d4a6760faf9809787c81e8a906b0e5a3b341a0abbfdf9cb4a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828029861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76acbfb4dc298a43b62470fe1dd8b0b4093ce9938b3d3a328ef1143141a61c6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:20:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:20:12 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:20:13 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:20:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d4f4c744a59ac227520b5e733ac7e2c3bb8792ebea040dedecf0dd290fbb44`  
		Last Modified: Mon, 29 Dec 2025 22:20:47 GMT  
		Size: 48.1 MB (48145327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c42cd93e2c4a2994963205e46b4ec55d2b2f4c4d5d38f34f8f4d10e4d0625`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a558267a225392878a35ac6136c8729fe970c469f2d9bacd35f04d21568a2`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b61952c0488abc61e0aa13adc437b892be0123d5a2807c46192869a8e19f42`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5a06c29fbab874cee300291b95fe0afc4c24577dfeb4e52b91e87b8bb4a0b6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:89e7f45b4d36afe825781bf842c1b2ad594dda583c304e016a0696b90fda9cdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174773190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4167b1c56d9d49dc5d7a01b75d801b66a4580bd14a318da164f777eb9d9edeb8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:25:15 GMT
RUN cmd /S /C #(nop) COPY file:66315e29abc155939f3aa5baae45983776d9ac6f972112c785969c7332675bc4 in \ 
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:25:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe3710db5e56686dc75936e84ccb581a06c42485c91cc068ecf53aaa4d44d03`  
		Last Modified: Mon, 29 Dec 2025 22:25:55 GMT  
		Size: 48.4 MB (48411694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393668b98eb25293e345abf4ea21e1330bfe707727dfcbb662b255a1023a5c0d`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098625c20c4915bce3bf639faae72ec50f5979f0862783f4328a18015219137`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90d470c03edd3b2ad3f78d40bcf1c32d676318db21ce688e573e024160fa6e4`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:82d3d16dde0474a51fef00b28de143d48b67f7a27453224d5e7b5aaefff26a97
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
$ docker pull traefik@sha256:13e903c820dfeab5cb464ca6cc9f3b276317f768e324402f440cd3472f3612b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51976248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f174a52e1993a764172bba2c07106a766f2895b2b069a19c7d3bb6f69a18d222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:25 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a471ba94e701f551e79684073e592976607816526d57a987948bff6526c5b`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0802690440f2ca58ae524161b78276377a7a1b65b3f8f6c5053ffabb41708d54`  
		Last Modified: Mon, 29 Dec 2025 22:14:59 GMT  
		Size: 47.7 MB (47654821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e800de571d9f8e3e1570b7ab6ffa6cf7518881c2467f3b4ed474c5332aee3`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:00a627efcd6fc72b53d3bdd7a4ccfa21a4b6ed7f733c3388ed4cc08255f2309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.2 KB (854240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64e165bdaee378a18e512759d5d70d3c7a5dd930282041a764309dcfce32bac`

```dockerfile
```

-	Layers:
	-	`sha256:ff45197c317b2ca934a8cc34ddb376986be02b75920b99d313d539e6e7c911fa`  
		Last Modified: Tue, 30 Dec 2025 01:11:08 GMT  
		Size: 841.5 KB (841474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86fb8844e05b2481883284fb064a496d50c1a26502d834595358d8626eb4947`  
		Last Modified: Tue, 30 Dec 2025 01:11:09 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5457c0a157f7ed95be8253228daf32bba1a12ae1db68ba0337fee123623c347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47249818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c44ed4360eecfed4fbcbfa09e59c09eeea8e674776865aa3fc1af12df3ad9e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:26 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f336e0c0ee4704e0d01821f3ad4ea570e26819a11a2b63dbb387cf34084e4`  
		Last Modified: Mon, 29 Dec 2025 22:12:42 GMT  
		Size: 43.2 MB (43219572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b178f7eca0fa59dd94e45d3d21766dca74576e55362c4962bf9b8ceec0d72572`  
		Last Modified: Mon, 29 Dec 2025 22:12:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:a80f6381e2f7d4ad95451ebe1f7f4bc0d17ec0a8abf35d2a042d68ac291db1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5061d5772660ee643e094c24fd496931f45d553812861885b99cf369df7de503`

```dockerfile
```

-	Layers:
	-	`sha256:ab584a1e249e5e6a4f4a0ceb6f89a8dff471278819ca51a8c8936df3072f5f25`  
		Last Modified: Tue, 30 Dec 2025 01:11:12 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f3e50962d4a55032f1bcb106d9d9e00a62f9500f07d48beea58ea88ef29cd819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47929090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b8b96e4b90391bedf7bc092fbac775f0e8a1507cda4550480b89b7db5693b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a276118be49d5475e0a06948e16fc8cd4b0bda3c3898430f6114e63b13f8fe23`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253096b3edd30e4dea19f06bf189e516335ef1a629a1b1dc6af7a813331a3042`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 43.3 MB (43269978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeccce14e96312025b4be6b969ea3e7729ba121e7a62ac30994e6b3b55ddcc6f`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:f9c8baaf32db379ef5af0c9f077cbfb6adf222c4b83c8b02aca2bd01b15fd10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.9 KB (853859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bbcfb9b4da509161f176758b2d50a6611cc531e0d8cd2de3c4d3558d94b8d1`

```dockerfile
```

-	Layers:
	-	`sha256:202977780cf1f2517394823fc0ad01200ee0e7fe1d684742af45433eaa725bfd`  
		Last Modified: Tue, 30 Dec 2025 01:11:15 GMT  
		Size: 840.9 KB (840928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cddd80706ffbef64d8b4e4108248b1dd6574a0c4daa989ae65199763cb7fda8`  
		Last Modified: Tue, 30 Dec 2025 01:11:16 GMT  
		Size: 12.9 KB (12931 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:f370bfaf055906751a40aa2602862664385167c1ed4702e7b2845646e09f1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45411891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4c43778d8848986aa9c6e57346998df3e0553b9f60f37cf46b1af9dd9cadad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a14a5a8b1e9f321ce7c2ee0dd494572157283dabd4908919bd42a2624bd9b7f`  
		Last Modified: Mon, 29 Dec 2025 22:12:33 GMT  
		Size: 41.1 MB (41120256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1c0ce4e6e90bd62ef1527e0b929814a30b66ab9dfa97b1fdfa5a10ca69246`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:14d63ad02ff72713a77bb9d2cd51f1a84807cca32f7a143e9be43ab2b7a8a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff23458bfec55077a9171f2ab6f84ee6b4504aafaec9d5448595db669dd79e7b`

```dockerfile
```

-	Layers:
	-	`sha256:92030776799ba4b7a5539a6f4eda6cc21d035b4bc63610bf72660d504c54ce84`  
		Last Modified: Tue, 30 Dec 2025 01:11:19 GMT  
		Size: 840.9 KB (840881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d937595ae2d0850f52fec601c1bf72a17b3a606174ad9de0fd4e98b024f34d`  
		Last Modified: Tue, 30 Dec 2025 01:11:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:fcad624b6c038a6ce9f23947bc913569ac3a582a361649bcec01cf7685fe1ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50131261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62d8c5216f1f866d94da4ac4114ab659a566122b37241eabbd2e9c0cb1e3e48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0941ee3a780b0edc04da4dbe59ee4854382951b9d7b3c7f0723617225bf179`  
		Last Modified: Mon, 29 Dec 2025 22:17:07 GMT  
		Size: 46.1 MB (46085759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0836a9f82df338c90828978f066ff4179a3786145f1409a81c9b0fda098ca079`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:4ee810a821586c1b7dfad2678e680c29cf91f9e5c939cb906f2836f399c58e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13baea432a1fff2eefd00a15970a4bb94d49230e48791f0ab1ad5f2ec56cdf35`

```dockerfile
```

-	Layers:
	-	`sha256:9dcc67bee13becd6a3dd7f1a1f4f19d3f8938adbf98359ce2bda9686e95c7543`  
		Last Modified: Tue, 30 Dec 2025 01:11:23 GMT  
		Size: 840.9 KB (840877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f6ac844190990794ea1badab8f0eb9008a988dae526b34259838d9c435ade8`  
		Last Modified: Tue, 30 Dec 2025 01:11:24 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:c90fb8eaf4f198acfcdc5ac5ee91d5017d85d7f1ee5ab34254e3e7413f75e7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50138784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b8c7e2ec2cce85fccc6ded5f989bcb54d35802064a883422107c8cec37788`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:48 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570fee54adbbcbd48c3264b6c1c48307759a232a8e62577915b34419d6908823`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2778402c6a2b9b0e23db64c01d948de928390074f3217c880d2e23fbad16d7c`  
		Last Modified: Mon, 29 Dec 2025 22:12:56 GMT  
		Size: 46.0 MB (45952359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82d9b41c12793837adea9cf222b43b978adf330a79cfe2facb415ae098f56f`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:f74a2a2e3a3fe763f6f53a84573d360bef963db9f78da5033b74dde5b86ed411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.6 KB (853589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d5912b64f161d66a4a5eecba009f5e5140eef5534c786abb8c0e7b13f74dd`

```dockerfile
```

-	Layers:
	-	`sha256:bc7b6070213f81954f2b800d7cec8f31869934919b88ebe831fad467713d455b`  
		Last Modified: Tue, 30 Dec 2025 01:11:27 GMT  
		Size: 840.8 KB (840823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb35d8c89e649d99bbb968932c09b39061aa837608b6d87face316071d01b18`  
		Last Modified: Tue, 30 Dec 2025 01:11:28 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5a06c29fbab874cee300291b95fe0afc4c24577dfeb4e52b91e87b8bb4a0b6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:89e7f45b4d36afe825781bf842c1b2ad594dda583c304e016a0696b90fda9cdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174773190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4167b1c56d9d49dc5d7a01b75d801b66a4580bd14a318da164f777eb9d9edeb8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:25:15 GMT
RUN cmd /S /C #(nop) COPY file:66315e29abc155939f3aa5baae45983776d9ac6f972112c785969c7332675bc4 in \ 
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:25:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe3710db5e56686dc75936e84ccb581a06c42485c91cc068ecf53aaa4d44d03`  
		Last Modified: Mon, 29 Dec 2025 22:25:55 GMT  
		Size: 48.4 MB (48411694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393668b98eb25293e345abf4ea21e1330bfe707727dfcbb662b255a1023a5c0d`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098625c20c4915bce3bf639faae72ec50f5979f0862783f4328a18015219137`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90d470c03edd3b2ad3f78d40bcf1c32d676318db21ce688e573e024160fa6e4`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:6a1d4363048b9caf4dde75474ab67fe10e742efd309cba4aecbfb6e6bdd80b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:e61041560509b551768ffe5ecf742e7f2668f06dcfdd0893fd284872dc853874
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828952089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f55d9baaf252e02a884479dc6a115e3d0dc82c3041f60a18031e485d203ab9b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:14:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:14:22 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:14:23 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493bb1b1e2906612559b21c8266db58d2befb0eef85e8f7c4ef50bb6a9b4e00b`  
		Last Modified: Mon, 29 Dec 2025 22:19:46 GMT  
		Size: 49.1 MB (49067574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a82646025bc5e6b27acd5447841931e26ddf6dedd74b01d003a9af276d112f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d4458d8a58188be1cc63f52855d2005c8db1495bbc7758a9c3b84c4bb898fb`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19bb40fd6917864ac17900b45224f4420bad7e7a17d608b05941a83b174282f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:ec06628f2693a846bdf0d84a20e1c2d13026963370c422ef3c301a0ec95122f8
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
$ docker pull traefik@sha256:dde8db8bf8a8c2b68181a5bf51bad71b145427f8f42d85543c063a2878c5430c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51045034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c73645b5a95f5868c73795f8be36f1b016096ba044ca898ec4ec6bdf67f49a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:32 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460d3ed754bcad38468a7e39c71a8ae0bd2a6e3f0fe243a6b06bf93fdc341ac`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf71e0662417ca9e09cdcb8dbe1ceaab2d24ca270364186656c3989fde4dd89f`  
		Last Modified: Mon, 29 Dec 2025 22:15:09 GMT  
		Size: 46.7 MB (46723619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccabf121282a73971c74c565541d08d7858279fd78860d4f539d7e055925dae`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:7b80c6aa4cb2a906161bb1363e3bab6e372c4fdfeb8e0905a5678b98b674a487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea0349cca0e8260efbb16808875c70ddb72cbe8efa0543b79bad57767ebdf79`

```dockerfile
```

-	Layers:
	-	`sha256:6fe270a0fa6590e1551a1ee4f6efd31418369e213caa83e16a1ca434588b3387`  
		Last Modified: Tue, 30 Dec 2025 01:10:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63df6effd3e9e12b969fcfa50ab1e9b2acaff2e83f72f2446a4d786944098fd`  
		Last Modified: Tue, 30 Dec 2025 01:10:33 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7a6812ddc9c24690d7a5a499003dc945857a175e7f5dda6981d1f7274749a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6243483a0b396d4fe7d53eaaf3249de044c8dc788057696eb33a805148646fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:05 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9a25acc457736a96b93a0281b7736208e4dc00987f78b5a473bb17e3487d70`  
		Last Modified: Mon, 29 Dec 2025 22:12:24 GMT  
		Size: 42.8 MB (42792487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2555957720388bf7fad85128cde658f26ed9c0878ea5e3587e5d61b776b17b`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:386b9114b5a54555c4beb1d339812a25a03b2a79342fc9c0a77f4a12689188c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0bdf4205aa969b25895232ca1c8c3366ef418998b9cad892302307b58a1d05`

```dockerfile
```

-	Layers:
	-	`sha256:9d9d0e6ec35917ebf98a85505427f212b0def2618d49faab2a9e6b98a4d12f1f`  
		Last Modified: Tue, 30 Dec 2025 01:10:36 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:068c114909900cf35accd4cb1e661d47fb16d4a9fc14cba2c991c5ec82143804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47288453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf94b991a93fcc4f35ceaa5860a12210bb8a3773a114e6dfbee0c00b361f1c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:27 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeadd60e258df383b0cc98606207bf109ef121df1971f4462b45ec54ee9f318`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 463.0 KB (462969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf7d2a33fd20248262d1c4cf1a1e70d0443286f144ff431455a223caa65601`  
		Last Modified: Mon, 29 Dec 2025 22:15:03 GMT  
		Size: 42.6 MB (42629375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c517dbb8d79767704a0d7fa570e4c08d418574401c1f3ed2aa365160213329d`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:c388de6c2b71abf77689d398e067a6bd8c9e90557af9ce13025e1e6a1766f53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb04cbf1de6bf71b2a625f6ccd7c33fdd963d4f1afd226100807e0e105080a7`

```dockerfile
```

-	Layers:
	-	`sha256:dbe071740321aed9566e9a7ce2de44c21da3fd82adef85df41ec2e1569447ddc`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4510a9494ca18bef567409f7d6cd142fde24682356b6be783ebb1f81b6a01b`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:3c36c86703831acb8abb0a22a2841be45264d32be03ee0076c136c81b12a1079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ef1b95ee8ae6ee6556e92f98edc54ea617c1925464e45e91d54911209e5e6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bedccbda7f6c026594b1bac44b809089174355a4e044e6ebfdc6286c9588756`  
		Last Modified: Mon, 29 Dec 2025 22:12:28 GMT  
		Size: 41.0 MB (40951452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a3d0d79b5160993f0c0a41639ed185b7a0f0bd4f4f8237368605fa4674ee2`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:4b586213bdae7d3e4ee91a8608d35500d306e36a06bc41c7f240ff60b6a15681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6810ccb80adb216f5b638e0a0253b8f04ebf89e679860c97482dde9e9bcb0c26`

```dockerfile
```

-	Layers:
	-	`sha256:595c3b71af7b44b03435988a57a0d7a6107af8e394fe81f30537110e5049411f`  
		Last Modified: Tue, 30 Dec 2025 01:10:44 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a33507a6c12c57f9d79818ef6f55e323f54095506204186caeef90c1cfea6f4`  
		Last Modified: Tue, 30 Dec 2025 01:10:45 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:d885398c11e1e2255f530086a8a38dd5703151f3d01ac65f37fa0ed677b3790d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49371197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423faff905cf66d01d4b68a15665db0f1efae634854bab7c395d35c3be94f799`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:17:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:17:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:17:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11e3a76c0fe809fef053b28f4223652f383a7155827cca3f996e6b5ad99347b`  
		Last Modified: Mon, 29 Dec 2025 22:22:50 GMT  
		Size: 45.3 MB (45325697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cded5f8ab82a089eef5c39ab4214eda5d15f737ee5865b41892a6b2a62423c`  
		Last Modified: Mon, 29 Dec 2025 22:22:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:cfd66037b02e24fbc4bf4e26ae9279b6f9cfd9034c24a39f5e34d0c15ae0bce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2d62009ccbbbac92862f457a0144b820e0544d6763726310a66361b80fbf9e`

```dockerfile
```

-	Layers:
	-	`sha256:745a3f8aa84f981044005ec6c920f6bb1dad5840785ce877c136dd5e098ed262`  
		Last Modified: Tue, 30 Dec 2025 01:10:48 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86df83cb3765bdd568c1f258f62e4e5a4b1fdaa5bebcdd69e11e5f9eba1d7ac9`  
		Last Modified: Tue, 30 Dec 2025 01:10:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:c8e0bcf5d966979dc1c7e217f9e49c4c4d37693e18a2e2521d82884dbf0b6f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49441303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2846fbc72078df664092ad73630af388378efe6d44006852635652c5f704974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:52 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa895b2e41ff3a43aa2644cdbbbf2b91678301e65d1804cc3ddd31bad02b85b`  
		Last Modified: Mon, 29 Dec 2025 22:12:55 GMT  
		Size: 45.3 MB (45254880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87e0c0d53b7263e6598aa3669471a57768b8f4f67198215ff65e4269eacf11`  
		Last Modified: Mon, 29 Dec 2025 22:12:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:9e2e342705e2de6737da28772b5f86362dd121c687d450ba873ca82d90f04e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282a7969c762c223edcd680164bca446cfe6172b44fdb559d211302bf1fcf083`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cf47226e83925db8f301df6f56d2a03543e2e5a7cf6b034bc1765b4e65e58`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a52bfeb8caa44a23436add6d2771844b859fa3c5503f91b4648602975bd3845`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e412515e710521fa7986c58e5d1c6760081b86409fbd7ada71c280008f6a7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:583653b643ac3f1f46003cb5420a6020ebbab38b4223e42dedccb73bdfb5a58c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173878068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3deb70fa9dfc3d168fd0f74db8842e94f92d1a34c9d1603651c6e4f2ae7206`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:26:01 GMT
RUN cmd /S /C #(nop) COPY file:bb401afdd9d3934a7a4f9b92a64ab967d454bd5889893f3e6bb99650a87af92c in \ 
# Mon, 29 Dec 2025 22:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282ed5ab3ad2747524afcc687c7af1981fee639f80841907ec190c541a8225a`  
		Last Modified: Mon, 29 Dec 2025 22:26:27 GMT  
		Size: 47.5 MB (47516598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c830cf11eb297146e37f3dc86b7d3eb61623f5ed17b3ad2c799157b35e1e24a9`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf10c5e839cb5e9a0e4e608989f75e46e276c01b90f16cf02628c3317ffe07e`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c62f03aa8b4ff4fbb3e842cb32d489adc9b7ff1cd733fbfdd369a333f7ca74`  
		Last Modified: Mon, 29 Dec 2025 22:26:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:89357a7b41ff2c571cfe33f4102c7933b0f7fb1c53a41bae1a30ddb83e7d7dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:9047cfdfe358271d4a6760faf9809787c81e8a906b0e5a3b341a0abbfdf9cb4a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828029861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76acbfb4dc298a43b62470fe1dd8b0b4093ce9938b3d3a328ef1143141a61c6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:20:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:20:12 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:20:13 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:20:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d4f4c744a59ac227520b5e733ac7e2c3bb8792ebea040dedecf0dd290fbb44`  
		Last Modified: Mon, 29 Dec 2025 22:20:47 GMT  
		Size: 48.1 MB (48145327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c42cd93e2c4a2994963205e46b4ec55d2b2f4c4d5d38f34f8f4d10e4d0625`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a558267a225392878a35ac6136c8729fe970c469f2d9bacd35f04d21568a2`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b61952c0488abc61e0aa13adc437b892be0123d5a2807c46192869a8e19f42`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:ec06628f2693a846bdf0d84a20e1c2d13026963370c422ef3c301a0ec95122f8
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
$ docker pull traefik@sha256:dde8db8bf8a8c2b68181a5bf51bad71b145427f8f42d85543c063a2878c5430c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51045034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c73645b5a95f5868c73795f8be36f1b016096ba044ca898ec4ec6bdf67f49a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:32 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460d3ed754bcad38468a7e39c71a8ae0bd2a6e3f0fe243a6b06bf93fdc341ac`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf71e0662417ca9e09cdcb8dbe1ceaab2d24ca270364186656c3989fde4dd89f`  
		Last Modified: Mon, 29 Dec 2025 22:15:09 GMT  
		Size: 46.7 MB (46723619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccabf121282a73971c74c565541d08d7858279fd78860d4f539d7e055925dae`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:7b80c6aa4cb2a906161bb1363e3bab6e372c4fdfeb8e0905a5678b98b674a487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea0349cca0e8260efbb16808875c70ddb72cbe8efa0543b79bad57767ebdf79`

```dockerfile
```

-	Layers:
	-	`sha256:6fe270a0fa6590e1551a1ee4f6efd31418369e213caa83e16a1ca434588b3387`  
		Last Modified: Tue, 30 Dec 2025 01:10:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63df6effd3e9e12b969fcfa50ab1e9b2acaff2e83f72f2446a4d786944098fd`  
		Last Modified: Tue, 30 Dec 2025 01:10:33 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7a6812ddc9c24690d7a5a499003dc945857a175e7f5dda6981d1f7274749a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6243483a0b396d4fe7d53eaaf3249de044c8dc788057696eb33a805148646fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:05 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9a25acc457736a96b93a0281b7736208e4dc00987f78b5a473bb17e3487d70`  
		Last Modified: Mon, 29 Dec 2025 22:12:24 GMT  
		Size: 42.8 MB (42792487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2555957720388bf7fad85128cde658f26ed9c0878ea5e3587e5d61b776b17b`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:386b9114b5a54555c4beb1d339812a25a03b2a79342fc9c0a77f4a12689188c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0bdf4205aa969b25895232ca1c8c3366ef418998b9cad892302307b58a1d05`

```dockerfile
```

-	Layers:
	-	`sha256:9d9d0e6ec35917ebf98a85505427f212b0def2618d49faab2a9e6b98a4d12f1f`  
		Last Modified: Tue, 30 Dec 2025 01:10:36 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:068c114909900cf35accd4cb1e661d47fb16d4a9fc14cba2c991c5ec82143804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47288453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf94b991a93fcc4f35ceaa5860a12210bb8a3773a114e6dfbee0c00b361f1c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:27 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeadd60e258df383b0cc98606207bf109ef121df1971f4462b45ec54ee9f318`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 463.0 KB (462969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf7d2a33fd20248262d1c4cf1a1e70d0443286f144ff431455a223caa65601`  
		Last Modified: Mon, 29 Dec 2025 22:15:03 GMT  
		Size: 42.6 MB (42629375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c517dbb8d79767704a0d7fa570e4c08d418574401c1f3ed2aa365160213329d`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c388de6c2b71abf77689d398e067a6bd8c9e90557af9ce13025e1e6a1766f53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb04cbf1de6bf71b2a625f6ccd7c33fdd963d4f1afd226100807e0e105080a7`

```dockerfile
```

-	Layers:
	-	`sha256:dbe071740321aed9566e9a7ce2de44c21da3fd82adef85df41ec2e1569447ddc`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4510a9494ca18bef567409f7d6cd142fde24682356b6be783ebb1f81b6a01b`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:3c36c86703831acb8abb0a22a2841be45264d32be03ee0076c136c81b12a1079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ef1b95ee8ae6ee6556e92f98edc54ea617c1925464e45e91d54911209e5e6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bedccbda7f6c026594b1bac44b809089174355a4e044e6ebfdc6286c9588756`  
		Last Modified: Mon, 29 Dec 2025 22:12:28 GMT  
		Size: 41.0 MB (40951452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a3d0d79b5160993f0c0a41639ed185b7a0f0bd4f4f8237368605fa4674ee2`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:4b586213bdae7d3e4ee91a8608d35500d306e36a06bc41c7f240ff60b6a15681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6810ccb80adb216f5b638e0a0253b8f04ebf89e679860c97482dde9e9bcb0c26`

```dockerfile
```

-	Layers:
	-	`sha256:595c3b71af7b44b03435988a57a0d7a6107af8e394fe81f30537110e5049411f`  
		Last Modified: Tue, 30 Dec 2025 01:10:44 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a33507a6c12c57f9d79818ef6f55e323f54095506204186caeef90c1cfea6f4`  
		Last Modified: Tue, 30 Dec 2025 01:10:45 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:d885398c11e1e2255f530086a8a38dd5703151f3d01ac65f37fa0ed677b3790d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49371197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423faff905cf66d01d4b68a15665db0f1efae634854bab7c395d35c3be94f799`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:17:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:17:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:17:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11e3a76c0fe809fef053b28f4223652f383a7155827cca3f996e6b5ad99347b`  
		Last Modified: Mon, 29 Dec 2025 22:22:50 GMT  
		Size: 45.3 MB (45325697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cded5f8ab82a089eef5c39ab4214eda5d15f737ee5865b41892a6b2a62423c`  
		Last Modified: Mon, 29 Dec 2025 22:22:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:cfd66037b02e24fbc4bf4e26ae9279b6f9cfd9034c24a39f5e34d0c15ae0bce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2d62009ccbbbac92862f457a0144b820e0544d6763726310a66361b80fbf9e`

```dockerfile
```

-	Layers:
	-	`sha256:745a3f8aa84f981044005ec6c920f6bb1dad5840785ce877c136dd5e098ed262`  
		Last Modified: Tue, 30 Dec 2025 01:10:48 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86df83cb3765bdd568c1f258f62e4e5a4b1fdaa5bebcdd69e11e5f9eba1d7ac9`  
		Last Modified: Tue, 30 Dec 2025 01:10:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:c8e0bcf5d966979dc1c7e217f9e49c4c4d37693e18a2e2521d82884dbf0b6f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49441303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2846fbc72078df664092ad73630af388378efe6d44006852635652c5f704974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:52 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa895b2e41ff3a43aa2644cdbbbf2b91678301e65d1804cc3ddd31bad02b85b`  
		Last Modified: Mon, 29 Dec 2025 22:12:55 GMT  
		Size: 45.3 MB (45254880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87e0c0d53b7263e6598aa3669471a57768b8f4f67198215ff65e4269eacf11`  
		Last Modified: Mon, 29 Dec 2025 22:12:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:9e2e342705e2de6737da28772b5f86362dd121c687d450ba873ca82d90f04e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282a7969c762c223edcd680164bca446cfe6172b44fdb559d211302bf1fcf083`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cf47226e83925db8f301df6f56d2a03543e2e5a7cf6b034bc1765b4e65e58`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a52bfeb8caa44a23436add6d2771844b859fa3c5503f91b4648602975bd3845`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e412515e710521fa7986c58e5d1c6760081b86409fbd7ada71c280008f6a7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:583653b643ac3f1f46003cb5420a6020ebbab38b4223e42dedccb73bdfb5a58c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173878068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3deb70fa9dfc3d168fd0f74db8842e94f92d1a34c9d1603651c6e4f2ae7206`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:26:01 GMT
RUN cmd /S /C #(nop) COPY file:bb401afdd9d3934a7a4f9b92a64ab967d454bd5889893f3e6bb99650a87af92c in \ 
# Mon, 29 Dec 2025 22:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282ed5ab3ad2747524afcc687c7af1981fee639f80841907ec190c541a8225a`  
		Last Modified: Mon, 29 Dec 2025 22:26:27 GMT  
		Size: 47.5 MB (47516598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c830cf11eb297146e37f3dc86b7d3eb61623f5ed17b3ad2c799157b35e1e24a9`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf10c5e839cb5e9a0e4e608989f75e46e276c01b90f16cf02628c3317ffe07e`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c62f03aa8b4ff4fbb3e842cb32d489adc9b7ff1cd733fbfdd369a333f7ca74`  
		Last Modified: Mon, 29 Dec 2025 22:26:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:89357a7b41ff2c571cfe33f4102c7933b0f7fb1c53a41bae1a30ddb83e7d7dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:9047cfdfe358271d4a6760faf9809787c81e8a906b0e5a3b341a0abbfdf9cb4a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828029861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76acbfb4dc298a43b62470fe1dd8b0b4093ce9938b3d3a328ef1143141a61c6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:20:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:20:12 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:20:13 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:20:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d4f4c744a59ac227520b5e733ac7e2c3bb8792ebea040dedecf0dd290fbb44`  
		Last Modified: Mon, 29 Dec 2025 22:20:47 GMT  
		Size: 48.1 MB (48145327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c42cd93e2c4a2994963205e46b4ec55d2b2f4c4d5d38f34f8f4d10e4d0625`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a558267a225392878a35ac6136c8729fe970c469f2d9bacd35f04d21568a2`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b61952c0488abc61e0aa13adc437b892be0123d5a2807c46192869a8e19f42`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.34`

```console
$ docker pull traefik@sha256:ec06628f2693a846bdf0d84a20e1c2d13026963370c422ef3c301a0ec95122f8
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

### `traefik:v2.11.34` - linux; amd64

```console
$ docker pull traefik@sha256:dde8db8bf8a8c2b68181a5bf51bad71b145427f8f42d85543c063a2878c5430c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51045034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c73645b5a95f5868c73795f8be36f1b016096ba044ca898ec4ec6bdf67f49a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:29 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:32 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460d3ed754bcad38468a7e39c71a8ae0bd2a6e3f0fe243a6b06bf93fdc341ac`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf71e0662417ca9e09cdcb8dbe1ceaab2d24ca270364186656c3989fde4dd89f`  
		Last Modified: Mon, 29 Dec 2025 22:15:09 GMT  
		Size: 46.7 MB (46723619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccabf121282a73971c74c565541d08d7858279fd78860d4f539d7e055925dae`  
		Last Modified: Mon, 29 Dec 2025 22:15:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:7b80c6aa4cb2a906161bb1363e3bab6e372c4fdfeb8e0905a5678b98b674a487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea0349cca0e8260efbb16808875c70ddb72cbe8efa0543b79bad57767ebdf79`

```dockerfile
```

-	Layers:
	-	`sha256:6fe270a0fa6590e1551a1ee4f6efd31418369e213caa83e16a1ca434588b3387`  
		Last Modified: Tue, 30 Dec 2025 01:10:29 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63df6effd3e9e12b969fcfa50ab1e9b2acaff2e83f72f2446a4d786944098fd`  
		Last Modified: Tue, 30 Dec 2025 01:10:33 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7a6812ddc9c24690d7a5a499003dc945857a175e7f5dda6981d1f7274749a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46822733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6243483a0b396d4fe7d53eaaf3249de044c8dc788057696eb33a805148646fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:05 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9a25acc457736a96b93a0281b7736208e4dc00987f78b5a473bb17e3487d70`  
		Last Modified: Mon, 29 Dec 2025 22:12:24 GMT  
		Size: 42.8 MB (42792487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2555957720388bf7fad85128cde658f26ed9c0878ea5e3587e5d61b776b17b`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:386b9114b5a54555c4beb1d339812a25a03b2a79342fc9c0a77f4a12689188c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0bdf4205aa969b25895232ca1c8c3366ef418998b9cad892302307b58a1d05`

```dockerfile
```

-	Layers:
	-	`sha256:9d9d0e6ec35917ebf98a85505427f212b0def2618d49faab2a9e6b98a4d12f1f`  
		Last Modified: Tue, 30 Dec 2025 01:10:36 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:068c114909900cf35accd4cb1e661d47fb16d4a9fc14cba2c991c5ec82143804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47288453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf94b991a93fcc4f35ceaa5860a12210bb8a3773a114e6dfbee0c00b361f1c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:27 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeadd60e258df383b0cc98606207bf109ef121df1971f4462b45ec54ee9f318`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 463.0 KB (462969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf7d2a33fd20248262d1c4cf1a1e70d0443286f144ff431455a223caa65601`  
		Last Modified: Mon, 29 Dec 2025 22:15:03 GMT  
		Size: 42.6 MB (42629375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c517dbb8d79767704a0d7fa570e4c08d418574401c1f3ed2aa365160213329d`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:c388de6c2b71abf77689d398e067a6bd8c9e90557af9ce13025e1e6a1766f53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb04cbf1de6bf71b2a625f6ccd7c33fdd963d4f1afd226100807e0e105080a7`

```dockerfile
```

-	Layers:
	-	`sha256:dbe071740321aed9566e9a7ce2de44c21da3fd82adef85df41ec2e1569447ddc`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4510a9494ca18bef567409f7d6cd142fde24682356b6be783ebb1f81b6a01b`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.34` - linux; ppc64le

```console
$ docker pull traefik@sha256:3c36c86703831acb8abb0a22a2841be45264d32be03ee0076c136c81b12a1079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ef1b95ee8ae6ee6556e92f98edc54ea617c1925464e45e91d54911209e5e6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bedccbda7f6c026594b1bac44b809089174355a4e044e6ebfdc6286c9588756`  
		Last Modified: Mon, 29 Dec 2025 22:12:28 GMT  
		Size: 41.0 MB (40951452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a3d0d79b5160993f0c0a41639ed185b7a0f0bd4f4f8237368605fa4674ee2`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:4b586213bdae7d3e4ee91a8608d35500d306e36a06bc41c7f240ff60b6a15681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6810ccb80adb216f5b638e0a0253b8f04ebf89e679860c97482dde9e9bcb0c26`

```dockerfile
```

-	Layers:
	-	`sha256:595c3b71af7b44b03435988a57a0d7a6107af8e394fe81f30537110e5049411f`  
		Last Modified: Tue, 30 Dec 2025 01:10:44 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a33507a6c12c57f9d79818ef6f55e323f54095506204186caeef90c1cfea6f4`  
		Last Modified: Tue, 30 Dec 2025 01:10:45 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.34` - linux; riscv64

```console
$ docker pull traefik@sha256:d885398c11e1e2255f530086a8a38dd5703151f3d01ac65f37fa0ed677b3790d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49371197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423faff905cf66d01d4b68a15665db0f1efae634854bab7c395d35c3be94f799`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:17:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:17:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:17:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:17:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11e3a76c0fe809fef053b28f4223652f383a7155827cca3f996e6b5ad99347b`  
		Last Modified: Mon, 29 Dec 2025 22:22:50 GMT  
		Size: 45.3 MB (45325697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cded5f8ab82a089eef5c39ab4214eda5d15f737ee5865b41892a6b2a62423c`  
		Last Modified: Mon, 29 Dec 2025 22:22:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:cfd66037b02e24fbc4bf4e26ae9279b6f9cfd9034c24a39f5e34d0c15ae0bce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2d62009ccbbbac92862f457a0144b820e0544d6763726310a66361b80fbf9e`

```dockerfile
```

-	Layers:
	-	`sha256:745a3f8aa84f981044005ec6c920f6bb1dad5840785ce877c136dd5e098ed262`  
		Last Modified: Tue, 30 Dec 2025 01:10:48 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86df83cb3765bdd568c1f258f62e4e5a4b1fdaa5bebcdd69e11e5f9eba1d7ac9`  
		Last Modified: Tue, 30 Dec 2025 01:10:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.34` - linux; s390x

```console
$ docker pull traefik@sha256:c8e0bcf5d966979dc1c7e217f9e49c4c4d37693e18a2e2521d82884dbf0b6f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49441303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2846fbc72078df664092ad73630af388378efe6d44006852635652c5f704974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:52 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa895b2e41ff3a43aa2644cdbbbf2b91678301e65d1804cc3ddd31bad02b85b`  
		Last Modified: Mon, 29 Dec 2025 22:12:55 GMT  
		Size: 45.3 MB (45254880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87e0c0d53b7263e6598aa3669471a57768b8f4f67198215ff65e4269eacf11`  
		Last Modified: Mon, 29 Dec 2025 22:12:53 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.34` - unknown; unknown

```console
$ docker pull traefik@sha256:9e2e342705e2de6737da28772b5f86362dd121c687d450ba873ca82d90f04e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282a7969c762c223edcd680164bca446cfe6172b44fdb559d211302bf1fcf083`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cf47226e83925db8f301df6f56d2a03543e2e5a7cf6b034bc1765b4e65e58`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a52bfeb8caa44a23436add6d2771844b859fa3c5503f91b4648602975bd3845`  
		Last Modified: Tue, 30 Dec 2025 01:10:52 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.34-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e412515e710521fa7986c58e5d1c6760081b86409fbd7ada71c280008f6a7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11.34-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:583653b643ac3f1f46003cb5420a6020ebbab38b4223e42dedccb73bdfb5a58c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173878068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3deb70fa9dfc3d168fd0f74db8842e94f92d1a34c9d1603651c6e4f2ae7206`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:26:01 GMT
RUN cmd /S /C #(nop) COPY file:bb401afdd9d3934a7a4f9b92a64ab967d454bd5889893f3e6bb99650a87af92c in \ 
# Mon, 29 Dec 2025 22:26:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:26:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282ed5ab3ad2747524afcc687c7af1981fee639f80841907ec190c541a8225a`  
		Last Modified: Mon, 29 Dec 2025 22:26:27 GMT  
		Size: 47.5 MB (47516598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c830cf11eb297146e37f3dc86b7d3eb61623f5ed17b3ad2c799157b35e1e24a9`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf10c5e839cb5e9a0e4e608989f75e46e276c01b90f16cf02628c3317ffe07e`  
		Last Modified: Mon, 29 Dec 2025 22:26:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c62f03aa8b4ff4fbb3e842cb32d489adc9b7ff1cd733fbfdd369a333f7ca74`  
		Last Modified: Mon, 29 Dec 2025 22:26:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.34-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:89357a7b41ff2c571cfe33f4102c7933b0f7fb1c53a41bae1a30ddb83e7d7dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11.34-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:9047cfdfe358271d4a6760faf9809787c81e8a906b0e5a3b341a0abbfdf9cb4a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828029861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76acbfb4dc298a43b62470fe1dd8b0b4093ce9938b3d3a328ef1143141a61c6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:20:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.34/traefik_v2.11.34_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:20:12 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:20:13 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:20:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.34 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d4f4c744a59ac227520b5e733ac7e2c3bb8792ebea040dedecf0dd290fbb44`  
		Last Modified: Mon, 29 Dec 2025 22:20:47 GMT  
		Size: 48.1 MB (48145327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c42cd93e2c4a2994963205e46b4ec55d2b2f4c4d5d38f34f8f4d10e4d0625`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28a558267a225392878a35ac6136c8729fe970c469f2d9bacd35f04d21568a2`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b61952c0488abc61e0aa13adc437b892be0123d5a2807c46192869a8e19f42`  
		Last Modified: Mon, 29 Dec 2025 22:20:41 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:82d3d16dde0474a51fef00b28de143d48b67f7a27453224d5e7b5aaefff26a97
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
$ docker pull traefik@sha256:13e903c820dfeab5cb464ca6cc9f3b276317f768e324402f440cd3472f3612b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51976248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f174a52e1993a764172bba2c07106a766f2895b2b069a19c7d3bb6f69a18d222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:25 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a471ba94e701f551e79684073e592976607816526d57a987948bff6526c5b`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0802690440f2ca58ae524161b78276377a7a1b65b3f8f6c5053ffabb41708d54`  
		Last Modified: Mon, 29 Dec 2025 22:14:59 GMT  
		Size: 47.7 MB (47654821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e800de571d9f8e3e1570b7ab6ffa6cf7518881c2467f3b4ed474c5332aee3`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:00a627efcd6fc72b53d3bdd7a4ccfa21a4b6ed7f733c3388ed4cc08255f2309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.2 KB (854240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64e165bdaee378a18e512759d5d70d3c7a5dd930282041a764309dcfce32bac`

```dockerfile
```

-	Layers:
	-	`sha256:ff45197c317b2ca934a8cc34ddb376986be02b75920b99d313d539e6e7c911fa`  
		Last Modified: Tue, 30 Dec 2025 01:11:08 GMT  
		Size: 841.5 KB (841474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86fb8844e05b2481883284fb064a496d50c1a26502d834595358d8626eb4947`  
		Last Modified: Tue, 30 Dec 2025 01:11:09 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5457c0a157f7ed95be8253228daf32bba1a12ae1db68ba0337fee123623c347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47249818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c44ed4360eecfed4fbcbfa09e59c09eeea8e674776865aa3fc1af12df3ad9e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:26 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f336e0c0ee4704e0d01821f3ad4ea570e26819a11a2b63dbb387cf34084e4`  
		Last Modified: Mon, 29 Dec 2025 22:12:42 GMT  
		Size: 43.2 MB (43219572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b178f7eca0fa59dd94e45d3d21766dca74576e55362c4962bf9b8ceec0d72572`  
		Last Modified: Mon, 29 Dec 2025 22:12:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:a80f6381e2f7d4ad95451ebe1f7f4bc0d17ec0a8abf35d2a042d68ac291db1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5061d5772660ee643e094c24fd496931f45d553812861885b99cf369df7de503`

```dockerfile
```

-	Layers:
	-	`sha256:ab584a1e249e5e6a4f4a0ceb6f89a8dff471278819ca51a8c8936df3072f5f25`  
		Last Modified: Tue, 30 Dec 2025 01:11:12 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f3e50962d4a55032f1bcb106d9d9e00a62f9500f07d48beea58ea88ef29cd819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47929090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b8b96e4b90391bedf7bc092fbac775f0e8a1507cda4550480b89b7db5693b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a276118be49d5475e0a06948e16fc8cd4b0bda3c3898430f6114e63b13f8fe23`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253096b3edd30e4dea19f06bf189e516335ef1a629a1b1dc6af7a813331a3042`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 43.3 MB (43269978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeccce14e96312025b4be6b969ea3e7729ba121e7a62ac30994e6b3b55ddcc6f`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:f9c8baaf32db379ef5af0c9f077cbfb6adf222c4b83c8b02aca2bd01b15fd10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.9 KB (853859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bbcfb9b4da509161f176758b2d50a6611cc531e0d8cd2de3c4d3558d94b8d1`

```dockerfile
```

-	Layers:
	-	`sha256:202977780cf1f2517394823fc0ad01200ee0e7fe1d684742af45433eaa725bfd`  
		Last Modified: Tue, 30 Dec 2025 01:11:15 GMT  
		Size: 840.9 KB (840928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cddd80706ffbef64d8b4e4108248b1dd6574a0c4daa989ae65199763cb7fda8`  
		Last Modified: Tue, 30 Dec 2025 01:11:16 GMT  
		Size: 12.9 KB (12931 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:f370bfaf055906751a40aa2602862664385167c1ed4702e7b2845646e09f1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45411891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4c43778d8848986aa9c6e57346998df3e0553b9f60f37cf46b1af9dd9cadad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a14a5a8b1e9f321ce7c2ee0dd494572157283dabd4908919bd42a2624bd9b7f`  
		Last Modified: Mon, 29 Dec 2025 22:12:33 GMT  
		Size: 41.1 MB (41120256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1c0ce4e6e90bd62ef1527e0b929814a30b66ab9dfa97b1fdfa5a10ca69246`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:14d63ad02ff72713a77bb9d2cd51f1a84807cca32f7a143e9be43ab2b7a8a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff23458bfec55077a9171f2ab6f84ee6b4504aafaec9d5448595db669dd79e7b`

```dockerfile
```

-	Layers:
	-	`sha256:92030776799ba4b7a5539a6f4eda6cc21d035b4bc63610bf72660d504c54ce84`  
		Last Modified: Tue, 30 Dec 2025 01:11:19 GMT  
		Size: 840.9 KB (840881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d937595ae2d0850f52fec601c1bf72a17b3a606174ad9de0fd4e98b024f34d`  
		Last Modified: Tue, 30 Dec 2025 01:11:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:fcad624b6c038a6ce9f23947bc913569ac3a582a361649bcec01cf7685fe1ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50131261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62d8c5216f1f866d94da4ac4114ab659a566122b37241eabbd2e9c0cb1e3e48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0941ee3a780b0edc04da4dbe59ee4854382951b9d7b3c7f0723617225bf179`  
		Last Modified: Mon, 29 Dec 2025 22:17:07 GMT  
		Size: 46.1 MB (46085759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0836a9f82df338c90828978f066ff4179a3786145f1409a81c9b0fda098ca079`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:4ee810a821586c1b7dfad2678e680c29cf91f9e5c939cb906f2836f399c58e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13baea432a1fff2eefd00a15970a4bb94d49230e48791f0ab1ad5f2ec56cdf35`

```dockerfile
```

-	Layers:
	-	`sha256:9dcc67bee13becd6a3dd7f1a1f4f19d3f8938adbf98359ce2bda9686e95c7543`  
		Last Modified: Tue, 30 Dec 2025 01:11:23 GMT  
		Size: 840.9 KB (840877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f6ac844190990794ea1badab8f0eb9008a988dae526b34259838d9c435ade8`  
		Last Modified: Tue, 30 Dec 2025 01:11:24 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:c90fb8eaf4f198acfcdc5ac5ee91d5017d85d7f1ee5ab34254e3e7413f75e7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50138784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b8c7e2ec2cce85fccc6ded5f989bcb54d35802064a883422107c8cec37788`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:48 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570fee54adbbcbd48c3264b6c1c48307759a232a8e62577915b34419d6908823`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2778402c6a2b9b0e23db64c01d948de928390074f3217c880d2e23fbad16d7c`  
		Last Modified: Mon, 29 Dec 2025 22:12:56 GMT  
		Size: 46.0 MB (45952359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82d9b41c12793837adea9cf222b43b978adf330a79cfe2facb415ae098f56f`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:f74a2a2e3a3fe763f6f53a84573d360bef963db9f78da5033b74dde5b86ed411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.6 KB (853589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d5912b64f161d66a4a5eecba009f5e5140eef5534c786abb8c0e7b13f74dd`

```dockerfile
```

-	Layers:
	-	`sha256:bc7b6070213f81954f2b800d7cec8f31869934919b88ebe831fad467713d455b`  
		Last Modified: Tue, 30 Dec 2025 01:11:27 GMT  
		Size: 840.8 KB (840823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb35d8c89e649d99bbb968932c09b39061aa837608b6d87face316071d01b18`  
		Last Modified: Tue, 30 Dec 2025 01:11:28 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5a06c29fbab874cee300291b95fe0afc4c24577dfeb4e52b91e87b8bb4a0b6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:89e7f45b4d36afe825781bf842c1b2ad594dda583c304e016a0696b90fda9cdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174773190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4167b1c56d9d49dc5d7a01b75d801b66a4580bd14a318da164f777eb9d9edeb8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:25:15 GMT
RUN cmd /S /C #(nop) COPY file:66315e29abc155939f3aa5baae45983776d9ac6f972112c785969c7332675bc4 in \ 
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:25:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe3710db5e56686dc75936e84ccb581a06c42485c91cc068ecf53aaa4d44d03`  
		Last Modified: Mon, 29 Dec 2025 22:25:55 GMT  
		Size: 48.4 MB (48411694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393668b98eb25293e345abf4ea21e1330bfe707727dfcbb662b255a1023a5c0d`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098625c20c4915bce3bf639faae72ec50f5979f0862783f4328a18015219137`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90d470c03edd3b2ad3f78d40bcf1c32d676318db21ce688e573e024160fa6e4`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:6a1d4363048b9caf4dde75474ab67fe10e742efd309cba4aecbfb6e6bdd80b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:e61041560509b551768ffe5ecf742e7f2668f06dcfdd0893fd284872dc853874
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828952089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f55d9baaf252e02a884479dc6a115e3d0dc82c3041f60a18031e485d203ab9b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:14:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:14:22 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:14:23 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493bb1b1e2906612559b21c8266db58d2befb0eef85e8f7c4ef50bb6a9b4e00b`  
		Last Modified: Mon, 29 Dec 2025 22:19:46 GMT  
		Size: 49.1 MB (49067574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a82646025bc5e6b27acd5447841931e26ddf6dedd74b01d003a9af276d112f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d4458d8a58188be1cc63f52855d2005c8db1495bbc7758a9c3b84c4bb898fb`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19bb40fd6917864ac17900b45224f4420bad7e7a17d608b05941a83b174282f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:82d3d16dde0474a51fef00b28de143d48b67f7a27453224d5e7b5aaefff26a97
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
$ docker pull traefik@sha256:13e903c820dfeab5cb464ca6cc9f3b276317f768e324402f440cd3472f3612b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51976248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f174a52e1993a764172bba2c07106a766f2895b2b069a19c7d3bb6f69a18d222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:25 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a471ba94e701f551e79684073e592976607816526d57a987948bff6526c5b`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0802690440f2ca58ae524161b78276377a7a1b65b3f8f6c5053ffabb41708d54`  
		Last Modified: Mon, 29 Dec 2025 22:14:59 GMT  
		Size: 47.7 MB (47654821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e800de571d9f8e3e1570b7ab6ffa6cf7518881c2467f3b4ed474c5332aee3`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:00a627efcd6fc72b53d3bdd7a4ccfa21a4b6ed7f733c3388ed4cc08255f2309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.2 KB (854240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64e165bdaee378a18e512759d5d70d3c7a5dd930282041a764309dcfce32bac`

```dockerfile
```

-	Layers:
	-	`sha256:ff45197c317b2ca934a8cc34ddb376986be02b75920b99d313d539e6e7c911fa`  
		Last Modified: Tue, 30 Dec 2025 01:11:08 GMT  
		Size: 841.5 KB (841474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86fb8844e05b2481883284fb064a496d50c1a26502d834595358d8626eb4947`  
		Last Modified: Tue, 30 Dec 2025 01:11:09 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5457c0a157f7ed95be8253228daf32bba1a12ae1db68ba0337fee123623c347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47249818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c44ed4360eecfed4fbcbfa09e59c09eeea8e674776865aa3fc1af12df3ad9e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:26 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f336e0c0ee4704e0d01821f3ad4ea570e26819a11a2b63dbb387cf34084e4`  
		Last Modified: Mon, 29 Dec 2025 22:12:42 GMT  
		Size: 43.2 MB (43219572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b178f7eca0fa59dd94e45d3d21766dca74576e55362c4962bf9b8ceec0d72572`  
		Last Modified: Mon, 29 Dec 2025 22:12:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:a80f6381e2f7d4ad95451ebe1f7f4bc0d17ec0a8abf35d2a042d68ac291db1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5061d5772660ee643e094c24fd496931f45d553812861885b99cf369df7de503`

```dockerfile
```

-	Layers:
	-	`sha256:ab584a1e249e5e6a4f4a0ceb6f89a8dff471278819ca51a8c8936df3072f5f25`  
		Last Modified: Tue, 30 Dec 2025 01:11:12 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f3e50962d4a55032f1bcb106d9d9e00a62f9500f07d48beea58ea88ef29cd819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47929090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b8b96e4b90391bedf7bc092fbac775f0e8a1507cda4550480b89b7db5693b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a276118be49d5475e0a06948e16fc8cd4b0bda3c3898430f6114e63b13f8fe23`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253096b3edd30e4dea19f06bf189e516335ef1a629a1b1dc6af7a813331a3042`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 43.3 MB (43269978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeccce14e96312025b4be6b969ea3e7729ba121e7a62ac30994e6b3b55ddcc6f`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:f9c8baaf32db379ef5af0c9f077cbfb6adf222c4b83c8b02aca2bd01b15fd10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.9 KB (853859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bbcfb9b4da509161f176758b2d50a6611cc531e0d8cd2de3c4d3558d94b8d1`

```dockerfile
```

-	Layers:
	-	`sha256:202977780cf1f2517394823fc0ad01200ee0e7fe1d684742af45433eaa725bfd`  
		Last Modified: Tue, 30 Dec 2025 01:11:15 GMT  
		Size: 840.9 KB (840928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cddd80706ffbef64d8b4e4108248b1dd6574a0c4daa989ae65199763cb7fda8`  
		Last Modified: Tue, 30 Dec 2025 01:11:16 GMT  
		Size: 12.9 KB (12931 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:f370bfaf055906751a40aa2602862664385167c1ed4702e7b2845646e09f1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45411891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4c43778d8848986aa9c6e57346998df3e0553b9f60f37cf46b1af9dd9cadad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a14a5a8b1e9f321ce7c2ee0dd494572157283dabd4908919bd42a2624bd9b7f`  
		Last Modified: Mon, 29 Dec 2025 22:12:33 GMT  
		Size: 41.1 MB (41120256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1c0ce4e6e90bd62ef1527e0b929814a30b66ab9dfa97b1fdfa5a10ca69246`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:14d63ad02ff72713a77bb9d2cd51f1a84807cca32f7a143e9be43ab2b7a8a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff23458bfec55077a9171f2ab6f84ee6b4504aafaec9d5448595db669dd79e7b`

```dockerfile
```

-	Layers:
	-	`sha256:92030776799ba4b7a5539a6f4eda6cc21d035b4bc63610bf72660d504c54ce84`  
		Last Modified: Tue, 30 Dec 2025 01:11:19 GMT  
		Size: 840.9 KB (840881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d937595ae2d0850f52fec601c1bf72a17b3a606174ad9de0fd4e98b024f34d`  
		Last Modified: Tue, 30 Dec 2025 01:11:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:fcad624b6c038a6ce9f23947bc913569ac3a582a361649bcec01cf7685fe1ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50131261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62d8c5216f1f866d94da4ac4114ab659a566122b37241eabbd2e9c0cb1e3e48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0941ee3a780b0edc04da4dbe59ee4854382951b9d7b3c7f0723617225bf179`  
		Last Modified: Mon, 29 Dec 2025 22:17:07 GMT  
		Size: 46.1 MB (46085759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0836a9f82df338c90828978f066ff4179a3786145f1409a81c9b0fda098ca079`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4ee810a821586c1b7dfad2678e680c29cf91f9e5c939cb906f2836f399c58e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13baea432a1fff2eefd00a15970a4bb94d49230e48791f0ab1ad5f2ec56cdf35`

```dockerfile
```

-	Layers:
	-	`sha256:9dcc67bee13becd6a3dd7f1a1f4f19d3f8938adbf98359ce2bda9686e95c7543`  
		Last Modified: Tue, 30 Dec 2025 01:11:23 GMT  
		Size: 840.9 KB (840877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f6ac844190990794ea1badab8f0eb9008a988dae526b34259838d9c435ade8`  
		Last Modified: Tue, 30 Dec 2025 01:11:24 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:c90fb8eaf4f198acfcdc5ac5ee91d5017d85d7f1ee5ab34254e3e7413f75e7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50138784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b8c7e2ec2cce85fccc6ded5f989bcb54d35802064a883422107c8cec37788`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:48 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570fee54adbbcbd48c3264b6c1c48307759a232a8e62577915b34419d6908823`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2778402c6a2b9b0e23db64c01d948de928390074f3217c880d2e23fbad16d7c`  
		Last Modified: Mon, 29 Dec 2025 22:12:56 GMT  
		Size: 46.0 MB (45952359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82d9b41c12793837adea9cf222b43b978adf330a79cfe2facb415ae098f56f`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:f74a2a2e3a3fe763f6f53a84573d360bef963db9f78da5033b74dde5b86ed411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.6 KB (853589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d5912b64f161d66a4a5eecba009f5e5140eef5534c786abb8c0e7b13f74dd`

```dockerfile
```

-	Layers:
	-	`sha256:bc7b6070213f81954f2b800d7cec8f31869934919b88ebe831fad467713d455b`  
		Last Modified: Tue, 30 Dec 2025 01:11:27 GMT  
		Size: 840.8 KB (840823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb35d8c89e649d99bbb968932c09b39061aa837608b6d87face316071d01b18`  
		Last Modified: Tue, 30 Dec 2025 01:11:28 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5a06c29fbab874cee300291b95fe0afc4c24577dfeb4e52b91e87b8bb4a0b6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:89e7f45b4d36afe825781bf842c1b2ad594dda583c304e016a0696b90fda9cdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174773190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4167b1c56d9d49dc5d7a01b75d801b66a4580bd14a318da164f777eb9d9edeb8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:25:15 GMT
RUN cmd /S /C #(nop) COPY file:66315e29abc155939f3aa5baae45983776d9ac6f972112c785969c7332675bc4 in \ 
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:25:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe3710db5e56686dc75936e84ccb581a06c42485c91cc068ecf53aaa4d44d03`  
		Last Modified: Mon, 29 Dec 2025 22:25:55 GMT  
		Size: 48.4 MB (48411694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393668b98eb25293e345abf4ea21e1330bfe707727dfcbb662b255a1023a5c0d`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098625c20c4915bce3bf639faae72ec50f5979f0862783f4328a18015219137`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90d470c03edd3b2ad3f78d40bcf1c32d676318db21ce688e573e024160fa6e4`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:6a1d4363048b9caf4dde75474ab67fe10e742efd309cba4aecbfb6e6bdd80b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:e61041560509b551768ffe5ecf742e7f2668f06dcfdd0893fd284872dc853874
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828952089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f55d9baaf252e02a884479dc6a115e3d0dc82c3041f60a18031e485d203ab9b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:14:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:14:22 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:14:23 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493bb1b1e2906612559b21c8266db58d2befb0eef85e8f7c4ef50bb6a9b4e00b`  
		Last Modified: Mon, 29 Dec 2025 22:19:46 GMT  
		Size: 49.1 MB (49067574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a82646025bc5e6b27acd5447841931e26ddf6dedd74b01d003a9af276d112f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d4458d8a58188be1cc63f52855d2005c8db1495bbc7758a9c3b84c4bb898fb`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19bb40fd6917864ac17900b45224f4420bad7e7a17d608b05941a83b174282f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.6`

```console
$ docker pull traefik@sha256:82d3d16dde0474a51fef00b28de143d48b67f7a27453224d5e7b5aaefff26a97
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

### `traefik:v3.6.6` - linux; amd64

```console
$ docker pull traefik@sha256:13e903c820dfeab5cb464ca6cc9f3b276317f768e324402f440cd3472f3612b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51976248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f174a52e1993a764172bba2c07106a766f2895b2b069a19c7d3bb6f69a18d222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:25 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:25 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a471ba94e701f551e79684073e592976607816526d57a987948bff6526c5b`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0802690440f2ca58ae524161b78276377a7a1b65b3f8f6c5053ffabb41708d54`  
		Last Modified: Mon, 29 Dec 2025 22:14:59 GMT  
		Size: 47.7 MB (47654821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e800de571d9f8e3e1570b7ab6ffa6cf7518881c2467f3b4ed474c5332aee3`  
		Last Modified: Mon, 29 Dec 2025 22:14:54 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:00a627efcd6fc72b53d3bdd7a4ccfa21a4b6ed7f733c3388ed4cc08255f2309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.2 KB (854240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64e165bdaee378a18e512759d5d70d3c7a5dd930282041a764309dcfce32bac`

```dockerfile
```

-	Layers:
	-	`sha256:ff45197c317b2ca934a8cc34ddb376986be02b75920b99d313d539e6e7c911fa`  
		Last Modified: Tue, 30 Dec 2025 01:11:08 GMT  
		Size: 841.5 KB (841474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86fb8844e05b2481883284fb064a496d50c1a26502d834595358d8626eb4947`  
		Last Modified: Tue, 30 Dec 2025 01:11:09 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5457c0a157f7ed95be8253228daf32bba1a12ae1db68ba0337fee123623c347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47249818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c44ed4360eecfed4fbcbfa09e59c09eeea8e674776865aa3fc1af12df3ad9e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:12:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:12:26 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:12:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:12:26 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:12:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeeeba1c6912c51d9c96fda324f536e2c03304f665f86c23f424f4e1c1c80a5`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 461.4 KB (461444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f336e0c0ee4704e0d01821f3ad4ea570e26819a11a2b63dbb387cf34084e4`  
		Last Modified: Mon, 29 Dec 2025 22:12:42 GMT  
		Size: 43.2 MB (43219572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b178f7eca0fa59dd94e45d3d21766dca74576e55362c4962bf9b8ceec0d72572`  
		Last Modified: Mon, 29 Dec 2025 22:12:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:a80f6381e2f7d4ad95451ebe1f7f4bc0d17ec0a8abf35d2a042d68ac291db1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5061d5772660ee643e094c24fd496931f45d553812861885b99cf369df7de503`

```dockerfile
```

-	Layers:
	-	`sha256:ab584a1e249e5e6a4f4a0ceb6f89a8dff471278819ca51a8c8936df3072f5f25`  
		Last Modified: Tue, 30 Dec 2025 01:11:12 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f3e50962d4a55032f1bcb106d9d9e00a62f9500f07d48beea58ea88ef29cd819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47929090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b8b96e4b90391bedf7bc092fbac775f0e8a1507cda4550480b89b7db5693b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:14:24 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:14:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:14:24 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a276118be49d5475e0a06948e16fc8cd4b0bda3c3898430f6114e63b13f8fe23`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 463.0 KB (463003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253096b3edd30e4dea19f06bf189e516335ef1a629a1b1dc6af7a813331a3042`  
		Last Modified: Mon, 29 Dec 2025 22:15:00 GMT  
		Size: 43.3 MB (43269978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeccce14e96312025b4be6b969ea3e7729ba121e7a62ac30994e6b3b55ddcc6f`  
		Last Modified: Mon, 29 Dec 2025 22:14:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:f9c8baaf32db379ef5af0c9f077cbfb6adf222c4b83c8b02aca2bd01b15fd10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.9 KB (853859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bbcfb9b4da509161f176758b2d50a6611cc531e0d8cd2de3c4d3558d94b8d1`

```dockerfile
```

-	Layers:
	-	`sha256:202977780cf1f2517394823fc0ad01200ee0e7fe1d684742af45433eaa725bfd`  
		Last Modified: Tue, 30 Dec 2025 01:11:15 GMT  
		Size: 840.9 KB (840928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cddd80706ffbef64d8b4e4108248b1dd6574a0c4daa989ae65199763cb7fda8`  
		Last Modified: Tue, 30 Dec 2025 01:11:16 GMT  
		Size: 12.9 KB (12931 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:f370bfaf055906751a40aa2602862664385167c1ed4702e7b2845646e09f1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45411891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4c43778d8848986aa9c6e57346998df3e0553b9f60f37cf46b1af9dd9cadad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:18 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a14a5a8b1e9f321ce7c2ee0dd494572157283dabd4908919bd42a2624bd9b7f`  
		Last Modified: Mon, 29 Dec 2025 22:12:33 GMT  
		Size: 41.1 MB (41120256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1c0ce4e6e90bd62ef1527e0b929814a30b66ab9dfa97b1fdfa5a10ca69246`  
		Last Modified: Mon, 29 Dec 2025 22:12:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:14d63ad02ff72713a77bb9d2cd51f1a84807cca32f7a143e9be43ab2b7a8a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff23458bfec55077a9171f2ab6f84ee6b4504aafaec9d5448595db669dd79e7b`

```dockerfile
```

-	Layers:
	-	`sha256:92030776799ba4b7a5539a6f4eda6cc21d035b4bc63610bf72660d504c54ce84`  
		Last Modified: Tue, 30 Dec 2025 01:11:19 GMT  
		Size: 840.9 KB (840881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d937595ae2d0850f52fec601c1bf72a17b3a606174ad9de0fd4e98b024f34d`  
		Last Modified: Tue, 30 Dec 2025 01:11:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.6` - linux; riscv64

```console
$ docker pull traefik@sha256:fcad624b6c038a6ce9f23947bc913569ac3a582a361649bcec01cf7685fe1ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50131261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62d8c5216f1f866d94da4ac4114ab659a566122b37241eabbd2e9c0cb1e3e48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:38 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a871247b950387d25cabd56f725806e9038dea17e76dc984ac2d2580eb8d43`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 461.2 KB (461194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0941ee3a780b0edc04da4dbe59ee4854382951b9d7b3c7f0723617225bf179`  
		Last Modified: Mon, 29 Dec 2025 22:17:07 GMT  
		Size: 46.1 MB (46085759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0836a9f82df338c90828978f066ff4179a3786145f1409a81c9b0fda098ca079`  
		Last Modified: Mon, 29 Dec 2025 22:17:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4ee810a821586c1b7dfad2678e680c29cf91f9e5c939cb906f2836f399c58e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.7 KB (853713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13baea432a1fff2eefd00a15970a4bb94d49230e48791f0ab1ad5f2ec56cdf35`

```dockerfile
```

-	Layers:
	-	`sha256:9dcc67bee13becd6a3dd7f1a1f4f19d3f8938adbf98359ce2bda9686e95c7543`  
		Last Modified: Tue, 30 Dec 2025 01:11:23 GMT  
		Size: 840.9 KB (840877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f6ac844190990794ea1badab8f0eb9008a988dae526b34259838d9c435ade8`  
		Last Modified: Tue, 30 Dec 2025 01:11:24 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.6` - linux; s390x

```console
$ docker pull traefik@sha256:c90fb8eaf4f198acfcdc5ac5ee91d5017d85d7f1ee5ab34254e3e7413f75e7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50138784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b8c7e2ec2cce85fccc6ded5f989bcb54d35802064a883422107c8cec37788`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:11:48 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
COPY entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 22:11:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 22:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 22:11:51 GMT
CMD ["traefik"]
# Mon, 29 Dec 2025 22:11:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570fee54adbbcbd48c3264b6c1c48307759a232a8e62577915b34419d6908823`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 461.7 KB (461744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2778402c6a2b9b0e23db64c01d948de928390074f3217c880d2e23fbad16d7c`  
		Last Modified: Mon, 29 Dec 2025 22:12:56 GMT  
		Size: 46.0 MB (45952359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82d9b41c12793837adea9cf222b43b978adf330a79cfe2facb415ae098f56f`  
		Last Modified: Mon, 29 Dec 2025 22:12:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.6` - unknown; unknown

```console
$ docker pull traefik@sha256:f74a2a2e3a3fe763f6f53a84573d360bef963db9f78da5033b74dde5b86ed411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.6 KB (853589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d5912b64f161d66a4a5eecba009f5e5140eef5534c786abb8c0e7b13f74dd`

```dockerfile
```

-	Layers:
	-	`sha256:bc7b6070213f81954f2b800d7cec8f31869934919b88ebe831fad467713d455b`  
		Last Modified: Tue, 30 Dec 2025 01:11:27 GMT  
		Size: 840.8 KB (840823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb35d8c89e649d99bbb968932c09b39061aa837608b6d87face316071d01b18`  
		Last Modified: Tue, 30 Dec 2025 01:11:28 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:5a06c29fbab874cee300291b95fe0afc4c24577dfeb4e52b91e87b8bb4a0b6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6.6-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:89e7f45b4d36afe825781bf842c1b2ad594dda583c304e016a0696b90fda9cdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174773190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4167b1c56d9d49dc5d7a01b75d801b66a4580bd14a318da164f777eb9d9edeb8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 29 Dec 2025 22:25:15 GMT
RUN cmd /S /C #(nop) COPY file:66315e29abc155939f3aa5baae45983776d9ac6f972112c785969c7332675bc4 in \ 
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 29 Dec 2025 22:25:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:25:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe3710db5e56686dc75936e84ccb581a06c42485c91cc068ecf53aaa4d44d03`  
		Last Modified: Mon, 29 Dec 2025 22:25:55 GMT  
		Size: 48.4 MB (48411694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393668b98eb25293e345abf4ea21e1330bfe707727dfcbb662b255a1023a5c0d`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098625c20c4915bce3bf639faae72ec50f5979f0862783f4328a18015219137`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90d470c03edd3b2ad3f78d40bcf1c32d676318db21ce688e573e024160fa6e4`  
		Last Modified: Mon, 29 Dec 2025 22:25:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:6a1d4363048b9caf4dde75474ab67fe10e742efd309cba4aecbfb6e6bdd80b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:e61041560509b551768ffe5ecf742e7f2668f06dcfdd0893fd284872dc853874
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828952089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f55d9baaf252e02a884479dc6a115e3d0dc82c3041f60a18031e485d203ab9b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:14:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:14:22 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:14:23 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493bb1b1e2906612559b21c8266db58d2befb0eef85e8f7c4ef50bb6a9b4e00b`  
		Last Modified: Mon, 29 Dec 2025 22:19:46 GMT  
		Size: 49.1 MB (49067574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a82646025bc5e6b27acd5447841931e26ddf6dedd74b01d003a9af276d112f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d4458d8a58188be1cc63f52855d2005c8db1495bbc7758a9c3b84c4bb898fb`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19bb40fd6917864ac17900b45224f4420bad7e7a17d608b05941a83b174282f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:6a1d4363048b9caf4dde75474ab67fe10e742efd309cba4aecbfb6e6bdd80b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:e61041560509b551768ffe5ecf742e7f2668f06dcfdd0893fd284872dc853874
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828952089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f55d9baaf252e02a884479dc6a115e3d0dc82c3041f60a18031e485d203ab9b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Mon, 29 Dec 2025 22:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Dec 2025 22:14:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 29 Dec 2025 22:14:22 GMT
EXPOSE 80
# Mon, 29 Dec 2025 22:14:23 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Dec 2025 22:14:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6e499f6581bdca1152a3e25ee14574435bc95419ba617f910896f7bba0d1556f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493bb1b1e2906612559b21c8266db58d2befb0eef85e8f7c4ef50bb6a9b4e00b`  
		Last Modified: Mon, 29 Dec 2025 22:19:46 GMT  
		Size: 49.1 MB (49067574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a82646025bc5e6b27acd5447841931e26ddf6dedd74b01d003a9af276d112f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d4458d8a58188be1cc63f52855d2005c8db1495bbc7758a9c3b84c4bb898fb`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19bb40fd6917864ac17900b45224f4420bad7e7a17d608b05941a83b174282f`  
		Last Modified: Mon, 29 Dec 2025 22:19:39 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
