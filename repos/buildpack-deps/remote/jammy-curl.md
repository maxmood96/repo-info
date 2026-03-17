## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:0c0473da24d965bb489837b189f437f90d41cf12b672af42d98ac4a16799ede1
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

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c1a971669bf147a2b667b7daf5866f687f054b036c8a03e5cb299d3227e89e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36643672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fde46bc74f215ecf47caa022bd8b378283c74480edf0468b4bd3617aab740b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd31ed89fd7d59ba427c9f431e17b158ade8eb04083b8b256c587fc6521fb6b`  
		Last Modified: Tue, 17 Mar 2026 01:15:21 GMT  
		Size: 7.1 MB (7105152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00aa9655fe1192c9eb7a665d96d843fa6e7bebe0928ba1e02059336ba77fd66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c843e9cefa22f78a1d0ecff609a233dcc58d1531c1c9e786f71eae74501c6e0`

```dockerfile
```

-	Layers:
	-	`sha256:0528b450df4349a3466962054315d5d29e0831d53959960ac9831ca119280094`  
		Last Modified: Tue, 17 Mar 2026 01:15:21 GMT  
		Size: 3.2 MB (3205215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:421be86ccc2de907b271d9e356ce983e949e67947347d4311d2bd9d5ceeb1db9`  
		Last Modified: Tue, 17 Mar 2026 01:15:21 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0d20052dae43719f11234f604b7d5d4ab2356b27f34b9196887ddc00905ca2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33656494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdb592bbe12c0801f26badecf1f9541e9e77ba45e4d810a0be7ec9abea2f2a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:32:59 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:32:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:32:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:00 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:04 GMT
ADD file:f12ba0d4c2b96568c5eaebe951355983398ad22bb0ad2b3a1a93ae2c24d13555 in / 
# Tue, 24 Feb 2026 07:33:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d411674a4afc7be17053720e1c67deb36aff030c844d1520a78ec3bea5895fbb`  
		Last Modified: Tue, 24 Feb 2026 08:07:57 GMT  
		Size: 26.6 MB (26647217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f10ddf28b37730bf44a2bcc60b1f3b94591cf93dc2d0f8c09aed80a257459f`  
		Last Modified: Tue, 17 Mar 2026 01:15:16 GMT  
		Size: 7.0 MB (7009277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b61c89a9697024fb8f95f748ef44c4673562c0200c12433d9b0edcda0c467b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f526d996cae50c1f41be2f0fd46b2af5b45895c3b4b318a01e1a83899066556`

```dockerfile
```

-	Layers:
	-	`sha256:1059fa44193dc5ff7e6f7c6a07c9546c7506fd55f5433b0bf2da227d7799f42e`  
		Last Modified: Tue, 17 Mar 2026 01:15:16 GMT  
		Size: 3.2 MB (3207522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca1ee61441e2f8e01834c87984314ff5a6339051a5ed15a56a0411421d333fd7`  
		Last Modified: Tue, 17 Mar 2026 01:15:16 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e7d1f198b40e7e98860a40636d6ad00674da4317dbfee7668df19f82336e911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34448234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63695913ccf066407d2924de33377cab52414e6e359d056da6c6850d74c5ec22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485dc332a06408f602b0cdb9b519fb93ef48ddb953b0ca66a482c8afa276f5e`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 7.1 MB (7059209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ceab4d7679b5330149926c149a2d5cee128aeeef8c1dea52ee7bcd2805ed3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c2b748b1cf45c059761b304fc82e30a7236053b70c2a7705204e9cd2648cdc`

```dockerfile
```

-	Layers:
	-	`sha256:46f8a51704d69e9cf6a72d6517bbe486198cb2a48cd8ffdd551abb9018ecd14b`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 3.2 MB (3205482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb25b05ac873b330461d4f287eda7f3bcd67fe33e72df736d78f82232a048585`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 7.0 KB (6961 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:545a716cf86a6b16a355789acafb76c0279fca1774c8423e44aacd371a0cdb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42628260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774be995f7c443e9f0ffac29ef41885fb73b4cd1e2b71ae27d35cd6b54ddbef2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:10:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0c5082d677587c47ec4b9795de90d25c2c4c43ee0d1491e0ca917ec619cedc`  
		Last Modified: Tue, 17 Feb 2026 20:11:11 GMT  
		Size: 8.2 MB (8182158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7b4dab5c3ec0ed38487bfe91680362c184ade4e375cb3f12078ad9ae9b714c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3216764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c37bc2b08ecd07af84ca537929682323538c2e967300693048b4b114a04cd3`

```dockerfile
```

-	Layers:
	-	`sha256:0aac1735269c5d8d68536d080db96cb4cd6f05453a92d88fc624728195ec077c`  
		Last Modified: Tue, 17 Feb 2026 20:11:11 GMT  
		Size: 3.2 MB (3209851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57372ab06b83df6bda5c23e3cebb3a3b0e87bf37f9e72e98c7d7bb921fadf2f7`  
		Last Modified: Tue, 17 Feb 2026 20:11:11 GMT  
		Size: 6.9 KB (6913 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:815ea9365f1d5394dddf70c37e7c83fb65fbc8d7f23716a30e34f7f531afff90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34159896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418248c217a5beead12e5a1aad53ff069b341d8014d3e2806058ce5f0ccf2cbc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:02:19 GMT
ARG RELEASE
# Tue, 10 Feb 2026 18:02:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 18:02:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 18:02:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 18:02:56 GMT
ADD file:3b51fe59d83aa358d9bb8a130e4a91b3db2c3d0b2bd7eb6728a96bba80590086 in / 
# Tue, 10 Feb 2026 18:02:59 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 23:47:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:24e07f5c8d50f99c16f01c34de1e70ac55dabd21b46d6db44abbfae066b41a5c`  
		Last Modified: Tue, 10 Feb 2026 18:14:00 GMT  
		Size: 27.0 MB (27043129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bffa09b66b81c41d371683e62d0742666c56cd1a1cdec99cdb17ad610b27b83`  
		Last Modified: Tue, 17 Feb 2026 23:49:22 GMT  
		Size: 7.1 MB (7116767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc0205c5e2d0a8c2d8f850bb3ee915fe79e8e0f5fafa6e654705628e7f9fc755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f52f08dde67f715180c1147bb38d90894a5d4e827e1b834dee32572e5ccff1`

```dockerfile
```

-	Layers:
	-	`sha256:6df1a260e00b3dd102938990780eb6f3deb455f607491f5e07f5337c81d6b8ca`  
		Last Modified: Tue, 17 Feb 2026 23:49:21 GMT  
		Size: 3.2 MB (3199103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1511e6476b6a2b70bcad4cceca82d15c4090497423ddf86219e5e911fe1c937d`  
		Last Modified: Tue, 17 Feb 2026 23:49:21 GMT  
		Size: 6.9 KB (6912 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4e0874f1417f0c17a6f10d3b955280163bb7630ccda5c490b67d3e77e0e68c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35024153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e1192648f1a962a26c813e8ec99b7cc34631f4c2ea7d1ff2c35f8edfef01db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2dee707e7ee901389a7d7012845d60c86c0f8b7b2c73c8a41b180a2d5814ff`  
		Last Modified: Tue, 17 Mar 2026 02:19:59 GMT  
		Size: 7.0 MB (7017051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a7da1c886dad434043337b4a14266079901e3babb896b07dc24a83286b5289fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4243cc93556703d310bb4562e66af340f4a2d5110eceb1bd58ddcd9bff81512c`

```dockerfile
```

-	Layers:
	-	`sha256:1dbf8c48d478bce5b427fe2efb814edff8783a8004518c0afd25c65ab8b152e3`  
		Last Modified: Tue, 17 Mar 2026 02:19:59 GMT  
		Size: 3.2 MB (3207432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94b347378ac1a2bf90b03739b0333f23fc0900f525ee8acbad918e8fa8c06be6`  
		Last Modified: Tue, 17 Mar 2026 02:19:59 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json
