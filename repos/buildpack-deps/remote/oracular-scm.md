## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:93e4db7e689310fd3c1bcc8f2a9af15c311613c63150a8cb616066bdc9cd6eb4
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

### `buildpack-deps:oracular-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9c4c5d6d8601b737f6324a4c6430f2d1c648d901479cec3f18a8ae18c6ebdb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92847832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3b2a7e0f7d79e4dfa160fb57d78622917c15040fe4b2e611b01b04ab8a3eae`
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
ADD file:764959978f9fe798d77bf581ad10e612d454a82cfa4151c252f99dfba77930a3 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:440a90d6b31c594198d5c8b7f0cdefd617cd095c8cccb6efe3152af757db0f83`  
		Last Modified: Thu, 08 May 2025 17:05:29 GMT  
		Size: 30.6 MB (30647018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caf06dc4ca048294638d860fdbe31b52df91fba85cc982ec96d4cfae787323f`  
		Last Modified: Thu, 08 May 2025 17:35:20 GMT  
		Size: 15.6 MB (15563441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f2791f340319af4abd181ca8dbaafcbeac7b2dc1efc999fc9a565cc4e5ebd8`  
		Last Modified: Thu, 08 May 2025 17:35:23 GMT  
		Size: 46.6 MB (46637373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5eda8ae26a7940ee6170e634f592f37cc782636ca0fe3ac5eb894171e052fd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed888582b2d956a58b065cfe697e99aeabd0a2bc51e5adb4119e635d27eeba2a`

```dockerfile
```

-	Layers:
	-	`sha256:b9169b5c123e40a3cf24ee0b00e8aa1148e0748ad87d070933e630a430f45e60`  
		Last Modified: Wed, 09 Apr 2025 02:11:54 GMT  
		Size: 5.1 MB (5084588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0e0851c02c494f1e5ac13e0228db72a56ff2c889feed304c56a8755047c2d9`  
		Last Modified: Wed, 09 Apr 2025 02:11:54 GMT  
		Size: 7.3 KB (7323 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:17e36ffc7be8422894044902c702faee1d28709abe2cdecccf457c0e6c52889b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91313111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffe81a55b925270f5ef63f38abf5da4569b9efc0473866f62be93a8a1ca1316`
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
ADD file:f13ab66af81cfdff78a6c942b3d1f102b5a17f8c923dfff8d28e2403245adf4c in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:090aa4b9a734ba6bec570aa125b6ad0489dc536d5cdd28a669b8bdd0a0cf0b7a`  
		Last Modified: Thu, 08 May 2025 23:28:00 GMT  
		Size: 27.6 MB (27554319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95637e503528dcbfe1fdb44aef45d4820550ec4b33d60a6ac713d5b873a3d752`  
		Last Modified: Wed, 09 Apr 2025 11:35:56 GMT  
		Size: 14.3 MB (14303290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dd76adb0395e9e97fae2b6b75e8fbf122e60f7c76228b01116cf3edbfe2632`  
		Last Modified: Wed, 09 Apr 2025 12:21:05 GMT  
		Size: 49.5 MB (49455502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ba4a62a85ce8a3c28e7e6e40c579fc3d6f415f9efadd43b1577c829bb8382e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bfdb575cab6cd22253b61c37a9aa0f8cc384f2b2e39d7281769f081cecaa53`

```dockerfile
```

-	Layers:
	-	`sha256:2f3b8142fda6126246eb7600bc3e68e7f6b7789afeda314c2321e7dc52734544`  
		Last Modified: Wed, 09 Apr 2025 12:21:03 GMT  
		Size: 5.1 MB (5085892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afbd4d70c10e9128b83d97641247d24001fa8bade12e5432ac32f6045d60c059`  
		Last Modified: Wed, 09 Apr 2025 12:21:02 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fb189b9fb37da3bd74439a436bdfe76026420222eb84fd0ade9f624f9d2d2a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92185022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5de10195173113aba884a380f004434282ef3f3a3c1d10a39177a5ba327afa6`
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
ADD file:458f2262832f9254682efb663e94ed73cf9f068bc4799f5a25ffb533a869ed44 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3d825962f62a727b0760fe9a4f96a67a09a0d2a8077e99007e7681149f2ab3fd`  
		Last Modified: Thu, 08 May 2025 17:10:33 GMT  
		Size: 30.3 MB (30320224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eacb0abd365e7ac96a553eb11a8b04ca8a62c023926633845107e9e215227a7`  
		Last Modified: Wed, 09 Apr 2025 06:11:20 GMT  
		Size: 15.3 MB (15330068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28478c451efafdd58825833b7a96ab18f7d12cc4d2cf5871b329ac70bc3074e5`  
		Last Modified: Wed, 09 Apr 2025 14:00:14 GMT  
		Size: 46.5 MB (46534730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:319a0819ea596ea10f298fe919f08e0d0daa7385d74f94f930f785d09c6c5cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19c177a5904c2e0993632d900bac1e8271f7ebec7199291e15f82c298464d09`

```dockerfile
```

-	Layers:
	-	`sha256:394f78099701510b4060c0509621f9f80815bdf47e6b284816f14e530619e970`  
		Last Modified: Wed, 09 Apr 2025 14:00:13 GMT  
		Size: 5.1 MB (5091782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40d844ebf3773e82dee16a45a701db6abb914ed4c83ec8342c0068595a16497`  
		Last Modified: Wed, 09 Apr 2025 14:00:12 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9f725b003f916a6681edf3aa47578df4577033ff535fbb5050bd7202b62008de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104424924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca53e83a5e805f6dca6f682c825edde134ab6ac08a4faedb3751a387efe4e844`
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
ADD file:1b338c439eae4a20ee7d1b84db98f2f0664cd0c53c3843407f28a1b33a48c0ae in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8617c693189c511af931ec6b7aa3573654d8d3d3274b061f881929dc7e9e831e`  
		Last Modified: Sat, 17 May 2025 01:09:56 GMT  
		Size: 35.1 MB (35116459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eca3df5efb1d2a7a155d29563d34a4cc59b77f1356adfd169ce229390b6bd91`  
		Last Modified: Wed, 09 Apr 2025 04:30:59 GMT  
		Size: 17.5 MB (17490417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdbf25494c1d33658a8d848c137015fdf810bc230f9fa986642899a607aab15`  
		Last Modified: Wed, 09 Apr 2025 07:39:13 GMT  
		Size: 51.8 MB (51818048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:634a3cb329a16d264c3f06e2257b1469ec4844f6cb62145750a792f0b9e6fb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f312995b9d40525dbcfcb5dd269da78fc741b29040d27c98625fdd16b5de36e2`

```dockerfile
```

-	Layers:
	-	`sha256:a7589b84822950ad3d95f8fb0adb3548de1af748e1135673a0cca7d48696f85d`  
		Last Modified: Wed, 09 Apr 2025 07:39:11 GMT  
		Size: 5.1 MB (5092292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df878a0803bba056b7fb1bf7a7c2523e63d4decea13d04ff02b8009d281fc65`  
		Last Modified: Wed, 09 Apr 2025 07:39:11 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5b74228496b567c29cf9b237e62337798bbc1598e27543cfde1664717b6179d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102599133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4b41f0df10b8a923997277224d960cbc9615064aead052f0876ff8d6f8e616`
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
ADD file:e17f3a566611e6e6aaf40f0cf67dace1148c4e227e136a582732abd5470cc4bb in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:17143e5c2a0de46dd660097f35b7d1c381a1cfd489bea2cdd1a596a3e3b08cda`  
		Last Modified: Sat, 17 May 2025 01:10:12 GMT  
		Size: 31.8 MB (31808054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f1c68219c9767213bddad50e7129bda08a3407ab786d2bb7b5a54df5e760ea`  
		Last Modified: Wed, 09 Apr 2025 05:21:45 GMT  
		Size: 16.2 MB (16187400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff1351043fedb7e8229fe0f7f54e7d9a6728f389ecd49c4378c8f4a18d98c04`  
		Last Modified: Wed, 09 Apr 2025 08:46:47 GMT  
		Size: 54.6 MB (54603679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:851f77500355debcc426e533b65afd230dbd76977baf2521cef9b8869b745d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8189ad49d5fa82dc03d69b0e6e160f02a3dd7b62581dda68bba0abce9a70adf5`

```dockerfile
```

-	Layers:
	-	`sha256:d7bfa5b51909e773a0ee35a1ed0fa806128ccfcfa88cbfab531e4e8e2b899202`  
		Last Modified: Wed, 09 Apr 2025 08:46:40 GMT  
		Size: 5.1 MB (5075120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32284ab5997db5f0a7a3ca50c071a13ea74b3f15b6d74cdbbcb2f27f1ca4776d`  
		Last Modified: Wed, 09 Apr 2025 08:46:39 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:52fee1156e50541884dbcde98e722c25b1950dd77e6dc9b9e9678bcf54f22a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96015097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1de7336ea4221ec74ba049634f882a3ed9b748985a2c0fc38c090a8fa78297`
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
ADD file:6836ca55f6c19fc0e06d3dc978a72aa71953f87a5bd8cbddc3ed081700c03924 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d97194ac694365d185a619f35f2e6568110c20c3adf2a9504567854113756237`  
		Last Modified: Fri, 16 May 2025 16:28:53 GMT  
		Size: 30.8 MB (30807587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd0f373b4fd69149d2e82b840da266bbef643b2959efd2fd5c3339bf6327c8`  
		Last Modified: Wed, 09 Apr 2025 04:13:25 GMT  
		Size: 17.1 MB (17133933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9317ef61611edda8e8ee6e896ffd5dae97da282073fac53c5c33b08abb4dfc07`  
		Last Modified: Wed, 09 Apr 2025 07:10:33 GMT  
		Size: 48.1 MB (48073577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e0cb02fd37d3bfa2f5f850565602ae9b11905e0ddd0275d7a64e6480a0b929d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8611898aa3bd092452006933ef74ef9c109d97b86d4d2a5601038484e5c754`

```dockerfile
```

-	Layers:
	-	`sha256:f7735d0d4eb74995ca8f65cd4486102b6f475cbc83fa569ee274fe5f261371a9`  
		Last Modified: Wed, 09 Apr 2025 07:10:32 GMT  
		Size: 5.1 MB (5086918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef51f4a4d772dc7ce20840ba466b608a467b0dcc073861a3426400d8e493909b`  
		Last Modified: Wed, 09 Apr 2025 07:10:31 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json
