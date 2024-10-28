## `traefik:munster`

```console
$ docker pull traefik@sha256:66e37237b371f2b25ce5f247cc371976929dcb18c041e05685f1de1df6422b72
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

### `traefik:munster` - linux; amd64

```console
$ docker pull traefik@sha256:e8a75d3640365b5a9f2b5fbcd8c745becdceabf3b7dc4e202094fb2bf03c1d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51213383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a77d0f20449bbe2c1a2f3577d2bf59e00bb439ec70244382a98094a3c5ac809`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.2.0/traefik_v3.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 15:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 15:43:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67834940f1bc7860576615be7be1f60478eeae5d14e9c8dcdfbd32d76229846`  
		Last Modified: Mon, 28 Oct 2024 17:57:11 GMT  
		Size: 455.1 KB (455126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b2e3bd9681f2060ec0f1f0314fda751e6d1e6d44420b2ed4d809156dcda141`  
		Last Modified: Mon, 28 Oct 2024 17:57:12 GMT  
		Size: 47.1 MB (47134081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec9a59d4a69cf00200845e88182e9e795a982fab7eb7eb0cb60272678f0a9cb`  
		Last Modified: Mon, 28 Oct 2024 17:57:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:munster` - unknown; unknown

```console
$ docker pull traefik@sha256:f583b6eed30cc91fb98b3c0f073c5b460f38e7aff42ca19edb272f64b88bbea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **821.7 KB (821738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e948dce4e4c0796fd6d43ced0d502a40129828dcb34525c8969c5a2d94aaa35`

```dockerfile
```

-	Layers:
	-	`sha256:a2fba8bc053117a893797e430c91b4423a34b7af70f4cf97a84b91f1b7da9af1`  
		Last Modified: Mon, 28 Oct 2024 17:57:11 GMT  
		Size: 809.1 KB (809130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8332d492dd4fab9f371fc9b4e95e0a2cfbbea63a1e2932f7ffdcf4ad7a5e2ebf`  
		Last Modified: Mon, 28 Oct 2024 17:57:11 GMT  
		Size: 12.6 KB (12608 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:munster` - linux; arm variant v6

```console
$ docker pull traefik@sha256:45fed7ded292854ad6d59a9b9f5468c361b5d7b5797c6ad168183334a76e6cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47962026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b1976094bc20ec3c7c594f5c51e41dc5f6ab65a4d743477e95449804906853`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.2.0/traefik_v3.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 15:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 15:43:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b198b4fc88f9f784e0d33686fd52862fdf1fe7e03ec4b3262dead44b2cff91a`  
		Last Modified: Sat, 07 Sep 2024 12:44:50 GMT  
		Size: 456.0 KB (456007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff6b599a618829a24a9b3d72151035d53b60a54ddbeb8fb54b89ab40a9c91c8`  
		Last Modified: Mon, 28 Oct 2024 17:56:40 GMT  
		Size: 44.1 MB (44139145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fae90c5d8ead14254c546cd90c02fa32fca2787f9cc94d69f7c4ba410332af`  
		Last Modified: Mon, 28 Oct 2024 17:56:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:munster` - unknown; unknown

```console
$ docker pull traefik@sha256:f098b7fd55fb0997e95aeff16d770a2694659b1c52d597e5f702a68269366d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 KB (12508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d875b2dc35ad44e90dedeffe007e689d103d60b943aa05690dda17be8751f628`

```dockerfile
```

-	Layers:
	-	`sha256:12dd9ad7e8720a1379bc2c0950dd04efc558029f1f61877b4994e4a286cd466f`  
		Last Modified: Mon, 28 Oct 2024 17:56:38 GMT  
		Size: 12.5 KB (12508 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:munster` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:14b9b4c31dbb3fd7b024c4b40d27434477e7806437485a56a8430eb3eb24920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48231630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b4da4a8c2e6edeb5606a37d6ce379658d13980b595549807d5b66a4534f801`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.2.0/traefik_v3.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 15:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 15:43:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd28039cf42b0f64f7e54f78d9ab70163308c6065494ce3c3b94933d8056566`  
		Last Modified: Mon, 28 Oct 2024 17:57:01 GMT  
		Size: 457.5 KB (457469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9466927b4933dbd0637f26201ca2cae64efad8d34143bb203da69997db75a57`  
		Last Modified: Mon, 28 Oct 2024 17:57:02 GMT  
		Size: 43.7 MB (43686146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7182767b82c51e1d6fe1444fbd5397f068a46cb5edeb52885afa1b9eaffacd`  
		Last Modified: Mon, 28 Oct 2024 17:57:01 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:munster` - unknown; unknown

```console
$ docker pull traefik@sha256:d91afb93c72f447f443917db040d38e9f7f53c7c904503f869c5dd86811fae83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.0 KB (822003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7480c1c94118432470d9715f4803af6e4376c41ee21a6f23b70124df1a6bb4`

```dockerfile
```

-	Layers:
	-	`sha256:0d78241ef8fa2ce70b35c87c34354b9aa465c64cd32168b57583397514e1eeb8`  
		Last Modified: Mon, 28 Oct 2024 17:57:01 GMT  
		Size: 809.2 KB (809234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6409a860ba33fe3e707899a78a18b62443923b32ae1dee4a201b551e2b8e6fc5`  
		Last Modified: Mon, 28 Oct 2024 17:57:01 GMT  
		Size: 12.8 KB (12769 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:munster` - linux; ppc64le

```console
$ docker pull traefik@sha256:cb2ed12c813b3526934248ebb25c7f4059d19e63e314fe287a92a031f147147b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46234008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff207f3a26750a8b2684aa446236fbcd0be66aae38f684e1a7a348ebb13c897f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.2.0/traefik_v3.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 15:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 15:43:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7344dfd024f1a54ee674177a4c7c77f21bca6f5d0d59c0709c1ec0da6571fe8b`  
		Last Modified: Mon, 28 Oct 2024 17:57:13 GMT  
		Size: 457.9 KB (457876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d885b3b1b6a6a2d3c4590119cc3625aa351ce404bbccebb86747ea31c873255`  
		Last Modified: Mon, 28 Oct 2024 17:57:14 GMT  
		Size: 42.2 MB (42203344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699580e753ee1867d046aea93168be805cc2f076cf1242b17e219dc5544f96f0`  
		Last Modified: Mon, 28 Oct 2024 17:57:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:munster` - unknown; unknown

```console
$ docker pull traefik@sha256:7468a7cd6f2bf54508012ad5b2bb76f805fa81bef72a36b2fd7ec7f87a097947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **819.9 KB (819906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ad6a32947f82f298f7ede273ba8c739d0a44c871fdec04caa808fb11a46a2b`

```dockerfile
```

-	Layers:
	-	`sha256:8f3c880c0c0cb7f876ea2f9b8ab88effb8afa107d97154f4f8a8f4346c5913de`  
		Last Modified: Mon, 28 Oct 2024 17:57:13 GMT  
		Size: 807.2 KB (807234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c03f9b739fb3508cfb479c21e58a21b4290cd4f3a3773fe119474f4a91d53033`  
		Last Modified: Mon, 28 Oct 2024 17:57:13 GMT  
		Size: 12.7 KB (12672 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:munster` - linux; riscv64

```console
$ docker pull traefik@sha256:2f13fb9fd42bf39fc8d67b0a26207235edb779645806624486c0a6b063ca478c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49180381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf59a0f1cc8f4135484dad9f5c50beec11ae3f5b9be29b7e547241e763351b14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.2.0/traefik_v3.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 15:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 15:43:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9782d9bb651b7b80a5b6dc6b8aa5e197330e400020c92b9e4ba59c8dccfb52`  
		Last Modified: Sun, 08 Sep 2024 17:42:04 GMT  
		Size: 455.9 KB (455888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8de0ed139b33a6ce497dbefed42a60cb26ac3287864159bb61247654edbd05`  
		Last Modified: Mon, 28 Oct 2024 18:02:30 GMT  
		Size: 45.4 MB (45352672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be6cfa1dc27b2215de6eaa9c7659878ddcdf3931d8a39c0337b15040841ed5b`  
		Last Modified: Mon, 28 Oct 2024 18:02:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:munster` - unknown; unknown

```console
$ docker pull traefik@sha256:11c0430f42007c6e2672c0546311976dfd2a6d069db2c1dda1c9acfeb46c8028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **819.9 KB (819902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0a4005afe177e460360142915fed0975120f16c251184ae1beb543d919ba76`

```dockerfile
```

-	Layers:
	-	`sha256:15046be9991319d592f541332dad5a493c17b41acddfd1c56f13b7d604db92e6`  
		Last Modified: Mon, 28 Oct 2024 18:02:23 GMT  
		Size: 807.2 KB (807230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b2b925e3e8a3fb69bb7e14983e2e9210a55f470f6f8fbb3ae462fdb35c1898b`  
		Last Modified: Mon, 28 Oct 2024 18:02:23 GMT  
		Size: 12.7 KB (12672 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:munster` - linux; s390x

```console
$ docker pull traefik@sha256:14c20bc27af2a1a77c9571cad8e1319dba891b70d7cc3d4a1a7558b7ebd1ff52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49525742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afde721e852394ad1990fdce90092134f893b14c4c40785eea7bd790d17a2fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.2.0/traefik_v3.2.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
COPY entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 15:43:40 GMT
EXPOSE map[80/tcp:{}]
# Mon, 28 Oct 2024 15:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 15:43:40 GMT
CMD ["traefik"]
# Mon, 28 Oct 2024 15:43:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559f652fd9a9f8a3a6d224500921f75ec5d4a02e5b286f03b3e0117bcd1ad7ac`  
		Last Modified: Mon, 28 Oct 2024 17:58:27 GMT  
		Size: 456.1 KB (456130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918ed97b7349a62627752c47fd85ec52d75df37ae11ec6763b94d35abdb372dc`  
		Last Modified: Mon, 28 Oct 2024 17:58:28 GMT  
		Size: 45.6 MB (45607645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380356ab4db7c2366c062059207da56a062d1882dd0b96e6cd314ebd12fe6cf3`  
		Last Modified: Mon, 28 Oct 2024 17:58:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:munster` - unknown; unknown

```console
$ docker pull traefik@sha256:8f97d94846538f795117e6147b1f927cd46b497ce1db6707819827171f94b402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **819.8 KB (819784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9680a2ac3ffea0e7cba3d36a564b4ba938df136b55eb6ea1f7541689ae6cc3e5`

```dockerfile
```

-	Layers:
	-	`sha256:695e5cbf432136143079101f233561377c52c011d83403e435a72dd59e2411c9`  
		Last Modified: Mon, 28 Oct 2024 17:58:27 GMT  
		Size: 807.2 KB (807176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bbb7398610da5afc7c89ac99d7f8ddad7879d68a3e4a94482a1674c8f79b4bb`  
		Last Modified: Mon, 28 Oct 2024 17:58:27 GMT  
		Size: 12.6 KB (12608 bytes)  
		MIME: application/vnd.in-toto+json
