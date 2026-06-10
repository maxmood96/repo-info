## `traefik:ramequin`

```console
$ docker pull traefik@sha256:e9ad2ada010742d2f91586a56f9ebb8355a2ceae7fb2973ef1c1877c7890e176
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
$ docker pull traefik@sha256:2ffe22bff6ac72572a3f6a06c4c5730dd7235bc1cc77a3bd872479827b3fae96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53217620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a424d315728c7af4100896b8f2b65c37082fa8a27fa9d4eea7a1e3282be815`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 17:56:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 10 Jun 2026 17:57:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.21/traefik_v3.6.21_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 10 Jun 2026 17:57:07 GMT
COPY entrypoint.sh / # buildkit
# Wed, 10 Jun 2026 17:57:07 GMT
EXPOSE map[80/tcp:{}]
# Wed, 10 Jun 2026 17:57:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2026 17:57:07 GMT
CMD ["traefik"]
# Wed, 10 Jun 2026 17:57:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.21 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a75aa05bae15c1ddcba3c7f6f9db58bd20220e875a9dc82723ca6e8f4c8c0e`  
		Last Modified: Wed, 10 Jun 2026 17:56:53 GMT  
		Size: 455.5 KB (455501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec34eb169601bbefd1f95dd74aeaf064ec259efb8c5ee63689d14a42db84f02`  
		Last Modified: Wed, 10 Jun 2026 17:57:30 GMT  
		Size: 48.9 MB (48897561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697af0213511f9169bfab2ea61d41a3f08888f5f102ba739cf2ed8a16807487`  
		Last Modified: Wed, 10 Jun 2026 17:57:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:f974981047988c62daeb1f30aff81bb27a7f1abbc26d0c577c409d60a278b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.4 KB (859385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803ed3519161344cb4422e5f914214801baf7de7712faf8f09d714d0e8d7e2b2`

```dockerfile
```

-	Layers:
	-	`sha256:37bb0855e9bb7483fe22540d6ddb55c87c2e8388a7a065dd5d8da2b5a30f2547`  
		Last Modified: Wed, 10 Jun 2026 17:57:29 GMT  
		Size: 847.4 KB (847376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc2a7264bb8965fb81857922aa154c02d0f7ba9e380572fd893456a26f37915`  
		Last Modified: Wed, 10 Jun 2026 17:57:28 GMT  
		Size: 12.0 KB (12009 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0d05e0192178dc202ad7d2b7053fab66b0e8c270fce099d025ddfb8fd9b18935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48437451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7feea36c160daf5f0fb6e22652f2934f13a21f33a157b3d0f6cc24e04bc777be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 17:54:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 10 Jun 2026 17:54:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.21/traefik_v3.6.21_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 10 Jun 2026 17:54:54 GMT
COPY entrypoint.sh / # buildkit
# Wed, 10 Jun 2026 17:54:54 GMT
EXPOSE map[80/tcp:{}]
# Wed, 10 Jun 2026 17:54:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2026 17:54:54 GMT
CMD ["traefik"]
# Wed, 10 Jun 2026 17:54:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.21 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0d05b914a0368c844a11c00e0282094d0ede4acb8b8bb05222ecc7e8596f60`  
		Last Modified: Wed, 10 Jun 2026 17:55:02 GMT  
		Size: 456.4 KB (456354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dec9cecc8bdc4379d6d17887edc0e9b74d6f0e123023b09aff0630fc5b96c1`  
		Last Modified: Wed, 10 Jun 2026 17:55:04 GMT  
		Size: 44.4 MB (44408866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3406a0a37d2e44d3b6fd3e0f052891d903175b5f4e7b49fb1ff866004e6766c8`  
		Last Modified: Wed, 10 Jun 2026 17:55:02 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:46d208e6bcbb6cf75932e5f01ba55dcb8c97fdd2b72df896e2963e91e9627a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 KB (11895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc56d9705707b25be68f131147ee8a65d40b172a2696e60b0b4b0a343b8f91e`

```dockerfile
```

-	Layers:
	-	`sha256:1ee864a915c99358173ea85ffe74c64d7b6170955abc92040cb524d8b80bd7cc`  
		Last Modified: Wed, 10 Jun 2026 17:55:02 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f9318483d3ccceadd98b94e4a3c95e22207f32e1788df3828e524a826b8a47d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48366817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cf60907d56c4a862c5f21fd9c036aaba06003cc6f28d0af5a2bcb8918cf8f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:09:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 10 Jun 2026 18:10:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.21/traefik_v3.6.21_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 10 Jun 2026 18:10:18 GMT
COPY entrypoint.sh / # buildkit
# Wed, 10 Jun 2026 18:10:18 GMT
EXPOSE map[80/tcp:{}]
# Wed, 10 Jun 2026 18:10:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2026 18:10:18 GMT
CMD ["traefik"]
# Wed, 10 Jun 2026 18:10:18 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.21 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db74bd980015a1d4106419b0a8586080d8e6402d918d8b847fbf5a1189583bf9`  
		Last Modified: Wed, 10 Jun 2026 18:09:51 GMT  
		Size: 457.8 KB (457770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7973471fa4dfcc7055873c9cdfa658eb205fffcf39e97cdc3b6f2ef1321d111`  
		Last Modified: Wed, 10 Jun 2026 18:10:44 GMT  
		Size: 43.7 MB (43708808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b3991473146c4c75e6de397ff48afc4be00534ff7be774a9b2f962fb5d094f`  
		Last Modified: Wed, 10 Jun 2026 18:10:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:3380e81d39f31c0addb4c61c41a487252ed660b92a55010e58a8327b572c2bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.9 KB (858934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4177ff4c8f0050f0e30d0b5d2db71f6550718add6f90698e3492a2ccac5ed1`

```dockerfile
```

-	Layers:
	-	`sha256:dc1b9624dfae8371cea92e6224b8ba4736412011c39f949f26ec8a99886f9b7f`  
		Last Modified: Wed, 10 Jun 2026 18:10:43 GMT  
		Size: 846.8 KB (846794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc9eb2bcbfd37bb3450f889103ea47cdbb12c8c6428a5c78bcde6f20e131492`  
		Last Modified: Wed, 10 Jun 2026 18:10:43 GMT  
		Size: 12.1 KB (12140 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:46a78945df85828ad83de5433e75a2b82c75aa03c21934634012884e2324aa00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46606991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91cddfefb714c7990ab1bfe5b4a7a9b37c00df1a3bd0e9528b88d4882e2fa7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:14:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 10 Jun 2026 17:55:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.21/traefik_v3.6.21_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 10 Jun 2026 17:55:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 10 Jun 2026 17:55:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 10 Jun 2026 17:55:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2026 17:55:11 GMT
CMD ["traefik"]
# Wed, 10 Jun 2026 17:55:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.21 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5c5615b636354b38c6e252f0d91db799b206304dbe496f9997696f5f8b7fcd`  
		Last Modified: Thu, 04 Jun 2026 18:15:05 GMT  
		Size: 458.2 KB (458181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d74e6d2c7f86d5d15680b2fc6c12c5aa013b0e2616def80dcba4dadacaa7309`  
		Last Modified: Wed, 10 Jun 2026 17:56:10 GMT  
		Size: 42.3 MB (42317512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390d729ce52e8abcab70698907b4823732e87ef8dfcd915783e990422baf66fc`  
		Last Modified: Wed, 10 Jun 2026 17:56:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:749c0d4039b8abbf58e519d1368fee14cca7a190fad32b276043ce9dc7fbf2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.8 KB (858826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3189f9fd91228f7094c66a9a9bfe481d6fed6ac1abbd29a3b130e4567ce05754`

```dockerfile
```

-	Layers:
	-	`sha256:f3706c22414a8f1d874e258cc81f28d33f26dbe96f6768145b5876f9131dc797`  
		Last Modified: Wed, 10 Jun 2026 17:56:09 GMT  
		Size: 846.8 KB (846765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30558b11cfe53a7981d5f483227237fe0c8fbbd06971b611be4fce67fa092988`  
		Last Modified: Wed, 10 Jun 2026 17:56:08 GMT  
		Size: 12.1 KB (12061 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:719375fbfcf5b5e7d80a9b2ebb258d1d685ab2abcdaefb90e4bf7924e7843664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51289512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d5168620fc0b610500115142c598de9d3368300ffcca5e4a39b64ed360c6b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 21:55:43 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 10 Jun 2026 18:01:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.21/traefik_v3.6.21_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 10 Jun 2026 18:01:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 10 Jun 2026 18:01:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 10 Jun 2026 18:01:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2026 18:01:11 GMT
CMD ["traefik"]
# Wed, 10 Jun 2026 18:01:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.21 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e303f921c87ae0f36457a84c9c4c730aafb81391e30ea18b39efc45d23a1eac`  
		Last Modified: Thu, 04 Jun 2026 22:00:49 GMT  
		Size: 455.8 KB (455827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a25211175180b4d4c16384a97719ab4eaf3ab98e5fbe4ddfb84a96799a1895`  
		Last Modified: Wed, 10 Jun 2026 18:06:13 GMT  
		Size: 47.2 MB (47245655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb36d760f4b1fe17896cd276e8953e68c41547751bbc0fdce56a359a54ee0cfc`  
		Last Modified: Wed, 10 Jun 2026 18:06:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:4c914991b7ba24567dd97f438122870b69929b535f5defaf2824f6f9cfc6e6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.8 KB (858822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484addecc035c15466837325306ba41c1db219b19b1cf45a946b9553778a6349`

```dockerfile
```

-	Layers:
	-	`sha256:0ada1ef93202abb85fe7138147c5f21daf7d465b0d4410334b05311d92bb42be`  
		Last Modified: Wed, 10 Jun 2026 18:06:06 GMT  
		Size: 846.8 KB (846761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:579ce096d4a200c45b4c2caebd3986b0d218f10eb5ce9eb1c034d0df87e80817`  
		Last Modified: Wed, 10 Jun 2026 18:06:06 GMT  
		Size: 12.1 KB (12061 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:1f60d75c86947b502a4e4ef9389d72a38ce8087c41bfae66ccd075e19aeec353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51254233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedbc68640121d3820237bcddaa6076d023403e3b6b9f78be0ebbf91d6190af0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:13:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 10 Jun 2026 18:20:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.21/traefik_v3.6.21_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 10 Jun 2026 18:20:10 GMT
COPY entrypoint.sh / # buildkit
# Wed, 10 Jun 2026 18:20:10 GMT
EXPOSE map[80/tcp:{}]
# Wed, 10 Jun 2026 18:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2026 18:20:10 GMT
CMD ["traefik"]
# Wed, 10 Jun 2026 18:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.21 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd843a525eda361ac29b49bfe49b99f8a532bb88914500c38af99cc05831c28`  
		Last Modified: Thu, 04 Jun 2026 18:14:16 GMT  
		Size: 456.5 KB (456472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9eb977c3a301409b41caccf177a1ebb70254f4b9fb86b04dd415b4b579a18`  
		Last Modified: Wed, 10 Jun 2026 18:22:49 GMT  
		Size: 47.1 MB (47070861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07402e4772b5f7470c67cfbddc0139ea4154b2b518546852dd2007b00e7b8706`  
		Last Modified: Wed, 10 Jun 2026 18:22:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:551757e30c8d2ffc82eb780b96d21ee082af6ba43c4be1f6ccd323c5303578d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.7 KB (858731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb67ab30aff7e291029d2d9c6c2c7875d79bd58942688cf613742a4840fdaaa`

```dockerfile
```

-	Layers:
	-	`sha256:e604b06609944025cfa8740065c9306979d3043dab5c740248664a4532b918d6`  
		Last Modified: Wed, 10 Jun 2026 18:22:41 GMT  
		Size: 846.7 KB (846723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eda6438549b6c3b29053426997fec7c187d6c66f2d61874b1e96f18a3f4bb292`  
		Last Modified: Wed, 10 Jun 2026 18:22:36 GMT  
		Size: 12.0 KB (12008 bytes)  
		MIME: application/vnd.in-toto+json
