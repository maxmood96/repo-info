## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:e73bc3919486fddc14d749f75f8e1c3f973ddc99745a6e07d9fd019e3f61d054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f6ff780ff6d9dd4454e7164151b28d72f3fcf1bba471138ce4e1f431bd71e0fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131402562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7f6c028fa86c7a1118b95cde5cb96316d9cacaa46a358a82613050902e582f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:39 GMT
ADD file:0ded1ec762355d6c32b4a9f1eff5fbd5e60d15824d6bde678ef85cbdd03fe0ce in / 
# Tue, 23 Aug 2022 00:21:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:50:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 00:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 00:51:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6649fedb76d916c1041e321eca86994acdb4cd14cc61ef93b5d2a397c15af4ad`  
		Last Modified: Tue, 23 Aug 2022 00:26:41 GMT  
		Size: 52.8 MB (52768784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52383a4258951f21b40d1c18a5c708ecfd3cc7f76838fc8fbe3c1fa248f7b133`  
		Last Modified: Tue, 23 Aug 2022 00:57:51 GMT  
		Size: 9.3 MB (9302218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8bf82596b529ddf3a818d599c3bed1bef1e54925ac4df0a1a6bf6467ce1bd2`  
		Last Modified: Tue, 23 Aug 2022 00:57:51 GMT  
		Size: 11.3 MB (11274041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f934be4bad0fbf951546a8aaa20f158e16a48d2a373a3b5cab06448c354bae14`  
		Last Modified: Tue, 23 Aug 2022 00:58:09 GMT  
		Size: 58.1 MB (58057519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7898539069871fcc91cdb4cceda9570567bc9b523428de6882445a6d4e42ae60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127096678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492f0b2ced30ba4bfa6eda150cd97683bd1046e1aee31157aadd60df1bf55919`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:23 GMT
ADD file:2829a8dbc1e67454e67c0015efaaceadaa4b04330ed9e60cc8248246cac2aae2 in / 
# Tue, 02 Aug 2022 00:50:23 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:25:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11a67d4cf31e6e9dc8797a5c01d3198f326d91410c372d1a490bf5592578d9b1`  
		Last Modified: Tue, 02 Aug 2022 00:58:37 GMT  
		Size: 52.0 MB (52021372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6833771528bea1307d56591db306804d9768947a466a60b5de4f6b545ab0cec5`  
		Last Modified: Tue, 02 Aug 2022 01:33:35 GMT  
		Size: 8.7 MB (8741294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2288f8703c485a4ea82b9d9a1de8905ae4f0e420ca4f317625f441977a31c0`  
		Last Modified: Tue, 02 Aug 2022 01:33:34 GMT  
		Size: 10.9 MB (10946981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbd5022e5328c139a6024dd9522e3ee6548067f8bf3200154271988ebb0457e`  
		Last Modified: Tue, 02 Aug 2022 01:34:01 GMT  
		Size: 55.4 MB (55387031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d8c512d64ae9ad3f2e481314f1d4855e30a77f85dfb63a640eb6ff02b4a5ff41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122110023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6687a2444cb5290af981f96b82b906a1625d2f8c7971813168b9f6add445c97d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:00:45 GMT
ADD file:a1d27fd37cd41b3026c10df50adfd5a93a40194548a87a372c97149f63b096b3 in / 
# Tue, 02 Aug 2022 01:00:46 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:50:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:51:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23e34b183a37464e321571d2a75fa33fded0e5a8506066db5c4f20153a665c2c`  
		Last Modified: Tue, 02 Aug 2022 01:09:03 GMT  
		Size: 49.7 MB (49735351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af50b5c584586bbf2589138734167dd8e14560e75cd854cd9bca75019a3f530b`  
		Last Modified: Tue, 02 Aug 2022 02:12:03 GMT  
		Size: 8.4 MB (8423017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4818fead9ad7b4ed572aa86d08f341272cc2cbb418cbe22f7f7d71f2be3778d`  
		Last Modified: Tue, 02 Aug 2022 02:12:03 GMT  
		Size: 10.6 MB (10589650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd163d2eebe4936202350772d43aa0c00eba5ca32eca150d0f23e01feae220c5`  
		Last Modified: Tue, 02 Aug 2022 02:12:28 GMT  
		Size: 53.4 MB (53362005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:63bf85ae860dbf4528de20d612dcc51c333e01dbb9abf1e5f3cf536ab2505a52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131233972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c8f4017b6299569189621efc421ec9f3ac8e6bcc68451b7e7451f86bc84b3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:38 GMT
ADD file:477966410dd9e274b01740d7af857db5c024b4c4e53a5e83b5da6854d5b0c209 in / 
# Tue, 02 Aug 2022 00:41:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:27:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:17bcb8e39c7f35480d4c2e5b46b6c0a58dac180206453cc49052707aa8053632`  
		Last Modified: Tue, 02 Aug 2022 00:48:00 GMT  
		Size: 53.3 MB (53311787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040e49dab65b12b89c427063ea6eec0802e14801664648c428e5a774754f3e73`  
		Last Modified: Tue, 02 Aug 2022 01:47:00 GMT  
		Size: 9.2 MB (9150009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b71a9f562c782f5916aedb7846293c7057b9f5f32ac072f785d2b21839f530`  
		Last Modified: Tue, 02 Aug 2022 01:46:57 GMT  
		Size: 11.1 MB (11062337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1205e62166cd9b96a2220ead9f68603c3996816c0b7e279fe1afb47d74ea5975`  
		Last Modified: Tue, 02 Aug 2022 01:47:20 GMT  
		Size: 57.7 MB (57709839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f05820f89144ef9fd4abdfa7b091a362e96a5babc1bd7fdded96cbb6445f5d8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134777701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6899c125d79e1d6f8e0f13938a0ff7560906f0008d90fe875828e8d43f0015c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:03:44 GMT
ADD file:56a765ed5b9c59576a105c4e82da61f928406a2ef950e7cada80b5c269a1acda in / 
# Tue, 23 Aug 2022 01:03:44 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:35:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:35:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 01:36:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05690d5133887cdda89e6ae4808c08e8a92acf2163ce992d8bacbed497b1ddd7`  
		Last Modified: Tue, 23 Aug 2022 01:10:25 GMT  
		Size: 54.1 MB (54133693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6de5521fae7f54e276230f1136f3c889618c53b37f387bcb06db2c09c9ea96`  
		Last Modified: Tue, 23 Aug 2022 01:42:35 GMT  
		Size: 9.5 MB (9480147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1ad46fde87250408a791d37517179cd6427cd46421e84e138f00437a005cc8`  
		Last Modified: Tue, 23 Aug 2022 01:42:35 GMT  
		Size: 11.5 MB (11473735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc96324d4abcfddd315fc320b0f834fa9ab7e220e914962ae1d8af8c95bc0b94`  
		Last Modified: Tue, 23 Aug 2022 01:42:56 GMT  
		Size: 59.7 MB (59690126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9f2e0633fd097c4b93d54591e6b739d66101b1fa75c18976ddcfd887dc5fbc95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129290133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43beb762e9b16618775de009b9e28cb2bbb96bfed3b221c499f5075eb1ce7810`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:13:16 GMT
ADD file:6165703835b4dbffafda027e272e21bf37cfc276085814fa1d03c1db0162e605 in / 
# Tue, 02 Aug 2022 01:13:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:11:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 02:11:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 02:13:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71112f7b4dfd928d54aaa23ee1023fef50d2dc747bf6e2168afe69932ce8aa1a`  
		Last Modified: Tue, 02 Aug 2022 01:24:23 GMT  
		Size: 53.3 MB (53305987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523353756f561bdc5914e25ea1cfeda5bc330e894285664b88d8ce11aa594a29`  
		Last Modified: Tue, 02 Aug 2022 02:30:34 GMT  
		Size: 8.7 MB (8659688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2258650534e83b3efae8fb3f1ce269322b09b63e553775a7c0b8c8104b2451b0`  
		Last Modified: Tue, 02 Aug 2022 02:30:34 GMT  
		Size: 11.0 MB (11041802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e365e2051b826228522cde5e4dc082e794b8ccbcf39513ac4bb385212b6277`  
		Last Modified: Tue, 02 Aug 2022 02:31:24 GMT  
		Size: 56.3 MB (56282656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c278e60ccdbc5c33aa70bc14d4f83a84fc069816f91338dacd8491307fd1e701
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141680593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c5b9e45930a168c1502ae008141969d057bc3eacf4bce6dc94010c80fa5034`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:52 GMT
ADD file:6911368d0ae9ca029c373628ddb642f29cabf3f909e9a77f8931355843b8ea49 in / 
# Tue, 02 Aug 2022 01:18:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:35:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 02:35:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 02:36:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a386a4ce4974e6c6fc3a96c6a7a96ce47fa8df11122fa0a4b856c23c5ccb46b`  
		Last Modified: Tue, 02 Aug 2022 01:27:09 GMT  
		Size: 57.4 MB (57440227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0eae2292d82f6824061d200408b3f0dfb525d1d5fcf719a2e4c01a7c4c82aea`  
		Last Modified: Tue, 02 Aug 2022 03:17:23 GMT  
		Size: 9.9 MB (9890501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465fd13cc41c21f92aad774503ecba5a1a350a8ee1c0affd0e437746ba26a774`  
		Last Modified: Tue, 02 Aug 2022 03:17:23 GMT  
		Size: 12.1 MB (12083644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b581263dff51b84efda62c2c01703a885a25f8bdc6e6ee4a4eb79046e734ac69`  
		Last Modified: Tue, 02 Aug 2022 03:17:53 GMT  
		Size: 62.3 MB (62266221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ef05116e1aa3a68409adae7bc8bacbfc541ba80ea3cf9d4557f97931554d87b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122361887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5da8a1feed0041190f96478c8ee800f1bd726c679e418e5a63f437c015ba7a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:12:03 GMT
ADD file:beb3c4d0f1887ccbbe2b266a156b7658d2e1d7d48cbcd416a0410554dfafdf12 in / 
# Tue, 23 Aug 2022 00:12:06 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:58:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 00:59:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 01:03:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11998c1ffc96119253ef35ecbcfd66c2cb0d69f51a294f603a54496ec02d329c`  
		Last Modified: Tue, 23 Aug 2022 00:30:27 GMT  
		Size: 49.3 MB (49268189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237ee2e31cf68d3cd2675680cbf1e3c574c76f74440375dc1b8c1ad1d3d9768e`  
		Last Modified: Tue, 23 Aug 2022 01:41:12 GMT  
		Size: 8.4 MB (8399080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69eb487c5f4d1ba65732a0b11d3a69780177b7ed0357581fce4eb347813a643`  
		Last Modified: Tue, 23 Aug 2022 01:41:12 GMT  
		Size: 10.7 MB (10659901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3572ed314e6c0604916ece49e3a546ec2fcc60391daae870152b56b8fdc14d98`  
		Last Modified: Tue, 23 Aug 2022 01:43:43 GMT  
		Size: 54.0 MB (54034717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1b28e370b7f14e632e1233e966d5ee08666aaf6b5ba3db430f74ab03e9e0325a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128798317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0683e4467933de232d93780c8cba1dfb4f123ec25ecec0298b98c61c8eeb3dbf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:43:36 GMT
ADD file:19dee33de85aac92620de3bd92768833a889db0b60b7445419bccb4285c46f94 in / 
# Tue, 02 Aug 2022 00:43:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:12:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:12:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:12:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:31888e988211ae2cd4058438d0fd3d3420a26d35f21e97741527c1e85ad2d476`  
		Last Modified: Tue, 02 Aug 2022 00:49:29 GMT  
		Size: 51.7 MB (51734666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd60a4351ebe5fad9f32c09d0a6f7ec29b6c6dcb5ff8c29e6650149557447e2`  
		Last Modified: Tue, 02 Aug 2022 01:36:55 GMT  
		Size: 9.0 MB (8960873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0db795ce4385e2a159326c7d9ab52e109942607b82b1c377894e874e601d`  
		Last Modified: Tue, 02 Aug 2022 01:36:55 GMT  
		Size: 11.2 MB (11166864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891cb8548d01d5cd140a6d90fa3462f4433c9891f74f6d5405b9556edaca1a0`  
		Last Modified: Tue, 02 Aug 2022 01:37:13 GMT  
		Size: 56.9 MB (56935914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
