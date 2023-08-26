## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:a16ee2f636e6c8c0d299604290de437590dbadf77cefb273992c067588a1cbef
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:320419383c5722c312ac3276a605568187bc2648d38c7d27c540d28de9d1fb9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69858085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003ab260ff03f81f050638da4297dfffcb7a999f85c02dcf58da0c9c100afddf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:02:32 GMT
ADD file:1170cd4ff0eb634606742ce298b7bef45db4b76df3573e41853850f4bb1fab87 in / 
# Wed, 16 Aug 2023 01:02:32 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 03:51:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4c74a9d7ecb9b51b7ca655015e97fe63c4c4643adaf35c9af51956deead7d037`  
		Last Modified: Wed, 16 Aug 2023 01:08:58 GMT  
		Size: 49.6 MB (49604152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2680ce991d97fcdc7ea794a58be8b5d9d19b0e51227bc662513d81e46b8554`  
		Last Modified: Sat, 26 Aug 2023 03:54:07 GMT  
		Size: 20.3 MB (20253933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c0849926a45b2c03c11a9782b7bddc34172517e4e92a0c683616566fc8b8e8a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67645396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2618e8d298d5ab31281cdeb2f17c60c23978b45a81b1b043b045f2500200a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:49:56 GMT
ADD file:d0da838ea8ff64a44e445dfb0001a4f6a2442085f0c0f942d0129b6f8054c7fa in / 
# Tue, 15 Aug 2023 23:49:56 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 01:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6d8f24fa9802404161e1d0ef0d1db6d5f4c20cb1f0e5884dd191e1d77f2373c`  
		Last Modified: Tue, 15 Aug 2023 23:54:43 GMT  
		Size: 47.4 MB (47395127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f867d323ed66972b6c492120ce3fa78d7e1d63e0279362a9a55229db8e7127`  
		Last Modified: Sat, 26 Aug 2023 02:00:38 GMT  
		Size: 20.3 MB (20250269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:527f2cdddf2c9686c79c4997c11b9e869016e5e0d5338225226a7696dab9798d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63776111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78878a837b2ec98d20d18e509dd342540cecb3b4e627905abed243e64146ba45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:19:37 GMT
ADD file:fcc6e87e54bebf4c148573f42bb67ddfe40bbb89b37b0c88d5a5ac8074852e50 in / 
# Wed, 16 Aug 2023 00:19:38 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 03:22:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:00b7ed9deba9ea7ab64452a4e5dfd73f0f68e2784fb8cd589dc15932edf9a46b`  
		Last Modified: Wed, 16 Aug 2023 00:25:41 GMT  
		Size: 45.2 MB (45176042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ab9b63e935a21ead032541d64b9383f6f790c568ab43af2005788226208270`  
		Last Modified: Sat, 26 Aug 2023 03:25:56 GMT  
		Size: 18.6 MB (18600069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:07a6298feb693f4d212aead137b90806a90e5224731919ae7fd085593fdd52f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69560118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83daf480e727a68a12ae06eac0e0ce21b12c83090213b1f8505f30b8ada3554`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:42 GMT
ADD file:16621389c05de9ece6b8d40e6c62ca81465940296cc58f7f1c56571fac05b33e in / 
# Tue, 15 Aug 2023 23:41:43 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 02:57:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c5fc9f67522f8eb1fc65844ccc91e1d93595f85d410842d334c85f7e0a15d841`  
		Last Modified: Tue, 15 Aug 2023 23:47:22 GMT  
		Size: 49.5 MB (49521978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392c849b78c27f87cf11f7bfc3a6c274880955ddcf718ceae8fe425a331d69fb`  
		Last Modified: Sat, 26 Aug 2023 02:59:50 GMT  
		Size: 20.0 MB (20038140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ae903244a0a7c407c348c787c1d71a807c2c4967fd0fea7cb34ed756fbb45ea9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71458433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75af6cb3cd46b8071500f06c320433c0fabeeb760fc4d382feac7d689b378466`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:32 GMT
ADD file:4d14eb57255656e664c93bdd44713aab3556f53199d3002e8b099b8a4f99ee66 in / 
# Tue, 15 Aug 2023 23:41:33 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 05:50:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92cb61533d6d73bc90b946ae69c5db6942d13512056cb4f565d14697cd7aa909`  
		Last Modified: Tue, 15 Aug 2023 23:48:22 GMT  
		Size: 50.6 MB (50618535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb29c4acf204aca1bac764fe7dc16e996b09849724a7e8aa9f0ad59c78a11e75`  
		Last Modified: Sat, 26 Aug 2023 05:53:36 GMT  
		Size: 20.8 MB (20839898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:be746b42835eaee36ca78347f90b242e18287e4c37e9e41454a7c3d4921a8253
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69008984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4ed154937e727781cd89f035d20789c5dbd95241f35f970000a354154c027b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:15:24 GMT
ADD file:21a0349f8818b8dfb23d9795ca922c9828660ac081ba9db3e4fe08efddeef0dc in / 
# Wed, 16 Aug 2023 00:15:29 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 02:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b01e2a8b457425ca543dc2e5fd0920c4c1baf753962560010906ca5d157fb3dc`  
		Last Modified: Wed, 16 Aug 2023 00:26:31 GMT  
		Size: 49.4 MB (49449783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951b7568185112b7ae667741ad45f90e22219bb33f27fe4b15461aea0fc1766e`  
		Last Modified: Sat, 26 Aug 2023 02:46:44 GMT  
		Size: 19.6 MB (19559201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:934ea4f5b325be2af72834eefee6d850a4860b8fe2f275065db6f1ee18df363c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79236191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05a618094778f6c639e3a734416548242b5829e84e79092ed10cfdcfbd75291`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:16:38 GMT
ADD file:28e774b3554d274fc742feac48f78a3bf6f120cb729e2824007dd94d5c414156 in / 
# Tue, 23 May 2023 01:16:40 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:45:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e109feef3fc6307cd9a880958cef6624de9c2c6f054987e479461a1ae51c7503`  
		Last Modified: Tue, 23 May 2023 01:20:49 GMT  
		Size: 53.3 MB (53312324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab84a55cc084469df8b38ab6a01658bfba2b29b7410a970ba6d9d2864846672`  
		Last Modified: Tue, 23 May 2023 01:59:19 GMT  
		Size: 25.9 MB (25923867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22bed57474f02f8fdab1953e387be86aedf43d44248f245cb15b61ddf2f53949
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68464444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f68849b5e250c2d0418721df67f9b0d87e971292a2a75ad2334bfa4d2c0106`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:45:32 GMT
ADD file:d99fe1ff201690fcb871123822de04002451af1e06ae75e1a18fd80ef531de86 in / 
# Tue, 15 Aug 2023 23:45:38 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 02:51:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:73c53ccb564b87caad8f214df94d16496ce4754e4b20ee558b3c8f3ac938e41a`  
		Last Modified: Tue, 15 Aug 2023 23:50:14 GMT  
		Size: 48.5 MB (48539809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a53bb03e6b4b7d81815de0b07a64fcbe6daba956f76e89e89d7b363f2792c8`  
		Last Modified: Sat, 26 Aug 2023 02:55:22 GMT  
		Size: 19.9 MB (19924635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
