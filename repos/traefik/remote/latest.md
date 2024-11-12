## `traefik:latest`

```console
$ docker pull traefik@sha256:78bd806c592d9b6c8c6c4ccc0be8ed5bf3eeffec5fc1610329b2c916219023f2
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
$ docker pull traefik@sha256:3a2a0d7933eedf9410023fa29d65852da2e34a1793dbe98c5fa674ab4756b1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51213479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f86889e433cf0d495ea9b888d257be86dc556fef887a82d88fb815b7880670`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ccd6d164c45a7b4e1b02afcc491b3b373dc5b9924e2a6f76c30d51243d0668`  
		Last Modified: Tue, 12 Nov 2024 02:11:14 GMT  
		Size: 455.1 KB (455127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e383386c44ff5c6b7e4cb20d96b3442615b098b6ada0f3ede5929f40796ed8`  
		Last Modified: Tue, 12 Nov 2024 02:11:15 GMT  
		Size: 47.1 MB (47134078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d51f1087c5a71c69520f66994702cebf7e4b5baee9c0f53c098ead33e8ee70f`  
		Last Modified: Tue, 12 Nov 2024 02:11:14 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:b2e3fd53aaa808c98eac8a5c92f1b24b6faddc8a7cf72bf5840c72024b0ad4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **821.9 KB (821937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92758bf9ff0e21d7fd6775c67dfa88dd81d62c452bd836109381b257ed24cfe`

```dockerfile
```

-	Layers:
	-	`sha256:2701b1057768536985073ef0a71c32f014df0b3b68a95c19efb5f22f9a464e84`  
		Last Modified: Tue, 12 Nov 2024 02:11:14 GMT  
		Size: 809.1 KB (809130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c4b0277297a5d5daac87526bfe7e570e11bc9f9cb40b78cb1590e7da7a34121`  
		Last Modified: Tue, 12 Nov 2024 02:11:14 GMT  
		Size: 12.8 KB (12807 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:945c03e4bc270f91934b16cc62c652731dfa0206137c948c0a20c7125ea364b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47962126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0eed5a7cbae2336e4dcfd29358f27d31f2489b381251750f94f1dc8e85647f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc2658b70735f2744c27b0ba22eb61aaa318147f9377f902c5caafcfa0e0b4`  
		Last Modified: Tue, 12 Nov 2024 06:29:42 GMT  
		Size: 456.0 KB (456028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393841022bbd03e4b14b42075892550e0147ca237c9f1814173a22c1ac3c6d7d`  
		Last Modified: Tue, 12 Nov 2024 06:29:43 GMT  
		Size: 44.1 MB (44139132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ffb1404cb5574517a0f0545f92ecc927988f22815df2ee849baf115cbbe002`  
		Last Modified: Tue, 12 Nov 2024 06:29:41 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:aae01e346e42087482a04251e3dff5df4fd767233a7a83a9b5522ae36b25d254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e8ccd74071612b2e202108d563f1dcb991d1db5714323efa94ebedf51d3e8f`

```dockerfile
```

-	Layers:
	-	`sha256:46edfb8623f9fc108cc4f44c6d66ce562baa8298d8a3d80cae37c5b504543607`  
		Last Modified: Tue, 12 Nov 2024 06:29:41 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

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

### `traefik:latest` - unknown; unknown

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

### `traefik:latest` - linux; ppc64le

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

### `traefik:latest` - unknown; unknown

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

### `traefik:latest` - linux; riscv64

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

### `traefik:latest` - unknown; unknown

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

### `traefik:latest` - linux; s390x

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

### `traefik:latest` - unknown; unknown

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
