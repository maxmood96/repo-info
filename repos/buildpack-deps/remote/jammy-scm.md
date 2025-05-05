## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:af456fe30f2f222d4cf306048db897e3fc8f735f4783ddcd502ffeb17887fc7f
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
$ docker pull buildpack-deps@sha256:f70fad5e99965020412f5374f74bab282a60e0ced7d9d226b889254d0026080a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76121949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ed4d6e1df5d3603b2f4a6a685508424435d588aaed37222e8fd6934821c553`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a371f1ee9522de0fd813c4772011abcbcdbb8f39e3cf1285f265032957183988`  
		Last Modified: Mon, 05 May 2025 16:34:22 GMT  
		Size: 7.1 MB (7102973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a55ee81f5cef0743ed75fca3b6a0943e54ae23976e64bbf789958a5fd3db77`  
		Last Modified: Mon, 05 May 2025 17:02:09 GMT  
		Size: 39.5 MB (39486362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9662128c9bb5942c03c3e6bdee5e03cadd1df333dbab994740caf5a89b8d22c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5609674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c907d967887864df985fbef3eb0fd9a3bd6bd826edaf434ad51b5a854014281`

```dockerfile
```

-	Layers:
	-	`sha256:7484b64ee49495b387981b022ad0c5fe5d01a1ded12ebddebf4b555fffb74bfb`  
		Last Modified: Mon, 05 May 2025 17:02:09 GMT  
		Size: 5.6 MB (5602351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddae7edd7956ada627cb0676d360219d984e98069fe51eb7791a3867f4e4210c`  
		Last Modified: Mon, 05 May 2025 17:02:09 GMT  
		Size: 7.3 KB (7323 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c512d02f5fb69236c26e0b33c688e0606b6719e2729007c8a5714c2fae92beb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75892764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bae2fd176afbba77dbc95fae8a447c0f97eaa63615b64e849d556e5d9ac7ec7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:0644b965bac173b3de427d73c19d20e4fb61d50785a17a303e350f86b7865f26 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bbd8385a156b4afe216eb6b84f86bc7178bca4ab42ae42bb98f3576ca9f4e17a`  
		Last Modified: Mon, 28 Apr 2025 10:43:57 GMT  
		Size: 26.6 MB (26640827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f265b1708f1af87f345085b8dd29b89823e9decbf63f3843e3c2f7e1c2db94`  
		Last Modified: Mon, 05 May 2025 16:34:29 GMT  
		Size: 7.0 MB (7007272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5f92d828f7e3e6d84951f6107620af98602a2f2f6bf366f2e077735cb4145e`  
		Last Modified: Mon, 05 May 2025 17:02:13 GMT  
		Size: 42.2 MB (42244665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:177231220d5807ba2bfb6677e562c403ce4e35a03af3db9c10c2bd4b59e7889e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442b103ffd168a6324bf11ef5f5fab51e83b22a22738f3f581aeaea53a9eadb7`

```dockerfile
```

-	Layers:
	-	`sha256:4ba5c726a8350641b24ea8a400e8db19e8d53a4c014f62ecc2b3e1d05b9d1095`  
		Last Modified: Mon, 05 May 2025 17:02:12 GMT  
		Size: 5.6 MB (5603631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c82fa103a4f398546374c01e83d5726b42423046afa579d995f459215d9793`  
		Last Modified: Mon, 05 May 2025 17:02:12 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5dd56d3b7a19a6a7ada7c4320544c0c989df29d509ca44c49b3a43ad2d41c975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73789762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bcce2d3a30e027251122aa5d466b44a208d167a35d371a6f407ef28c1dcb19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d148e2bd6a66aac817f1bf6f5776ba3feb2e4f521badef764b6c1ac175ef1a69`  
		Last Modified: Wed, 09 Apr 2025 13:58:05 GMT  
		Size: 39.4 MB (39386567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e2988d9c2f90a2a9ff6d0b3e551144197c774d44d979893e905df64f7b82689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5616149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e761942f634e0b18aafa2a417bb2c0992a789cdf0c6cd522d774ad0c74c8ac`

```dockerfile
```

-	Layers:
	-	`sha256:9d2a455722917e255d116e5a52067495aaee55040cb2c76baac82f47dd746c18`  
		Last Modified: Wed, 09 Apr 2025 13:58:04 GMT  
		Size: 5.6 MB (5608745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee38bd1d75c9964dfafede8148035b9d27bb995f24b2a854e1fa77225658670`  
		Last Modified: Wed, 09 Apr 2025 13:58:03 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:28c5d9ac749d4efee4b2218dbfa2d700c30583d14e63d078558cc80f2f48dc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86390955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3654095a4bbb17daf8f5ea58c37c103bef61e11df9afad89199fed63e828a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5758b64feb475315648569dcc19f6eed14e004ac6509fc2bbb6103a5d796c3`  
		Last Modified: Mon, 05 May 2025 16:34:42 GMT  
		Size: 8.2 MB (8180679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3889a4754b0feee9a228b59fcfe165963f32939c591cde6e313e5c3f0a2993e5`  
		Last Modified: Mon, 05 May 2025 18:52:15 GMT  
		Size: 43.8 MB (43767061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3d2005e96176258d61ac6619cbcda9446164c33439e782a2b1377ad907f8a0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9240c304234b2ddcb8a11a1c7805951efffc2694eab317dbabedec857c41316a`

```dockerfile
```

-	Layers:
	-	`sha256:21d3b6d092252a521bb7303bbd9b652e23d84d9ba8aa82ccdd0dd4c374d9ff53`  
		Last Modified: Mon, 05 May 2025 18:52:14 GMT  
		Size: 5.6 MB (5610019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8264ecb9927361c329abcb494d85864a2700711ae11e4888ba9284fe51be2a74`  
		Last Modified: Mon, 05 May 2025 18:52:13 GMT  
		Size: 7.4 KB (7355 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ccd68f51eb2da4e2085772ec9a7b1612490687162ad80dcabd5ffe45877db135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76458582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b20eb68ea1ba8192c8574d69b2a4591bbe2dae39bb823b6c71b897d6cb5674`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:a912be2a3089b5a563b27ae9282741b713c9ece03916c09152cea320960e7562 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:47a929027d1fdf0b4cd10889cdea1d02472669c913e59a827d925ddc426e60b6`  
		Last Modified: Mon, 28 Apr 2025 10:44:10 GMT  
		Size: 27.0 MB (27039778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a659e4c4181f5ed1c99b778be6557f6506e560b5c7fbdc1c6c9e734912d6bb34`  
		Last Modified: Mon, 05 May 2025 16:36:33 GMT  
		Size: 7.1 MB (7115958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0226ea590af05a88ef22f461bc56c43e6f6c54c4dc9c53a2444b6a16746a684c`  
		Last Modified: Mon, 05 May 2025 17:06:47 GMT  
		Size: 42.3 MB (42302846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b1f16f8c3e4e014ba81b0d8ed614c970279f3449db4dd24ccd5b9744d9aae4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5600209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b34953f895463d030e1d79a52ae5ad0814e685f5bbbb960f696cdd38413aa8d`

```dockerfile
```

-	Layers:
	-	`sha256:368f0bcbd2f5dfb0add7965f652ee988b2ce5390c28f4e8a2c6c74926b849ee2`  
		Last Modified: Mon, 05 May 2025 17:06:42 GMT  
		Size: 5.6 MB (5592853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da05a92847a6859b6c6c62a127834227ef380d347d658e2f1787b71682aa31b7`  
		Last Modified: Mon, 05 May 2025 17:06:40 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b866ae9718a4391b64f3e05d68ba6a25d879d93671c797b5b7b1b0b38e65a91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74446757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9516f25515edd135732ce393f243b6347837d3eccb06e11dbd3ba8ef358a391c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Mon, 28 Apr 2025 10:44:16 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b49a07b4500b025709913bc7a8c4f77122cc7de6dae3a2c1373bd7d008969c2`  
		Last Modified: Mon, 05 May 2025 16:34:21 GMT  
		Size: 7.0 MB (7013627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31451ee2fbf9551525c75df18422514688cc1330494f70335266302c17324df8`  
		Last Modified: Mon, 05 May 2025 17:48:06 GMT  
		Size: 39.4 MB (39433146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:76461ab3f881c73f8c4592ed7b211f783f9f3a066eb8f25f8454752d06cfb9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5610593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16be1349f63ef03ffa0347c8f039fdbf26eb64fa21bf416d646f414185239bc5`

```dockerfile
```

-	Layers:
	-	`sha256:ef0989e6fc586f3fa6cde18b22728bdcdf12f12bbd8a477b1a1135c250b2f527`  
		Last Modified: Mon, 05 May 2025 17:48:04 GMT  
		Size: 5.6 MB (5603270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:054cc50cb6f8437c8b6858bfbc47f21acb6a474026aada81ffca853f7857df6f`  
		Last Modified: Mon, 05 May 2025 17:48:04 GMT  
		Size: 7.3 KB (7323 bytes)  
		MIME: application/vnd.in-toto+json
