## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:ec4bc5317b68a07667a48fb9299946423e43f1c041be374e72d46409a8962798
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
$ docker pull buildpack-deps@sha256:365c8a7733be5c7282297c7c93b15a28fa056b0fa0d437a2c053c0dd6428a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130745737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbac9a557e864504199a014da47339b82a0cf6b98c6802069c452d0480a8186`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b459539689f4bcb0541f8fe008fcb91875bac32d67b941da366b3489408bc8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2617d916a248d9eabc116d7e3314bd3d4e8665fc2f85b43806cc029d4d79ee8`

```dockerfile
```

-	Layers:
	-	`sha256:df6ddaf29498ff5a48cfd1e79f7e4f0aaa0e5ef4d7226e1fbb7d413ca55cc604`  
		Last Modified: Tue, 25 Feb 2025 08:36:46 GMT  
		Size: 7.8 MB (7754322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46ae043c42d3260462c20ce7a5a93fa19c5ce0553357ac6435545302ace47271`  
		Last Modified: Tue, 25 Feb 2025 08:36:45 GMT  
		Size: 7.7 KB (7722 bytes)  
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
$ docker pull buildpack-deps@sha256:cf9b964715c41d9ac3a819ed29b940a4afba3899790dc1dff05523ca347b2b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147869001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe51bccba20a2aa40e57f99f059d605ce404e03cfe968a3426e1d7ec0c9130b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c89e69476cc317a6683ff920f578bf0090df074847cd30bf37d432893a45be13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d9e702fcc18265068cf3f8dd1bb8952991fd0d603fba0a5a424f9bcae42175`

```dockerfile
```

-	Layers:
	-	`sha256:7590acfe787de3bc2d13fca99100705600d1a11d0fb97f09cd1ebb72cc37b123`  
		Last Modified: Tue, 25 Feb 2025 08:19:23 GMT  
		Size: 7.8 MB (7760471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6040fb42be5de79b3bc552e7bd96e4682fb5a728f5000cc63af202009adaf6`  
		Last Modified: Tue, 25 Feb 2025 08:19:23 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:af91eeacc8fb8ae198f1755232a291f990e15de64f39d04630f34f535b077fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134686693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa97d97827e5b72588bb57615e41bcce54198e09daa8cd7b4e15bf1da0c367fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ac15c286fcfc4049c5c829f6f5f2dedc409d2c808632d48d8c911b78b7cad1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3d63830f9a47c849fb74ad7dfc6bcf36df34c8f3747e544abb0b85be20f7fa`

```dockerfile
```

-	Layers:
	-	`sha256:3fcf91f7f9a3035ccfcba01ed43dfc2060f50e6bbc1d22b77600cf4fee46fc2a`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 7.8 MB (7751969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624333c5c089199c8b67c6323aee3a0c5a8cc05278e5090c7e48a8fe2f4b883f`  
		Last Modified: Tue, 25 Feb 2025 07:16:47 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
