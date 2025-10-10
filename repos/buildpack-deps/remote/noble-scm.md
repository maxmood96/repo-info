## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:37b7722e9502392c3f030c20b9d6b209a552760c7cc58dd78b09afb34909a61c
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
$ docker pull buildpack-deps@sha256:20c52b605a16233843983c21b0eeb5032928a609efbbc5aec529e48149572fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88682420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3785fef3599354083fdc4fdb2c2f826c7e0b9479f58769376315c5bbf94b11`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4da1c38cd39a1dd115e9a6c26965a439c65b03d482b5fa7a24467582eadd75`  
		Last Modified: Thu, 09 Oct 2025 21:31:21 GMT  
		Size: 13.6 MB (13625081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf06f1df562fcf4f04a84ed229e7bef8b2385ff7761d3b16236ff11be8f0eb1`  
		Last Modified: Thu, 09 Oct 2025 22:13:38 GMT  
		Size: 45.3 MB (45334192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eb3204415f8990a030dec8ac437792dbaabae31f3952a2fa5d4b3f3b488849e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461d57f418aa8dacb1a5f6912ef4c01109d39f2a62697870c27413a54d3f10bc`

```dockerfile
```

-	Layers:
	-	`sha256:c793abfbd131d2a489600526477ac28fcbf4cfb8ac201b5994b29637060f43b7`  
		Last Modified: Thu, 09 Oct 2025 22:20:11 GMT  
		Size: 5.3 MB (5274574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513de523acc234e01d95a5f6b1161fc99cc00ae63c4052a31c05f7d585938e09`  
		Last Modified: Thu, 09 Oct 2025 22:20:23 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:89d2f592c3f07f5b7e247a2082664d2e742a4fb6c4cdf6a22c74c466e91c49f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88501807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db974353ce83e2632eec46abe8f9fdf896d6d6491b2f369fc680acb9792c053a`
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
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022ffe8d142b8dd5e375cb3bbf3b7f0d742fcf24654020fe40ada08aa8d2bfe4`  
		Last Modified: Thu, 09 Oct 2025 21:08:02 GMT  
		Size: 12.8 MB (12784406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6168ce6859325b4e6307d2e5462c00745a7afa8be1928d087849949ffeff2cb`  
		Last Modified: Thu, 09 Oct 2025 21:17:41 GMT  
		Size: 48.9 MB (48865669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a65f818bdefd102c5b6eaa25d633a1de2606a4a515b157f59a8548a941377bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d710024da084c981e499736a65eba24b1748ae800bd48f538b30530822d6a07e`

```dockerfile
```

-	Layers:
	-	`sha256:e4bfab6e4ef9ebf6273b2dfc7d50867dcf02b6fdabc4cc41fce4b69ed5578eb8`  
		Last Modified: Thu, 09 Oct 2025 22:20:29 GMT  
		Size: 5.3 MB (5275872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8402b197917ddbeac68f93f87c8096689a9084376d04567f1913ed0d9a941dc0`  
		Last Modified: Thu, 09 Oct 2025 22:20:30 GMT  
		Size: 7.4 KB (7369 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2c534084e54d21b77eecabc4c38a4628306dc0ef64fb9251f535e533b143e3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87596924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfd3f974e7a28e1a6cd5e46664d6ce4b04d951a8140fc3459120158120c504a`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd70ea204ed4db7ba47a601ca9a11c75a0084d32a61213dd88df48189d57b7`  
		Last Modified: Thu, 09 Oct 2025 21:09:03 GMT  
		Size: 13.5 MB (13460697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d49dfd9b0c2e4777e0eb65d385c4fbe4ac4f35cb1096d5ae1801095edc9d20`  
		Last Modified: Thu, 09 Oct 2025 21:32:19 GMT  
		Size: 45.3 MB (45274515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:77dd5e3e99dd9afc96b5f24dc90c6988eabe4b75fce4af6533f1e63e7047c879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271f12c983c0fd19f000375e6acfc35c79733f71c07c7ff4f127fce8e16059cd`

```dockerfile
```

-	Layers:
	-	`sha256:cfb080de1fb0af7cbd0cbb1b9c3839e758e333cd93e771c7ccb2ecdaffa61f7f`  
		Last Modified: Thu, 09 Oct 2025 22:20:59 GMT  
		Size: 5.3 MB (5281766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9fbdd1853c2aacebea8c2d9f46455f9517e3fede0cf0356fdc61d04054f0917`  
		Last Modified: Thu, 09 Oct 2025 22:21:00 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dbdfa791db7cdbfd95f97a7c946f8d2d3cda565adae31f007ddf5569dbdca466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100662272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4060bdba91e33f7deb38ddaa96ad040f64b0bfadcada774ea2306c9a8173c72`
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
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff2c43d036e8b55e943cd93e0bc732e1fdb6b9a5f8fec89a5e868148e6bf1fb`  
		Last Modified: Thu, 09 Oct 2025 21:09:03 GMT  
		Size: 16.0 MB (15953193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0519421d01f87184f984ce44c220694d718f4d07feb1a3dc151316502799631`  
		Last Modified: Thu, 09 Oct 2025 23:05:04 GMT  
		Size: 50.4 MB (50405554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca565357d0a2db6705a69cd2b959ab357460416d8c41b9141ab6c73fe15f9f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80219d22ebce30106f36b49cc7391b263bde9545c55452bed11c018f2c8cbede`

```dockerfile
```

-	Layers:
	-	`sha256:27b659df6de2fb201672610f98961efa7f46c4a043d575547c7a4f8daa36fca5`  
		Last Modified: Fri, 10 Oct 2025 01:19:41 GMT  
		Size: 5.3 MB (5282428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccf0f7b19a208e3a66d4bc698c3387732c78f3b4e325b8b3f4edcd562f444110`  
		Last Modified: Fri, 10 Oct 2025 01:19:42 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:01e044b6f65839403e6e5c7920da5935bcc0a452dd9ea0bea022ca37511c6de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101262285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67ff0ad03b7f4ca3e751734aadfb430a20a3bc84260a8dc9250725f43ff9590`
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
ADD file:13e2355f84c9f5f1ba6aa2fa1db4359cbe23312f7b2905fc8b976899a09fdfef in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d699e6bd7ed3cc40f40b8118f763dc4303b0e97b911de163cabf78f19b5d434`  
		Last Modified: Thu, 02 Oct 2025 23:21:18 GMT  
		Size: 31.0 MB (30950446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a1db83f9703600be5ef129fc760e5b31ef0ce74e9f5924ab56f5b6ec409253`  
		Last Modified: Fri, 03 Oct 2025 17:45:18 GMT  
		Size: 16.4 MB (16435787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d83160000fbf1db26da602d9d80b60c5e13216d6b8e724bff6ad7132b7430a`  
		Last Modified: Sat, 04 Oct 2025 10:51:34 GMT  
		Size: 53.9 MB (53876052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:318b638df5a81da2e7fefa18e0cf4ad7b42974da93341f7d153ef7ec774b7163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ee837850e67cdb32710c92e8adab39b05afb02cbd76f1e47f0c55b44eaf3e3`

```dockerfile
```

-	Layers:
	-	`sha256:2d39bc809968a19c87295b29af350b48112acb389d90454489e0cce02d053721`  
		Last Modified: Sat, 04 Oct 2025 13:19:47 GMT  
		Size: 5.3 MB (5264970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be47bb8933654ce59f90aa3acd314d7931ba8937644129b465d917e1fc44f306`  
		Last Modified: Sat, 04 Oct 2025 13:19:48 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:525dd0d52f06d6d8276ff7a30fe06b6078dd9bee6b554aa82684208e96102ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91657981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b459f0218571cadb8e004cfae05154beb153d50a4fd518ed1c9d08e73be9c6fc`
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
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcae3965c70c7cb3a760d4160161a0695e258329f001c8a190e4c43e7741035`  
		Last Modified: Thu, 09 Oct 2025 21:09:01 GMT  
		Size: 14.9 MB (14938071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dae70b370244b74d48002094af6772c75d26b87a7e01ac35ca230e7d276ca0`  
		Last Modified: Thu, 09 Oct 2025 22:20:06 GMT  
		Size: 46.8 MB (46813759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05c909017fca4c5eee881e739854e2366382ce29ba817fd9668ec3c9307d2b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5284211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aaa915f21a73826ee528cbf68cc0e575484f886797af5de505d1ac54aad66f`

```dockerfile
```

-	Layers:
	-	`sha256:55fbcaf70ad8659d23f31e8bcf12a1e953cb6686d5d1bc72e883df957f973047`  
		Last Modified: Fri, 10 Oct 2025 01:19:50 GMT  
		Size: 5.3 MB (5276906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e880781482b32704e84b80a61c2f6d95a4cabfe107bf891ed187bebc1fe4759c`  
		Last Modified: Fri, 10 Oct 2025 01:19:51 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json
