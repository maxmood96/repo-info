## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:4d161611be72e8b95c29f5effaaec028b6831ef8d779324b33c90cd4c9423e7f
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
$ docker pull buildpack-deps@sha256:d9066c3186976f95bfe99710ca862a37006835174c9e6c24a42fd56820a49139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88648296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698c7406ec6461ee828557695df7d602272a93dac8feabe0b2dee7933a8c794f`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69309ca3d9d60664f532872b9e1059b60a35b8bcd9da011efbec14de1397debb`  
		Last Modified: Wed, 09 Apr 2025 01:11:36 GMT  
		Size: 13.6 MB (13620217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9c07a4a3cd036ac7c92fc3ace1538882a1927198a7a271a4ed8154cb5a6610`  
		Last Modified: Wed, 09 Apr 2025 02:11:56 GMT  
		Size: 45.3 MB (45310427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5547085dce01a1b6373532ead170f391b0ff305f93c2cba28e8c1363e0f8531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73adafc6114d94abccca804f9532ae41bb3ee2e50c0819c9013edd8e4e869a43`

```dockerfile
```

-	Layers:
	-	`sha256:55bc2028d53e41c666b47f8ce76729708f600810622b545cf491fc33fe79c815`  
		Last Modified: Wed, 09 Apr 2025 02:11:55 GMT  
		Size: 5.1 MB (5072284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2da6b4a2ccf8c7d93cbc593e5a4696e1868f3913540387ff9ff4fff5e8094ad`  
		Last Modified: Wed, 09 Apr 2025 02:11:55 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:786300ad756ca5ab92e8ccbd1eb9926a2400e581a8f40c627fb8558ae17a67a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88483815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190c5709bdfae1d436bd3a6b6b7c9257c22229841612730ed27e44dceac359f9`
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
ADD file:0c96eee5fced5e61820b5d18bd668a362ad0e5b3fc04c115f9023e8c295e7000 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34560582cc6246fb88c88648a1db5ef09d8b65d143991211ba2abe7378aee811`  
		Last Modified: Tue, 08 Apr 2025 11:53:53 GMT  
		Size: 26.8 MB (26837532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61ae8c309ecd2f4c2830c9d05cde6b1ec98b1230dc3ccc9ec8e2f33256e2c3a`  
		Last Modified: Wed, 09 Apr 2025 11:34:51 GMT  
		Size: 12.8 MB (12779568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b800cf45f3970426537a7cc29d993e5d491f2825c492b5e484a4000db5300da`  
		Last Modified: Wed, 09 Apr 2025 12:19:53 GMT  
		Size: 48.9 MB (48866715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c5c117cab0461eb91526525e84d6926c905887aaf36c27359fe34a7b0a5f63d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5080947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4f49bece62cf75a0eb8d5696db1abee2412a87ebac377ec0393459b77e4620`

```dockerfile
```

-	Layers:
	-	`sha256:7f1a5582cc3920ab38eafd50617f891758da75d5f7bc94d21ee4dd6eeadc0ca0`  
		Last Modified: Wed, 09 Apr 2025 12:19:52 GMT  
		Size: 5.1 MB (5073582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b464a89917db1746e04b68755d00134e1276c43121aea89206135f5f0bef1a`  
		Last Modified: Wed, 09 Apr 2025 12:19:52 GMT  
		Size: 7.4 KB (7365 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:aae27cd5c9d838fe0de9caf5180da6f2eadc1bf161ea9c3a77b36c65f34c78fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87608326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b285272a2417801b1c4c381a2cdded7263511d6f46ce6214346c9fdb54cd74b`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174dd04251589e381fa1e70743cfe3191b94d8402a613012606a57ed34a68108`  
		Last Modified: Wed, 09 Apr 2025 06:10:17 GMT  
		Size: 13.5 MB (13455387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a904ada7ef806ede82f5e0601df0e536eb15f82a961f6d97b71a72e4e6feb539`  
		Last Modified: Wed, 09 Apr 2025 13:58:59 GMT  
		Size: 45.3 MB (45305981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7922059e6ebc5c3ba71659c1709c08e01f5c7598c2b2b52d42e25152c8bed5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3128a7a19aa3094d9c67ed1fd9e3280df2020ec6c1c7a457069b485936ad6714`

```dockerfile
```

-	Layers:
	-	`sha256:79eb9309bc05fcbb7b80fd81a186e0ed098c3aa71f4d7920ae0394a10acf064b`  
		Last Modified: Wed, 09 Apr 2025 13:58:57 GMT  
		Size: 5.1 MB (5079476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:651a1a2fd9ff312d52f671fc154704b0bd1a811c406c42cee15c35a7f16304d8`  
		Last Modified: Wed, 09 Apr 2025 13:58:57 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6ef6131df961664a8a4c4e2cdde9512735b1f9b3ca0456701bcdb77be8ba5cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100664619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b55a40e8aa70431fe8f18fffffad5d6b6cd5fe3266ad4c48c6bc452ab018895`
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
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1c8bb3d99b4917c8ba06f9646b55d42ffc7d868b7d8010468bba3dabffc300`  
		Last Modified: Wed, 09 Apr 2025 04:29:36 GMT  
		Size: 16.0 MB (15951765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c952ba13ea9a62012e20c05b5d9dd20b6885153704ecbf859c6fc8f1f3da578`  
		Last Modified: Wed, 09 Apr 2025 07:37:17 GMT  
		Size: 50.4 MB (50371987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fcc622e77f1d0dc2a7211650359fd7fa87569bb7a08e056af49bde7018f5bb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e00bf329a4cc925a55dc0d2c74718d9ee242db253b7e81e8b87f35aedd61b7`

```dockerfile
```

-	Layers:
	-	`sha256:923dc08ebceafdd5690a00b2db49d6c702a5e937e72c2781919ca3258f592639`  
		Last Modified: Wed, 09 Apr 2025 07:37:15 GMT  
		Size: 5.1 MB (5079974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68fa183ba65752e0d0dbec5186c21cfbef662337b154c074feb6377b02b7c9f2`  
		Last Modified: Wed, 09 Apr 2025 07:37:15 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b2f5ad8c2e20001842357787bf9f0903280079a6e2e5eb2a8098a0309ec64f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99075030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af73b1033d9a3cd226b151012ecae270970f21572680517cbbfef27a467b476`
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
ADD file:ef7c97f5dd8d665aae899afe52c54f7acaf71fa51e9d7f26e13ed6073141c666 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ba2f284f7444fb0b78fa804d74c44dee4b397610267539e4a6e9c41ae41e06a1`  
		Last Modified: Tue, 08 Apr 2025 11:54:06 GMT  
		Size: 30.9 MB (30943202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5f313a1c6dbd13467e879d320aa46ad9e7a8abb607e47f5fcd4fe19d104810`  
		Last Modified: Wed, 09 Apr 2025 05:18:21 GMT  
		Size: 14.3 MB (14327361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb39271530bef5884da7d90dd3fff241bde4855d8423132d8efa1eadcc6ee74`  
		Last Modified: Wed, 09 Apr 2025 08:41:09 GMT  
		Size: 53.8 MB (53804467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:32fd2267fc72a93a45d43451f2497f05b0b52fe610ccded4ff7b1c592a72f904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b84f586b86e0756b86ef195e03ad6d5e99e39e0f91d4282f516d6c8623a84f1`

```dockerfile
```

-	Layers:
	-	`sha256:add426d534c0b380d789cc49a1256a6014663ef37dc151a585c814ae0f3b6817`  
		Last Modified: Wed, 09 Apr 2025 08:41:01 GMT  
		Size: 5.1 MB (5062808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb06909d550d25b4ee250835ee3472df4683fb3b2d9957ed9e21382ed61c80ac`  
		Last Modified: Wed, 09 Apr 2025 08:41:00 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:73b27122bfe3e20d77f46787bd1203d029dec1c00deb7b4dca2087fa77bccba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91638151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d31f62e095da590d8335b25f9d6ef74600fb02101eddd88871a47e9be78602d`
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
ADD file:8f287f40ca940c9bd87c8706751f5f1c5bbd0a83fd75f7d938832b226fdb936d in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5722f32c6281fa87f1e5f7ebe307864b50aa95a116496a205ce47478bc9b52c`  
		Last Modified: Tue, 08 Apr 2025 11:54:12 GMT  
		Size: 30.0 MB (29956206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e704885473e9016559440f7dd673fed8248fa9c173ce47190caab5bc5ba71e91`  
		Last Modified: Wed, 09 Apr 2025 04:12:34 GMT  
		Size: 14.9 MB (14937511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13864cd5d972733632aa5cddaa489533b9cfbdc5130cf29bbcf6bffbc8be43d1`  
		Last Modified: Wed, 09 Apr 2025 07:09:02 GMT  
		Size: 46.7 MB (46744434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b18ab90d7ef6d627c57e6aee60877577a1504dbf9c5ef1c6e86332ffeee24678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc55cf6e159912dc1597ff97b572e3d5cbe73531edcd15d0b599bfabbfe81c2`

```dockerfile
```

-	Layers:
	-	`sha256:2257962eb36827dfad0c53756936c73f61e6a6298e09ab0bf830434825f4e54f`  
		Last Modified: Wed, 09 Apr 2025 07:09:01 GMT  
		Size: 5.1 MB (5074616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a0014b68f13d6070b10e98a0b2809cf1f4a6d91b6c6e0a964428c4fddb076ae`  
		Last Modified: Wed, 09 Apr 2025 07:09:01 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json
