## `buildpack-deps:hirsute-curl`

```console
$ docker pull buildpack-deps@sha256:d9d204ef4e72662d40254e7fae4aea4e480604d60a3b3ee89c1222df0cc7bbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:hirsute-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:918bc0b71f14d70837ffc51eb9fa341d3b06f2ef9deed3dd1a565b7f10e111cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40795225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1522d3e4c966bba439294c429a3688eb083e602095e8308b5ec6979ddf0b5ea`
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

### `buildpack-deps:hirsute-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2d230394b683fdf5e3e856d2c6d7b0c95ab49ce823d7a6c8cf63be67907666a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34856952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe84b73356152b7afd8fc8c78dd430cbfa28f4a3eb076c34c16c26d3579a2c8c`
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

### `buildpack-deps:hirsute-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ea96a21adef2e20f6652fb529e8e2111dfc5435109a42191d3d5d5a927f71069
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39007450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef1a07c6b4af133652e14c64e70ad16aed37e25673f1b5efebf2d161c118d80`
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

### `buildpack-deps:hirsute-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f3da3935c3c5d3bac031578d9b96350aad84e812fb494f32b0c03846c1e6e039
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47934274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca9acb067cec36cb3ef12f24def85d8fc12e44ac548a597896e99581b49a2eb`
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

### `buildpack-deps:hirsute-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7e862bc7d1cb08cf6dad215ca6f59db47db7d959575b43894e35b95c93416048
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35265046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f55d1ec6617facda3b50613b4f7fb6a78d2470d443cac472a975792ee47e01`
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

### `buildpack-deps:hirsute-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fd29e4a614f0c5be3f564d4c3f6d33cae0a9322a2336e08cb523f10f9681b3bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42492350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8ffa83733e51ab024db0d55e68fca96230e246adc5968ba5248839e469afa6`
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
