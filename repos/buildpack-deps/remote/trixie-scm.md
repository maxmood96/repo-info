## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:c3df705d89055d83ef1f1af26a0cca92e753768c0d1da1e484f240f79331f391
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

### `buildpack-deps:trixie-scm` - linux; amd64

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

### `buildpack-deps:trixie-scm` - unknown; unknown

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

### `buildpack-deps:trixie-scm` - linux; arm variant v5

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

### `buildpack-deps:trixie-scm` - unknown; unknown

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

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9907fe2f8d7980756504e2503210d0af67b9a91074a326b4c17f53dcedd640d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131801495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793f5db2ee7183bdc8266cb1e8f305cdaadf7695eeeec6341c26e9a9903559f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1268bec7b6bf92bd5fc4d4120fd51b9bde5a9c50d4b8a8decb59fbe4a53da6fb`  
		Last Modified: Tue, 25 Feb 2025 01:33:55 GMT  
		Size: 43.9 MB (43903193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe307003fac8d59260832b7e5476d782c0d94c51fc746df3d40b574a8cd73406`  
		Last Modified: Tue, 25 Feb 2025 07:18:31 GMT  
		Size: 25.3 MB (25278377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd6bd387fa259196771b277c7da226c32cee7039e9a1a5ee0456db83179c99f`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 62.6 MB (62619925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:050db9df21598fd2e9caf4e5e27b21f7940dab2aede1048c584ddda75d757fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db910e083faff089d90e623e3313f958bb72c026b8668267f260bae8623539ae`

```dockerfile
```

-	Layers:
	-	`sha256:84c6ffe7bf01eeb93a53146b662fc5c68058377d02b874c637ec16f98ee0e86a`  
		Last Modified: Tue, 25 Feb 2025 14:21:38 GMT  
		Size: 7.6 MB (7601299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83b91b0c7baa2aee20b237842b224a4a37ef33e33c7d34c11c522684efe0e9e`  
		Last Modified: Tue, 25 Feb 2025 14:21:38 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c7239ed1c0cad237381738d496e98ade027fcce8ccb4c78bf9e5983a6442b05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142268923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2202c756b07b2672bd0306a805ccb34561601f77322bf561d99bdf1c337825`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4febb367456c7cd84b8043b3b3b3c93073aa9439fb54961fd46a9370758fe523`  
		Last Modified: Tue, 25 Feb 2025 01:33:49 GMT  
		Size: 47.9 MB (47858532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f249b42e8ca4f2ab0a926162c24ad19731e17ebec889633ecab6f0a37257460`  
		Last Modified: Tue, 25 Feb 2025 05:43:15 GMT  
		Size: 26.9 MB (26882202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f03309824abf50aa8e904201f7f1a31ce290f54469b02ae3362c1a5c1d7b23`  
		Last Modified: Tue, 25 Feb 2025 11:56:14 GMT  
		Size: 67.5 MB (67528189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6c72e2b6417dfa28512a340b185352d9ff07e1da9b4b85741fe3f1be934502e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7616483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6853bb24b562ba731ff11ff5ce1959c0aec391327aa7e9afbd8178a4c971dd7e`

```dockerfile
```

-	Layers:
	-	`sha256:7125150c9b210a65a1ed5b7b8f70ba72e317e443d776f8e554e8ba23e57fa802`  
		Last Modified: Tue, 25 Feb 2025 11:56:13 GMT  
		Size: 7.6 MB (7609090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4da627cdf587725b98e3e62d311c39e3c2da4b98b8819fb6610b5bd5b786ff2`  
		Last Modified: Tue, 25 Feb 2025 11:56:12 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

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

### `buildpack-deps:trixie-scm` - unknown; unknown

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

### `buildpack-deps:trixie-scm` - linux; mips64le

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

### `buildpack-deps:trixie-scm` - unknown; unknown

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

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:489cbcc42cbb74dd81fe59bdefc2602ab482ea86e21e5ee82863081dcc9cba7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (152997745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeab6381330afc1eaa6f8cf0c2f305a358c9ecae237dea7eb733b928c4392ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ea3e230c71f31965fdc8d0bdc4e71749c73ddb97789439e708ba01bec0516b7`  
		Last Modified: Tue, 25 Feb 2025 01:34:02 GMT  
		Size: 51.1 MB (51131291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7136b138a9fbadd117790fd6473b3c1516b6ff1b1b1e5e321ff71f2a2c4c08c6`  
		Last Modified: Tue, 25 Feb 2025 04:34:33 GMT  
		Size: 29.0 MB (29016584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7bb81cdfac8e52fedda82eb71511b491bce0161320904fa9a6cf3542f360d`  
		Last Modified: Tue, 25 Feb 2025 08:22:16 GMT  
		Size: 72.8 MB (72849870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1a0c5ea61bf72445ad603e3f0a919815f04bbf1ec098b1f75a6eae3e7b070b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3410f9541cb3d4948c7c851214e8ed536aa73ea920d4dce4c3e2d20932da42c`

```dockerfile
```

-	Layers:
	-	`sha256:3e79957f795f20fea9bad86264e2f07607f6ac2084ef23e267a1a58f366487dc`  
		Last Modified: Tue, 25 Feb 2025 08:22:14 GMT  
		Size: 7.6 MB (7613978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0091e9531de0f98ba4de3037729168d47136afa5c1cfeffb876dfa25074b25e0`  
		Last Modified: Tue, 25 Feb 2025 08:22:13 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

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

### `buildpack-deps:trixie-scm` - unknown; unknown

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
