## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:da401452000c8402d9204bd1021aece2222242a49695cdd42c12f0c60d02a5ed
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

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1188bf8e99d160a3c226aafc7c799a0ad149eb3f6fdb99bddf16d0fc6624aa7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71047046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3daa7ad5dfdd4bacbfa1c950fe1c68cfd3d10f276bc1218936f710b50c924a5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:40 GMT
ADD file:6944d322f4c04bd2192061822af5cbec8ac0a6b424c461d66174d32aed604972 in / 
# Tue, 23 Aug 2022 00:20:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 00:48:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1671565cc8df8c365c9b661d3fbc164e73d01f1b0430c6179588428f99a9da2e`  
		Last Modified: Tue, 23 Aug 2022 00:24:32 GMT  
		Size: 55.0 MB (55007555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e94d13e55e7a4ef17ff21376f57fb95c7e1706931f8704aa99260968d81f6e4`  
		Last Modified: Tue, 23 Aug 2022 00:55:37 GMT  
		Size: 5.2 MB (5163019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c7528c685216129e8e67bf362a7702e7b1daa585ab85546a41508830657d6`  
		Last Modified: Tue, 23 Aug 2022 00:55:38 GMT  
		Size: 10.9 MB (10876472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b37068ff29d49f3d2147b16e9365d9a9c6428506d3787af90b13b7a6b787f0b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68181734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc48fff76e4daf904cc8a1316ab9db624c7d2e19261dc7858395aec7733a98e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:48:56 GMT
ADD file:65b6a0035ef4a346da86a22a499673984c4b73a4b452d00e2c4b98602c549f15 in / 
# Tue, 02 Aug 2022 00:48:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:20:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5826f50a5f3740e379d88292ebffeaeb2ade015a12b20a318da380c24d4f15eb`  
		Last Modified: Tue, 02 Aug 2022 00:55:32 GMT  
		Size: 52.5 MB (52537339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d82149657cf6707459a498876268409796397ee5bc67b9601847fd7f1802cf9`  
		Last Modified: Tue, 02 Aug 2022 01:30:26 GMT  
		Size: 5.1 MB (5070704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b5b336b172a8f3853e2662363701eca7bb1cf8f3c22f2317eb0be0f914b652`  
		Last Modified: Tue, 02 Aug 2022 01:30:27 GMT  
		Size: 10.6 MB (10573691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7431c6d03fbc43421896b8fa2a87259b5c84329218dfce6078f775ad62311a99
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65344095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0b88cce511eaaaa1e12d3f3e38ed6668be64a1991dc2068e1cc9bf85096601`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:36 GMT
ADD file:4e2780cf1c53cc1c475d2ebae48d4bf03029fa68ba9fbc991be76ac9e3944977 in / 
# Tue, 02 Aug 2022 00:58:37 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:47:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:05aa23077de69478dfc20e56aa2d54a2b13bbef07c4d2578524585d098af4e72`  
		Last Modified: Tue, 02 Aug 2022 01:06:07 GMT  
		Size: 50.2 MB (50195271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a4ec510d3ede75fd285276ee8b3d9dd3c1d2bce8f21ae0f2de4898c015b9e`  
		Last Modified: Tue, 02 Aug 2022 02:09:14 GMT  
		Size: 4.9 MB (4930860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef792f88dc77db1940eec048a6d0b4d691c7650b28cd058aed9314fea5f708b6`  
		Last Modified: Tue, 02 Aug 2022 02:09:14 GMT  
		Size: 10.2 MB (10217964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4b189d6e3695953f5e43fa5acdc95c35f840d736d37e1db4805b6329fd725cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69489400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f592236f4f3e3748dfc61da60dd44e60e4dbeb9d5d0d030b3696ca8ae8831dea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:24 GMT
ADD file:5972a7ce0f1d89d63e5ed48011838c998fa506cd34f8e5f0b0070039cd74c5b9 in / 
# Tue, 02 Aug 2022 00:40:25 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:24:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:114ba63dd73a866ac1bb59fe594dfd218f44ac9b4fa4b2c68499da5584fcfa9d`  
		Last Modified: Tue, 02 Aug 2022 00:45:33 GMT  
		Size: 53.7 MB (53683005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0b8a8acead4d7bf71c232054b2a0a8e08eb3e1e2cf46f9f3dba68723e88c85`  
		Last Modified: Tue, 02 Aug 2022 01:44:32 GMT  
		Size: 5.1 MB (5148901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ea641ee67989acdb6af3d8b9b984ecd751a2a83c3b7ce071542b31c9ac1304`  
		Last Modified: Tue, 02 Aug 2022 01:44:33 GMT  
		Size: 10.7 MB (10657494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0d9e01a77b19864476557d06dadfb768771a3b89333dbbf3b7c3fd10138e3fa7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72131190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c00fec5790de3e13e4285b83054a6850bd58812ba11a6858bbfc8607533256b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:24 GMT
ADD file:4012c41187a03bdb3d37bec80f6255a1d46582e3ed145b4f313e42196529e524 in / 
# Tue, 23 Aug 2022 01:02:25 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:31:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:31:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6f683b9c66ef80b527ee5e4cb11969c6e0c1400ab69a4f1279af90f5766d70c7`  
		Last Modified: Tue, 23 Aug 2022 01:07:53 GMT  
		Size: 56.0 MB (56012624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f506948c8aa6d2e0693b583a388ce5e10b4393763bd2ea2529af3bfaa07f0c92`  
		Last Modified: Tue, 23 Aug 2022 01:40:01 GMT  
		Size: 5.1 MB (5085725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915cb3138c0c978b1806934d3f979cff24ecaed321fe7e13caa292cf9ca73dcc`  
		Last Modified: Tue, 23 Aug 2022 01:40:01 GMT  
		Size: 11.0 MB (11032841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0fad16d0bfb6f3a1cadf34a7e5b22899a0fd5649db378901d71f997ddd61329a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69047905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b87c27a1389d392de0afbc828bcedf593a59537ed475ac24928af644c94240`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:09:59 GMT
ADD file:d4bcd76354f6ce92e52e206333ebbe2399c24e2ee5b19ae5f758b25dbda35efa in / 
# Tue, 02 Aug 2022 01:10:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:53:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3b6232334ba5947043903a2c95b6b7c6e6b613d66b10b9cad82702032585b0d8`  
		Last Modified: Tue, 02 Aug 2022 01:20:18 GMT  
		Size: 53.3 MB (53263487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77db3f931ef8e6c6e59d3af4773381ee1557b70b35c21e01543324bf664e132`  
		Last Modified: Tue, 02 Aug 2022 02:24:11 GMT  
		Size: 5.1 MB (5123478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cd018f526c1a738a2f7b90dbeb1439a31059e66e9d09c98807c316b6c72e1a`  
		Last Modified: Tue, 02 Aug 2022 02:24:13 GMT  
		Size: 10.7 MB (10660940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:64f26f5a77709edaa947d88565f4b338743f8a30545beea0ec7ec06871de0bab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75937343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbfe17ebeeba3b4d729b5692d812d417575c82c7d89b8c1871009f0980988b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:09 GMT
ADD file:1f74997bc1d99e4422725846bbc41271bfe62a55c74ceca37359472aa428233c in / 
# Tue, 02 Aug 2022 01:17:12 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 02:28:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6e9f012d4ab4ee25199c288014d1f6269e3700e4e09eb5ae543813498561f2fe`  
		Last Modified: Tue, 02 Aug 2022 01:24:00 GMT  
		Size: 58.9 MB (58895967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d6dd9efc333a569ba52868102f1e78cd75b0efffc233c5c65ba5945d450e63`  
		Last Modified: Tue, 02 Aug 2022 03:13:51 GMT  
		Size: 5.4 MB (5412588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2455336548c69e380d20bd4477ade107af9001c638afb2afb34020b626a8444`  
		Last Modified: Tue, 02 Aug 2022 03:13:52 GMT  
		Size: 11.6 MB (11628788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:eef5a7af835f77a13fdc5a093dd33fffc7839d60621afc3d6776b58137576fd7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69176033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df46931d58fe1ae710ee8d10584d79b88bd60272686ced0798071277caeada5d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:09 GMT
ADD file:86774aefa6717c0535c25f8700d8730f44cc43c33371edeb7dbd33e29cb68d32 in / 
# Tue, 02 Aug 2022 00:42:12 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:08:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:08:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:718eef7927531d5ec3c355d6b6e5c4ab83c23778e693b087ac8a3b9adb4f63e0`  
		Last Modified: Tue, 02 Aug 2022 00:47:40 GMT  
		Size: 53.3 MB (53269308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c9e8bd2b82703a7391c7c97d600a7dd7c19920de10bdd95845e75ef24b782`  
		Last Modified: Tue, 02 Aug 2022 01:35:15 GMT  
		Size: 5.1 MB (5141077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c031131df71d864714d521c4e6f6628302c2013df50dfbc03a037f443dc7e2`  
		Last Modified: Tue, 02 Aug 2022 01:35:15 GMT  
		Size: 10.8 MB (10765648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
