## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:34ff5843d517222f4da44124cac4a1c6ddf1c92a34588ca9cf9e3ddb60bc6880
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6d5ff44bed08ece9e7acb31c775e6b08c87abc393a2c44904123d482cc064153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124313665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2137ee82057ea80944c59e56d4f29671834bfcde357cf0c4d6009b5050830dbb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d9f854f908f28a433fd2d5b08b5e68ee58c9ec953dac233ca6864ced59f24`  
		Last Modified: Tue, 07 Apr 2026 01:47:01 GMT  
		Size: 15.8 MB (15790676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14034e66ee3f8bcfd399019612c7f333cc777166161c3dee1a945ac1f0659fd6`  
		Last Modified: Tue, 07 Apr 2026 02:43:11 GMT  
		Size: 54.8 MB (54760196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:23c713cc5d2995c1b6bb73284a04bad35d1a1ac5624dba2e92d9c4ec33393d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7928693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccaf0afab98c077fd36b881425d8eb21c9802bd16073377eb3758d83277868e`

```dockerfile
```

-	Layers:
	-	`sha256:b271e2fe9c7a0f10b03df56a8251722b611ea5d16a60226e68b2626f4b6a5019`  
		Last Modified: Tue, 07 Apr 2026 02:43:09 GMT  
		Size: 7.9 MB (7921377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4c09258974b11a13599c962ad40df96d547c9dff90b80ec19f7249e94419cd8`  
		Last Modified: Tue, 07 Apr 2026 02:43:09 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0d0319c2e0ba4ea8dabb098ed40c2a8359de2dcc3323ddcecbd2e1e34eae5257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114599979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91aa2266a92bc3090b254ee50a31604057ca6d4de6e472de350de5c68662606`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:00:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:49:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dc8695d526078f14ae00d8def0c6b77226df91b02937f7fe93806b494d0eed07`  
		Last Modified: Tue, 07 Apr 2026 00:59:40 GMT  
		Size: 49.1 MB (49053930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2f7a30a3127c8f109eb33c9b6e0a069dc1bbaf940f09c9ad55a2749c25bb59`  
		Last Modified: Tue, 07 Apr 2026 02:00:52 GMT  
		Size: 14.9 MB (14905095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4649005b124b78e09f68f36f64106a1bba3934081637a27e5d71125cf525a33`  
		Last Modified: Tue, 07 Apr 2026 03:49:27 GMT  
		Size: 50.6 MB (50640954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c40f8f8c50e4768e0f6c0cc74c0819075394972c5bd5b564d7ab3f2c15f0f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7930159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34aac326b002fd4c78bc373a52e30d4f5775d251011b120e18f8bd2bfa3cbdd`

```dockerfile
```

-	Layers:
	-	`sha256:b0173389048f6e270f1c4a0f2dcc4465b44b05b70e60bf850a3a1ff90429c0a4`  
		Last Modified: Tue, 07 Apr 2026 03:49:26 GMT  
		Size: 7.9 MB (7922779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a561c37c866431b53094f8e51546614625eec16c8102b4bcbda75c410eca88d`  
		Last Modified: Tue, 07 Apr 2026 03:49:25 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cad2d911bc59c26d58ddee5e212b76af61e68736a2bdd5a088bbd81eb87e1caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122897151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8e0c1400d3739df29f123c00a0a5e58c76e413fb00a7b42d05ba20863ab33e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:50:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:53:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345eb533c7aeb250dbac747a6aa1b325697577f8ad9955a623ef30caa4570d0e`  
		Last Modified: Tue, 07 Apr 2026 01:50:17 GMT  
		Size: 15.8 MB (15774862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee75a3b1c8d866e1824aa2b7c94bd00f1b85e31431f049e7c8d6baabcf7a5a`  
		Last Modified: Tue, 07 Apr 2026 02:53:49 GMT  
		Size: 54.9 MB (54874674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b7b19b85c3f2c5aa888d3483aa969005d089d9a48ad4acac90220a47acab48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7934506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004658285a347e4c7a0be9ec1f48c2336f27d051c61bcd46b1a1198c542b5d3e`

```dockerfile
```

-	Layers:
	-	`sha256:3424b41ff689877589cd1b88560e213ba3f0a63605515c8ded1d4efe090d3955`  
		Last Modified: Tue, 07 Apr 2026 02:53:48 GMT  
		Size: 7.9 MB (7927111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceeffdc86a6c3c04203d59b966a5db95d03e26c26c9fa907899debd421643aa9`  
		Last Modified: Tue, 07 Apr 2026 02:53:48 GMT  
		Size: 7.4 KB (7395 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:05e4f136ba0bb9de16677355e7479dcb4f7c881c19930d619f5323f7d3e04560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127056746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b6d19cdb33eadee9b7d2eba0b83fec1568249a354ff91b5320282a4b20a3f6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7d7ea2b68c41d012b622a11d60c4b7330f09ed012ac9774c3894afce154803`  
		Last Modified: Tue, 07 Apr 2026 01:46:11 GMT  
		Size: 16.3 MB (16295659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354a70b77dc85f405fa11ace8b407313b02fa39bd8320ba0a6a1e2b1c856fb04`  
		Last Modified: Tue, 07 Apr 2026 02:41:03 GMT  
		Size: 56.1 MB (56058498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b87ee5ebad38beea28197f48c032128257a37f6910f9c9d1fb990c4dce4ad92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef88b15626c7fd33e2cfa848981a4936b5fcc3737ad179fd43010d500b1c124`

```dockerfile
```

-	Layers:
	-	`sha256:a5b3312e431a54bf8b197a4ea81f88dce61efa19b9d9796f5234488c3207a7f5`  
		Last Modified: Tue, 07 Apr 2026 02:41:02 GMT  
		Size: 7.9 MB (7916947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06d829b6d2de39805e99ba77ebe5ae497e940a254d5265eb967875d84361374`  
		Last Modified: Tue, 07 Apr 2026 02:41:01 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
