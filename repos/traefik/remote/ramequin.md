## `traefik:ramequin`

```console
$ docker pull traefik@sha256:cc1799c50550f730f686df9b368e690f9199542787db8d1dd328a7c3779f6eea
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
$ docker pull traefik@sha256:8bb318ab853db934ca8a1e0719f8b52e58019727c41cdcc0d0b7418ff26b50cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53218427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2263fb4230e6a82c5d1d9f05dd217c27c0b7ebce8d8abdf20b68a6e1bb5025c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 17:23:24 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 05 Jun 2026 17:24:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.20/traefik_v3.6.20_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 05 Jun 2026 17:24:01 GMT
COPY entrypoint.sh / # buildkit
# Fri, 05 Jun 2026 17:24:01 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 17:24:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Jun 2026 17:24:01 GMT
CMD ["traefik"]
# Fri, 05 Jun 2026 17:24:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1746ab794c40fe71a8213b7b1d25e857a40b5c877ce0bfdf7df7cd916dedfb4`  
		Last Modified: Fri, 05 Jun 2026 17:23:50 GMT  
		Size: 455.5 KB (455513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28fa9a8090f936ceec5aa9b1cad0c2ca51b19f826363c886800075f1f3f626`  
		Last Modified: Fri, 05 Jun 2026 17:24:25 GMT  
		Size: 48.9 MB (48898359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31af4c9eb03894b2a124a2ff0688536376db4cbdcfe6ffde22404d9c1f961869`  
		Last Modified: Fri, 05 Jun 2026 17:24:23 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:a1652244967c4d3d3134e1744eb4320e7002ccd99137213098c1916dda1aef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.4 KB (859383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5dcaaa22b21a0951575c71c61dba02672a24fd6649bb9738e1a6a02053cae1`

```dockerfile
```

-	Layers:
	-	`sha256:d1c9759bd15b50b5dfff01c31869fa2f65a50a318f7bf630ffb38143fedc0c1e`  
		Last Modified: Fri, 05 Jun 2026 17:24:23 GMT  
		Size: 847.4 KB (847374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c65c6b6c4dea78d0664323038634f033f9e2748b449d98287e7410f1937daa3`  
		Last Modified: Fri, 05 Jun 2026 17:24:23 GMT  
		Size: 12.0 KB (12009 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4510719f7b02364a11ac8be5c2227d30a9707bc76e084c0e86a4542d6e8e3846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48435673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906b24e38b3a952b141b7767712ced257611401206a32d7e7e3de96623db25d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 17:23:03 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 05 Jun 2026 17:23:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.20/traefik_v3.6.20_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 05 Jun 2026 17:23:26 GMT
COPY entrypoint.sh / # buildkit
# Fri, 05 Jun 2026 17:23:26 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 17:23:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Jun 2026 17:23:26 GMT
CMD ["traefik"]
# Fri, 05 Jun 2026 17:23:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615df52d692bb457e90b43f346edea833529a277ade0b1e138c7ef01ebf8f65`  
		Last Modified: Fri, 05 Jun 2026 17:23:15 GMT  
		Size: 456.4 KB (456360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051fc369481e422bc8dab709898153c7532552ac0773cfd7d6eb372b1e6ba305`  
		Last Modified: Fri, 05 Jun 2026 17:23:35 GMT  
		Size: 44.4 MB (44407082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da815e113c2fe2e20d0ac0f473d396b860416c2c7ac9fb8c2b331641d9cc79c2`  
		Last Modified: Fri, 05 Jun 2026 17:23:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:c5bb7e98d8642c7c0a44cf1e00da0205a7ad0996642eac85a5cd8f0c7048433b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 KB (11895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f012a1e65f5b0d4c71657d8bf2a99f5b269a2f71dfb56210a180e4f7355a65`

```dockerfile
```

-	Layers:
	-	`sha256:7609e5f0159cc56d352b5d55a01493f164d0b85a44837b1a1a0ee882241140fc`  
		Last Modified: Fri, 05 Jun 2026 17:23:34 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:19f9e3f683998df873785e51be84cacf147b625999fa98c2a32a3f478366e8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48364039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1d7addca7dd07cf4270d3d2294c1b6694bc42cdeee6fcb7b0853e037ab85c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 17:23:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 05 Jun 2026 17:23:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.20/traefik_v3.6.20_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 05 Jun 2026 17:23:58 GMT
COPY entrypoint.sh / # buildkit
# Fri, 05 Jun 2026 17:23:58 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 17:23:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Jun 2026 17:23:58 GMT
CMD ["traefik"]
# Fri, 05 Jun 2026 17:23:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad77fa852f8ebecb1c7c4e115f9db3a59638f631f865a8ec796175bd99f8ecdc`  
		Last Modified: Fri, 05 Jun 2026 17:23:44 GMT  
		Size: 457.8 KB (457763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcb29832145b38c276eb43b310112080b9731980f5a35e0915776a1533a5dff`  
		Last Modified: Fri, 05 Jun 2026 17:24:24 GMT  
		Size: 43.7 MB (43706038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fe4241287bfe75b6615d0ca9b303c3725dcd16b4c1b3115f5f1b19562ffc21`  
		Last Modified: Fri, 05 Jun 2026 17:24:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:b61d514614c304c121a0899f1fe6e70805a50cdec09033a6ce7f0199ac47dcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.9 KB (858932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821851456f1c6d3605e040c78acc5ed055664a4e128d510c50c59d1b40b05d51`

```dockerfile
```

-	Layers:
	-	`sha256:80ed946070b20c69269cea48e04ed74bf33888551991f95e61335efddf403c4c`  
		Last Modified: Fri, 05 Jun 2026 17:24:24 GMT  
		Size: 846.8 KB (846792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:105bdca896ee5bad8732b45e88657350cd988016c58dadf40a3fd519fb2c58b6`  
		Last Modified: Fri, 05 Jun 2026 17:24:23 GMT  
		Size: 12.1 KB (12140 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:74d87c7e3cefdd0d98f102d75bcd7fd7d5baa08c0a0381c73abad507141f9bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46598300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592ae7f01dd6ddf6dad69708b73eeadf967d7e907bbd82cc2b38838e786e84f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:14:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 05 Jun 2026 17:27:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.20/traefik_v3.6.20_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 05 Jun 2026 17:27:08 GMT
COPY entrypoint.sh / # buildkit
# Fri, 05 Jun 2026 17:27:08 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 17:27:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Jun 2026 17:27:08 GMT
CMD ["traefik"]
# Fri, 05 Jun 2026 17:27:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.20 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:274c06b220395279b424525ad8b6a02d30fd8feee4d9fdf7781a017acae52ee7`  
		Last Modified: Fri, 05 Jun 2026 17:28:04 GMT  
		Size: 42.3 MB (42308821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de46b30aac84e69cda53f1bc4058b14b7297292e15b60d943859c7f2910e6c3`  
		Last Modified: Fri, 05 Jun 2026 17:28:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:213c60d235b91a3194ae2d3f0cad75d0256760a061ddf74ebd6f4715be627220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.8 KB (858823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc394d4d2e9f1c511c95de08e2e70777a6bb9e6d4d7f4bc21f22aad79574bc80`

```dockerfile
```

-	Layers:
	-	`sha256:dc7825f8f79039d3cd9b4c284b079aa7348105b6c53eedd58216f23b56db2707`  
		Last Modified: Fri, 05 Jun 2026 17:28:03 GMT  
		Size: 846.8 KB (846763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f59da38e5b91c2f36348513c006b34631b2a78108dcb02d9a71cf6956a56d78d`  
		Last Modified: Fri, 05 Jun 2026 17:28:03 GMT  
		Size: 12.1 KB (12060 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:2e06bcfd28348e8de65805c66bc9696d803e2e1526fd431ba5189101ebf74762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51286160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0413e2a9f6dd84be28e049f4d4b065512080105b37f12654f649b6056e562e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 21:55:43 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 05 Jun 2026 17:28:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.20/traefik_v3.6.20_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 05 Jun 2026 17:28:03 GMT
COPY entrypoint.sh / # buildkit
# Fri, 05 Jun 2026 17:28:03 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 17:28:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Jun 2026 17:28:03 GMT
CMD ["traefik"]
# Fri, 05 Jun 2026 17:28:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.20 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:ffbf68f3da716665f9525f2ed8970d5949dcf2235e503ea1930b6114ad469510`  
		Last Modified: Fri, 05 Jun 2026 17:33:02 GMT  
		Size: 47.2 MB (47242302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601b2cbbb85aff868fd73f71c80c1cff870a37d7483112293693cc97e376504b`  
		Last Modified: Fri, 05 Jun 2026 17:32:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:d752b2908722759cd6c3a3d2f263cedb7b44fcf1dffa764b910ce53b7edc9383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.8 KB (858819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc621106f36af9ca21b059cb0e400f48d023df72f30411469aae29adf6cb51e`

```dockerfile
```

-	Layers:
	-	`sha256:bf83ac01eb0d9695848aee9e4f26c38982bfe1334d7a84a9be6b47338df127c9`  
		Last Modified: Fri, 05 Jun 2026 17:32:55 GMT  
		Size: 846.8 KB (846759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def16e052a85d40d87054822d1be48ed0cbf8c5db893488ce64cbf31384209de`  
		Last Modified: Fri, 05 Jun 2026 17:32:55 GMT  
		Size: 12.1 KB (12060 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:c42249e6bee338583dd5dd15ad7d2529a3a209edc6284ebff8c96e5bb057a81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51250831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4392a6445e74dcfdbfa2b2fc01db81842b63f7eb044d5d84c7d8360b94dd89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:13:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 05 Jun 2026 17:22:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.20/traefik_v3.6.20_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 05 Jun 2026 17:22:22 GMT
COPY entrypoint.sh / # buildkit
# Fri, 05 Jun 2026 17:22:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 17:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Jun 2026 17:22:22 GMT
CMD ["traefik"]
# Fri, 05 Jun 2026 17:22:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.20 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f1bdb3a1352961fa540c744cd7040525500ecbd2be84c3b294470a4b72be6884`  
		Last Modified: Fri, 05 Jun 2026 17:23:16 GMT  
		Size: 47.1 MB (47067458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fe70db70f02c4e2ab000d2016cc2bb27850d8b5c584636cd9395c982a48238`  
		Last Modified: Fri, 05 Jun 2026 17:23:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:f455fe0d1d959ae418339aae9e3c1a12243f398dc405e9f77105109b86d0927f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.7 KB (858730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0b00afeffedf336e6fa6d6eceb83537a69ae1ba133bcc90fcb1331ca25b02c`

```dockerfile
```

-	Layers:
	-	`sha256:7103cc801bc6c066856bc5dae5d067b6a2e3a7d3f5b7121bcb88768a2edbb8da`  
		Last Modified: Fri, 05 Jun 2026 17:23:15 GMT  
		Size: 846.7 KB (846721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3552e78d10b028acf322d6e26fc4fccaf174a19f092b94df7ed7e4bc7eec05f9`  
		Last Modified: Fri, 05 Jun 2026 17:23:15 GMT  
		Size: 12.0 KB (12009 bytes)  
		MIME: application/vnd.in-toto+json
