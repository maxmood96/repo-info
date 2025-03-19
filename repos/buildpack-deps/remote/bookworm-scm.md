## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:4332a0bc58e96b1311c7d9a9c53d0a4dcc141c801869cbd555e7d7797ea95c3b
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

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b908f2087ebc17532cda0c93729bcd812ee60ae6837bfd205f6afff59b8d57d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136875458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db189da5ee9214bd00d3f763405b360cb3e9c0b42c72b5e8bb78e9a23071a0d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091eb8249475f42de217265c501e0186f0a3ea7490ef7f51458c30db91fb3cac`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 24.0 MB (24011136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255774e0027b72d2327719e78dbad5ad8c9cf446d055e45be7fc149418470bae`  
		Last Modified: Tue, 18 Mar 2025 00:18:51 GMT  
		Size: 64.4 MB (64396484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8501be6d4328863533b6e7c37574c76d5e1908d006e15fdce7604f8da65e5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7756729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7118e1169c28621706d58d94178118d0f16aa735f247beeac605ed35b7ea8467`

```dockerfile
```

-	Layers:
	-	`sha256:b67a853f4bdd1f540485530b34d4138faf4ed2a385bdade498c3aeb997673cbf`  
		Last Modified: Tue, 18 Mar 2025 00:18:50 GMT  
		Size: 7.7 MB (7749074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797c440802ffa5ba048e466752e73b98b582995120a2f897b95d2959e81ea576`  
		Last Modified: Tue, 18 Mar 2025 00:18:49 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:585bbae69e12b2a683c11164bf9aae1994a24249b01db8e50eddfbcad8f68827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130702061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359cdf713cd76963032551e36925406766ad265f1152a7a4498b7c473f894949`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92f0eecb0902c904cf1dad1c6151576f52ed736aab0bfbfdbdb998f9c806cc41`  
		Last Modified: Mon, 17 Mar 2025 22:17:13 GMT  
		Size: 46.0 MB (46004626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa782283a247b6a373c2a1bb96b43e6d698fec2513c0ac7f808329b094bcef69`  
		Last Modified: Tue, 18 Mar 2025 03:23:28 GMT  
		Size: 22.7 MB (22689640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef2233f8ee805831f1163a865bf6577beb83ad9b7b57094d092d33957478138`  
		Last Modified: Tue, 18 Mar 2025 05:16:31 GMT  
		Size: 62.0 MB (62007795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:293fd521668310a015fa1ec21d85ff01c5738b3bc9a6fa6f924bd4bf855c7bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7758355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6f6a1bee9e2a3d7f1bd88af5dceffd234a4a1dc7740feb29882846fbd4bda1`

```dockerfile
```

-	Layers:
	-	`sha256:554e4f95afa72792e99738c4e41ad89520ad2aee70fcdc8192d48bea35f286a0`  
		Last Modified: Tue, 18 Mar 2025 05:16:30 GMT  
		Size: 7.8 MB (7750632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0c5aecbdb1b5c54babdd145b691906e18195331709a9357b8ff0b000fd908f5`  
		Last Modified: Tue, 18 Mar 2025 05:16:29 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e809745f9b1bb9bfeb8fc9594131f174029da194ac2f2d7fdb9f786d2245d57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125735284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47da6764caa3314b9f25d6bc814c31d9d4e0a1b2b160bf7096299c72d5a56c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a74b4e8462942e607f293396c42ebc8b7c1b40cdfd8ff8639d0372774f66cc85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7758081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a651df6839a49b1266672007c8471d09ca114a9802261c1588fcaa0678936c9e`

```dockerfile
```

-	Layers:
	-	`sha256:d1f7aa3f1edcc93a26bd090d11dcb676adf6ac9e4f9f41fc18936321b0e1c425`  
		Last Modified: Tue, 18 Mar 2025 15:26:52 GMT  
		Size: 7.8 MB (7750359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4920947a728d8f6172125f1b2f3999e47b458db464ffdd5aa4e4a33cbd3f31c9`  
		Last Modified: Tue, 18 Mar 2025 15:26:51 GMT  
		Size: 7.7 KB (7722 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b552978120350673b7664bce9e3cf5485c7eea4201fe31f4ecf6b624eafe49b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136204995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a95a30719fd4b930a12d1ab6c74b9aa4a90d29d4d561302fd207d89cb021161`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fb18e452397680b2ab2f9b7ff72d3d2a24e519dfc765190f239d988d02b75e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7763226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83513f9abf72296128256e32f66b45084665db8dc649870b9da9ea3020a793fd`

```dockerfile
```

-	Layers:
	-	`sha256:ecb027d0d75a458468866464dddfa5c0e0e762cb61a848b2607bf201b1177a8b`  
		Last Modified: Tue, 18 Mar 2025 13:13:05 GMT  
		Size: 7.8 MB (7755479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072b4d1bb09f8086ff1e5bde3486aad9da18eb60bef7141ab1d2dea9327d4997`  
		Last Modified: Tue, 18 Mar 2025 13:13:04 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:94d3fcfe59866a9683b9c85590b2466be58dcb8314cc831a4d7fbe73ddb92d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140538719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad680aae718a5347ba22b53bd36cbc1ddb47a912a73f48bec3d5aa2648f7b612`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbfdd287e687c9f2dc0d376a6aadbacb1983900ed87870c01bf958f5ff36c993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7752782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b0bc3b4d73b7044e243bcb74092a8a4efb25c16953ca8d30da1d4a171d6d31`

```dockerfile
```

-	Layers:
	-	`sha256:79639a332a413864145b04f3c33483280ab90e612f70e85a2e38f751f2dbe9b1`  
		Last Modified: Tue, 18 Mar 2025 00:18:51 GMT  
		Size: 7.7 MB (7745154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60728a6f3915a6a0f48e08005b1a1f3c83cdc6333161da08b934bc7ab05f5329`  
		Last Modified: Tue, 18 Mar 2025 00:18:51 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0bdd8e6ce508bac2e68736efe12556e651d1677f848b577a840aee01c988c210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135660294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e9abe397b1b12575dc837b9b4120dcf1e73ef4a7a1f74c92703bd1df1cad25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:579ff6a9178b7f862c70c40b253d6f0090e7792eed3ce083de0732adfc5f4826`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 48.8 MB (48756170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc19bfe112f8e8e887df88219c2ac69098bcc8afda18a25b53168674379a8365`  
		Last Modified: Tue, 18 Mar 2025 16:33:21 GMT  
		Size: 23.6 MB (23595590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0a4688093ff24a7c0a47c52d04ce08c1411187824a95dc1fb509b4ab01c8c4`  
		Last Modified: Wed, 19 Mar 2025 05:02:22 GMT  
		Size: 63.3 MB (63308534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4407c0bc97bcd4747b49c6e6f6c4b49e488211959d2d5fde1515f5de981b68f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acd49b0877b2ab1ce2e30f6086f067f6c941a4bd3b156e9aa87bcb013e08aa3`

```dockerfile
```

-	Layers:
	-	`sha256:85925e88d4207fafa4538f06057702188d56c177bb6f2981cbfd0f00f9735093`  
		Last Modified: Wed, 19 Mar 2025 05:02:15 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:26a9880e0f621718be7d2ecb02cf2ef7d5a86ffcde5886b8ce71f6099f3cc9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147800208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf2fd883045f4606b33924a25a0e53f7148af9126bfc669c37b4fd9c0a5882b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3219f8cada3f1c641a91887b1112d0699cc708ea02d9c8f85a77e08659008bf`  
		Last Modified: Tue, 18 Mar 2025 07:04:49 GMT  
		Size: 69.8 MB (69844086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3690699543176652c6c080d22b8419f2da19d1f031068d32a5b772199798647a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4c4a0122cf189845d821bd88f6bcbc42bca629970429f4523d26e2db039e47`

```dockerfile
```

-	Layers:
	-	`sha256:06fff3df6bfd5362eaee7dc0308a334b396725f2b471db142239988e1251e53f`  
		Last Modified: Tue, 18 Mar 2025 07:04:47 GMT  
		Size: 7.8 MB (7756775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d323898f7a09792b55d5e111a356f7b8c733293a67b2a82a7008fdc48adbaa9a`  
		Last Modified: Tue, 18 Mar 2025 07:04:46 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:084fd6f27e0c5ed6a8b10ca6abac5cc1ec08d955905829a2cd37089fb72201fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134634297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4458f96f88bbff8a4c5ee80aa874679d5720dda406e16d6b158e98430a7c0b3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:178486f4f62c2327e3032d4ba336ef94cf832a760b981d4bb0038fdaefbb07d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7755934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a2340e95c58d8646a38c79395088c92656c5ddb957a713c38c1595a2a184d4`

```dockerfile
```

-	Layers:
	-	`sha256:fee9c14b428cee05d32231cd8d4a0b8db397fa8fdd7b0d48d2c5c11d1ceb439f`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 7.7 MB (7748279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d138c2b7c9024462bc7f4777b3b4560a73165a7b4bef63800699007d6084bdc`  
		Last Modified: Tue, 18 Mar 2025 05:55:50 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
