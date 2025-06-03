## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:2a469f123d11ba9928ec75bedb84de76b3e4148852f6a4eb4ea2dfb53f2b1b43
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

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1e65c02da86dd71b19330c7cad1dbee61d88732046c3de6af18066d836edc699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88644911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee81748264422aea9cf8250936bcbc45529693b74e0e2b4005bd7f33a4e4d4e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1521653fda6cd0a5792ccce948424ec895da66a78dd341dd761cf5d863079a6c`  
		Last Modified: Tue, 03 Jun 2025 04:15:43 GMT  
		Size: 13.6 MB (13621261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcab7b82fcbccfbf0a9487149491a20ab8e4066e46b6e6b12ac9f4ec1a5e632`  
		Last Modified: Tue, 03 Jun 2025 05:11:42 GMT  
		Size: 45.3 MB (45308313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:361deb72e0c29cf80fd1a51921c30f64468acdbfe6b0898804e9ee5fae5cc3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5110692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0648f08a40670ff231262bb54e2bed984a165eeda169e8eb6daed3ed3f9020bd`

```dockerfile
```

-	Layers:
	-	`sha256:b33915dfefaa42d25aeca7c603f56cd7bd96f47837b488a66e52a85b58c17f53`  
		Last Modified: Tue, 03 Jun 2025 05:11:42 GMT  
		Size: 5.1 MB (5103387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3384d60d6fc45385e973aa6a6a04684a7e185064425dbe291ce8cdfd4e2384e`  
		Last Modified: Tue, 03 Jun 2025 05:11:42 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5e8be34e4353eb77ca8b3805fc67d0e14b008fbb343e915f2d207336e61e9c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88489763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac105e7ce0d2155519c9b82b49680f54a7d177778005cafb1edb203e8609c83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:f5b71e3353c1f92a265c88e163d98b6fc00235db4d001763328933c4838f3576 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76393e3f1626a318c4984c6e6d91f17fe6888451b277b6cc175eab3a1032ebf5`  
		Last Modified: Thu, 29 May 2025 06:11:44 GMT  
		Size: 26.8 MB (26842221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca74547492ebc6726e0a1ef9887a16bf144497b7eff9f2f4d1b9b96fd524d65`  
		Last Modified: Tue, 03 Jun 2025 04:16:36 GMT  
		Size: 12.8 MB (12780568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc7ee5bd9c76349491b1d6eb575462fcbf5da5b8524ca927456bb287c669459`  
		Last Modified: Tue, 03 Jun 2025 05:12:27 GMT  
		Size: 48.9 MB (48866974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7be8e721d10bf8b0585e6df1fe4f099f46fa139f57b5c8aeba49d6caa9e0a253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5112050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e232b7b6394b13b59713b25d64115734296dd69bec677e29fd2e73ec4e24145c`

```dockerfile
```

-	Layers:
	-	`sha256:e533e0ce242d76fc76bf07781810e376046af7b2aa3e793674609923645b11c7`  
		Last Modified: Tue, 03 Jun 2025 05:12:25 GMT  
		Size: 5.1 MB (5104685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0816cb634f7e6de7fe1db822526db32bb974b099ac9dadc3312180df34fef8e0`  
		Last Modified: Tue, 03 Jun 2025 05:12:25 GMT  
		Size: 7.4 KB (7365 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:77d3fbf4e3a521f487c69c9676d3387cbbe4606cbc93c703be90da5076419e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87645995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4857ba93d5c05c55a531441c8a6ed9a600db950cfacabd902748da6a08d9cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Thu, 29 May 2025 06:11:37 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b69317717db81c94bb0365bd720346e2a43a6b03173cf89d340cc19a993286`  
		Last Modified: Tue, 03 Jun 2025 04:17:41 GMT  
		Size: 13.5 MB (13456235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759b17809d1c47c854abc09c29619c5c3e1ecc066ba58350e83935a74d8b2f18`  
		Last Modified: Tue, 03 Jun 2025 06:47:26 GMT  
		Size: 45.3 MB (45337861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b5af6e22b74fa6ea43ff14f19735d20c81bc79d491a9a109b0c3e1b745bfff19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf7f155040c85e199f80e9c411905ccee1424176f81d66daafb725f8a545b2c`

```dockerfile
```

-	Layers:
	-	`sha256:bb37df611bf58680c9a38eb1ec561ae5970a96431eac9961694300d7aa36b664`  
		Last Modified: Tue, 03 Jun 2025 06:47:24 GMT  
		Size: 5.1 MB (5110579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9234dcfbd98c400486138261669159dd0f3be6f11a03375e0e4b11ee4627e433`  
		Last Modified: Tue, 03 Jun 2025 06:47:24 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b5fa8d619918bf3ac3f9973542366deb5221e711fd05f596c6ef2294a2ebd272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100716768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09835146196aa90844d0c6899853bfb1eb4d8e1e24f438d15aeae319fc49795d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Thu, 29 May 2025 06:11:52 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b8bfbc006efc56c6755ed0088bc7e2319e113b78600a3ddbd68b5426fba260`  
		Last Modified: Tue, 03 Jun 2025 04:17:18 GMT  
		Size: 16.0 MB (15954183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8164017b162a84441c445117a482b3279cfe5281941001cae73acc870be8f689`  
		Last Modified: Tue, 03 Jun 2025 06:31:02 GMT  
		Size: 50.4 MB (50437375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:41525d4fefe3e02e363b03585f99e646d2278f09cd9baceff59d23bc5cb7a5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5118577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574133ff5befcaa7f7947e86b2d821344666f3382a7700d01fab96e895849164`

```dockerfile
```

-	Layers:
	-	`sha256:0d31ad64553463849b48c450091f079ad4f65628ba920b5cb266ff62f24a354a`  
		Last Modified: Tue, 03 Jun 2025 06:31:01 GMT  
		Size: 5.1 MB (5111241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30df1e9cd4259302503594aa0cea8edb7db6bc045dd0f1583413605179baac1d`  
		Last Modified: Tue, 03 Jun 2025 06:31:00 GMT  
		Size: 7.3 KB (7336 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:753afac3af101cbf88be74d33f95881c5f6a276b2fe840922330e49431e2fd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99137683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d17461fcd925d921efe1bc172d0572bc49f40cc437896fca32a531990f28b3a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:f68263cf915d0f5d61ab9caa83da511fc9ef55d936429cb8fb542906fc38a8fa in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ac2db62b9f8401057b5c4ebae4764d70573ec599f6a1f0b5dc2c4491ed8e39a`  
		Last Modified: Thu, 29 May 2025 06:11:59 GMT  
		Size: 30.9 MB (30947484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f34a9ec93701ff69dabbd7cfb519ee4f1c3aea72d284f88712f56d2d510da2`  
		Last Modified: Tue, 03 Jun 2025 04:20:54 GMT  
		Size: 14.3 MB (14327998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0dc15b68fdc69e46f38c05f839bcd5a0103364875b543486932c8110c33ae5`  
		Last Modified: Tue, 03 Jun 2025 06:50:42 GMT  
		Size: 53.9 MB (53862201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a269a7d9f10d904fd363855e00d480d819ceff5287e9fbe83f4d6ace78b27529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5101120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69943a2062ea1222bcfece946b0bd44ad354f8c3c3ee0e402ea0b7d16678420a`

```dockerfile
```

-	Layers:
	-	`sha256:22ab6d2172f2de2f261afd91b2c30fbc76cfd371dc189a936cf0ac249b5c04ec`  
		Last Modified: Tue, 03 Jun 2025 06:50:35 GMT  
		Size: 5.1 MB (5093783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99e720cd395d087aa6ac02fa60201d40125f395ef1b6a209b9961cc5053b83d4`  
		Last Modified: Tue, 03 Jun 2025 06:50:34 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d9efe00e88e684b3b9173cb19b8c34cffaafdac416ddec468b551b650dbe2eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91606704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d45e995f5044d53dc973b24317174229d28b3f41fd974f7579610115ff6b35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:b6b8557b3fef6c06eb943ce735f649cf7033ab3925e70e6b43901f1f29b4d5e9 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fa55ab2f467363da0197dee4a8e5af9e7ba7ef5686c6f0951bc509c387b765c`  
		Last Modified: Thu, 29 May 2025 06:12:06 GMT  
		Size: 29.9 MB (29930056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de52c2fdeab987f45f86ba773c7a796e45606740580a41f52ad841cf7937f80`  
		Last Modified: Tue, 03 Jun 2025 04:16:39 GMT  
		Size: 14.9 MB (14937985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a419ab9a4b62e5fe13ab2f0ca43ddbbcccbe7da113416be348882575840fa555`  
		Last Modified: Tue, 03 Jun 2025 05:16:47 GMT  
		Size: 46.7 MB (46738663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d5ebef85b9e63a60449009fee355578270a0c4c515cad9789a5c2d7beba5d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5113024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf40d87f522d0402ee5b2d8972a3461c1ed7d5324e1ec306e8b83629cf8a47b`

```dockerfile
```

-	Layers:
	-	`sha256:5fd84244dc558e82d665a136679df08b730a7ef0f757543b5edd5cb33628ce27`  
		Last Modified: Tue, 03 Jun 2025 05:16:47 GMT  
		Size: 5.1 MB (5105719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b8fd4771e27bd62faab43c547c3ef7a79829df4e3d1ec7202586198177a1f91`  
		Last Modified: Tue, 03 Jun 2025 05:16:46 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json
