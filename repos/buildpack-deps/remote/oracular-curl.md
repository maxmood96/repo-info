## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:61a28c17055a6077fa9d3cbf04c022fa1a5d4a09e9d868153446ac706188c67d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:oracular-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cc493c516a4c43b47c3d45657a63dd70a07aec5f2c4682e2371d6bc0a52c9e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46076562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4e94b84b938bc6d05409eacb1a43ca1a998295e68ed25f7005e6a327dcf6c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:8e4ff40a1983cd8e3a737555205d0155f8245cf78c17eba45447c5ff8bf42a62 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ad109e5dce93c39830a72466a5071a150963a59aaf6898904da6372c54117c25`  
		Last Modified: Tue, 03 Jun 2025 13:30:51 GMT  
		Size: 30.7 MB (30677976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2b8cee836776204d1ab24be8c1d658151b007d82d4fe58787962f5d3eac961`  
		Last Modified: Tue, 03 Jun 2025 14:20:31 GMT  
		Size: 15.4 MB (15398586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:953dd9dd366e5e7119e29b92ddb53a2dcc6f684e9d42b67fd70bb944c6a72aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2489184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98057b323cad95dd090e8a303389fdc75324f6dc82e8ef77c61f6f5715ee5a6`

```dockerfile
```

-	Layers:
	-	`sha256:61041e0d87c784aa96d21dd0eb44a0111f2192452bbfad8c9adae4c4533dcbbd`  
		Last Modified: Tue, 03 Jun 2025 04:15:38 GMT  
		Size: 2.5 MB (2482206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c947b6f2e1e937fd5a55b013c93b2e239a162a3bd21990c5a21ca5ff7d2817c1`  
		Last Modified: Tue, 03 Jun 2025 04:15:38 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:56e7d90ab9b0ae0d3dc83a8ab3f23ed3d84344e988a3869551000276a7f9d5b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41636975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fb7e76b8c31a50ac7b21e6458f84849e962e8c20ad768f6ea26b286f02d34f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:4bd97a769ac0690d3e7b50b15f6e685a8b191f6fb2a06a7ef3ac828715a8068a in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7a3f105306feae40c7cb270b7035492092da412b5fc113c7216ed37da473f3d9`  
		Last Modified: Fri, 23 May 2025 21:42:34 GMT  
		Size: 27.6 MB (27572634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da83b7fa93057f388593602c3bda3fb3e5ccfee1a1b433dc035980fae16e2d61`  
		Last Modified: Tue, 03 Jun 2025 04:17:37 GMT  
		Size: 14.1 MB (14064341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3b4e98000e6e7450898bdc42ea534497f052e05616517e0a827937b87a0c5d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2491545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104ec6b3bcd89669bb3fb0ece50c8f684b5a0dc36d0553ff299863c893c687c4`

```dockerfile
```

-	Layers:
	-	`sha256:44a2ae73adfc075897506bfd0b5dfe32999177e1adab3ffc12e2d314e3a55f56`  
		Last Modified: Tue, 03 Jun 2025 04:17:36 GMT  
		Size: 2.5 MB (2484507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8885d0085fe899da4497fda08c44c0bd1cb1195062b2668fe295fc6f916d4b`  
		Last Modified: Tue, 03 Jun 2025 04:17:36 GMT  
		Size: 7.0 KB (7038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3d336df402cc2d3d4b931f8fe4849c5aef8e042bf06651007c1f86c0ac3b611a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45518657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6b5900ed7689f194b6f2b5e2a355edf66d1bd435aab0ce6e0d2923dd5cff88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:a40da24a8e51e4c2464a3df010bde0f506614895bb3727a3e66f9bc02badb637 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8da1f8455284f5e2b02f2affb00d86bf56295abbbd1317ed54c64b9d08c6af55`  
		Last Modified: Tue, 03 Jun 2025 13:31:44 GMT  
		Size: 30.3 MB (30349442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91d92fe32ae20074e9999cda436f7df9811a96714d68dbf3e6188d634edf899`  
		Last Modified: Tue, 03 Jun 2025 04:19:07 GMT  
		Size: 15.2 MB (15169215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8723a09c9a70f2d750e5059bfc63bea95f418a9fb96ffce316e8d1404d2d5362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2490321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8f3156cc36999e377c57d4285494b46c31c9f828dd41ed4fb8246e72f285dc`

```dockerfile
```

-	Layers:
	-	`sha256:ae8ca1571acb535fcf9d5f8eaba36b579ef1d8926257eb6252004338d2856c19`  
		Last Modified: Tue, 03 Jun 2025 04:19:06 GMT  
		Size: 2.5 MB (2483263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6cffd9130e6425efc2814e70a05a1f2073dc53b18a79d162eacbd3a5da5737`  
		Last Modified: Tue, 03 Jun 2025 04:19:06 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e63501c59455da12ab22593d933ef8de6d8863c26a08fa540a879d05595fb60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52407542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c536a1b94158fbb1a97aa1bdb9dfe69d79afa45b8fd1a9e938f956ba5a47255`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:65b6f40e2debbcb8d2e9827457e657cb13bc4d979cc1b686146256ca3f879353 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:94b0fb7698cd39e8c6701b7a2749fdd4bc96ead7357a49f71c747fa9ac72a479`  
		Last Modified: Fri, 23 May 2025 21:42:40 GMT  
		Size: 35.1 MB (35134874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924de3f3a37fa7311811de099636508e16ff7f811d88f728c82a0824d811df43`  
		Last Modified: Tue, 03 Jun 2025 04:18:28 GMT  
		Size: 17.3 MB (17272668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9752284a1ae69ad9bcc7ae3d9154cf6faf3d854f7b62c5b1772c073d2210058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2493833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff680a9737bc7209b102f6ea40899c16d186a2d1ff1c66293be58c9591be286`

```dockerfile
```

-	Layers:
	-	`sha256:52a1ee979b176e1e6c0c8a3e6c63c8dfb293152ebfd8eaf4e87ea06d644c76d3`  
		Last Modified: Tue, 03 Jun 2025 04:18:27 GMT  
		Size: 2.5 MB (2486824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3662cfd56c4a8d47716e2e54e651653776984d6b4910596685b466147a4bc4f7`  
		Last Modified: Tue, 03 Jun 2025 04:18:27 GMT  
		Size: 7.0 KB (7009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a7ce20a4f51f3cedc7b7d0a4c3103b8e470db504020757da58b813c3998f9496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47709633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ffa2fd171d7d1843f4fc8556d26e99e1cfac919f027dcfa7e70cb1f9ac1fac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:09bf7d8280c93d6db7f1d520c36d422a42b991003113c76d03045fbe9e0fa62e in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:99f369994d53c480a8d425453c885d8c689ba87e422c730e1542f0a357f64b86`  
		Last Modified: Fri, 23 May 2025 21:42:47 GMT  
		Size: 31.8 MB (31816016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431eac0742c4354ab04e06371d14503d59d5a945c816f9ea93c920414c58bca2`  
		Last Modified: Tue, 03 Jun 2025 04:24:11 GMT  
		Size: 15.9 MB (15893617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:57cd880d779524edbc0ba6cfd721276574c94ee577b8a6d35ab1a917b48ab244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47500b751a04c252328001403a80feaca09130f73fada2b73c4200981d5cb9e6`

```dockerfile
```

-	Layers:
	-	`sha256:d6f1f91efb71c5ae4867ebf315fa71066803fb5de2eafb0ab39643a301608b3b`  
		Last Modified: Tue, 03 Jun 2025 04:24:09 GMT  
		Size: 2.5 MB (2476110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cff1665def1e6978f6f81071fa5e8f504e3fb6d3979baf26f104fc9d2ee8ee`  
		Last Modified: Tue, 03 Jun 2025 04:24:08 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:828dd23482f648da3d6939d1da4f5258d2269daecad5cabcc68616ba712a9e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47800917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1df94fdc48ca2ce60888938f3bccdec45bb644877235219310bcdfd6f3e7a61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:eb903d7651ff3dbf09f650f4f09293336b52876503a80b8a4055a1ee62e3681c in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:eb0749c1557961032471b04d5d1ae0eb7c6319cc8c49244b9e349a1baf046b25`  
		Last Modified: Fri, 23 May 2025 21:42:53 GMT  
		Size: 30.8 MB (30838341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4ac8e25728fec411be64a8d6a2f3e5312d6aa9e0894a84e88bcab877eba1ae`  
		Last Modified: Tue, 03 Jun 2025 04:17:23 GMT  
		Size: 17.0 MB (16962576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:974a3c4b81b628b916ec38a8d7157e0c29f1f42df14dbdb7d5a90afcd6e4708f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2492010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1857df3ef7d50d116561c309331129b27438447d2a3ce31ba0306f1773d146`

```dockerfile
```

-	Layers:
	-	`sha256:800b4693a9973fcb886cc9a98eb32435239723caa307d4f815a70afa8beaf33f`  
		Last Modified: Tue, 03 Jun 2025 04:17:23 GMT  
		Size: 2.5 MB (2485032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a00e593d9d74ad7e04b3e5ee0ce66c6f54edb65f42069ecfeb3f18f50013a97`  
		Last Modified: Tue, 03 Jun 2025 04:17:23 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json
