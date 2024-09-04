## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:f3a4197dfc1d8b28321950ff62769a06d90f912a6f2b545ff195945976318231
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d8514e63c4a3c2e2f85d4780764a310dd571053dcebfd8a0272122338b1b2a9d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73269774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda8c74ff25e51a0b26780901814ecb3e483a365f6c61063abc2624f7e46ece9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:11 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
# Tue, 13 Aug 2024 00:22:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:47:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000d3eb244249a76a53e7b3f03c8e999bbac83be7058bc1aa1fe0eebb494baf`  
		Last Modified: Tue, 13 Aug 2024 00:52:48 GMT  
		Size: 20.4 MB (20428585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:74a6d5c9024d72b7884bf858c33e518a1543ad7d7efb7edaf5e835a5cfdf8fac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69312471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccc470cd309502af687f9b3a2bf5569a07ac66f2f48fef3e0f34bd5bb62206d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:57 GMT
ADD file:368997aa7bc3d0c868f5058460057cbd845e2ba7a356c40f3a1573421e53e41d in / 
# Tue, 13 Aug 2024 00:56:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:12ffeaa53d9595553187a53d5abdc0f1c023c82e8a57f8058812fe9bc5e86aef`  
		Last Modified: Tue, 13 Aug 2024 01:01:44 GMT  
		Size: 49.9 MB (49871614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e1ca7e0ec63179505bc4d7b369ec98cb8968fcebcdb5cc723a2d9011e899`  
		Last Modified: Tue, 13 Aug 2024 01:33:03 GMT  
		Size: 19.4 MB (19440857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e4e94f528331556fb1aa524c96d1c0d359010bce1f3f4a08f39b186084aa54b4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66130810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dd430a07ecd5eddd1a860b3ddfcd084f68b640451c3cbe7b6b87142a6d1c18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:59:15 GMT
ADD file:99761e9b65792d17a2f1d115ea8ad35dbc2936acb0f636cbbbcf63ed20bf10c8 in / 
# Tue, 13 Aug 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:30:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8bfff960de1d4efc80e46f547c59070161e89055685b260aa43880326ecea728`  
		Last Modified: Tue, 13 Aug 2024 01:03:57 GMT  
		Size: 47.4 MB (47364130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd50d3da00085a24eb625c358426e1b80bf8ce08f61490cb333acadcd859662`  
		Last Modified: Tue, 13 Aug 2024 01:35:26 GMT  
		Size: 18.8 MB (18766680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:df1b58b717328f01a3319f41400cb48c12ea81760537ed99307bdbd2b9696f7a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73829151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8952df3538af05ac37f9c33f6947b1d08bd149d5179bf1575d8ef3dc1a5270`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:11 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
# Wed, 04 Sep 2024 21:41:12 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d236efb8ab77adb7cfeaa0b050d56eeb60763492d44b452ca5124c4dc3e14`  
		Last Modified: Wed, 04 Sep 2024 22:10:41 GMT  
		Size: 20.2 MB (20234813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5d4fec0eb7d196988a99411e3ceb68545272536f7c53235a2c611ec0d9ecd380
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75222611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98cf295bc53b37cf4460d54ffcde842606c4ed9ef6385b5b153980e8310264e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:15f4221d0909a0a194569119853ff29658dc1f889737b850287710eea385be9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72451746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c21850609b583715012b80582f592f169ead5c14fa3533424ba84be9efd2b5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:18:15 GMT
ADD file:bcae38f0c6409385ec90f5e766061248a9443b81bfb083c2bb38b2fee95e3241 in / 
# Tue, 13 Aug 2024 00:18:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:75b1f153ec57b50eabb508ba15b89fcf272ebf8f1075f5358064b7d13318179d`  
		Last Modified: Tue, 13 Aug 2024 00:29:38 GMT  
		Size: 51.7 MB (51717612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc5979bb9a19cf877f4c704e0c836440a8fb779e7dc36bf701723c94696438e`  
		Last Modified: Tue, 13 Aug 2024 01:41:12 GMT  
		Size: 20.7 MB (20734134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3bce3224a9ba2a7d7a2cb0c7f63972f5b9da48d9a06cd80cb52215aad19bca96
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79857919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5b17d7afcbb3df3e911dcec159e948d29c4cc333f4c25c7ef7826182f426b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:24:25 GMT
ADD file:2ecbeb97ee4f1fa94ffb8d689b43061a3e219246a7cdcde111969dcdcac0aa81 in / 
# Tue, 13 Aug 2024 00:24:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a059b294be9a535ead3acf658974bcf9ec161d20023a04804c129791e3dccbc`  
		Last Modified: Tue, 13 Aug 2024 00:30:11 GMT  
		Size: 56.8 MB (56775584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9beceed51fa25589c06ddeea2d1cf90183fe7061b5f0c746fde5c8782f8e623c`  
		Last Modified: Tue, 13 Aug 2024 01:38:19 GMT  
		Size: 23.1 MB (23082335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d3b907b51131d5d2b70343e955daeb1d39c52afa545332bedd50924f6e57560a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70873705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f7d9fcb1032a127bae5c6f5d1b116341dd27b2dc10788c5f24d37adeb9402b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:13:20 GMT
ADD file:83cbcb6055e53dd5bbbdb284d5c1129bd8ef0b02c2f174e4bad8a86a9a470700 in / 
# Tue, 13 Aug 2024 00:13:22 GMT
CMD ["bash"]
# Wed, 14 Aug 2024 18:09:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:664f4e8f311a644728086c0fb1ccd2a113bc5c8af1174d6b42e68ae243e81646`  
		Last Modified: Tue, 13 Aug 2024 00:18:53 GMT  
		Size: 51.1 MB (51127228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291979be21ad443cd3fd97607b813c6af48dece7333db3d66cb6aeba7d3399db`  
		Last Modified: Wed, 14 Aug 2024 18:10:32 GMT  
		Size: 19.7 MB (19746477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f204e1391edd06914c2eb6ab6bd9d83380b14aed0842bfed5c8e1c04ddc2bb28
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74014141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce202fb8d3590d31c47d7b239b0472150c735cb7bdd5ff6baa8e017741285e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:45:25 GMT
ADD file:44d3a49280c3105abcfd85839c96a9ede97d8553a9bf4a53c274041f1929ef4b in / 
# Tue, 13 Aug 2024 00:45:28 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3b50b414b30fa7e2898d8a041d2ca183b6d95dae25e656b8d6bec87a2fd533b9`  
		Last Modified: Tue, 13 Aug 2024 00:49:42 GMT  
		Size: 52.5 MB (52480914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef15ecd64bb80ffd29cdce30241b3a9b2dda360fd5c66fc2caee9b085278bea5`  
		Last Modified: Tue, 13 Aug 2024 01:27:05 GMT  
		Size: 21.5 MB (21533227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
