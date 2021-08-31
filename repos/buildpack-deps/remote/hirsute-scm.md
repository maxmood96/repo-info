## `buildpack-deps:hirsute-scm`

```console
$ docker pull buildpack-deps@sha256:0e63d7d04671f447f35c721d0cc0329e2e6bbf0421f4b74e8e0ed0f9c7abcc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:hirsute-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:53963b8dedc84f611319c16f86c364bb1ade2088bd39dcffef7bc047e2606111
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84337882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070fc06a5156d80575b1bd08707831468912b0a8af4a60a8ddbbac20d0f8acde`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:03 GMT
ADD file:4ac73e113682ef48b7466c4f8765ca7fd54ae98228caa319438a76c35d762b1b in / 
# Tue, 31 Aug 2021 01:21:04 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:57:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:58:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 02:58:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d7e10407b4d96b1866d5b77b368ac8b2b9b3ef9b210bad0b4784407405121b92`  
		Last Modified: Tue, 31 Aug 2021 01:22:35 GMT  
		Size: 31.7 MB (31703609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2bdc17338d4753c86d8e5520aadb12207bd763dac1f00aa8eb9042fcd88034`  
		Last Modified: Tue, 31 Aug 2021 03:13:50 GMT  
		Size: 5.4 MB (5430701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03dd940109a3cc748ce9b671747e7089353d649088e88252f777dcf586a8963`  
		Last Modified: Tue, 31 Aug 2021 03:13:50 GMT  
		Size: 3.7 MB (3662065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa3b3922cd293eb3f32aea33d2e5e755a7eae3fce018122e98ef65dd1094a4c`  
		Last Modified: Tue, 31 Aug 2021 03:14:08 GMT  
		Size: 43.5 MB (43541507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2e03a791f00acdebdb202ef33d78e6946ecbbabb9b3e2a6b6c42d561a9504308
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74811608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa7a2751d29365ef5f45ca3f55897eea12bb3795441d0f5ccba9ce32318a043`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:41:17 GMT
ADD file:cd7671d88520bafabf9a3bea20bd80ee0d2881b895c7f5ce1aaa4958e396074f in / 
# Tue, 31 Aug 2021 01:41:18 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:18:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:18:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 03:19:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48989deb32eb328d42c26dae334c8da758b723afff40db2647f6780446ec97e8`  
		Last Modified: Tue, 31 Aug 2021 01:45:34 GMT  
		Size: 26.9 MB (26860548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fec9a0a8408a0d36cfa8cb75d2b9e32ea29b69e96c4038df08fc8f06ef52d8b`  
		Last Modified: Tue, 31 Aug 2021 03:38:16 GMT  
		Size: 4.9 MB (4859278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811318e550593783ac5850dd96d8ac3a3fe682126dabd9493f201cc9f9d0c78`  
		Last Modified: Tue, 31 Aug 2021 03:38:14 GMT  
		Size: 3.1 MB (3138679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36aaae4759daf4d1e91747ae90020318048e7da07cf05181f7ab2f9999eb3ff6`  
		Last Modified: Tue, 31 Aug 2021 03:38:56 GMT  
		Size: 40.0 MB (39953103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a0e40d34528ab940355ef0e5c6e5a4331f9bb512e5e3104310ea9db74dc73d59
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82728192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32f751faa503b8fea9beef96876f4dbec6142b5dce0a0f3112fd89eb7c213c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:53 GMT
ADD file:93dcfc1791d96861438a84bfd38f5c0520353febfcc59bde5510c9e85eab2cf8 in / 
# Tue, 31 Aug 2021 01:40:54 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:11:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:11:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 02:12:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4fbd1b15195364f20d4b603e346a2b5c64ae93e9de90f5c1bd82a61e92851632`  
		Last Modified: Tue, 31 Aug 2021 01:42:57 GMT  
		Size: 30.2 MB (30162874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d54fbc3de08027791a7280c6d2d7f821165cc126fd0e08c6cba66c1d6fc122`  
		Last Modified: Tue, 31 Aug 2021 02:20:51 GMT  
		Size: 5.4 MB (5401544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f7180cc8ab79571bbc48658748543060674d12cbbdf7683a598d89f6086677`  
		Last Modified: Tue, 31 Aug 2021 02:20:50 GMT  
		Size: 3.6 MB (3638240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826a66d619e21f0b3656bcd20cb8925d105fc0e444b4a72eb69d81408ecf67ed`  
		Last Modified: Tue, 31 Aug 2021 02:21:10 GMT  
		Size: 43.5 MB (43525534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:08c18882a70aad8af2599f0170a98f8c20db30a91fcc5a77d3b043e5bfc7614c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97332366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5211c4bfed288ada093bfbb9e2f58c5f291103d5c360755d5ac8be047e188f50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 02:11:01 GMT
ADD file:28ec82d5664675df3fbd80ea2405c9f6441adb338e5969157339ef7d3b9cb690 in / 
# Tue, 31 Aug 2021 02:11:11 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:57:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:58:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 04:00:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76dbcd36047f3dda1663b45891fb64b9bb6c0ef0e5611c1f8280ac85e57cc7af`  
		Last Modified: Tue, 31 Aug 2021 02:14:46 GMT  
		Size: 37.2 MB (37185952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615e5e41d59fe32c6e6c5284994935d713f08ed29bdc3f9841683f0793cf8394`  
		Last Modified: Tue, 31 Aug 2021 05:20:33 GMT  
		Size: 6.2 MB (6155437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99aa8209221f270d9ffc050088f6998d6ceefa228f2ca68f9eb5bc410b24fadc`  
		Last Modified: Tue, 31 Aug 2021 05:19:57 GMT  
		Size: 4.5 MB (4523763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e43d357f3322abb3a717de7eaf87420b14cbcae1a2c006e9267578aa7c7881`  
		Last Modified: Tue, 31 Aug 2021 05:22:13 GMT  
		Size: 49.5 MB (49467214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:92d46888b25701d05c84398baa31995dd2f2f9cece8d00a6d36ae0b98b41ed12
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75595398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a3029ed135684d6a7d55a4aa6663061bf0bddaaac730e68a265ebb4392da89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:17:33 GMT
ADD file:c9125fcbdad41a027e81c7fc0616e4698eefb4bf591e9c215748c44001492a71 in / 
# Tue, 31 Aug 2021 01:17:35 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:03:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:04:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 02:07:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de98d6361415ec89b2135480af53817e96bf60ae2c78c53dad37c447f0f7b040`  
		Last Modified: Tue, 31 Aug 2021 01:33:15 GMT  
		Size: 27.1 MB (27143365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225134e3c31562a8c1d476ee61f8672ab2a39bc9f6dd1aa9d2334027bacf22c0`  
		Last Modified: Tue, 31 Aug 2021 02:44:14 GMT  
		Size: 4.9 MB (4945167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55ca77fa5925540bdc2a4cf61c8acfdf7fc0d169793ae57fd6e0b7a6465022d`  
		Last Modified: Tue, 31 Aug 2021 02:44:11 GMT  
		Size: 3.2 MB (3177763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98a854c5e99476d386d6334136c9b5839b261270f40552a56a5557336599fcd`  
		Last Modified: Tue, 31 Aug 2021 02:46:12 GMT  
		Size: 40.3 MB (40329103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:946ba36daa4e4c0d9d38cda5253c2dfd87343e5523921f9a8f70978f0698ae7b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89878914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e2cfd6247f86f57d874973213ecadf290768b88929aad3faf6c98c3ffda491`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:38 GMT
ADD file:ba5c2c420b69d0c125e25122344e156fa468282be3e91af99f6941eb676f308d in / 
# Tue, 31 Aug 2021 01:42:41 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 02:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e7ad6541ebda77ecfec574e1268bb944ba28f14ca69dab7bad1d63702975176`  
		Last Modified: Tue, 31 Aug 2021 01:44:29 GMT  
		Size: 32.5 MB (32491578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66e7ecd9588795e7cf09605e17fa940cd2b5566b310df2b484b60ba5faee036`  
		Last Modified: Tue, 31 Aug 2021 02:46:51 GMT  
		Size: 5.8 MB (5802191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36acc9b914fe8f7ad986a1869bcd54799c01524d5a43634c1cff6407f77d9a14`  
		Last Modified: Tue, 31 Aug 2021 02:46:51 GMT  
		Size: 4.2 MB (4185117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeae36ed176d953e43f3ac748df4f3d272212947102e33987f59a8cecb55002`  
		Last Modified: Tue, 31 Aug 2021 02:47:06 GMT  
		Size: 47.4 MB (47400028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
