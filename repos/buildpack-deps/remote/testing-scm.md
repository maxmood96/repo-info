## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:9bc7adf41f7bfa4a83dbb172de3a54b10092a2539f90e0f1af6f2eea7728dbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d650be418934c90f6e9e3efcb52bef7ad660324074002efb8541e7baf9aab6d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142992921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d652704e9a00d957fc5de5a96e89b65a829acaccfa3de508ebcd9040d9ce0b6d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:23:42 GMT
ADD file:93e647bfd891e82156d7a13e0f0b194003855008967ec51e962ea0d70fc59ff6 in / 
# Tue, 12 Mar 2024 01:23:43 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:59:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 06:00:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6fbaa46799c378c8b00a06cb5a2319bdd5ab7abe194cd97bbc9aec2daf476e9c`  
		Last Modified: Tue, 12 Mar 2024 01:29:57 GMT  
		Size: 52.4 MB (52360823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1767d006c9347102620ba4282bc383135a85f2d494cc82af4568dbaa79a48972`  
		Last Modified: Tue, 12 Mar 2024 06:08:15 GMT  
		Size: 24.2 MB (24160710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af29457b55c7e48f1d7a6c2a6a8953b155a7d1f248122f397d12e999c14db9a`  
		Last Modified: Tue, 12 Mar 2024 06:08:33 GMT  
		Size: 66.5 MB (66471388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f50fb54a71e7ca5f8ba2f9a471145eafe72b794171708d1cdb397c84933a9505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136569171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a844b3d0f7fc87c5a39e852cc966c16bd36f423def0686a781b932cb7278a6f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:49:56 GMT
ADD file:3e60918b2fc6eb291458158f2b94b782320f758effe373fd6d0a5c58dd3e2319 in / 
# Tue, 12 Mar 2024 00:49:56 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:39:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:39:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d768e5bf180c947f8692477b575df3498b64f65e904bac933d0260cd957c8aa`  
		Last Modified: Tue, 12 Mar 2024 00:55:26 GMT  
		Size: 49.4 MB (49418029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb2336dddcb338dd0f592faca75df5ec1dcd20bf4a99dac4ce09223036087fc`  
		Last Modified: Tue, 12 Mar 2024 01:45:26 GMT  
		Size: 23.0 MB (23040791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4717627ab561eb4522e931062c30f6a46c82295340d11e5dc75d76edc1d9ab28`  
		Last Modified: Tue, 12 Mar 2024 01:45:46 GMT  
		Size: 64.1 MB (64110351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:531f6562dbdc6b9bb7c4a20a3a6144c19030d9b6b8e27b8eb47e606eb806b7a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130738842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9e08fa15eba1ac01452eec5d937678742a0204698500aa4c94b09832662dfa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:01:42 GMT
ADD file:653b30d78a37c262fc23750e2a51b4c22f86c5a03a005268cedcb42011759039 in / 
# Tue, 12 Mar 2024 01:01:45 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:15:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:16:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:84940e63db1cf18d5cf1aa5d0b2d913f1cfeaf6d1392975ee4542b2b21627246`  
		Last Modified: Tue, 12 Mar 2024 01:08:19 GMT  
		Size: 46.9 MB (46919137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f950b5c77433bb7df3cf43f999646d938e0afeca45ad4123d681d5aa08f1576`  
		Last Modified: Tue, 12 Mar 2024 02:23:27 GMT  
		Size: 22.4 MB (22354857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdfb6eab2ddb5d810e5dba3e205db88b240377b7edec7f49cd3ed75f824b230`  
		Last Modified: Tue, 12 Mar 2024 02:23:44 GMT  
		Size: 61.5 MB (61464848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a7bd71ef1ea41bdbb8fb7469aac29e8ac87211134091c1473f3308a91c84cbc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142641589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a680cec0f95597eead792508f33a80b5928787501c8edde46d4d29f17dbabd2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:47:23 GMT
ADD file:822f8ebf81dcb8d0c3abe6092460eb4cd185e7a4b5b794a9ebc4221cc30518c9 in / 
# Tue, 12 Mar 2024 00:47:24 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:abb8ff6184544bf5d189fbbab4286e594f2b7adc7d1feb51af49c007cff0e2c6`  
		Last Modified: Tue, 12 Mar 2024 00:53:00 GMT  
		Size: 52.2 MB (52191351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f6a2f77ef2eb04a7b071796c5ec48f48d3cc5f0577048728b1f064cfc42453`  
		Last Modified: Tue, 12 Mar 2024 01:38:42 GMT  
		Size: 23.9 MB (23878999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cbf246385c09e5150a227c27b3c398dc21e65ecb2d6e2cffb90763484c5e89`  
		Last Modified: Tue, 12 Mar 2024 01:38:58 GMT  
		Size: 66.6 MB (66571239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ca387afdf0e91d05db41030b363b68a3df8bf459fa80447c8aaa0e92d6748c46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149296900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01436b9ac474e17d8a06155260b7b95b4b6bcc35a0ad139578ccd2d36a12d94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:45 GMT
ADD file:48adfe9ef1da0d6e87fe297dd6cf8e9e117db33c490c41c77b6f2aadda29a275 in / 
# Tue, 13 Feb 2024 00:41:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:27:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b1a72a4bdfc8e16b8965d5db9e85a05a0f23a851b8b45d3b9e7376d79f2f223b`  
		Last Modified: Tue, 13 Feb 2024 00:49:03 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52348cdaee951cfde5088d97935929bf6f09626868b2b48c50a688783d5fad8e`  
		Last Modified: Tue, 13 Feb 2024 01:35:17 GMT  
		Size: 27.9 MB (27886423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f591e946a39d16953fde73e2ef14b2bfd79e49f9bd7d3f7f47afa1b2b5265f`  
		Last Modified: Tue, 13 Feb 2024 01:35:43 GMT  
		Size: 68.2 MB (68243501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:361b39cd3f17589b69ce21963e23dc967d03aba72bf95a8b2dfca172578cb8d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141299374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1dfd3c5d9a74b4124970e402b12b352920f515de4eac789ab55da3e1b6fd02c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:12:54 GMT
ADD file:b1a1fd9e7f874d3dc6cae10f09e49e08335ad86924ba543f9ff6c777d93c7314 in / 
# Tue, 12 Mar 2024 01:12:59 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9b0712382998885f6ab26afd04e80c46f04069a2491aab0d33d167a8539090c2`  
		Last Modified: Tue, 12 Mar 2024 01:25:01 GMT  
		Size: 51.4 MB (51407725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f9dba4bf2ad9240436865bb873640b08db96046b128861417790bef43c9163`  
		Last Modified: Tue, 12 Mar 2024 02:52:06 GMT  
		Size: 24.6 MB (24624765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add9f4278749b45fe2f852673b16441b5b51bcb148434e457ef125712328347d`  
		Last Modified: Tue, 12 Mar 2024 02:52:58 GMT  
		Size: 65.3 MB (65266884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b8d4f92597bcd9a1efec7cb9acdbf1ad11625fcf57a1f50d6b62baf55ca02c43
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154452774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d763881b12d285f5b4dc254aff491e09629cdf82393c079b10781f2de68548c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:34:27 GMT
ADD file:ee3f9725c5da5d09634af5073dc8d63c0cf10c6ece6c7b0084a82d44eeaa487e in / 
# Tue, 12 Mar 2024 00:34:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:08:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:df0d8d793e684337100029abc1076242a4e60e57c67bb9ee5002155393dd3737`  
		Last Modified: Tue, 12 Mar 2024 00:41:55 GMT  
		Size: 56.2 MB (56240791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0231f2ef2e18927b6d6939bd530fca98be4ea26cbda154232692c64973723b7c`  
		Last Modified: Tue, 12 Mar 2024 02:23:59 GMT  
		Size: 26.3 MB (26256378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78176af6a8d257c809c4e8791b9ef8922786ed93b43b0d048108141528b3f6cf`  
		Last Modified: Tue, 12 Mar 2024 02:24:21 GMT  
		Size: 72.0 MB (71955605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6ef5e8408bd072a0ac31f8f64a403c226cfe3ef7da8e0a494dbfc930023532a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144583481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136dee4d4045ab4df58a51a0604007c8690124098bcd865054a422502b810c31`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:12:17 GMT
ADD file:a763a87b7a749afb8ffcbc72555a671734dd9d842834384eebb8dd784135bfc9 in / 
# Tue, 12 Mar 2024 01:12:19 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:26:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2f13ce6fc956957d2abf0abd272bd88a159c9cdf4a731647c572eb2581973c57`  
		Last Modified: Tue, 12 Mar 2024 01:23:47 GMT  
		Size: 51.7 MB (51738519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4953941dae1a90e29387e6e32120bb7c2ebca24adab5d68977c75cbd85a709bf`  
		Last Modified: Tue, 12 Mar 2024 02:50:10 GMT  
		Size: 25.3 MB (25296799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6744696380aedee2755d9dc38f57a9a70817812b1b1a78dccc3f68e5fe21f170`  
		Last Modified: Tue, 12 Mar 2024 02:50:27 GMT  
		Size: 67.5 MB (67548163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
