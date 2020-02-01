## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:7626f422f2db8aa21624e64685274a7396a1d1991ca3196247a553d2fd02250f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5059137ff1b7f15dad3f841c59a6255e9c862349516ccd76b62e9303eae32305
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60518079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2f4d2f3ec40a34180cfa79470e1b3a65d1015a61bd3ce795f1ffd42c49834f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:feef47536e5b3ea5e1704125485199daff2e5add9520702af76462df4f33367e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58098558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4195798fb5c53d221a1ce56c7e45351f763bc3725647645a3fe6fcd3d458d5dc`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:52:56 GMT
ADD file:003f4ef6ab6701f1cce91c9774e3c1d199cf937ba1641ab43af5ba549c235c21 in / 
# Sat, 28 Dec 2019 04:52:58 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:42:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:43:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e58f920d198d7f6350a4f92bed980e92dd883ddad00ee7e4667d621ad90766eb`  
		Last Modified: Sat, 28 Dec 2019 05:00:03 GMT  
		Size: 44.1 MB (44073023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e028558990d3fc06833bbd77b26478420ced119418f35d5c6adf417d49e254`  
		Last Modified: Sat, 28 Dec 2019 05:54:48 GMT  
		Size: 9.9 MB (9866285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3a77129a757a347e5e95b9d58eff15f43b2e070ac78e55de3747284d43fda8`  
		Last Modified: Sat, 28 Dec 2019 05:54:46 GMT  
		Size: 4.2 MB (4159250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9bb48b48c5b076f15429fbe65de91655f7cc150e0a91bddfd6ea27044a3e84ec
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55525049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fae715ce7f0329818cb57499df9ef4a37b6f332456fb49ccdd4c8fbab6c1ede`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1b0e3ad07703593e86be54901dc6831120bc87f91e36f48217d4c6bf3ce3f759
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57009657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd190b3581018b950acb37a76c3b813237869f187e64f3c8d6307f88d47405d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf173a01baf7d45b479bb380ece219cbf0ea52178e9b8cdc5b87891759d1122`  
		Last Modified: Sat, 01 Feb 2020 17:39:19 GMT  
		Size: 9.7 MB (9748586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3392eac7bc27f3bd5fcb024413ca55ec4115c22da3e229567d5fc03cd4ff4e4`  
		Last Modified: Sat, 01 Feb 2020 17:39:18 GMT  
		Size: 4.1 MB (4094322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1d830a49f0e43f839fde4fe5ec653a2af94b8f8f11581ed5c85f9d20eb262c54
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61479314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d37381d1ac39b281806c80785a0a9fec3803388a6b110a6e8f07be11d74aba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:51 GMT
ADD file:f348ed8c5f7efee9f7e88d9a9bd1d57bca1bf445d486996cb6168da85c0bd43b in / 
# Sat, 28 Dec 2019 04:41:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:38:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:410821d7ff8b427b8dfb93dcf31b1836a617f5c09be71f83a16ef2c5946ee700`  
		Last Modified: Sat, 28 Dec 2019 04:47:20 GMT  
		Size: 46.1 MB (46100094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eeaedfad53e910bdc66ac7862f5f3947575aad9685d5feea1b7c59abce08f95`  
		Last Modified: Sat, 28 Dec 2019 05:47:05 GMT  
		Size: 10.8 MB (10817785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25ac55b31a6a0657f064091eb17ba42f3d06984c79ad2029702e0e6abfcff01`  
		Last Modified: Sat, 28 Dec 2019 05:47:03 GMT  
		Size: 4.6 MB (4561435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e708ea9071494ce40d73b50fb4156f53c0f3dd78bf8e2e109fa089c573a39575
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59951074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66ca9da2c0ef929470c6a0eab3dd59671a24512300bcaafc00803ae9d908e5f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:22:59 GMT
ADD file:0da9c5c67cad579be1a33f0f66df515de7f3ad992050c39cbaac281a01be41b3 in / 
# Sat, 28 Dec 2019 04:23:02 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:12:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:12:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:32185d9fc6268c6a6d87060ea324482fa22129c0f06d0f35e1376ca27b5399a0`  
		Last Modified: Sat, 28 Dec 2019 04:32:44 GMT  
		Size: 45.7 MB (45652475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff48b558393a869138bac45b7d540a1536280a8a4a86a3d0ff0dcab238a6418`  
		Last Modified: Sat, 28 Dec 2019 07:25:43 GMT  
		Size: 10.0 MB (10002000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e334b7fa51f55c0f060923f801160877cc313f1e3e40cf76efd21d94691cd565`  
		Last Modified: Sat, 28 Dec 2019 07:25:41 GMT  
		Size: 4.3 MB (4296599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e4bbe0a7353cf90090cea82b05b925500b74e8fbafa1d41bf3d6a2665c79c8c9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59937834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdbe98394d930109b8c291ca75583e036f0d26c91417b47899ebc54ac6ab6cf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:08 GMT
ADD file:b85ece7344f0ad0749b115e76a51a3b9f322e23bcc8c692cd2edff403ba8840e in / 
# Sat, 28 Dec 2019 04:43:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:49:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5bf261872a9b22035011c2bf77259c73389d0d5786e4b43bee1df89b5dfada2f`  
		Last Modified: Sat, 28 Dec 2019 04:46:24 GMT  
		Size: 45.2 MB (45241644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc7bfba26bbc482688409940aa0ec283a70804eb1cc6d540e0643c19909078`  
		Last Modified: Sat, 28 Dec 2019 05:54:58 GMT  
		Size: 10.3 MB (10323981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2623665c6d27c8c2e9ab44efeae2139d495077f86d1be219a93c300bef788036`  
		Last Modified: Sat, 28 Dec 2019 05:54:56 GMT  
		Size: 4.4 MB (4372209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
