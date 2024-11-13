## `traefik:latest`

```console
$ docker pull traefik@sha256:d12741b971f5c833919db2b680191dc23d5d96ef17e41a914e3c593a8c663ac4
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
$ docker pull traefik@sha256:55ef2c8977354c7d4bdb1bb26ae9c51e4c813d4b8a032cfb6e384ffc75bb29c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48231740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d98b542a38e3cefde5eae6aa1657a7d9a34255bb51f7fdaaf9f9d9e4fd77986`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56489d36cf523e2371211c73771ff2a38fb5d1130180c83a6cef55a4ae8481f1`  
		Last Modified: Tue, 12 Nov 2024 10:44:14 GMT  
		Size: 457.5 KB (457476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11be660bfcf598285a02476bd65aebfe8f7a2035a4721c31d2ab2afb8dcd4492`  
		Last Modified: Tue, 12 Nov 2024 10:44:15 GMT  
		Size: 43.7 MB (43686169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfd2b190e4799adbf4af77ae724559befa5b16a2991297c8bd2bbb5fd78061d`  
		Last Modified: Tue, 12 Nov 2024 10:44:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:85d7c56ce0a7cda895ceee6dd50c013f83065902119d8fae28ede376f0d0cabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.2 KB (822208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a614cca2563e00047a0d60bc1f5994508c7a459c78734a030be6a97c5dd876`

```dockerfile
```

-	Layers:
	-	`sha256:c95fcf93527a8adc5e5d62012df61ba7e37aa0f125f23e7bc5b305dd3e158d9c`  
		Last Modified: Tue, 12 Nov 2024 10:44:14 GMT  
		Size: 809.2 KB (809234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa02ff37943a447ee40aa5ab7812f14cc0f1c16468b6220ba9ee1a3ffc285f66`  
		Last Modified: Tue, 12 Nov 2024 10:44:13 GMT  
		Size: 13.0 KB (12974 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:aeb136d37f8068bfce1c6ecab8f639de479f62e70260366cadfd7b89447c2a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46234058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad462a9dc3d8d3a05bedb955dcc07557135db0688dbbae8b8f574c87f9caf22d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097dba9846b541fffc23cc1517cabbf63c3a79b79a499e411deeb91442e575c1`  
		Last Modified: Tue, 12 Nov 2024 08:09:18 GMT  
		Size: 457.9 KB (457880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2b4f36796a7299ed8adf1cbd333c63fc22e62434fd79b0eaaa216b088d6cd3`  
		Last Modified: Tue, 12 Nov 2024 08:09:19 GMT  
		Size: 42.2 MB (42203350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e01ec422d7dc1535a081d161888808848e864bacdf2535a63a5620e1e52db32`  
		Last Modified: Tue, 12 Nov 2024 08:09:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:857cc75f09b2e40fb814aeafad0b8c1a5caa9f2ffcf5bb032eacfbcf0d0b3f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.1 KB (820111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dc6e7f9c4061d22ce78c6279fa98575d6983cfaec30b3392871c7e83458ecf`

```dockerfile
```

-	Layers:
	-	`sha256:9aed1379aefc29a3e32fd0d1bd8282067c696f8b80da5ac930f4b1517391c503`  
		Last Modified: Tue, 12 Nov 2024 08:09:17 GMT  
		Size: 807.2 KB (807234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cab9d366fab797c9c530acb21580db7786544f53597f378ff3a9823db82c730c`  
		Last Modified: Tue, 12 Nov 2024 08:09:17 GMT  
		Size: 12.9 KB (12877 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:f7ff9456295743c3f3648e4f5ecdcaf5be9951e80a91cbd0acc56077df50aa7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49180440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add2087dbd22aaa5e8a817739b8e3267d4568f28534eec377f71d460d2d7535a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fb36ea9e749ac6a70d059b7c1201bd2e476ffb29baed36a045e3156a3d6916`  
		Last Modified: Wed, 13 Nov 2024 01:30:51 GMT  
		Size: 455.9 KB (455909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a511d5727862ffad8978d07f5e3bc861c1a8f995c2629919abd11c9f4dd9e963`  
		Last Modified: Wed, 13 Nov 2024 01:30:58 GMT  
		Size: 45.4 MB (45352679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39dcfe9890694c9879d3f0a00b274a620d17ede2af3945a240c6f66582031b6`  
		Last Modified: Wed, 13 Nov 2024 01:30:51 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:077b4ab2e8bf708ca127e4404856ee76d7b9f9f5dce9619709e0e53507e7f413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.1 KB (820107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f10910f956fa5684f52dd615cbe2aa6cb2960df0046429e131581673e37664`

```dockerfile
```

-	Layers:
	-	`sha256:d2baeae5dfcc4c69f5369d93b313a03a6ed5e2760b86e6a383b38620820cb2b3`  
		Last Modified: Wed, 13 Nov 2024 01:30:51 GMT  
		Size: 807.2 KB (807230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0af96a2a0f2867ee23fdacfa4248ad95214ce491fa2bf9163ba4750ee23808a`  
		Last Modified: Wed, 13 Nov 2024 01:30:51 GMT  
		Size: 12.9 KB (12877 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:9b81bb13eca178ed2be2725d084aef5cbdaf72aea1f832c5b5990665f8def3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49525753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a3f2c58b2c836d5fecc960cd2e80b20a65d01fa3c81677a5873f96f2aa7755`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cad909027556b526959742adf2017b5f01fcdce31e434af11d319a1b0f5ac7`  
		Last Modified: Tue, 12 Nov 2024 08:44:58 GMT  
		Size: 456.1 KB (456143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df1ba3a2be1af1cb6747e09921648948ecd59d426c6b67e06c9eced890571c4`  
		Last Modified: Tue, 12 Nov 2024 08:44:59 GMT  
		Size: 45.6 MB (45607633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36aaafc16fa16100639c5f1711cb05db5df63f2dccd9aa14f1aa60ec80da88d8`  
		Last Modified: Tue, 12 Nov 2024 08:44:58 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:6ac91230d3cc759061cb80842815a82bd513ba79fddefcf86bf5676282cdea9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.0 KB (819983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acab1dfda612d61186f3c95f35c65932f92065c3da3f6acec66d26b6b0d69e6e`

```dockerfile
```

-	Layers:
	-	`sha256:cd5b5b9fc92dcc59b1f5cc8d4619b84e067684059039270d8743e6f6a1877403`  
		Last Modified: Tue, 12 Nov 2024 08:44:58 GMT  
		Size: 807.2 KB (807176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ec0291c9f5c6b348f86845694792b17af513fc466454c1f6f17fc799b20c08`  
		Last Modified: Tue, 12 Nov 2024 08:44:58 GMT  
		Size: 12.8 KB (12807 bytes)  
		MIME: application/vnd.in-toto+json
