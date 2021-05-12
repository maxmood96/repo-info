## `debian:testing-backports`

```console
$ docker pull debian@sha256:ebf9ef1f6a7a1bc35267af6e5a02bf52ae298950a6d047db8783dc0c500de261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:41a4ab395cf1a8ef0a6183b59fb1fbc1382cc895a0c36d84194045aece09ade3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54897947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277459180bad448c3c9112ade329800212a76313efa9e876015e5f457c1cad67`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:23:36 GMT
ADD file:c01b0e0066701c0767df4bd4031f343aec0e9297361eb5bef1303c304943a088 in / 
# Wed, 12 May 2021 01:23:37 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:23:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:420047682034904224708ffcbc863130ba6bce56f9d642605dccd2d375af6969`  
		Last Modified: Wed, 12 May 2021 01:30:45 GMT  
		Size: 54.9 MB (54897723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059d311e9055ca711b11a62fb7a25cc0d9e9d34bfa29b1bde98ba4f472a4afd3`  
		Last Modified: Wed, 12 May 2021 01:30:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8730c16047fa920bb393af6d593d34b91d7722e56689177972f85e146a6d4a43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52439243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b454c910a1886d27433a4103f72b7401fa00e1c40e6826b3492d81a3f9bb670`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:02:22 GMT
ADD file:25a672d3de6053092579b7acfb24d479714db8f7d145e85311957ef18c02a4d9 in / 
# Wed, 12 May 2021 01:02:25 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:02:50 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bc7aa49e7777af543678240bd21c48814dafda10dfbd613d1864961ea33aff9b`  
		Last Modified: Wed, 12 May 2021 01:13:43 GMT  
		Size: 52.4 MB (52439020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a021b9fd96156ce280b005b83b2f8e31169b9a12ee2f196f80aaa817ca4175ff`  
		Last Modified: Wed, 12 May 2021 01:13:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:193e3ff08330af3a56cb1d1f85bbefe03bc87bb494bf4cb0b373fe27411032f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50102094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5beec4a0f0b43f5d7f70342321342ddd2e0970cf1ca405e3f6cff7b99b658af3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:13:36 GMT
ADD file:73773fba37d57a56c2354a4176f9b0be3578a6f8fe23ed6b12fc87d1f57126d0 in / 
# Wed, 12 May 2021 01:13:41 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:14:05 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cee17f10b1dc96d7050d3028cbf75ee0e927499c8fe8ead51c5a1e75308e48f4`  
		Last Modified: Wed, 12 May 2021 01:22:06 GMT  
		Size: 50.1 MB (50101869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80335a5db6c3812ce2dda352bf91dba6f409856b37e8e2d1197f2a0014472a8b`  
		Last Modified: Wed, 12 May 2021 01:22:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b8b1dd3cab51c94b8d2ef7ebab976cf15856a73d9bf717e37945bd70c3bc53d5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53582850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a18a17830170e931d4c78a8a443e3200bd3b147a7edac2786cdbe602c24c83`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:57:19 GMT
ADD file:8547dbbcd16e89317ea6ca0f6e95003b629d9e8cb415ce91c855fb55a99caaa1 in / 
# Wed, 12 May 2021 00:57:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:57:33 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:721093678769ac87e8bcbcebe8c3b3e98eb8866bb1fb2613606a100b0dd99fd6`  
		Last Modified: Wed, 12 May 2021 01:05:06 GMT  
		Size: 53.6 MB (53582627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5a63fea5c04f7d36356ead180d97a272915b66bf9f1786aabe4789d9eabe9a`  
		Last Modified: Wed, 12 May 2021 01:05:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:adb992d623f7f01da27513ce993e3f283b4606a32b2a398dff63f97fafcca1e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55909602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec073602a2cba1f0804e8ffaa3209e8a05ada07891bbbe358371423c296df02f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:42:16 GMT
ADD file:b4808df881925a58cf88a45b01b479eaf187b30b50efe270b00d42330263141c in / 
# Wed, 12 May 2021 00:42:16 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:42:22 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:79fdfe0cbcd9f084e394a7b80e4087f0d3d949028a2c82540cb182e155070f63`  
		Last Modified: Wed, 12 May 2021 00:50:12 GMT  
		Size: 55.9 MB (55909379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a75e912d778f65db1fe5bc7d3d6bb39ffc3f969b465daac5a994106d46e854`  
		Last Modified: Wed, 12 May 2021 00:50:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:dc5d699cdd77d5806dcec4499b186f1b0fb89b4dae96969ce95e8d6d31a08149
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53151928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639ab37e2321955a045d1a91ea9b220d3d336ddaa3a5a86a8c32e4a6d7f2cf69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:12:02 GMT
ADD file:70424368c5745ba194627063e05b284a3b66c237120637e2ae0698ba4daa417a in / 
# Wed, 12 May 2021 01:12:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:12:10 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b50eb7259e4b880fb905a4293e40f6010ceb16e988a7fccf2191cb2f31b2278f`  
		Last Modified: Wed, 12 May 2021 01:19:52 GMT  
		Size: 53.2 MB (53151705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457a25ad6a4d2c54cde10439faf8b2accf65b2ca455804b6e55c3b255479fe70`  
		Last Modified: Wed, 12 May 2021 01:20:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a40f63dbf85e9e607b676d9c7f011461b827ecc8970b7427d336b0aeffea4b3a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58795482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919ebc971ea41b6174cde5ed39f35900e2a7b210000e2bbf87fc6d42f626ee49`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:37:49 GMT
ADD file:19d7245a9d58f6d6bab388538fd82559f00f5b68b650526f83c9f5471bd42c23 in / 
# Wed, 12 May 2021 01:37:57 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:38:08 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bdb6fa51051143276263acc581c41c185b4f264f90608942d81caa05ae216602`  
		Last Modified: Wed, 12 May 2021 01:49:50 GMT  
		Size: 58.8 MB (58795257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb19685548c06162f16194ea3b0341e1acd355d5ce7a6a7d43933313984cfba`  
		Last Modified: Wed, 12 May 2021 01:50:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:664866a5dc37c22b9bd99befb56b49b0f8d149022fc886a075ce37e81a225b16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53177431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb4d24e47769c22d37516e94c6533fd3fbcb98eaf7e371cd7c0cbc47a18851e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:45:13 GMT
ADD file:06fa5ddf633e03d1a7b4c730088e3d7cdaac7c6c5b5984ce15813118c5171ac7 in / 
# Wed, 12 May 2021 00:45:19 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:45:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:784e1796a94170ee98278d7808b3fe3ef612743b9a024256790bc5705100bf01`  
		Last Modified: Wed, 12 May 2021 00:49:08 GMT  
		Size: 53.2 MB (53177207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb41527716e4bf3fa30de637f7fc2234efbf5e3006c4df9f26eb2f0b0cd01c7`  
		Last Modified: Wed, 12 May 2021 00:49:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
