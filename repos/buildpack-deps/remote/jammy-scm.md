## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:d5a70618b8d8d65b3b96e77356c2210f00426e9beee2ace15be46e10d7c282a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:63533a6531029f5a5a2a34d20ae05bd512346ea6d901965cd0a005342e511790
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77012427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1cbe194e1ec811c6a0bf0b692152d53e09dde661d2a239821d3c41062422b1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:15:16 GMT
ADD file:3f673e2aa3a51c7980f0f25985b44578e091d31b3e0a8f481069c20b363a216c in / 
# Wed, 02 Feb 2022 02:15:16 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 09:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 09:27:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 09:28:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c610536171e3c233fc979d34130a90e9c9bc030425e5af141fd0c3aa8bcf5fb2`  
		Last Modified: Wed, 02 Feb 2022 02:17:11 GMT  
		Size: 30.5 MB (30532381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfc2f9d7d5477c6aededb78ddedb1c8decb0294fbdcbb22d89d3dc0b0551cff`  
		Last Modified: Wed, 02 Feb 2022 09:40:10 GMT  
		Size: 3.8 MB (3818925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a14c37a224f0c145333f74075b0d11d54a5f48d2c2474192e417635a26fb351`  
		Last Modified: Wed, 02 Feb 2022 09:40:09 GMT  
		Size: 3.6 MB (3559196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b96db7b49342063a87dc2f8ed7f6245ebcb6ea0469d30c55d05198af2216a03`  
		Last Modified: Wed, 02 Feb 2022 09:40:25 GMT  
		Size: 39.1 MB (39101925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4cf327b506ad90c53725708b4449e4f069aceee82356b13331115acdbccb94b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76349527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5fa75f9cf16128909d03622d9c6b7b6348e770058a581bb33282aebfbdcf72`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:26:27 GMT
ADD file:b3b2c8a5926e6c518af00fe93b63ed2cd402eaef6cea20252e33036970294826 in / 
# Wed, 02 Feb 2022 02:26:28 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:25:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 04:26:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f5a2de327ec5f0d66e0972ba3099491610a0a555eac3b8beb23e150ad81b1e53`  
		Last Modified: Wed, 02 Feb 2022 02:31:18 GMT  
		Size: 27.6 MB (27599998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ba0d77c40be8b00ac928860b3599cd5f3978a1b462c068142a2be356893624`  
		Last Modified: Wed, 02 Feb 2022 04:52:37 GMT  
		Size: 3.6 MB (3569811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540d6f0472085ac38d9c751f76a8d47e2513845c6e30325c5981f26622a4714c`  
		Last Modified: Wed, 02 Feb 2022 04:52:36 GMT  
		Size: 3.7 MB (3712299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0426340ba99faec414bed87601a4ccdd2ec246065a46a6a7048990450906c5a3`  
		Last Modified: Wed, 02 Feb 2022 04:53:17 GMT  
		Size: 41.5 MB (41467419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ad77267cb4ea4fd0605486ea29081deb8b1ae6ebbb7a6394e746f72345d368b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77297080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21be0a0e931247d10bfa97f11d0f0499b90bd86957bd2f6318b5747ebd38b1c3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:19 GMT
ADD file:bf6034dcd564f7c5f9ddf620c1dd7e0b870410717176db4e4db91c1bc6ee326c in / 
# Thu, 03 Mar 2022 19:41:19 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:12:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:12:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84df7bf04e98552ca258d4623ba2ee5c455a4f5eee4622923511caceaa69c6a4`  
		Last Modified: Thu, 03 Mar 2022 19:43:18 GMT  
		Size: 28.4 MB (28424704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de81b8d223c70c2ecff8735f6588279de47e4a3c3266d19bf621c5c4ffc048c`  
		Last Modified: Thu, 03 Mar 2022 20:19:41 GMT  
		Size: 3.8 MB (3792303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49986fba69bc0eae7347e2c6882c0b760ce11a31a258fb2694ff83665931577e`  
		Last Modified: Thu, 03 Mar 2022 20:19:41 GMT  
		Size: 3.3 MB (3319390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8402a169943d97ded64a733fe9cd21896e521ec0e8b9fe4524d7ae817818ae`  
		Last Modified: Thu, 03 Mar 2022 20:19:59 GMT  
		Size: 41.8 MB (41760683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a0c859ea55c9388182ca737fa9d4f2c61a8cb65ad9c37d816d9506286fb8e28e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77586665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768f0994531558a74395641fb0ce61f77af5757276f8e1b88393426e810e33c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:20:53 GMT
ADD file:b24b04eb8b8b5c5cc58011f4e63b5596c57fa8b6317f8472712142ad1bf70e0c in / 
# Wed, 02 Feb 2022 02:20:55 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:47:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 03:54:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5c28c21c482bb799d18f7bcf823f1ac5990e89d600522966a3cf5fe82c052779`  
		Last Modified: Wed, 02 Feb 2022 02:40:32 GMT  
		Size: 28.2 MB (28217972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b251be260817347597a970777f84e0b51e124647e8cea5c780244d783f2916`  
		Last Modified: Wed, 02 Feb 2022 04:37:05 GMT  
		Size: 3.6 MB (3613365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2069686b7922a3f2a8cfad58aed19b9bf47acbe38944df441dc99d25c5108f16`  
		Last Modified: Wed, 02 Feb 2022 04:37:03 GMT  
		Size: 3.8 MB (3775454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b88b9bf3c33ffe460a8482a33680fe74eaf193bddedb131de3f4bf58687438`  
		Last Modified: Wed, 02 Feb 2022 04:39:02 GMT  
		Size: 42.0 MB (41979874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:051fc9123f3279f13d06a287e0b004074b02951c9a2ef59a8f9071e9ca25c42a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75771031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ee16aba743307df030f194d971f2be6f62caee15ff7e1a4ab2485292c98cbc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:48 GMT
ADD file:f63d347e51816a3655e11557a605d3c23560bc9478c726a1be3dfc202bba24de in / 
# Wed, 02 Feb 2022 01:42:50 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:14:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:14:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 02:14:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:50fdfed8ab37d65d6d796980d94adb16488809e0bd451c26062fec334cbd37fa`  
		Last Modified: Wed, 02 Feb 2022 01:44:45 GMT  
		Size: 29.4 MB (29425828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f6c6fa41b18e9fae55e546bfa9205b25e48dadab0dfb2943b0a5d64f10b263`  
		Last Modified: Wed, 02 Feb 2022 02:21:53 GMT  
		Size: 3.8 MB (3820059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e9f1da527a0c9b5af6226fed9a876b942f1e0ab69894e1a2cec098707c31f`  
		Last Modified: Wed, 02 Feb 2022 02:21:53 GMT  
		Size: 3.5 MB (3470153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f626a0d4c09c057829e5d25439dfaaa5a19b842dded9c2ff67b8369d1f482bfa`  
		Last Modified: Wed, 02 Feb 2022 02:22:06 GMT  
		Size: 39.1 MB (39054991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
