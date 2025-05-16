## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:2fdd58a764e59435223aeb015778e3ac7c483f33c703da86c9f61d81757d5d88
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
$ docker pull buildpack-deps@sha256:148e10d3a2e28b79f6e0f6fd250d6de19dc86d4b257467815b6357cd84504237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46210459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4422d999aa56d7129e7733346fae90a0864332bff03fc35fb72200478c02f0`
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

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cc91039de98d8c8c7f028def823064f160b68a9c034acf77f0e63e9d74018ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99859574e83a4eaf6d463ef8ad739e7984ee4691120eb19f98b5a2f97d3828c4`

```dockerfile
```

-	Layers:
	-	`sha256:cf9ada4bc418f7266b0ee8c5bdcea4b00129bdfd799b402335840b970adaafb9`  
		Last Modified: Wed, 09 Apr 2025 01:11:47 GMT  
		Size: 2.5 MB (2456760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:775c3e5d248a402c2c9b3b563a055ff9fbfe6d7108b1599a5b77ae43caf42b4f`  
		Last Modified: Wed, 09 Apr 2025 01:11:46 GMT  
		Size: 7.0 KB (6977 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c93dcd9ce1d607f29260a738e208bcc92d63ea87a3862461e6c8ed935d8049aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41857609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2146f95246d62aaf25a285a8e57c77b54447575f297bd90909161344ebfaa3ff`
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

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7fc4034734e1d01b6392537cdc4c205ac8280c8298a7a5520afa9f72045200c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4926eef2f2477ae92d180a1e6f8c50f38da02f1acf66364bba0e7402676ad75d`

```dockerfile
```

-	Layers:
	-	`sha256:63f09d389b70578116428988afbd2149b9c3296e2e646bc3831582a087accd83`  
		Last Modified: Wed, 09 Apr 2025 11:35:56 GMT  
		Size: 2.5 MB (2459061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30053c2c1c361e76e86f06ae683ea4e69de47dc0afc8689a005e2c7cd1d1d6a8`  
		Last Modified: Wed, 09 Apr 2025 11:35:55 GMT  
		Size: 7.0 KB (7038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:469fab1d41fada4687145614f86e607f2a4d3a0a96e528e310883e1b9cb07440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45650292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b9eeaf473a6c3ac6e7307d5d7eec2e69c910c5682a172df1e430eb2b2774f`
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

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:818787fa27fce963d6a7faf225068009e538ca054bd76dff74e2e13cf6c4f7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f13a41a69c27fc9477bd314a51792dbf1e8f0b03303ec6ed6202b7778e29a14`

```dockerfile
```

-	Layers:
	-	`sha256:6fcb9f0d6fdf2e7a4a100dc036486d84faa6c2d0a0c44c1ebec9893438eb0eb9`  
		Last Modified: Wed, 09 Apr 2025 06:11:20 GMT  
		Size: 2.5 MB (2457817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0bf4de16ba5baebedd12776f9f503ecaa6b25f2e2c26da4e03cab58cb52cf4b`  
		Last Modified: Wed, 09 Apr 2025 06:11:19 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e8c70e5f446480f6f3fd98874a154f37b05772363a1e378db4bab3d237cfe4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52606876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5965886a288278bcf0babb820bc8ee9b4af0f27f04fb2e64b5e3ba72940129a`
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
```

-	Layers:
	-	`sha256:8617c693189c511af931ec6b7aa3573654d8d3d3274b061f881929dc7e9e831e`  
		Last Modified: Fri, 21 Mar 2025 09:41:03 GMT  
		Size: 35.1 MB (35116459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eca3df5efb1d2a7a155d29563d34a4cc59b77f1356adfd169ce229390b6bd91`  
		Last Modified: Wed, 09 Apr 2025 04:30:59 GMT  
		Size: 17.5 MB (17490417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b1ca43aa2a9e009a6b9141ebb8b8df319c2923974c22998b2ff72a3fd2e29927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ae49e1349744f52ab3262c38a2940004d79b624fd904c6061656971cfc1f50`

```dockerfile
```

-	Layers:
	-	`sha256:6739d5c0ba43883eee95ad22a8933e8cb2e2725d389666077faba9858821460f`  
		Last Modified: Wed, 09 Apr 2025 04:30:58 GMT  
		Size: 2.5 MB (2461244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70b9f6aac6d8525f6191a3face353e6d81c2ce6bdb5b9daeb8e959d58fca0d00`  
		Last Modified: Wed, 09 Apr 2025 04:30:58 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:93bd19f70d87b9d7216dea52925bf67b67e2b23a9dec5a6257696c062f17fd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47995454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73fe9c70cdbc76679ea8add0addba60cf1a1c12bedb88b57f506a883987901c`
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
```

-	Layers:
	-	`sha256:17143e5c2a0de46dd660097f35b7d1c381a1cfd489bea2cdd1a596a3e3b08cda`  
		Last Modified: Fri, 21 Mar 2025 09:41:10 GMT  
		Size: 31.8 MB (31808054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f1c68219c9767213bddad50e7129bda08a3407ab786d2bb7b5a54df5e760ea`  
		Last Modified: Wed, 09 Apr 2025 05:21:45 GMT  
		Size: 16.2 MB (16187400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:45e9dd733b66b1a8db1bce084eedc05f5602dbebf3fb08907f917635abdc9b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e46683c55d685c2a1e41cb0da66e91204381ee991c4c648dc412cc1d97ee277`

```dockerfile
```

-	Layers:
	-	`sha256:e5705b27225e61b53df6e29941898471706217381ae16200a4063aeafda86fac`  
		Last Modified: Wed, 09 Apr 2025 05:21:43 GMT  
		Size: 2.5 MB (2450822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8977929b379e0359ecae0d9950d7003a53745306daeee2100f293ee43c86725`  
		Last Modified: Wed, 09 Apr 2025 05:21:42 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1748f9eecd044738d8c30fdf9a2a067fe1643ea0af3248c6bbcac5147e775d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47941520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8982955e80e86cb3c1d5daca29dd5ce3632555dcdc7eed22dda8d405c3e8aa`
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

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:69f4bee47466f3271cd3f4bc96ab4f8cfbe6f94ea7ff1da4153d640fbd9a46c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0be13dcd8decaf16fceefa91747576c978a81af9ec9c0b1794081d5548411de`

```dockerfile
```

-	Layers:
	-	`sha256:e85a2c32c2e3f3bb2026a63958114137cb2a46c692943e82d2df92ed60496eab`  
		Last Modified: Wed, 09 Apr 2025 04:13:25 GMT  
		Size: 2.5 MB (2459586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e54e034ccb1e516e74e2defb550dd28c0122b5d5baee2cc4f277c9e0c62e3fb9`  
		Last Modified: Wed, 09 Apr 2025 04:13:24 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json
