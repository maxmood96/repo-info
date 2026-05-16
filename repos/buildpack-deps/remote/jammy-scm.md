## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:8c62aa36a9bc0948b661ff1979ed38aae8ea0526f7108a826af9da9385bab49b
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

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b0fe262436183de57412179b85bcdbdf57fbd2d5b7c212efac2345bd7d0a0876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76332199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11929073d5dbb1d98e17d074a9de816b2b56fb57c27241977564c0ca2bf5413d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:42:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0aeb1f8fc5f0c234e2220faa9320cdfd32528ee5a33d4b932677603206a1e8`  
		Last Modified: Fri, 15 May 2026 21:11:00 GMT  
		Size: 7.1 MB (7106733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a078f2bb490cd26302da7fde31026fbac682708b81357a1ef250612fa53782d3`  
		Last Modified: Fri, 15 May 2026 21:42:20 GMT  
		Size: 39.5 MB (39488782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:670a9ad108058938df853c7bd7d739a15944b984daf021ce35c5211c9c0c0885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5819983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a238ec3a968c959395647095563623f1aac29b224686e10147c701f95e5963`

```dockerfile
```

-	Layers:
	-	`sha256:6be345396c295992ecd68f946fc6c2ea2fc91c050ceeae61356d5ce6b4ad814b`  
		Last Modified: Fri, 15 May 2026 21:42:19 GMT  
		Size: 5.8 MB (5812702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcae4bbac1cdd7f9b48295a7cdab694add21971436532f845c1bb67ddbe50980`  
		Last Modified: Fri, 15 May 2026 21:42:19 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:885cf677c0435f8c14b093043f19473b961f9f0f8a99701e954e98025f4ffe98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76124892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73278c755ba71b0f32a9fcf51fed973c8aa34be0453fee54323e2097d74bccb3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:51:37 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:37 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:41 GMT
ADD file:1699ef25ec41cfa214b8beff2f000963a775084d9ce11ff74fa817bb458c27c3 in / 
# Sat, 09 May 2026 04:51:41 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:41:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:422dc0f0ec960f769d890f368bdf0a0ba195325ef487f5b07a4d06efaa7b2c41`  
		Last Modified: Sat, 09 May 2026 05:25:04 GMT  
		Size: 26.8 MB (26841796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957e620b1e61061910c1027253dc62e684fcc45b084a25cee92e097c48ba1013`  
		Last Modified: Fri, 15 May 2026 21:11:02 GMT  
		Size: 7.0 MB (7011093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4570887fb8811ff4b45280b29f11fcb74cab3633a779f1709fe2700c204922`  
		Last Modified: Fri, 15 May 2026 21:42:10 GMT  
		Size: 42.3 MB (42272003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1b43cb799b07a66ed0b4868cb6c6d75805289986e92bcd7b00f28653e719e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2d541335a9b4268d8a429295c43a37c9464930f207b68e3f908e62e6bea699`

```dockerfile
```

-	Layers:
	-	`sha256:91cb772ed4601688b2875ad877f2f788e295c5ac15dc023c4411acffa9a1ab6e`  
		Last Modified: Fri, 15 May 2026 21:42:09 GMT  
		Size: 5.8 MB (5813982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f367ab56cee065a42f292836c1249ab2273118d660c3f7fb4e83e998aa95c48`  
		Last Modified: Fri, 15 May 2026 21:42:09 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fb9f166195c1693641e74df807e79288e7d6ba995e62ba37f458cd2489300e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74079586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc68091023ca4c1c48a9d3ab00b459b6d489c64ef2354a53cf2bc8e368b77d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3443b99bfd9ba84dc508ac1e64f30df03b505f391957f7bb18008ddaa77c1`  
		Last Modified: Fri, 15 May 2026 21:11:07 GMT  
		Size: 7.1 MB (7061756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383b78cb0f0ad0176746ccce65e6ff104cd291e41eb5a5e430f6d695ef9d0b6e`  
		Last Modified: Fri, 15 May 2026 21:42:46 GMT  
		Size: 39.4 MB (39411207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:830bbf7584f79dcc84148d433c188b218b9532ce92f3dff9d5f058d7d0f1c950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5826457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bc928be5b15ae42a6b41e651d80794b45e3e5f08641fba55cbd90b0ff82592`

```dockerfile
```

-	Layers:
	-	`sha256:ad6e6aa44ef99e2660ba4a3271b3e92bff3601a8d5562a1cda20b95d799da40a`  
		Last Modified: Fri, 15 May 2026 21:42:45 GMT  
		Size: 5.8 MB (5819096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85dae0a74eb66ae08dea31ca0fcac934797ffc04159c826685794eac1c0f58a8`  
		Last Modified: Fri, 15 May 2026 21:42:45 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bc15c88838ff37425ac3055b0dabdacb3fb978883ec761196a55a97b40104c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86610027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03163f8b674cf11433f15f4519867bdc2b8a3056210fc3871911309872ec31e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:56:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92df60d93ea7ba54145745adaeba4ff8f95b06acfd1fd21b54527b08b1549166`  
		Last Modified: Fri, 15 May 2026 21:10:26 GMT  
		Size: 8.2 MB (8187802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e2910eb3e418d31a2ad934c438e2363b6894322b78cc2948f8c25e84e0013f`  
		Last Modified: Fri, 15 May 2026 21:56:33 GMT  
		Size: 43.8 MB (43775505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c7cbea4b87d67b65e5ccdc0a88e9fbdfdd960a6b7df5d2675f859a896d09543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b24676c4c21e334c06ff663496bb5489c666165a3d28853e100d3b8dd05142f`

```dockerfile
```

-	Layers:
	-	`sha256:5e0c43c6218d6c99c12144aa964118fd18b6f8ba8077d0049cb62fed907afc6d`  
		Last Modified: Fri, 15 May 2026 21:56:32 GMT  
		Size: 5.8 MB (5820546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea43072e3674bda3d1df58e78642ffbbdc47d0d85bec0fa19b7be22b67c9e76`  
		Last Modified: Fri, 15 May 2026 21:56:31 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c98adebb61dd9dd7795bc9fc49fe4100b0dfe25a87bdd1b8e9e9d02bfa1f2f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76666913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b945a7dcee5c5fd6f8b40fd9382cb85a5de9bc412b4e0adebeb2771fa5ce1b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 10:46:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 10:46:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 10:46:31 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 10:47:09 GMT
ADD file:7ae2692e9ead2e53576d53cdb893209a70fe6f0a62ff35308c9fe5c855c10e94 in / 
# Fri, 10 Apr 2026 10:47:13 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 16:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Apr 2026 15:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:116177a8ef78c1de97a5262550388dc00d9881fcb4c367e06e4e52bbdb5a832b`  
		Last Modified: Fri, 10 Apr 2026 11:01:22 GMT  
		Size: 27.2 MB (27240349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74ddabbfbd66006e6d36799950a3c7e93532654f0837cde6fe2521d8c52ee83`  
		Last Modified: Thu, 16 Apr 2026 16:41:28 GMT  
		Size: 7.1 MB (7118338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144adc2ee8321b5f81e7424187eca2a7ced16978dd9f89b2dca14b113fd47f46`  
		Last Modified: Fri, 17 Apr 2026 15:20:34 GMT  
		Size: 42.3 MB (42308226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f16094003f760a9e9fc891233ecea3b14dd22911afa378652b1408493995d8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49466e97547cde357a1d665a1001a5ed2cf1702a8122d61e8ba03f35a904ce63`

```dockerfile
```

-	Layers:
	-	`sha256:2976657b94217663302085dba94a516dc6f9f639a84fb8c269ecfbc79643a2aa`  
		Last Modified: Fri, 17 Apr 2026 15:20:28 GMT  
		Size: 5.8 MB (5803084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aed84cbfc42961307e4c9484b6f941b5d93310180763ef10f9b198ed9c85b62`  
		Last Modified: Fri, 17 Apr 2026 15:20:27 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f8188f3f3fe96b35f93657123a6518d50dcc1f102d222a6851913e6956d0d314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74641320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becf6b7e50bf8c6be379fcacf7ddc8c56d0c58f72c471eccca54fa84201f79f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:41:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d78cbe544454213adb2a0a4ba71fd136f33191159e4da5a835e672c6cb14f90`  
		Last Modified: Fri, 15 May 2026 21:12:47 GMT  
		Size: 7.0 MB (7020058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bd45bbf55b63390cb3b04f33ae88a8ade1be53931b0152ebf550f6e7b199ae`  
		Last Modified: Fri, 15 May 2026 21:41:47 GMT  
		Size: 39.4 MB (39418957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d2378d95479acde33b92ae76985b4b0d97af12b353aa3bea2818f626df33b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5fbddc473fd0f858d32ee7639c87b7db99ca46835c7c6ac7d0f180397b1644`

```dockerfile
```

-	Layers:
	-	`sha256:9993a3401323c34db6d8e8fa4194826fdb522aa06cd301a210b64803ac748bc2`  
		Last Modified: Fri, 15 May 2026 21:41:46 GMT  
		Size: 5.8 MB (5813621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b1aa1f02bf4687b4b7bb2fd9cefe23c64129401ab5769e8fdc3af7c972a612`  
		Last Modified: Fri, 15 May 2026 21:41:46 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json
