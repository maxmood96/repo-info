## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:fe9c15491cb65d3f14345a29773c261f1e96f8bba82d71370fc7fa3d542a6267
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
$ docker pull buildpack-deps@sha256:6d50b3e92542a04322fbc2914286d49e5915ddaffcf191c07e06661fad7f646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88764230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131aa2852b90e0ada1162bf44687db88ffbac12639b7a8d6f057c2bfa7a0354e`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5235aa939f41c34b69f4fe37736745fde8e1a4676950add7459e7b957c4cfd55`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 13.6 MB (13617608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cf16388a9a3471d6a91777a42a673b8db99767b831de048212ce4136744cd4`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 45.4 MB (45394654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3f04deeea996b84aa1dd1dfee85837b0a2f1bfe56fd34469d8686c2b2df4193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8858ee1939cf86150c60e81cac0c8fb87a608744c7ec96f3a8af6fa531324a19`

```dockerfile
```

-	Layers:
	-	`sha256:addc9e17fc74d7040b9ab7245bbaadcde580f924bbad026c4091e477cab1bf6e`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 5.1 MB (5076115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd67f97ec250bb62ffa5140cbe45a6491aab2a87e36613851e4c406872536f6`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a61b5717e3959eb12f5a88893dd831ac31b1ec5d51e4d4203c76f3f14d4398c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88532245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9757377196fb583c02518c6b25a5b02129b34159f1d6bb14e27e0bf15fe7cb6`
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
ADD file:9ba898ef47e3bf423fea81a90820aff75f6eed50ba716f3cba79e91e03e5cbbb in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bca51b985bec22ed70905f426f055641ef48b89c81b90c99246fed6ff752a789`  
		Last Modified: Wed, 16 Oct 2024 12:48:18 GMT  
		Size: 26.9 MB (26869468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438c124744710d655a244db3dbd84835fa0be9d4a64e316e7f71e35ad7d8c979`  
		Last Modified: Sat, 16 Nov 2024 02:56:56 GMT  
		Size: 12.8 MB (12774782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d88d138eebcfcf40fc6d4ae49dae17bff1beb7da88f9497177c78c91965824d`  
		Last Modified: Sat, 16 Nov 2024 03:49:56 GMT  
		Size: 48.9 MB (48887995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fc01bd2711827e775475a502dff7f12d1d9f1452b274b842ab8e546cd490013c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba70c17a2e355e9fd936ada3e077ef7cfd041d882a895226b286aeb68c7a41f`

```dockerfile
```

-	Layers:
	-	`sha256:a6452d4218be5a656fcfe4d5a862f2a1360472729b9fa300bb4de5dab0daffad`  
		Last Modified: Sat, 16 Nov 2024 03:49:55 GMT  
		Size: 5.1 MB (5077389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fceec7cdb2963a36c0318221b4ec5864a023645eb8f6814e873bbbb2ccafadcd`  
		Last Modified: Sat, 16 Nov 2024 03:49:55 GMT  
		Size: 7.4 KB (7365 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d4e3364b459f91ebe8d2c98bdd71a77562b67b6b8fa02b064c57e1e224fe0ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87642570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e794272d13d3fa99ede6217b8530802b022f32a044b397afdd0c36fb474f0c5a`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578430ada813a1dfbd9fdf0f08ac85e283f768e4d6a97b577fb934529488d67c`  
		Last Modified: Sat, 16 Nov 2024 03:06:38 GMT  
		Size: 13.5 MB (13452735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7099dd99e11f65d04b9850eeb2afaad9bab1be3de5848effb8f1d6d823d5fff`  
		Last Modified: Sat, 16 Nov 2024 04:08:10 GMT  
		Size: 45.3 MB (45297410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:91bc05c7f5581f09da7cb3048640e2b2d2bfeee5740ef189c1af429a303cd133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5090679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b308b489ca3abf98c2967b856613971d99fa2a3b7be2da719cf59168c323ddc`

```dockerfile
```

-	Layers:
	-	`sha256:37a42359c88e39c7c087b184a11bdfab05d65b234587c2b6ba8d403ff55a71f3`  
		Last Modified: Sat, 16 Nov 2024 04:08:09 GMT  
		Size: 5.1 MB (5083294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1863b83a2d4abe914e004077b40d051883d1c7cf7ecc4de4b7e4af7b90f85da0`  
		Last Modified: Sat, 16 Nov 2024 04:08:08 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:357e7748ffbb41d10bb4c25996a54ee3be84055baada24a0efe8e31a57649fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100871194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f121f486b76174523fb4f1bec86fc3818711e60848866df6118a985fefa3b3e6`
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
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0264183e622e4755eaed163fbd2bbba3a6ed157dbe6aad9b1211d970e1cab5cd`  
		Last Modified: Sat, 16 Nov 2024 02:56:49 GMT  
		Size: 16.0 MB (15980175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fff3e6cb8c0f3410138c8adcda0bf8c1806da7bf9d5714691e0e22a9162ee0`  
		Last Modified: Sat, 16 Nov 2024 04:08:41 GMT  
		Size: 50.5 MB (50502197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:52050f13db0cf90d003fd500088fc8f6222b5bc68979dcbcd7e47322cb095228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a15ddcf7cd722831616f9dcb7f9c45e6dd28972dc9438e50fc89d06dde8ba25`

```dockerfile
```

-	Layers:
	-	`sha256:82cb0120082d088c060fe6c39a34cccbc3f2237190d9b7b6bbfb468f51ba4e77`  
		Last Modified: Sat, 16 Nov 2024 04:08:39 GMT  
		Size: 5.1 MB (5083785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96b730af5b3dd93ffedd3d9fbe2b9977ecc2c871be9f0f9e63c07e6a8826f0cb`  
		Last Modified: Sat, 16 Nov 2024 04:08:39 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ed4c4dd3d21dc7243d9273df07db656615e9b799ed535f734fd296ffd7e04419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99158145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21675b0a4c4d47ecf3846572423fe77cd3243ab999c99d848be762281e4e7539`
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
ADD file:c7a07ab82f7f269608b3c78a3d2b0cd74630ea7220aee252fb2a61f78978b08f in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ee732b5fddd0a964c04b11ad9b9ec9f70f7df9e1e96825973cdf803cf1fba8e5`  
		Last Modified: Wed, 16 Oct 2024 12:48:30 GMT  
		Size: 31.0 MB (30980747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978c2b446b91443c02372245ec5634f837dfb1031d788fbae576417921386887`  
		Last Modified: Sat, 16 Nov 2024 04:40:21 GMT  
		Size: 14.3 MB (14320790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c905c758c1b2b699e28da83ca3345886fe32f2ea7f8b79f8b263d552dfd45c`  
		Last Modified: Sat, 16 Nov 2024 07:55:07 GMT  
		Size: 53.9 MB (53856608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87f18247a590a11c54ef990184aa778444d2538feca3b06e90a301849a1e3f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5073976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83ab0c10a0ed7dab6409c6abf786aeb7cdd54788489dfd3a1001a3ae79502ad`

```dockerfile
```

-	Layers:
	-	`sha256:716bb8838808d06e9ce099fad74c795b69cc9cda71da56dab2f76c349d646e14`  
		Last Modified: Sat, 16 Nov 2024 07:54:59 GMT  
		Size: 5.1 MB (5066639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f7d4328b354181f33fe9856d67d668184b9d9a325f2c58d85603e7d9512bb6`  
		Last Modified: Sat, 16 Nov 2024 07:54:58 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7f2a641ff15f643132730573eccc97bf3e0e0f1e7f75d1f3530c7523945881d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91905067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3e8d5fac09d0c21e64b370dbb7d89668674c6437aba7ce746a33242814c2b7`
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
ADD file:1c592b6de2557bde912d6291330e1604327193966f24da30f3ecf513f06fd372 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4d3763c838a1509ac75e9b37aa0fba11067b054033fda0d642f7e32e542b7994`  
		Last Modified: Wed, 16 Oct 2024 12:48:36 GMT  
		Size: 30.0 MB (30021284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dc197e074c4e27330b2c116bf933ae7f39fc83dcdba25dae0043d055e114c2`  
		Last Modified: Sat, 16 Nov 2024 02:56:27 GMT  
		Size: 15.0 MB (14960585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae20f92c5dbf3057e82a5c4fef15d79cee423bc0d208fe8f2354c290f520725`  
		Last Modified: Sat, 16 Nov 2024 03:49:31 GMT  
		Size: 46.9 MB (46923198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:71aec99d1f5c06b282b7cf7b0da107e415d57ce8c0d33849eb07be4a7f847b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287560bb6aac73b99412be00298b990d3006eb3f8a4e3bff1991ee20af280e93`

```dockerfile
```

-	Layers:
	-	`sha256:906784182fcf6e6828291dee8a526a0783a7fefc091ff8a40b8c7a2ad97c38e0`  
		Last Modified: Sat, 16 Nov 2024 03:49:30 GMT  
		Size: 5.1 MB (5078432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0b8f195da05af25fb3e91113296e28f74c998076fc5eee5b5a548d5f1ee9ab`  
		Last Modified: Sat, 16 Nov 2024 03:49:30 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json
