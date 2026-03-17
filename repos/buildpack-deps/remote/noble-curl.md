## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:64cf41cac739293f48474c5d6aa38698d5c8384d11636673f66f46bb7a7645d7
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

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2a389f7e2d36c754e1a7571ed7d7b1acde1e72507ac31d55927f2e7400cda8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43355351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af51450100d81df9f040ee116c84463ebe3400a0093568293beb4c0a53375744`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c8a6fb9740c3884e8704c3750f8ea0885ea49dcd0559b6345527766060a8d5`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 13.6 MB (13627740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:369b00003f45e15d21a89115c2e4b1bcc6b736d97e48e889bb9ffde266e15e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e79cbd1a22daff663342c84bc33f8731b59d43c9d448bbc4af3d7367133891`

```dockerfile
```

-	Layers:
	-	`sha256:6d2b7994950c7f27f94e12a1a34b926dc0ad7dacf964ad664c10c923b5952098`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 2.6 MB (2607821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:115a58ba2263c766163a8e2c8f4d2a225d04749a2cb9ca05282039ae38eadd1d`  
		Last Modified: Tue, 17 Feb 2026 20:12:02 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:26cb2f6bf48bf0f3599208293f08a886d852eac05d8b118dc4a7e0d50c2468cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39640888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3ae25791e509b4957cd42a67f31e4f66d6e4c39bc3d5c55d164e3c504143cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:51:23 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:51:27 GMT
ADD file:9633092e110ed5475e9e31841bcc6e288ca09c116e102d75694089f384f549b3 in / 
# Tue, 10 Feb 2026 16:51:28 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:dd135084b7c993802b7c1ba97d192c201727ddf710812c361d5441cb729f5c20`  
		Last Modified: Tue, 10 Feb 2026 17:41:49 GMT  
		Size: 26.9 MB (26855457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86066a2c0cee319af3a1fc2959296da0853a5a25ac26fbf28428bea5a43b759`  
		Last Modified: Tue, 17 Feb 2026 20:11:26 GMT  
		Size: 12.8 MB (12785431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:560165ed177b0c4fcbe1735580abbaaf6300bdfb7a56b17ce01bdc72e3df28d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8e3df05c3f43954d0d747ce75b3d849fdbc6f08639c62b54ba211cecd3b1ae`

```dockerfile
```

-	Layers:
	-	`sha256:435b537dfc8dc66b06b8c03cd8e9fc4cbbb424c1e5775ce6a330770205b85740`  
		Last Modified: Tue, 17 Feb 2026 20:11:26 GMT  
		Size: 2.6 MB (2610125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca0f3bc6dc7419d34e3652d9f68fc2fcf6463b1a51301aa7ef453133ae0de1a`  
		Last Modified: Tue, 17 Feb 2026 20:11:25 GMT  
		Size: 7.0 KB (6979 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ccac5e49f927460f31a22eedf74475fb0a14281861eefdde396ae9acaa3ee5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42335650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5383663b9896534754ba5e67010eeb00629530a95deeab5ad3dfd99e743ad6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c14c4233e7d75a38c201e9c5e7f07020dd6f8701769cbea2931551396595d3`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 13.5 MB (13465941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c885a73319206cf00836009800fd79f652acd55a092ceee057c4badca1fe0861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb904dceb90c44d301989d5c4b3c854b683c42874855a31c43b539ef20b3af2`

```dockerfile
```

-	Layers:
	-	`sha256:ca4232983cec16c35be21f5486d54d0be72d36dd081a016da8292816a7e61c59`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 2.6 MB (2608895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8365c904be26aa2f5f1c6bd55c1218b03d3d66e82aafb0f6bfee8ffb68d47d74`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 7.0 KB (6995 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8112bdb10e7346a0f7c313055d371f32292fba181191527e830f3b47bd8da3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50263194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b75d6669798c6ad1bee4559afd052b0149758e9733985c801d718dd32d320c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca93a66bdf3fa40b5c5ab2fa85f68e7a3ea39b2c49a65eefe83983c813fe050`  
		Last Modified: Tue, 17 Feb 2026 20:11:14 GMT  
		Size: 16.0 MB (15956288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bbcd0d9c3119858d3bcee05ee521226d6bc4c60907d6936f8143d4cd331b4b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de4cb9be6d8c59a9e570bbe71750120190cc23c0464ebb29f4fa0fd3b960673`

```dockerfile
```

-	Layers:
	-	`sha256:c9b0dbabf4c0b0355dd135229aa7be9bd60838c45567c0c4cc59199dd767dd27`  
		Last Modified: Tue, 17 Feb 2026 20:11:14 GMT  
		Size: 2.6 MB (2612440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f481d3dac4c8937f5d467330a5bbbe5f3e9338af17142caba02ac4390ab2bf52`  
		Last Modified: Tue, 17 Feb 2026 20:11:13 GMT  
		Size: 6.9 KB (6948 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:e85f3d197cd01e7d9d5028a79343bc330292607ca5cd6bb5a3ad60e71bf3c809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45287217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb3f5c5e4ef368b9f85a5fd993038ec0fda662baa1c5f6d1fd191d96c93a284`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:33:09 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:33:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 17:33:55 GMT
ADD file:b4821892707dbb5cc8e8eb3b4e757edc2d124db81fcdedfc3b244dcb5c1fa6c0 in / 
# Tue, 10 Feb 2026 17:34:00 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 23:51:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f2683d5e2cbe038b4f1178e139d507e705e0a3a566f8b9c89bf3484f426119af`  
		Last Modified: Tue, 10 Feb 2026 17:42:05 GMT  
		Size: 31.0 MB (30954431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37a7e09736ece201cac91607fd45b546145661c1936ccaf437107414a69ca71`  
		Last Modified: Tue, 17 Feb 2026 23:53:08 GMT  
		Size: 14.3 MB (14332786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d425d7a71695fa0d5432dd314f11f078e0f6d8049f03b93eb872e6453601e2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5534da502bc217021704b8c8f4acc1a3e207c9c9570d98b24b44356894c58be2`

```dockerfile
```

-	Layers:
	-	`sha256:d76faafcb848ad84b14f807f14334d48cee7ca69dfedab836c37e4a7fd4bb6d0`  
		Last Modified: Tue, 17 Feb 2026 23:53:07 GMT  
		Size: 2.6 MB (2601720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e829fa5e912dca0197bcc1032888f2ce36b6975b8a6929e6f5ad4546b7c97c38`  
		Last Modified: Tue, 17 Feb 2026 23:53:06 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0f66d5d8a75593388e6ece02d3646c6fa4013bbfba289dcbe394f8364e470e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44851172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f4664dbcc429b80c24cde001ea273812586ab334f410ea8855abb3d60faa53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:10:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791303199d68c9f312a5d0bfd906c93cc0e8d90e0628258a53b896296dbca649`  
		Last Modified: Tue, 17 Feb 2026 20:10:50 GMT  
		Size: 14.9 MB (14941388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3e19e77fd86fb3d47d0c5308177d5c2a7d2ae189532a370ed7b0950e240a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f049f15ff46ee4b67d6e5813f1135173300d6002a396146e9dc2bd439c3e72`

```dockerfile
```

-	Layers:
	-	`sha256:c0a57abcf5d7d416a9a6d868530b5fd4ed0a5840644c113d03258645b41cc85e`  
		Last Modified: Tue, 17 Feb 2026 20:10:50 GMT  
		Size: 2.6 MB (2610646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd842056e20eeb89ae7f9c2c498ef815c106d27aea2f7b260fb6868c2bf21b0`  
		Last Modified: Tue, 17 Feb 2026 20:10:49 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.in-toto+json
