## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:f0841cace4f5a1111355ee705d15754e2ee69e4fb90f6fdbac552ebab5914209
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
$ docker pull buildpack-deps@sha256:d00c5eac2654b2af54f3c89258cc6c37bda3a78961978568de89fed6d3e23fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36641622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc608e704c4ac1058b0335d8f34748b31ad9cef2df316cfa714522cbf214607`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541b91de6cf313637ee71aa147f2531502925472ffdf0e07e45b3dc2475d2a7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:07 GMT  
		Size: 7.1 MB (7104256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1b942f956fe49c46e861c82d3d4017ea83f41f2b481e99bede7e43168f956142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8bfa0c67da7bdb1f24d5cb513b7b2149f0bd6672a330ed2fe3752242a02083`

```dockerfile
```

-	Layers:
	-	`sha256:88e3852c3c63b0242decfa2c8739379a7bf8ba77ba530abd52511f34a07a970b`  
		Last Modified: Tue, 17 Feb 2026 20:12:06 GMT  
		Size: 3.2 MB (3205215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f1f9e5f199d0e19735b2e51990295a06363a5985a9f62f2dd535e1fc3ce1508`  
		Last Modified: Tue, 17 Feb 2026 20:12:06 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:035377b8903e5c8b4097f66b206e6afc94f33affe428186521cacfadfb68b56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33652642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dda28a8cf89714762ed69224d5c64608e93240176206013418909731217ab5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:55 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:58 GMT
ADD file:5c6b4f7fe4e36ff387edbef0b3a7c72fa9a66f82297c2c1a27259d6be00727bf in / 
# Tue, 10 Feb 2026 17:41:58 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:10:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8994f3e4ab606dcbf77ca1a5364851191cbe725563408ee7cd2a667cb364bed0`  
		Last Modified: Tue, 10 Feb 2026 18:13:45 GMT  
		Size: 26.6 MB (26644404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501a50f996ee1a16a6508e935ba239b1abd7392c7136e9c1d97a48d75ea56fc0`  
		Last Modified: Tue, 17 Feb 2026 20:11:04 GMT  
		Size: 7.0 MB (7008238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd675b14fddf4cc9bbdd5d6280eceea9533ec02f8fd056648b2f7b6f18de2d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aa242131869d5fe0db8bd21041303de6eb81abcff19f1d6f3ab3e7670c949c`

```dockerfile
```

-	Layers:
	-	`sha256:1556e47ad9dd974767c649b9a00667ac0ea229603739ccfcdaf9cc4b5db1598d`  
		Last Modified: Tue, 17 Feb 2026 20:11:04 GMT  
		Size: 3.2 MB (3207522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e5b23c0e978a75bc49d34ad92c8a63fccf56f1045cce46365beadc703d17b7`  
		Last Modified: Tue, 17 Feb 2026 20:11:04 GMT  
		Size: 6.9 KB (6945 bytes)  
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
$ docker pull buildpack-deps@sha256:e16cda8b678fdded845793548de208d431bf146ab55634332991272f38f102c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35019543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8637d151c63aa8ab37d299e5b47eaef27ebfdfdc69d8ac52c7bf2f115432d96`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:33 GMT
ADD file:682bbddd1f3d784d0c4ab5eef9460f0b47a94f3c62f629b59163a7f6543a159f in / 
# Tue, 10 Feb 2026 17:41:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:10:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e2905dbd81d6a42c24ec5f7ce51f2d8f24a616b4fe2e90d0be791922a8d3b5f`  
		Last Modified: Tue, 10 Feb 2026 18:14:06 GMT  
		Size: 28.0 MB (28004382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221356e6453c622cef031449e75d40ab56e4d979372191cf03af1c7f88a098d7`  
		Last Modified: Tue, 17 Feb 2026 20:10:31 GMT  
		Size: 7.0 MB (7015161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c6b689339aa5e180df5c4310b44d4675aa31852dddd1d0c384071a903bf965c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3214313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0f79e0d6c7575b2e12b52da25bdbaceeb9b2c1d8dd2c4b122d597b2bfe2e29`

```dockerfile
```

-	Layers:
	-	`sha256:65d6e0ab382cced97668a20140919bb6f9f9dd8f3fd18823aed811d70fb3e449`  
		Last Modified: Tue, 17 Feb 2026 20:10:31 GMT  
		Size: 3.2 MB (3207432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700c1ebf7bfea6d87ed6758834a8bc318334dab6720ea403198040f7b47c514e`  
		Last Modified: Tue, 17 Feb 2026 20:10:31 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json
