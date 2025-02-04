## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:b8921eb6d9c99f9c2bf37f929be3c7a74c50a58149662f72b4dfd90591547e5a
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

### `buildpack-deps:stable-scm` - linux; amd64

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

### `buildpack-deps:stable-scm` - unknown; unknown

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

### `buildpack-deps:stable-scm` - linux; arm variant v5

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

### `buildpack-deps:stable-scm` - unknown; unknown

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

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:49e4ccaedbca671c339d8a55242d7f25e1af167a096aca68b56da8a26e979622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125784661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5d6202e1e5273856a4827dd5f9a1aaf9c5c9df9e95e406f72acc587373ce0c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f893443c0cff99fae6cfd9ee2d82f7d9fa1764c42e4b44d6bd02b54a5f8860e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71830b5b97fe489d694c4fdd593c37b208f010a9b30f5fbbd200b1d5bb8f78f0`

```dockerfile
```

-	Layers:
	-	`sha256:ed0713d12be1303423be5246de90d43ee0ccba8f617f41d991598bef4a257e57`  
		Last Modified: Tue, 14 Jan 2025 16:15:26 GMT  
		Size: 7.8 MB (7754031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab6ec41bbe5e21c735259ad96692c0dc9cc772b9c0cf51e02e186b1620bc8af`  
		Last Modified: Tue, 14 Jan 2025 16:15:25 GMT  
		Size: 7.7 KB (7722 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3d3e7297c13b3097bf5fb9991ffa9aad0816798a907a8fff792165491174b39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136261554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413ebeaa354b3c0feb020579c81777bbfe6e0b44434cbb51e0423a9a5e072539`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54b58bc89d63d6cb7a969a37a81bd05045e92b0531f2dea017d34389f50b348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfdf225184ecb259a96744ec5072a8b6321e328e75488d08232ee1c90c8287a`

```dockerfile
```

-	Layers:
	-	`sha256:ee5a579a1304a0cd9ab66a341c82f90bd0673cbb06d2d921649dc6204d1298a5`  
		Last Modified: Tue, 14 Jan 2025 13:31:04 GMT  
		Size: 7.8 MB (7759151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b7039d4910144475f784c47b0f938b47a0c5c3de6783cc5280520c1dea87bc`  
		Last Modified: Tue, 14 Jan 2025 13:31:03 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

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

### `buildpack-deps:stable-scm` - unknown; unknown

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

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fe602d939df4cbddd8102a3ecbfbd2b79407c0d8a77a3c3a8b61111134ca7a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135706996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c87c17f18e534fcf9eaa672e16e2832528995e9e5780ff4c8964ebef619f07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Tue, 14 Jan 2025 18:10:17 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be7513211e793708951d273ea21ae802b4bdb4109f4b12ca6122e317851db90`  
		Last Modified: Wed, 15 Jan 2025 02:00:51 GMT  
		Size: 63.3 MB (63296729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:63f9dd3ac1b3f3fb150b43d7ee5d7172d3f9881b5149b99d19d50bfb75821e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328981011361d0b51ce891a6cbbdd73023d076afad56601a031dafc25d1c316d`

```dockerfile
```

-	Layers:
	-	`sha256:ea2b61c81e84d989128047eb14c01db001abea44f3d40a2da08f942d63cb38cd`  
		Last Modified: Wed, 15 Jan 2025 02:00:45 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:05b4402223200277f406f99fc728e47988998b5946ff282b1a2f2b55db8967f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147875066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07253a39195775999a73cfa312e0fa0c5fa1cb97359e3cf5503e14f02d7368a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9d572ddeddf65e9c94b552da6a41ddb37bb717818328f59458a028ff53349cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee4e94cc9d33bf313cfc300eb9c016f08f8e9c4621491174b10461db746fb4d`

```dockerfile
```

-	Layers:
	-	`sha256:231c3fce7984cd3e3de5dd5d140d65478f0236395546611c454b0e0421150d73`  
		Last Modified: Tue, 14 Jan 2025 09:41:56 GMT  
		Size: 7.8 MB (7760453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75b5ea659daa8cc266903efd448b1e7d046a092e5d48598c2331e3ca388f11a`  
		Last Modified: Tue, 14 Jan 2025 09:41:56 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

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

### `buildpack-deps:stable-scm` - unknown; unknown

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
