## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:c164fa64e638f4997dcaa470666b91ab75faf8ead983b14b8ea508356ee06b18
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
$ docker pull buildpack-deps@sha256:107b7c021186efe3ed164cfea1c3d06c8ed6b8ce4582f691ff74a2dc4901a562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136932334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc6260661cca62da45094b3d5d01eb10b3ae352ca934691651dd8543956046a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c45671abb650eed88ec7038f7152842ad8d557322d1c488be20f05be096cb46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7760401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2a1f4e1a96a61d654b4ceb41ea6775eaade5e6d735639e5bbea80e9f6294dd`

```dockerfile
```

-	Layers:
	-	`sha256:b87149b2f1486609a2af0770d2c2c37d036fd5e551b650c92f01ea43a97e54c9`  
		Last Modified: Tue, 04 Feb 2025 05:19:11 GMT  
		Size: 7.8 MB (7752746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16de0d9ec26360b8605a9e23ae24c8fa01bba49c7df7a2c647e0c7c43e7a807b`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4485452def37f53d9fea2e251dce6eec0c7a015f96823123284127e52bd259de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130743483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bd79e1728ba3eb164b6a77dc3f9b0cd9778a70d2143f9d9af57d9e10a42a0d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f77895e90931fefcb9b0f936aeec6e8c95f160c764c504ceb6084ffc29b46c`  
		Last Modified: Tue, 04 Feb 2025 10:20:41 GMT  
		Size: 62.0 MB (62003807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9325e1f31ac79d5ec224fd4a72d88769f24ae26a8b0657571c7ed3ab028f0b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cbcdcc4c7120567403bfd7323fcb4c9cfc1f4ad85dd84655b4106038f895e1`

```dockerfile
```

-	Layers:
	-	`sha256:787a1a81ca68983478e9b85146549b7060b5bda7b817fb5fa748e29968505496`  
		Last Modified: Tue, 04 Feb 2025 10:20:40 GMT  
		Size: 7.8 MB (7754304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ae5dbc955356ce8d85cb9395d5a07e003732510094b71b218d7c7f691b41fb`  
		Last Modified: Tue, 04 Feb 2025 10:20:39 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d1e072586740069d1b5e9086fdcd828de918bfb913d5055e1aaa194f62dcc265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140593719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29f7944ff637b8f0ba1c24926e7d9ef677ee299088eb49272b3ed9d4d155cfb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 05:15:47 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a8c7b49ce3106d816ea038fd374c442087a4e89e2fc93a79ec4684633bac082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7756451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5b2ac5fd703de6ab1eddd79d25bbe48d83b138aa053a7a88e51177e6a976fd`

```dockerfile
```

-	Layers:
	-	`sha256:9d2a829989dc2c4ace1d5075358dc1cf0e96b3108c0e3b1e30669aa7592e69c9`  
		Last Modified: Tue, 04 Feb 2025 05:15:46 GMT  
		Size: 7.7 MB (7748823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51ba6d7dd98693c417109d9f16fa8a019ed6cf65c04b4b463211d4e1d1ea1b9`  
		Last Modified: Tue, 04 Feb 2025 05:15:45 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ffa9908a4c08d7d090e6f5aa221f2997365592599656590e9ce382df411488d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147873264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7236e9ec4eb41b54d1798387dcfc878e0d007b4ace383bc7780fb55f25b88b72`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 01:37:34 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7451c2aa1d936ee2bec4ea4db323da11f1dc2694095c250c16b70763100f29cf`  
		Last Modified: Tue, 04 Feb 2025 15:46:48 GMT  
		Size: 69.8 MB (69842739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:412deb1b7b5ceb2253bfb96485e0de375c4e7c101f4d3daecdf30e5e17ad105d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492b9cddd85e3818123ca38a9c0062bcfe705b6149e7311693065d992156eefe`

```dockerfile
```

-	Layers:
	-	`sha256:dbaa978990c0f7e78edaf7cbfb37f6a38b05a5e491978065da22a7ba8f0b3222`  
		Last Modified: Tue, 04 Feb 2025 15:46:46 GMT  
		Size: 7.8 MB (7760453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff09ebdb5e629f6d7f3667ae0b7c36313571809ba2ee52ef563b843c3fed4065`  
		Last Modified: Tue, 04 Feb 2025 15:46:45 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5261ec0a644e8aaf0410d07b3f6775921eb9dfd59122eb9155529fc4dd8e12d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134688525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a46e44795d80467cac123f20812bc46798d0bebc2ca9b6c72285a776183381`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2ca21cdc0403c9f431731aa97d0c4db85a946a2bacf211d0cfe3ee4e5418bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5459c93da646c41b36d9e5eeee87162119e171e15ef61c37b7f488c907ac80`

```dockerfile
```

-	Layers:
	-	`sha256:e5d1da80e53060d3414c9fee17945ae782d9600f01876fe0136f6c4d962f8be8`  
		Last Modified: Tue, 04 Feb 2025 11:34:33 GMT  
		Size: 7.8 MB (7751951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd51d33d5be0950a97f8ce96f83c03da82e3ff767c4f51b3c48d301197f978df`  
		Last Modified: Tue, 04 Feb 2025 11:34:33 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
