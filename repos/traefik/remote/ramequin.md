## `traefik:ramequin`

```console
$ docker pull traefik@sha256:6684baec5fbfae10e2addba5d1015160de7aca87741b26bead52fe1603699a18
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
$ docker pull traefik@sha256:c175497f5ad669a499179ffe02b1e4bb344fc85305acc6e03f7d8bef3b238a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53215348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a6d397eb53fd699d9c7e8ae135e20b7dcd7b70a7bd9238e56aa7b71c9020cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:12:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Jun 2026 18:12:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.19/traefik_v3.6.19_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Jun 2026 18:12:44 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Jun 2026 18:12:44 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Jun 2026 18:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
CMD ["traefik"]
# Thu, 04 Jun 2026 18:12:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.19 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d860d5432cbedcd3c3b278e73d7da17fb7d2162a5ad3e0fd0ac0f2e1aded2506`  
		Last Modified: Thu, 04 Jun 2026 18:13:07 GMT  
		Size: 455.5 KB (455502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e74ac72cea3e90fe9c60fca20f3344c6bb4fa0f991fe71cdc110ad1b32efe6`  
		Last Modified: Thu, 04 Jun 2026 18:13:08 GMT  
		Size: 48.9 MB (48895288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a3f1b516593bc3498509ae525348ff155608ce60b6fbfdbd0833765337291f`  
		Last Modified: Thu, 04 Jun 2026 18:13:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:0dcf8a6114d806e662b3a47be1d2cbe35423c01cc5553f9bcd27ba0e79121c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.4 KB (859383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1aba8feb49a39d621edeac2d4a4fad0a5822333b20a527147958d774d7a80d`

```dockerfile
```

-	Layers:
	-	`sha256:ec4eb1a8cd80fc95897502fa328aa5bb2984ff146a1f42230e60cf514dbd78e2`  
		Last Modified: Thu, 04 Jun 2026 18:13:07 GMT  
		Size: 847.4 KB (847374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e844a10bbf6e9856f9245da9111eefdefc36614bdc87a6c7469da4d1282d3b25`  
		Last Modified: Thu, 04 Jun 2026 18:13:07 GMT  
		Size: 12.0 KB (12009 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:30bdd52118212d7dee4734ce67e7045d296d3bef6428655b55d309b2174da6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48432014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eafc3cf0cbbe08809bbb0c9d2586acc16546d11d113e942db4de3f0a2b919a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:12:43 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Jun 2026 18:12:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.19/traefik_v3.6.19_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Jun 2026 18:12:46 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Jun 2026 18:12:46 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Jun 2026 18:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:46 GMT
CMD ["traefik"]
# Thu, 04 Jun 2026 18:12:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.19 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178d473c1bb334310ee2f3175de44c9261dd8ee76ac392c34c057bd7b53ab24c`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 456.3 KB (456337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5070e690014a6c836f43248966db9a128d151301a4806f3898525c90374ad44b`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 44.4 MB (44403445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f270cf14e83a34d1895165474b8638ec04413f706767aff0fa0b59421d424b4`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:84cf82955ef8b13097d3c59c42173e9aab53f6d978f96f6ca59072098e56ef21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 KB (11895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954b56fb5fa7c65ac66df07acd6a68d07ef93f7946018f7efbc6bed9a7048123`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c7d758371ae50d15400856ed60752b92e9559201da3c2177158a578ee1544`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:04e3de3d584d6978fb003922f3ab98addc3668cae5482631b55451b750ea322c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48357815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d923231f29f36c08f2e903c3f1d20d1a9c2dac4b0f1199731f9bc2432dba1dbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:12:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.19/traefik_v3.6.19_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Jun 2026 18:12:45 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Jun 2026 18:12:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:45 GMT
CMD ["traefik"]
# Thu, 04 Jun 2026 18:12:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.19 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ff59e39973a1bfcf3861676d1ec295fc39cff72cb55610f959c75269eb5acc`  
		Last Modified: Thu, 04 Jun 2026 18:13:10 GMT  
		Size: 457.8 KB (457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f334a3e8ea25a259135d6b3ef6f009d2733a5d9694bb6a7e9568544e2e44bc`  
		Last Modified: Thu, 04 Jun 2026 18:13:11 GMT  
		Size: 43.7 MB (43699800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f270cf14e83a34d1895165474b8638ec04413f706767aff0fa0b59421d424b4`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:0487016520a6bdf212a817b919df8aeed0d1fe5a424d876ef3026838bf1ea0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.9 KB (858932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17700b345e7d97b093a301b478083b3d104c09d904afcb02e3b385fedd66d58f`

```dockerfile
```

-	Layers:
	-	`sha256:58b75f76e3ca5a403ac5c4cddec19911d71f8da4256d44044e9d979d2919ab77`  
		Last Modified: Thu, 04 Jun 2026 18:13:10 GMT  
		Size: 846.8 KB (846792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53870678fee836be4a0b6e8b3361ca9876c36347e9c1460671cf44123074e15d`  
		Last Modified: Thu, 04 Jun 2026 18:13:10 GMT  
		Size: 12.1 KB (12140 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:992c13de0c9a229813c1d386741b04756761c7bc6c03c9d8e2827b6e5d6a7e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46591539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d539b69caa325283f30d67333c3bb9567e4e1627003eb5a9f60fbdd8727ee4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:14:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Jun 2026 18:14:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.19/traefik_v3.6.19_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Jun 2026 18:14:15 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Jun 2026 18:14:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Jun 2026 18:14:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jun 2026 18:14:15 GMT
CMD ["traefik"]
# Thu, 04 Jun 2026 18:14:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.19 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:9c27ec8e21bde0168a94b08b45f6f872d6962f33dfc3024ed91754800547f58b`  
		Last Modified: Thu, 04 Jun 2026 18:15:07 GMT  
		Size: 42.3 MB (42302061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23319c1ee7e3c96f0d14b8d8b03c79ff482e92acca0ca313a18811e13ce5e9d`  
		Last Modified: Thu, 04 Jun 2026 18:15:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:a27a4b1ec606277af468f327b2e8f09fad7156804b9e070d7dec42c82499dd04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.8 KB (858824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2baa66fcc22b1bfe77a0ffcd527bcd96fe3e9553fba766bef26b48186cb7262d`

```dockerfile
```

-	Layers:
	-	`sha256:84a0ef5a834d6ed8da4c2a95f9b64c5b5d71108592c9688377416640ee870d96`  
		Last Modified: Thu, 04 Jun 2026 18:15:06 GMT  
		Size: 846.8 KB (846763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2e9d6266d5036589aa78da6b1e08d0e543b6c1885f8087d3762cbe7ea0f152`  
		Last Modified: Thu, 04 Jun 2026 18:15:06 GMT  
		Size: 12.1 KB (12061 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:80f0432d39a1d548658f04d645c6d4fa1978a36d82b57a9ac4f44ce89538f86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51262854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8429e3eb8f310d50e7aad24e1d9dd9061b41f080dce6e12ba00a4a3ed795ecad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 13 May 2026 12:19:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 13 May 2026 12:25:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.17/traefik_v3.6.17_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 13 May 2026 12:25:22 GMT
COPY entrypoint.sh / # buildkit
# Wed, 13 May 2026 12:25:22 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 12:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 12:25:22 GMT
CMD ["traefik"]
# Wed, 13 May 2026 12:25:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.17 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fec3377cecfaabfbad434bb7a79f5b7898b4b04500ba155118bee98bec26258`  
		Last Modified: Wed, 13 May 2026 12:24:36 GMT  
		Size: 455.8 KB (455808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62904511525388658c03752b35a8b24f49c46a19f28028ef80520755f777b883`  
		Last Modified: Wed, 13 May 2026 12:30:13 GMT  
		Size: 47.2 MB (47219015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46403617f9e75a35db5dcf56bff3db027e404fc7e06187a8b5937478b4bb08e`  
		Last Modified: Wed, 13 May 2026 12:30:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:198567ac9343500ec8fc7b4691a0751ae60508b2260a63884ce236a4f3a33385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.8 KB (858818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112e664c9aff24ed5abec359b2fe6c336f54f8bd6360c08b4287fe449e4e52a3`

```dockerfile
```

-	Layers:
	-	`sha256:3e2c961854e8b26fbba9b505c3722c8b79d3b2ef85211f921028c77f1a595abb`  
		Last Modified: Wed, 13 May 2026 12:30:04 GMT  
		Size: 846.8 KB (846757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cab741a4adc5b16e1856563c9be12abbedb483da4e13da76572538353887d54`  
		Last Modified: Wed, 13 May 2026 12:30:04 GMT  
		Size: 12.1 KB (12061 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:9b5896efe67d11b420f2cbc647d8840be87b92a07d9e20bd3c78dfafe28c0de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51250835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91650ee64cde2ebec416210fdaf4f87aefa91d4b546c406549e441fa500ee029`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:13:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Jun 2026 18:13:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.19/traefik_v3.6.19_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Jun 2026 18:13:23 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Jun 2026 18:13:23 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Jun 2026 18:13:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jun 2026 18:13:23 GMT
CMD ["traefik"]
# Thu, 04 Jun 2026 18:13:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.19 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a2f30ae67af9028819234a76281ffe381ee5584d14c2a7d636212f6c26162782`  
		Last Modified: Thu, 04 Jun 2026 18:14:19 GMT  
		Size: 47.1 MB (47067462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22447a5ddfb2220512771daa3836503eb01cd725fa97806c437a8070d2f8f44a`  
		Last Modified: Thu, 04 Jun 2026 18:14:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:182d08d20053ac62f822595af6e9a59cfaabc5824ad410a0cef6279bf759f54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.7 KB (858730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59d5b6672f22db1fe6e6553e1c169cd9edf00c6414c20c4b0a277d61a62ddd5`

```dockerfile
```

-	Layers:
	-	`sha256:cef4dbae9f59ef5b59a7ae87ed3aa5514d608b9ba7b4b666a5702c1148f33d39`  
		Last Modified: Thu, 04 Jun 2026 18:14:18 GMT  
		Size: 846.7 KB (846721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d37c271fa8f4d729974f3255a98e8e97d1d4fd740498c12b0848a7ec7f9a4c55`  
		Last Modified: Thu, 04 Jun 2026 18:14:18 GMT  
		Size: 12.0 KB (12009 bytes)  
		MIME: application/vnd.in-toto+json
