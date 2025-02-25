## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:18b93b0a7aa161c012413c52fefac3a96adab7c13e3af70b78304668ed9868f6
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a109ea5b5015b258e32481f2a375f0983dc974f7673314420323537c62f98d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136928845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7334e655726fcc4f8af85cc55c613e0fcd8d5b8e1c2f172fb5beb9c88f0e91bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:45507434896f47f7edc452cf2cddf537efe48aaec327e7d7356590f894262a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7760416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c4eb1d06957773befcd1468b45d052cb40e41c8453e931ed80fdca0744ada5`

```dockerfile
```

-	Layers:
	-	`sha256:57d5185bd10317bed1ecc0f7af6daa547f310b4ece22fa0fe189fbaa742a6970`  
		Last Modified: Tue, 25 Feb 2025 03:13:35 GMT  
		Size: 7.8 MB (7752764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b1e0d85031ea1a991a04d9a5217ac08397754e18b68a23ba42dae0dc3309412`  
		Last Modified: Tue, 25 Feb 2025 03:13:35 GMT  
		Size: 7.7 KB (7652 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

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

### `buildpack-deps:scm` - unknown; unknown

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

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fc14b2cfc73a95da7f6cd7f7fa3d13f176c1202d748012034e8bad9450a9af82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125783284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dbe1671e6dcb41329ffe04125056f6a03c94f2742b79bf325bcffbb7c78dd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66806698bb37ab9f15c9072a66ade0dcacacec8794e48afd7fdc2e801ccb928a`  
		Last Modified: Tue, 04 Feb 2025 16:20:53 GMT  
		Size: 59.6 MB (59639147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:62b490b31cdbe37d3ba401736eabc3a5e966f0c2e4ab35fe892f9167e32523fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd0b5e1f570211db29ed22a51e52a7761a7c03e98109dc32dff1d28a399448d`

```dockerfile
```

-	Layers:
	-	`sha256:fabf481e6075d2b5b9e429f181c4a6484d5a98dd60661e51cf1ccc65c74a3ddd`  
		Last Modified: Tue, 04 Feb 2025 16:20:52 GMT  
		Size: 7.8 MB (7754031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6473f990acf48712edb616b879c7bb7f1b0dd741a2f6914da1bb1b3ef5d2bc17`  
		Last Modified: Tue, 04 Feb 2025 16:20:51 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1ced57858e5e83fd864357355b381229ec8c66606025e0f0dade4ea17650e84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136262486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d557fbc059a0fae1b2c30d68a2d40fe0e25907d175658b1e6cc06e7abda54b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Tue, 04 Feb 2025 19:01:50 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fc3534dfb80c847a38ae06a08ded2271e98cb61db4bd0dafd326dc68b70eb0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec342fca1d9a00dd08ff6456229eb19dda146d0db3d2830bb8b732d2d70ad9d`

```dockerfile
```

-	Layers:
	-	`sha256:72390a008256c69241a5285ca5340f1c747203a3e5db54e4bed76841569720b9`  
		Last Modified: Tue, 04 Feb 2025 19:01:49 GMT  
		Size: 7.8 MB (7759151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ca0aae52f38542b280bc29ace2c19d58206173b4c3c53086f16716ff120125e`  
		Last Modified: Tue, 04 Feb 2025 19:01:48 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7583cd92934cd7dac71cb9305a0af39fc510ac661525f4a53901dabe221b6536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140595619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10d59089ac14df72b588540df727ec78ade948909194f308ef8d77e49a7a0e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c393be974eba6dccc52989aa5386e033d36d47f1ca1e393888364cd4da790251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7756469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27b267545648f1641ca25c70dc6e8e56ebbb595c9a30cd35e0ac09c7573d9d2`

```dockerfile
```

-	Layers:
	-	`sha256:fae3530789bed003551e433262e59ef746c0773f121050c207c6cba9d4a5d761`  
		Last Modified: Tue, 25 Feb 2025 03:13:34 GMT  
		Size: 7.7 MB (7748841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce3cd9e6188b3a085213b27ba81f49c2854c5633ec1ef2c0c05f778c56e8186`  
		Last Modified: Tue, 25 Feb 2025 03:13:33 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:94f144c06be7776b5d877d4a1a428b7d56a99516276577f02ef347ecfbcabeee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135716386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e3c73be2fa0d2683387891b8b20d8c5dcfebed13b8ad10934a7b07c5ab143`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:467081b053e1cbae3c04ca1529cea6d968f9b38249f5cdd15b07f60be084dd00`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 48.8 MB (48757800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7faf65582b7e0fbb4eea14df7537078630b3bff0936e1fc964a494519326b5b`  
		Last Modified: Tue, 04 Feb 2025 19:25:23 GMT  
		Size: 23.7 MB (23652224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12393adfa37a97fbcfa8d29955e04828c6bd657b4d83082cf837413910af04a1`  
		Last Modified: Wed, 05 Feb 2025 02:53:44 GMT  
		Size: 63.3 MB (63306362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eef48b145dfdf76426fc972e52649480dc32d1aca40c405af80018a627dfa9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3133cd6c88724ddea2a0d4481e0dc3a1d3cd7bf4fcb1f25950394637f529a5d6`

```dockerfile
```

-	Layers:
	-	`sha256:481c3206c219f87f02f3a18d37b33379801e307f51e20685c267d2dc4374ecb2`  
		Last Modified: Wed, 05 Feb 2025 02:53:37 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

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

### `buildpack-deps:scm` - unknown; unknown

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

### `buildpack-deps:scm` - linux; s390x

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

### `buildpack-deps:scm` - unknown; unknown

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
