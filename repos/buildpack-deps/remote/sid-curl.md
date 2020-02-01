## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:32dc7dd00a32e1946f7a8e54d1550f3373ba81fb59e5d9d1079d4fdde6a47ad0
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6a072ed2846ff5274fcecf3dc370292376fa984090b4a0006ddc4bf96e44dd86
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69582895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e0416cab1b5d1a8103f74fbd2c7e7011132810d438bca9ecf6f0b9e26c5474`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:22:47 GMT
ADD file:68b1541306250f957e5f1035d80f5683c1ed22e73cf2f2b563adc52424897a09 in / 
# Sat, 28 Dec 2019 04:22:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:56:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:57:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d0b468739e287d7cd8fa8bcb34afb10216f12567d28caab345db8873c4246896`  
		Last Modified: Sat, 28 Dec 2019 04:27:19 GMT  
		Size: 51.5 MB (51479608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44261d6f427d89f764fcd9898d2845c7327812575dcc485436bb888b2ee1d0c7`  
		Last Modified: Sat, 28 Dec 2019 05:03:30 GMT  
		Size: 7.9 MB (7919965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd42132ce8afeea96ec992f4170f1b4fe9fa1a621a93dc2d236088351e29685`  
		Last Modified: Sat, 28 Dec 2019 05:03:30 GMT  
		Size: 10.2 MB (10183322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d28739f5005c3fbff72dea17bfaee8dd0ebda10ab7646964c1122c513cfc89d2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66847863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665aece8839d5ca6cb66867e56490c9abefe85748d63d6faeabcda81b228bd99`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:51:51 GMT
ADD file:03cc60d1d72b99d3b1d122da1d59f729e29848dbbf6dd18cbf657a4c38ef0b5f in / 
# Sat, 28 Dec 2019 04:51:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:38:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:38:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:58904a701fa9ff155e476053cdd7da105682fd34a283dfecfc029765d82bc148`  
		Last Modified: Sat, 28 Dec 2019 04:58:52 GMT  
		Size: 49.5 MB (49475991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8962cbd68da3db27dc20b92f9e448d10c3a6823e53156f2ba301e54789b010`  
		Last Modified: Sat, 28 Dec 2019 05:53:19 GMT  
		Size: 7.5 MB (7494157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f950a4075ac360274a49d98d4a4c73c351f221ac1f7acf157df1e1b62627fe`  
		Last Modified: Sat, 28 Dec 2019 05:53:20 GMT  
		Size: 9.9 MB (9877715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3e6a323cf8b0c4065f78e624adf6b51dc662e1e2c8eacf5d2274abc24154d66b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63974345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457437be464e169b41259e1fecc75ee1db7cde9b94e133ee11f6b078f0f3c0b3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:01:32 GMT
ADD file:b5c7da33763f5d6cace9605e53bf483375c1f792de0982f47885c85b47304392 in / 
# Sat, 28 Dec 2019 05:01:36 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:55:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:56:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9d5856d0eb425d736e9f4c60a79333c1933bada38a126c109eff8f1eb43a9c21`  
		Last Modified: Sat, 28 Dec 2019 05:09:48 GMT  
		Size: 47.2 MB (47210722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3768cabb2504bdc0d3bf15c2e022ab2e94f61e198eb24b077cb6c5e620d5ac`  
		Last Modified: Sat, 28 Dec 2019 07:09:45 GMT  
		Size: 7.2 MB (7234041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfad613eea011450300250c8f76f687229e6483a59e575849962e519e171c0b5`  
		Last Modified: Sat, 28 Dec 2019 07:09:45 GMT  
		Size: 9.5 MB (9529582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6f72ad10ec6f1980ca1d9e1563a7f60fac241d7b1a5806ac6fb4d3097099fbbf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68551681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198216a0da7f9255c3d05108c9781f871197b9debedc93bcc2242aca845a4372`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:58 GMT
ADD file:636edb6845120aa418f3291c0858ab38c7d658cb2790c08b113e8068fe152a32 in / 
# Sat, 01 Feb 2020 16:42:00 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:26:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:26:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a3f06cbd9a524c44b9b8c92922dc9c06d87668d76af414bd34aeb7238502e475`  
		Last Modified: Sat, 01 Feb 2020 16:47:18 GMT  
		Size: 50.5 MB (50505966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66da598f357ac8ab4c813dc7a16cf57b1d0fdc7579b59a9a2cee24efb09f057d`  
		Last Modified: Sat, 01 Feb 2020 17:37:33 GMT  
		Size: 7.8 MB (7793001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a8f172b9e64796699f56dc5a838982165c0591f68740791b1d1e8971e09602`  
		Last Modified: Sat, 01 Feb 2020 17:37:50 GMT  
		Size: 10.3 MB (10252714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:26ab61b13abcf9a44c08aa0b9c60d748ede05d95fb2037ee555f41e82ae5cdda
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71395451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6c43c712fd8fda7a88e24090be4b4e9f3c12eab94d9f52dd781b792292e463`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:00 GMT
ADD file:941e54a7461d61d84748dacc44e888cce50acfb10e34f38a7e4083e19f23b7ce in / 
# Sat, 01 Feb 2020 16:41:01 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:36:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:36:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8901e4e25f1677947cce32c9111e1a14e167a08c1c9b0f38aa3b62ad8dfa24aa`  
		Last Modified: Sat, 01 Feb 2020 16:46:18 GMT  
		Size: 52.7 MB (52679793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a37f13c8736e8d302836bf7f36d02b6d21c78ea34eaa0d441bfac8ab1e8c15`  
		Last Modified: Sat, 01 Feb 2020 17:44:29 GMT  
		Size: 8.1 MB (8093419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf161fe0fa72e46e5ea25da7008f0141c7c33bd269c543c8f95df1e56c25b90a`  
		Last Modified: Sat, 01 Feb 2020 17:44:29 GMT  
		Size: 10.6 MB (10622239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:59949494fcd4f5ac5603368b5e8b05599ae015265a73994ba492b926dc7e45c2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74583647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fd1b12f2f6b339e667ea209637e5482f2801ff17149a4b9a5f0223c8332c65`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:44 GMT
ADD file:d7ba1f92f51134645d0c28cccf74dc6cc9cff62c18d1e7ea24e9306b603cc4c6 in / 
# Sat, 28 Dec 2019 04:21:49 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:04:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:04:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a19f8e61b2d8b008c7115d66fcae892bce80e022931657219cecb2a15110c398`  
		Last Modified: Sat, 28 Dec 2019 04:29:56 GMT  
		Size: 55.3 MB (55284979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814b37b063181f0e69d2ffc211b88d130aa8935273a93f9155d2df7a1bf9c150`  
		Last Modified: Sat, 28 Dec 2019 07:23:51 GMT  
		Size: 8.4 MB (8352650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1122a79a4397f123afc0998256257fa3fcdfa99567d9a6e43d19cdaac02f9ee`  
		Last Modified: Sat, 28 Dec 2019 07:23:51 GMT  
		Size: 10.9 MB (10946018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2b3b032bc4de8c276b6ab2a224c871c9c71acfedee8973697c1e98b63ebdd275
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67792557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab69d514bea7130b515830fde78c847335d5be99cd8f7f194760fb47ecad57c8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:32 GMT
ADD file:ebe1df568622bb8e8e8e3b2318d11550389d84f3196d3ade9aaa9ecfdecd1028 in / 
# Sat, 28 Dec 2019 04:42:32 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:47:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:47:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7d0208a582df93acf7a81d059abd969865a1e647765a53c87e2123fb6b283a34`  
		Last Modified: Sat, 28 Dec 2019 04:45:42 GMT  
		Size: 50.1 MB (50131585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46a42bc5c7805eb22e48c27565c0a108b60dd3c74386aea7cb2a2b367d00d07`  
		Last Modified: Sat, 28 Dec 2019 05:54:12 GMT  
		Size: 7.6 MB (7591630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77c311db77933f5cbc7d2dc6e649e1d95c34ce4c806932601722b88f9b28a61`  
		Last Modified: Sat, 28 Dec 2019 05:54:12 GMT  
		Size: 10.1 MB (10069342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
