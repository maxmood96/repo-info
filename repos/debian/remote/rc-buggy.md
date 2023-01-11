## `debian:rc-buggy`

```console
$ docker pull debian@sha256:f04dc5d1044ee0f4a1a9e63162dc783f17a3d5c1198e3078d4e8938099b58d69
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:96186c9a90ba837abbcb7a69cf883c610eea307392b21e754dc25a69b41e29f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49040975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64f7b5e4b2a62c039f5705d804ae60f3f62b6ca59af50cacb9458f15584113b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:41 GMT
ADD file:3bae49887734af64f153e9e3668684efface6dd04ba31139b3d6b3aeb7589128 in / 
# Wed, 11 Jan 2023 02:35:41 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:37:04 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a0e522725e09a558b80e5d58e7b360150ad3fe901915db5358002bba7e461b9c`  
		Last Modified: Wed, 11 Jan 2023 02:40:40 GMT  
		Size: 49.0 MB (49040747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0236c185ae78c3240c4787f67aa6df295e8c95cab2fead8c17840a9a1788318e`  
		Last Modified: Wed, 11 Jan 2023 02:42:46 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:6180f2e9ec600c3baaeda22e557dc23ec1c0d684aa748dee66d06f0580776089
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48018169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edcdcf62f780bf7a9a6646eeba2e6fcd27a8d234ef1ebe7cd366a0215a8c27d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 01:55:48 GMT
ADD file:c258ec7f780b3ff9c8cd584e0032e838b39a09afc46940f4ac745695130b67ed in / 
# Wed, 11 Jan 2023 01:55:50 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 01:57:28 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a63c02841fd8a16e36e06a2fa4539584c2578f39a3f7bd88934a6c67fc294d9e`  
		Last Modified: Wed, 11 Jan 2023 02:01:08 GMT  
		Size: 48.0 MB (48017943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8511b3c682c7b63132d3e00bff6c8575e2ab26a83f56f93ab431b773ce60def0`  
		Last Modified: Wed, 11 Jan 2023 02:03:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:6bc5e7520e74f56604002695658b50a58c6ddb39933aa8135735f10aa9d89bf1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47080909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ae1bd5eca538805d8db82bc7c53038c23a6dd2ecd3a18c900c136a0aaef44a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:59:31 GMT
ADD file:9f6e7ad60906ff390d6369133d129df5057cc1505edafd2cccc2eefa5265ddaf in / 
# Wed, 21 Dec 2022 01:59:32 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:01:13 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4d12d04403dcef32bd0b6201954d02c0de421dabf04dd54d568898f376cb96c5`  
		Last Modified: Wed, 21 Dec 2022 02:07:07 GMT  
		Size: 47.1 MB (47080683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ebe23422c442112a0a3f871266258bf49a89cfd421c44bcb612b5ff476051a`  
		Last Modified: Wed, 21 Dec 2022 02:09:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2032e97b3f0a8a25e0be5795ab0775aa428a61549873361cdb23ea7b12964f67
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49084778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d6d5d998d3b07e7a06e37e78cbe7cc23cf2361875ca92d531cf047a4540299`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:58:15 GMT
ADD file:b780242785904e4fb27dec85c00f7e10bcc0dbb0d7006b133d9038c4328c7d83 in / 
# Wed, 11 Jan 2023 02:58:16 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:59:13 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:57ec0bfa7127b6c459b1b1f099459b850b4fa150e388b2c3ba10105c4a746caf`  
		Last Modified: Wed, 11 Jan 2023 03:02:47 GMT  
		Size: 49.1 MB (49084551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8f54d6fffd7f9efbc59f7b8ca852f84b118247c51ead2cb2559956fafbf5bd`  
		Last Modified: Wed, 11 Jan 2023 03:04:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:b7e16cd8e5be9e6cc3e47adb7a7163f3c059e3d108e61cc43714a2977b931592
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51340353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df8e2f10a407806de4ead3331e27288cddaf8831030fb13c6e377bc5ef3ee0d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:20 GMT
ADD file:d73a77dc412cd093f533d8c6403c7a4a629d7a7d31b1ffc8555e0f7876d98ec3 in / 
# Wed, 21 Dec 2022 01:40:21 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:41:45 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e5477ffb90e4da3fe8a2c9a63f402783b74fb55b190b59240e4d1d7e5b55a2da`  
		Last Modified: Wed, 21 Dec 2022 01:46:35 GMT  
		Size: 51.3 MB (51340127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893750c160ac4d4a8262136ce99c0ed239823e01386d14a9fdb5f9627bcbfe4`  
		Last Modified: Wed, 21 Dec 2022 01:48:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:4784b4da74e5ecd7649c797bcd5566fc636793e2863c92cd68c8459bd1099858
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50293174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f39fd58d2a9059103f0965bf008d54f6129deae35b424bc4f1e9bc33d0026f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:11:07 GMT
ADD file:bc4f0f717f54bc1982dd6d104f684f180c7b8da660351e5be4853a56b38e374f in / 
# Wed, 21 Dec 2022 01:11:13 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:15:28 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:22a773956e0933f1a01038ae977c7c99f46cd5ce02f672c66be9a1c837de4eac`  
		Last Modified: Wed, 21 Dec 2022 01:19:25 GMT  
		Size: 50.3 MB (50292945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbac5846049f646e00726b2427a9325410332fa41ecad99b2ef194b4565aa11`  
		Last Modified: Wed, 21 Dec 2022 01:23:57 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:bdebc967c838bdeb57625c533682f1c4b07277a81911761b391378876b6d0b58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54333215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798b316c2494544076a927932f48584f1da97a100633e960dda0196e47496a3b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:58 GMT
ADD file:4af1feaa33ee2a3c1112b5ed0efbcccec637c4dc23a5af7d55343f6ab7005920 in / 
# Wed, 21 Dec 2022 01:18:01 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:20:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:47dc200f753ddc67a9fec80382c7c2b6f164cb907748c309862373fa8d94c504`  
		Last Modified: Wed, 21 Dec 2022 01:23:50 GMT  
		Size: 54.3 MB (54332986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56334aaa76047ddce75ea1b17b7bc1c38062b9c34153037287836794ea5eb5d5`  
		Last Modified: Wed, 21 Dec 2022 01:26:52 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:2c5907d18e50689678073dd2ac2c69bc48f99a3e9ae45218aa7061fc649c2c8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47434309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29126d40f599335919396b9f83d281dc54ab9a8a39f2a13cd1ca26b12696a029`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:22:39 GMT
ADD file:603b8f38f314737d8b96d7fa7c31b4c6ede8fec5c46d30621085354a718b7cf6 in / 
# Wed, 11 Jan 2023 02:22:43 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:24:38 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:63d179f68a4d4f8c050f7c24ec5c73831d75b928d359ddbbf2e658360463fd13`  
		Last Modified: Wed, 11 Jan 2023 02:27:08 GMT  
		Size: 47.4 MB (47434084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ffb10c437b8cc9b52f50c89b779bc4b800f742e48d41d2b099d8319fcce278`  
		Last Modified: Wed, 11 Jan 2023 02:28:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
