## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:95712c982d07e54a0009be0df92c0903ab6af536f0791e6bd8aad2f687997df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
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
$ docker pull buildpack-deps@sha256:7ca1287501f4f5d82be0f2f0174a5c2061cf38749f536b89fa79ffda063070e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128315605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fbf604fbcaa2c054e72a2292f0a0da68d9c6b7dc5e44167be72a171e592f5c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:02:39 GMT
ADD file:1fda4c82a4eaecf44b3fc4eb92bb0aac8d81c1c87822bd86f8b52b3620b70420 in / 
# Wed, 22 Jul 2020 02:02:40 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:58:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 02:58:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 02:59:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c07b17c5753ba5920876a4091c37318cc0787c8027550cb13d9c1bd7ebfab87f`  
		Last Modified: Wed, 22 Jul 2020 02:09:11 GMT  
		Size: 54.1 MB (54102477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d597760a8071b7dad395d547ed7915e05c7d4fba09ba2c81e36fcf54c4a712d2`  
		Last Modified: Wed, 22 Jul 2020 03:15:18 GMT  
		Size: 6.6 MB (6607399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e255324867b8c5356029c240f78c0cf753ace14e42bbc98bb34675857b8afaa5`  
		Last Modified: Wed, 22 Jul 2020 03:15:18 GMT  
		Size: 10.6 MB (10584304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716c6c862a6ed53f272071f72c0799b3304e67fe7335a4527865c9f20e553bb`  
		Last Modified: Wed, 22 Jul 2020 03:15:34 GMT  
		Size: 57.0 MB (57021425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:37c64821384dc635686638d4472e5982e6f3ba4a6e681b7f81a0ff1d449b3e31
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123130946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c8208be501094eee77d2df17d7ed83cab879a689c00f1c8e9ea7949025c4a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:49:13 GMT
ADD file:057073afde8372e5586242898989764dc7739ad5fc93c170548a9831952368b5 in / 
# Wed, 22 Jul 2020 00:49:17 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:22:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:25:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9cdb0a98bd26018b67bc273d7a9bbd7c5d47c8ed8ba0b72c2024f049430a2e1`  
		Last Modified: Wed, 22 Jul 2020 00:57:48 GMT  
		Size: 51.8 MB (51782291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77dbfe5f595e23e67fa5c93bcef27e0855291352f61d2818001054fe906d1f1`  
		Last Modified: Wed, 22 Jul 2020 02:00:55 GMT  
		Size: 6.5 MB (6486760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2244202796f405d730ccf4e2e91cedd51e3cb380515ba202422d289179a182`  
		Last Modified: Wed, 22 Jul 2020 02:00:56 GMT  
		Size: 10.3 MB (10271646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40ece8618b3e24af2eef118d18af9a0d027ac6a700decd318bd6c2cf58612bb`  
		Last Modified: Wed, 22 Jul 2020 02:01:28 GMT  
		Size: 54.6 MB (54590249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1c9e7c40979d9c0eb189312e4863997438b0f6c01151ce403e6633a642e12218
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117938293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2495c5d23004abbe268f08386fa030417a23af77e3ff73d6288ccff8e64065`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:16:07 GMT
ADD file:b12e6ee23a8c36af2c020959d86c9277008b6b54ceff80954502340dee6e145e in / 
# Wed, 22 Jul 2020 01:16:12 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:21:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:21:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 05:22:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9142e33629754cf85d79355e893c9c07e344f32f4fbe710c344514aada5f1b92`  
		Last Modified: Wed, 22 Jul 2020 01:39:35 GMT  
		Size: 49.5 MB (49461754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab191c0042bdb971560c33a6e7bee561ff37ce4309087897cad70ea149a1c831`  
		Last Modified: Wed, 22 Jul 2020 06:00:20 GMT  
		Size: 6.3 MB (6296595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588773c504d467808703f4e8fb464799ea4ce5a0db4e5d91e73995846917d34b`  
		Last Modified: Wed, 22 Jul 2020 06:00:22 GMT  
		Size: 9.9 MB (9919209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12803f25cfc88d50ce8e086428f15a6ea8545773d80a6b6326e1e467f109832a`  
		Last Modified: Wed, 22 Jul 2020 06:00:48 GMT  
		Size: 52.3 MB (52260735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:06537bb9d61c1e7e6fece52511270125626d325532e6236f28c42945810fb550
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127316061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3ceb06299fe8bf1cf0bfbe7636f66e6e53f31e30214e1b09ef88d73f3ce785`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:39:52 GMT
ADD file:19b87dac8088f103e1a9992c229b17344439af0da8af45bc6d678f69471077d4 in / 
# Wed, 22 Jul 2020 00:39:54 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:08:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:09:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:12:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:508fd3fb95b7fcde22f3f927caabf293cc04dcbdb4c45b85a5130d5122e12a0c`  
		Last Modified: Wed, 22 Jul 2020 00:46:40 GMT  
		Size: 52.9 MB (52886369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5915a33a39d2dc36bde47815617bc03c29dc80e9539719e24091c59faeb64f73`  
		Last Modified: Wed, 22 Jul 2020 01:33:46 GMT  
		Size: 6.6 MB (6634801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ea5d467b9d2286b1dcd428b411982c7ca3d5a2471f013ef721842af48ec9b`  
		Last Modified: Wed, 22 Jul 2020 01:33:46 GMT  
		Size: 10.6 MB (10591622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ce2f62ac83f0fb7af53d2e4faa8b93e2b37157d2cfd0eb7725e95b633a33e1`  
		Last Modified: Wed, 22 Jul 2020 01:34:12 GMT  
		Size: 57.2 MB (57203269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8a63083748e694db89809802d1a192c1c46a15a9768ae84fefa6f04ed6cc7dd8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132011272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbce6a91c9c6d44f2730dcb160508d36551a02aa289fe32bf724ddb92ec5ff7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:08:16 GMT
ADD file:ca0e279e6fd6eb980b9731b695496074a130913346e67625acec79226fc6c10b in / 
# Wed, 22 Jul 2020 02:08:17 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:17:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:18:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:18:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f7fe72ad45ca30a1e73e494824a081709c2e449cb1bac8b4deb1b1a29c62e6c`  
		Last Modified: Wed, 22 Jul 2020 02:14:35 GMT  
		Size: 55.2 MB (55225022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3647f8e1aff936bbcccf16d2eb142f694cf4736d8d8adfaf3114569bc553035`  
		Last Modified: Wed, 22 Jul 2020 03:38:03 GMT  
		Size: 6.8 MB (6808980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a520a2450f762082c65c471256beae8c5f1c15f69b32c692c574b4c4caa4a20d`  
		Last Modified: Wed, 22 Jul 2020 03:38:03 GMT  
		Size: 11.0 MB (10964527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b88bc4c73fa3892709b4f76b34086d1ddc06082c734c3e2fefdf5692a46913`  
		Last Modified: Wed, 22 Jul 2020 03:38:38 GMT  
		Size: 59.0 MB (59012743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:da29a2785802a8a51d84e7da601b99487f5379dd6828daa8b099da7bf965f0aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125506503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5317d1f43fbdf7458ac55f7fb7f32c1c5cbdf89fdf35516b6a04fa4bdb46db47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:08:31 GMT
ADD file:7401625ebd06dafb2256bbcc5a70246e5e6282bcc356478f05fd7ddcaa55003c in / 
# Wed, 22 Jul 2020 01:08:32 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 10:28:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:28:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 10:30:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c240b05d7ff10891b36c505769b275684894e6a8ed8b5d40f20220a3da221e14`  
		Last Modified: Wed, 22 Jul 2020 01:14:40 GMT  
		Size: 52.4 MB (52358232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f2b31f704addd955e451fd2986f5159585f197625488725aac773df35e8478`  
		Last Modified: Wed, 22 Jul 2020 10:43:19 GMT  
		Size: 6.6 MB (6568575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30eb65f190ba6e9a301c9609ece037a9e82a8414a773e19a288860911d2d844`  
		Last Modified: Wed, 22 Jul 2020 10:43:21 GMT  
		Size: 10.6 MB (10602660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7563c2a484b0d69603f3e34a17264d58b347499d427207d3713673838df0295`  
		Last Modified: Wed, 22 Jul 2020 10:44:15 GMT  
		Size: 56.0 MB (55977036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d4363c8e4eaf9d272ab4758ede654089247cdb60d53e278ce90bfe3d02b0bb01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138962517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7a67c728e007b85d1cc49e1bf2c8e41d67c55f2e6e7702a7c5c7bcc2841cee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:13:38 GMT
ADD file:92efdcf349a6f1580ab27a2612939d75fc0e449e05e20e6385f5f7e409cd6684 in / 
# Wed, 22 Jul 2020 02:13:52 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:52:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 04:53:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 04:56:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1eb910fa0fdd2afbde1007491a0fe3461e3029a0c5950e2a5ea3a69d15cab80c`  
		Last Modified: Wed, 22 Jul 2020 02:22:28 GMT  
		Size: 58.0 MB (57953394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e46d2506c2944fcb5f8a4602131b518bc797e95e34ec5068a32eea4f31d2db6`  
		Last Modified: Wed, 22 Jul 2020 05:52:43 GMT  
		Size: 7.0 MB (6990284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2b78285d9f403581b34af8b80dc4d9f5f258ba139298995ee9c8fc3bf6a899`  
		Last Modified: Wed, 22 Jul 2020 05:52:43 GMT  
		Size: 11.3 MB (11331208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5785ab810f904f56ab9454018dbab7c040384b76f7a8c3fdabb9055e335ce954`  
		Last Modified: Wed, 22 Jul 2020 05:53:55 GMT  
		Size: 62.7 MB (62687631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e590faf77511cad09295b85af96444fdda31c74f5d2ffe483a9ff7732619c44c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124674101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9132c06da589a1e23cb2b90111ef45b301444a95e2a5ac87b08ea70507c7797`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 01:16:37 GMT
ADD file:be061a89b8959a241d8303ec83a6494b37d71fe20736b073046173371101421e in / 
# Tue, 04 Aug 2020 01:16:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 02:19:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 02:19:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 02:20:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:67f968df5fed9ab1993b2cba53f4810f984f47936fce947baf7ef2e7d8a5a20c`  
		Last Modified: Tue, 04 Aug 2020 01:19:19 GMT  
		Size: 50.4 MB (50416822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789709f3eb6ec781e7bd5d546a438d9f93b42d8201f34934bb917541d98545eb`  
		Last Modified: Tue, 04 Aug 2020 02:27:09 GMT  
		Size: 7.6 MB (7590147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17405c3991955650e0612638adcfcaec522e3c07552eb6b1924bd354bc8e608`  
		Last Modified: Tue, 04 Aug 2020 02:27:09 GMT  
		Size: 10.5 MB (10456481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68e926add9df5b913b9031846ca2cf9730906d323525f8cf01eaea4906b08b0`  
		Last Modified: Tue, 04 Aug 2020 02:27:23 GMT  
		Size: 56.2 MB (56210651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
