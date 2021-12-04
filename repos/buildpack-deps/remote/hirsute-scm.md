## `buildpack-deps:hirsute-scm`

```console
$ docker pull buildpack-deps@sha256:24d0961e1b27aa938e9a399ea96746fe957eefd15bad3dac94c8a4917e401466
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
$ docker pull buildpack-deps@sha256:6f93d35b1ad5d7542dfd5025c84db3c6a86e6b140923aa7152eb58705db4289b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84337786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b86faf85314b0faa79c8de08d2e863503b3644532877ffacd0bb3476c283a2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Dec 2021 02:20:56 GMT
ADD file:b94883edb5db8add88bbf8934deeda5ddd0acb4e2ce2a19a774de29ee04b7399 in / 
# Sat, 04 Dec 2021 02:20:56 GMT
CMD ["bash"]
# Sat, 04 Dec 2021 02:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 02:39:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Dec 2021 02:40:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9e6a0d5477cff31ce49b4d3bc07409ebd27609574e968043d0b9c10acf854ebc`  
		Last Modified: Mon, 15 Nov 2021 05:13:30 GMT  
		Size: 31.7 MB (31703945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6ac1808edf35dc4bc9c2a238338455fcd9bb473e3e2eefb62149a83d4d2177`  
		Last Modified: Sat, 04 Dec 2021 02:44:58 GMT  
		Size: 5.4 MB (5429044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c979fff1be3bf3600792310b88676b7e33d23f01d3e4ab4fd460170dc74b8905`  
		Last Modified: Sat, 04 Dec 2021 02:44:58 GMT  
		Size: 3.7 MB (3662236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76654756b0591142a7600b7119f7793b38d291a915f19aae4e231dffdd1d0caa`  
		Last Modified: Sat, 04 Dec 2021 02:45:16 GMT  
		Size: 43.5 MB (43542561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9804a4fd9b159a2bf14e2e9fecfafd454b98c57b208e9f1cd046c5367321421e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74810383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa57e9ca19a6490459f1d1b27fc9522ba5af6d70e5bf5de22e6d43365e578599`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 02 Oct 2021 05:59:26 GMT
ADD file:0ecbd9f51121128f5d6ca097a4f697705e11f91abe0a7f83083e18bceeeddfef in / 
# Sat, 02 Oct 2021 05:59:27 GMT
CMD ["bash"]
# Sat, 02 Oct 2021 22:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 22:24:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 02 Oct 2021 22:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:615bdbfbc600b147544d8c25eedf00ddb7eebaf2e9005c1da9f5885a6bbc6c1d`  
		Last Modified: Sat, 02 Oct 2021 06:03:33 GMT  
		Size: 26.9 MB (26859487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8944eff0f4815cf5a70868ad5afaed083de9f7ead5a73bc97fa5dc147a04f9`  
		Last Modified: Sat, 02 Oct 2021 22:40:51 GMT  
		Size: 4.9 MB (4858463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bed8cb9d9d7259532d0d30040f4f46ba30d3dedae6e7d37d51c4bf9f60bc54a`  
		Last Modified: Sat, 02 Oct 2021 22:40:50 GMT  
		Size: 3.1 MB (3139002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8efec2f84a292f59a270ac67ccb130692e15a90a3105f135600dd1ee32bed4`  
		Last Modified: Sat, 02 Oct 2021 22:41:32 GMT  
		Size: 40.0 MB (39953431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:aa35ad991964b1caab97be7a86a789c739c7ce3c2b2bff8260c6a8d12dc57ec4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82540354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d746a6db65951127d29c9082ac04b180089cc78856ceca1a4e4b71370be8bb36`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Dec 2021 01:44:14 GMT
ADD file:f6fe7852db10c8de6e161babd3110304c6e20b10825c02c995338bcb4e41f12d in / 
# Sat, 04 Dec 2021 01:44:15 GMT
CMD ["bash"]
# Sat, 04 Dec 2021 02:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 02:03:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Dec 2021 02:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fcd77b4f4e1fa4d6089acc7856f15d5d2760bf81f44a94e52eb8e81423928c6e`  
		Last Modified: Mon, 15 Nov 2021 05:14:15 GMT  
		Size: 30.2 MB (30174348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330d08f54fb4c8a29eb513eb66bcfa0c760ac8f6d038f4aacf0934c31fdf9edb`  
		Last Modified: Sat, 04 Dec 2021 02:07:58 GMT  
		Size: 5.4 MB (5401275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3135edb0f3a1007f770789719e3271330d6cdf2f5f2c634dc148953996b3e0`  
		Last Modified: Sat, 04 Dec 2021 02:07:57 GMT  
		Size: 3.4 MB (3431827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1641da95097e52ac220bd32b64969d5fff25d51626371b86e0319dda0a8b5ecd`  
		Last Modified: Sat, 04 Dec 2021 02:08:15 GMT  
		Size: 43.5 MB (43532904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7aafbea658135808a954f4ebd5ddb175c5ceb3ea44cba926629eb6f9f1eed504
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97401472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede235c97d7480839d9aaccf5e3d0b84d38e02dad497e882800ae72c44799b5c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Dec 2021 04:51:15 GMT
ADD file:b886fe9246afec77612c8d5d8486a4a3279a8901f839d595de9f85557df15e8c in / 
# Sat, 04 Dec 2021 04:51:20 GMT
CMD ["bash"]
# Sat, 04 Dec 2021 05:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 05:35:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Dec 2021 05:37:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f377fb2e26a40c932d4950b215a828991db4c020a09012e5c61f902d3acf364e`  
		Last Modified: Mon, 15 Nov 2021 05:15:19 GMT  
		Size: 37.3 MB (37255750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50e678d30afbb7776c7b3b7c482b0f5423f33b06314cded787857f6b0faeb83`  
		Last Modified: Sat, 04 Dec 2021 05:49:32 GMT  
		Size: 6.2 MB (6154791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96b548eca1656576c79f554628ddf83687d802551b71fdb711282407582bbf0`  
		Last Modified: Sat, 04 Dec 2021 05:49:32 GMT  
		Size: 4.5 MB (4523733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868d8d42684d6398adc044a5a601816f0ce1709d542675b043aa2a1c2e6a70e0`  
		Last Modified: Sat, 04 Dec 2021 05:49:53 GMT  
		Size: 49.5 MB (49467198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:561345d30c559a320a5b4ede2e455eb00fe7f994d9117b94f1d0da5b0f16ba8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75594811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9d1372653b3ef10145b38645bac3aeac40b4fbd560aa64903e06730174b195`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Dec 2021 02:16:08 GMT
ADD file:add8105f670e14bc4d78d32115b5f7224ea4d551aa5ca27348ef2c463e4d566b in / 
# Sat, 04 Dec 2021 02:16:10 GMT
CMD ["bash"]
# Sat, 04 Dec 2021 03:18:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 03:18:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Dec 2021 03:22:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f5b550b7a55252b040f79672fb02f3d4cf285d778195c655fcf320b01a2716ea`  
		Last Modified: Mon, 15 Nov 2021 05:15:46 GMT  
		Size: 27.1 MB (27142131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97990f84e7c5aa1d13db231fc0c282cd87aebe2f68002fe8c959626515581906`  
		Last Modified: Sat, 04 Dec 2021 03:49:03 GMT  
		Size: 4.9 MB (4944752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f8a301d420a74616aae577a045b1ac5b02668053ec3d88903d47a24ad41ceb`  
		Last Modified: Sat, 04 Dec 2021 03:49:00 GMT  
		Size: 3.2 MB (3178163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d16119e1f19775a16fab82daa0d1566eee3274d5044e0647cca301931e4b59`  
		Last Modified: Sat, 04 Dec 2021 03:51:00 GMT  
		Size: 40.3 MB (40329765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5529ff3b356b637b2a43bf5a365244d3f95b1f978d962cdaf738ff9d6e0877e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89892183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f61d130271e0ded0357375c1373d8db78018a885c214eea564dced21df8a4b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Dec 2021 01:43:38 GMT
ADD file:6d66c98b5da6f242f1ab27703377ccbafff619c8e83fcf52e7ef7efead5c5899 in / 
# Sat, 04 Dec 2021 01:43:40 GMT
CMD ["bash"]
# Sat, 04 Dec 2021 02:07:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 02:07:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Dec 2021 02:07:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a5e1e0bcff39834997ae03f59105b3cbb3f26fcab688703ffc81b4c0b5894c6`  
		Last Modified: Mon, 15 Nov 2021 05:16:19 GMT  
		Size: 32.5 MB (32505784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc9eb43d6eb95c883a6edca33efa98e7f034a7dda1146a503ab15352a49500b`  
		Last Modified: Sat, 04 Dec 2021 02:11:11 GMT  
		Size: 5.8 MB (5801275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5925df3a30ee8e993d47fcfe7b912e8dd219a903a346cf5abbaf916e7bb7440`  
		Last Modified: Sat, 04 Dec 2021 02:11:11 GMT  
		Size: 4.2 MB (4185291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d632201b9a3763071a69f82731e615442e7842bbe1d745896133ddf999c2044`  
		Last Modified: Sat, 04 Dec 2021 02:11:24 GMT  
		Size: 47.4 MB (47399833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
