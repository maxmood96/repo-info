## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:00fe6b5fbd8cfb5482cf3ad1000532ca879c0dd757ef7be5ab2a84a35459e073
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
$ docker pull buildpack-deps@sha256:39791de344c548ea9c2deb463b9582ac1ec4ddf30445ac4a7bc561c897106178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125780150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa16331d59e99af8afad1a1363318050e57a4b6891a673e26cfd43d3539b8c4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8592de27a346567711b9d5bf0e451c3dbcdc0bbeb9bf4843dd4c8f6ebef15655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a4fb7b9b118f21ebe1bfb4be33d14a62eb5b0e2d13596029b543edde596211`

```dockerfile
```

-	Layers:
	-	`sha256:3399092fcb2fe59bed6db9a3e61626a43bc14eb449e2aa03f8787483bc61b13b`  
		Last Modified: Tue, 25 Feb 2025 14:17:55 GMT  
		Size: 7.8 MB (7754049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e22ce1d08c9fe606fd5ff68fad7c02fd8c0f4d3fe4c2257e7eac36c07b1c2710`  
		Last Modified: Tue, 25 Feb 2025 14:17:54 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6c08b5317b5686587018dae72a0b483aaf90844691531fee0cf40ca8da016d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136260663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd72a28af86a41ea52dfefbe9ad815d2265d6a14e25310607f280453ea3b76b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:848b5af127b6a9045bc6875fef406b3f9e4f1bd1f53bfbd600a88087ce545ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a83980bdbc32d38c6a6c47e4fba74c92bf5f32a4778970c7422715d882cdbd7`

```dockerfile
```

-	Layers:
	-	`sha256:189a9eab59f0e5a994413a0271803e9327231f64db7e08a89b1f2c274c58c2f2`  
		Last Modified: Tue, 25 Feb 2025 11:54:00 GMT  
		Size: 7.8 MB (7759169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311ac702ff94438f66db3242aed6bd289eff8a22b3d926cddbe72bbe22b292bd`  
		Last Modified: Tue, 25 Feb 2025 11:53:59 GMT  
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
$ docker pull buildpack-deps@sha256:1a76091d1b67ef781470a197f9de81422fd4e13e6ee4cd0a058cca494a2da53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135718014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efef9c1e2896199aae6ec9557072b978645d4ae022b309bcbf8a76c57fb1c11b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54f151aa1b87c0945bf97dbd3c72581adb102deeee7a48dedc6ef51580d82ec8`  
		Last Modified: Tue, 25 Feb 2025 01:30:30 GMT  
		Size: 48.8 MB (48758989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93e2f55385d2f9849f5c49ddc6a441349700a7ac20dcafe37c022942621cef`  
		Last Modified: Tue, 25 Feb 2025 14:48:27 GMT  
		Size: 23.7 MB (23652239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406e93c581655a2c5138779556e6b049332bee85d015285d3106e767693cb64d`  
		Last Modified: Tue, 25 Feb 2025 22:26:26 GMT  
		Size: 63.3 MB (63306786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c478489db428c7d20a046c624463124657a949187231c51dcc7376018ced5a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d254719292ff7eb43c9955c29956d28d0d1e0a93900577dc1335465598f7093`

```dockerfile
```

-	Layers:
	-	`sha256:99932405964b4323645192e856fda87f29fe29daadbdbf88ec5028bcfc867978`  
		Last Modified: Tue, 25 Feb 2025 22:26:20 GMT  
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
