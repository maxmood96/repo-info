## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:79eed6378665d91846b6e5c5f7525ddd8c4c8c2116158ca78d8ed89f69b91317
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:662b99f67e224e6ac22c92c3c0321e83258f65b966c68b571283e9af4e33b9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140827077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2149fe105e28674924fe90dab77901075742c1916efd804dc62e50fc8efc6225`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b312498eaedc471a9ee574437ddcf442ef14eadb9305c2ea1c843f2af922d473`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 47.5 MB (47513473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307579de8afb457f38a2a818765fbf595dc7bca2e9022efb29cd9a1e5c6b6b9d`  
		Last Modified: Mon, 17 Mar 2025 23:14:00 GMT  
		Size: 26.2 MB (26230971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8328f6595bc164f14568dbbd4ea22c25dd2666776b4b2c83c26194060e04be`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 67.1 MB (67082633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:977a1d6dc644e37314fc72f6c03e49927a2e5e731fa01260ce84e35e5ee4410b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7580737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175e92a6fe7126267a372721d169cacc119407c7473a8949887767f9b99cb14c`

```dockerfile
```

-	Layers:
	-	`sha256:aac6961803cd1c5aa867a2dd6d65a3c0b025cd1143d6069f29c34196f38d0bed`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 7.6 MB (7573423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193fe9e0e3d258110df44697005aa7f4de7fe3d776263d9c984195e423438299`  
		Last Modified: Tue, 18 Mar 2025 00:18:58 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:acb8af149400ddd9742304bdbf51e6dec7ebd1e865e9850323f870a2697fd8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135459791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace13e5a4b372e7ba795a40834f2b10f04804ee2fe2c39d25ceb5442c5584468`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:43d6e898d3a5beca16572b1a502b9433116891c583ecdbd0b66dccfd8af9e4fe`  
		Last Modified: Mon, 17 Mar 2025 22:21:05 GMT  
		Size: 45.7 MB (45737144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023a0e893b154d7d5e322d742da1db8537753d0cf777b8cb73ca869670a0c807`  
		Last Modified: Tue, 18 Mar 2025 03:08:29 GMT  
		Size: 25.0 MB (24957496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86725112f5149cb61d854be49fdee119e7f61817be65303ade6d8bf0230a955`  
		Last Modified: Tue, 18 Mar 2025 05:18:53 GMT  
		Size: 64.8 MB (64765151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d99b1adbf2068b7e2f636d834693ba9e86ef1176e89f80dce106ee883d7c585d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7587105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bc16c24780fd72a8b6e04837ff32556ff3d6a31350e7074fbe94a3d5d8b5f7`

```dockerfile
```

-	Layers:
	-	`sha256:37a0188c5940d5d3909380e614c14b52b799f1ab3244a759165f82e4d8fc70c3`  
		Last Modified: Tue, 18 Mar 2025 05:18:51 GMT  
		Size: 7.6 MB (7579732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d51ea33a0aa8c1438a73dfc8fa29d19091b3d653a31b40f63d61a88f22195db`  
		Last Modified: Tue, 18 Mar 2025 05:18:50 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:747cb91b81f509c576e463b522f42cac115e0df15198fe9a7c5d044931f5b067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130344806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b7ca2d142d7fc51469d5bfcd189d5716173e68dd475489baeec817b255e2ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:344116a397737c11dc2811d8baccf64c6e4150467542a11a0c5572ed1b6038c9`  
		Last Modified: Mon, 17 Mar 2025 22:21:24 GMT  
		Size: 43.9 MB (43934171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d1689e965c6a71d99b5f45c9a0e5483f83d9ca9f7db740f0b984c85e463e9c`  
		Last Modified: Tue, 18 Mar 2025 07:20:09 GMT  
		Size: 24.1 MB (24112343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6fc84037c86bb908f0e3c32b087f23cd1e04e67f611071e98457da630f4516`  
		Last Modified: Tue, 18 Mar 2025 15:33:45 GMT  
		Size: 62.3 MB (62298292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4d1016260aca559515a7ad5f5c8041d72a0588d94afde858cfd9ceaa07c7a6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7580650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48f3e4028fb3fe26a4c9b884bab48ccc2bb5f36241fe9677ef4e070a06e7269`

```dockerfile
```

-	Layers:
	-	`sha256:2c81f59ea237c95eb0aa21c2d5fd523bbcf9c23f247315fa04fab48518277ddc`  
		Last Modified: Tue, 18 Mar 2025 15:33:44 GMT  
		Size: 7.6 MB (7573276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e125d94fa36eea27d2e9d50b33ee95813afae5b68b0db0886e71bc901f72a53b`  
		Last Modified: Tue, 18 Mar 2025 15:33:43 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4f17545335e3e20ce6df85aba7ed953de40eb90f59371d12efa7ce88a219a7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140707334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4251c1fe545eeefe0fa85f2258511486a137a79dd6519245a372dcdcb04d0d08`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f094fa2db11dac08419411aeaf2d9c561365872610ec591de05f23f2fadff3bd`  
		Last Modified: Mon, 17 Mar 2025 22:19:09 GMT  
		Size: 47.9 MB (47886359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84822f7d47020ba3b073f3f8ebb18e27a90b8e25a519c2b492131234a060ca6`  
		Last Modified: Tue, 18 Mar 2025 04:59:07 GMT  
		Size: 25.7 MB (25690430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcae46c8b749bfef6c1f2eaab2853deec3a02eb1815b00768b45dd741aa09214`  
		Last Modified: Tue, 18 Mar 2025 13:19:59 GMT  
		Size: 67.1 MB (67130545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1dbf27f4bb97f58302f208897fe01422f9d410c08680afb463b4996f9b833eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7588478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a0cba9e18d62bd05efa5cc9a7ad58ee5efb4cc250be240a0d26151091a450e`

```dockerfile
```

-	Layers:
	-	`sha256:9c6d874d43cd83324e7791e86fc62e6a9056709fc66a2428c83e2a320e848c40`  
		Last Modified: Tue, 18 Mar 2025 13:19:58 GMT  
		Size: 7.6 MB (7581085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:272ca11343202a357fb8fb9dcc1a3e234f278c4c60a09ea7523147da85497cdc`  
		Last Modified: Tue, 18 Mar 2025 13:19:57 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7eb53031babd7fe1be6f99c85ad6011ddc763e90784cf2336f24c392d260cf44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145262617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504cac4029ea96b97903fc04aebed70d1f39de4cdccc94b5bee4526f159c496b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7f35c21acae2ef6b77873a46c174f1da0b28fbc4ea787b7f5bb3bd79c145883f`  
		Last Modified: Mon, 17 Mar 2025 22:18:02 GMT  
		Size: 48.8 MB (48831362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2417ac61f214f6f239ee6ce6ccf4e9a29aead09dd8338aeca7ca8645adc7a0d3`  
		Last Modified: Mon, 17 Mar 2025 23:33:10 GMT  
		Size: 27.4 MB (27380417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825d4e842f60fe8bed8af22c7d26bd8c640142408d7c59da73f8a94bc3c79992`  
		Last Modified: Tue, 18 Mar 2025 00:19:28 GMT  
		Size: 69.1 MB (69050838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed176c73e43ae031741d5307139f6f3edd7fe72358b0314111ee26d76582d5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7576134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4984e00b5f77503b242567b0a2254f59d18b5ccf080c1d28eb279edc6d7a39e`

```dockerfile
```

-	Layers:
	-	`sha256:e0c346fbec4d5622463fe88fb740816fd92165ccfe37d2ebe63ae1edc439b515`  
		Last Modified: Tue, 18 Mar 2025 00:19:25 GMT  
		Size: 7.6 MB (7568842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0109b8cb99d24293e63787c51171d48d18a63f0255d31a0e835c226fdbc8abbd`  
		Last Modified: Tue, 18 Mar 2025 00:19:25 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:edbea362dd93e91cca5dd14b3ec7442bc7ae4c915ac18f2952a67c9184eb8940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141818528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fd5a7dc7e0f7f44463ef6b49ee46ed28ad37304fa952a7a91a2f758e1a55c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3018c8b96b9ba22f17940c42dddfbfef3058b787c07b7ccd94c52adb65aa552`  
		Last Modified: Tue, 25 Feb 2025 01:33:17 GMT  
		Size: 47.7 MB (47684440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d568a834d28f352d6c862c921a5a1525795a3ba966e684f287dc047fc5a62e6a`  
		Last Modified: Tue, 25 Feb 2025 20:40:18 GMT  
		Size: 27.5 MB (27466813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30dd389c4f7f75e0238dc8b5aaa6b88b1024d42ca2aa910e605d4197c6c892`  
		Last Modified: Wed, 26 Feb 2025 02:28:14 GMT  
		Size: 66.7 MB (66667275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a8c9fc52b92269c7d7b7aa24a07de06b692927261926512f6522fbb31a6192e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db05ff5f9d0f8862b98d1c01e2f7a7920741cf817d558d9bb98f6810c074b7a`

```dockerfile
```

-	Layers:
	-	`sha256:7ff109c6257be225cbb0af031db400e94cdb4d025f384a6017e2274ad5cc07ba`  
		Last Modified: Wed, 26 Feb 2025 02:28:07 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b6f05e463fa80a4ae343275d4c2751f2c51bf417d77b4bf9c7d5ac60108f239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151380191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b8310e8d55fafb34de32cf8a234aa8dc15108b6196e6e5fb5ea9c58b9f8f87`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:895a5f19953067f7b5f8d8697fd370f37def792e6b968ea95a15dd11594bc1a6`  
		Last Modified: Mon, 17 Mar 2025 22:20:07 GMT  
		Size: 51.2 MB (51162729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aeaa0f265ddf4206f6d845d5494e3733ac72919e3d0329859f2ce1f44f19c11`  
		Last Modified: Mon, 17 Mar 2025 23:57:42 GMT  
		Size: 27.8 MB (27773366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f105bd00bb4fe66e0c28648fd8c55c5c78baf7508cbe6b000b0ec61ceebf10`  
		Last Modified: Tue, 18 Mar 2025 07:15:25 GMT  
		Size: 72.4 MB (72444096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:afc324bc504138af8937c6e3ffc69b3af691d30dc690282dccc1cebf078d6bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7593277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b241aaa7f0189ce6b619c3d6ca54bd4577244b9abe318e8cb4dff860699594d`

```dockerfile
```

-	Layers:
	-	`sha256:7e14fbb15393330ed6f52f83cd81f8bdea60c3df6042b0ab62960dd6f6f2c4bd`  
		Last Modified: Tue, 18 Mar 2025 07:15:23 GMT  
		Size: 7.6 MB (7585931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98092041515f6b50d72455ee11f312f591a4d42c0c7dab09fc18e7013d41b725`  
		Last Modified: Tue, 18 Mar 2025 07:15:22 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:40b7ecabf49de5be9a42ad4fcc940270736fd6785c7dac6ba82c3f00ca13daa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143064756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b40a97ff036f4920fecbbec7c12969fe729f4bc7f627724b5801d74303f49dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d25d70cc33acfbb261e54e41a50ee310f48343b555ff5a724ee79cad7214fbf`  
		Last Modified: Mon, 17 Mar 2025 22:51:24 GMT  
		Size: 47.5 MB (47548830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74e201480524a9e7f1671230b2cae3b456d6d6a91a8a4a2b07140f308c08518`  
		Last Modified: Tue, 18 Mar 2025 02:48:54 GMT  
		Size: 27.4 MB (27392489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe56110fe210f7a220bd33778fbc68a1d3b26729f0b2ea2d7d03b68e494f18f4`  
		Last Modified: Tue, 18 Mar 2025 05:57:55 GMT  
		Size: 68.1 MB (68123437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2d51928db5934796361047b5166e4d0d5059efadcdb47356d6a56af3cbaf1728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7587215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1beafed3e0c9cca8d0cb38c6a608428f2afe2ab9b07ccfccf09378dd2402c5bd`

```dockerfile
```

-	Layers:
	-	`sha256:ef2889a98845aa09d1e4258683ae3a3a47a06af5fe5170ad9417fb489e45416d`  
		Last Modified: Tue, 18 Mar 2025 05:57:54 GMT  
		Size: 7.6 MB (7579901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f1ef2ebcb4d9825d46a5c2d28cef4f0e2c235b59c6d5784bd1c81fb0b99102`  
		Last Modified: Tue, 18 Mar 2025 05:57:54 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
