## `debian:rc-buggy`

```console
$ docker pull debian@sha256:9dc0936f1b411c29e114a566fbc2bb76beaa4c296d0f4dd34ccefb29973c6097
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:94eda6771c55d0c3619b329e901b349ee21c5f9626bdde828431aed591f2194b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53272098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1762de392a1548d422e32f58fa85d2f179b070537745b0d216c0fa7da9c25468`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:21:22 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Thu, 17 Oct 2024 00:21:23 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:23:01 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e263ba096289a2844bf39669b475de009f157519e172fc468f4dfe2ede16628`  
		Last Modified: Thu, 17 Oct 2024 00:27:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:a692b0ff12e9022f99d084a573bd1bd4afd31e94824802c1b2739741f07a663f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50147809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcf7d70742fa7d6f12987299175b98ea629e5d2395102cc7a0c3b5f35fca1e5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:41 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Thu, 17 Oct 2024 00:54:42 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:56:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a459f6360e2bf91f40b708330f548dcb15395b373695b1d433ee15f0242804b`  
		Last Modified: Thu, 17 Oct 2024 01:00:32 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:88733e64af1621246040007a6ce6df5e05f0baddeafef85e609a72983aea5857
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47691621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005ec61078a79446531d528fbc6486a223fd21047b0e6249ab8a08a99ca7ca48`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:04:18 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Thu, 17 Oct 2024 03:04:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:06:01 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7286d0952df47aa05d9e3dc5a57ba209e8f0a9dc5cd2e290d503873366257a5a`  
		Last Modified: Thu, 17 Oct 2024 03:11:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4f8d7e2c1cdc0dac820ffc03218644cdb3dc0ce7aa9a43d75f4a8818cd7d17e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53629712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f168efe4c4daa3a658ee36121c5fdbcec6ea7f4ca62aad639f7959253f83f983`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:35 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Thu, 17 Oct 2024 01:12:36 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:13:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3f7e18d97c6b3416611e28364576f97f39cf5231c4b4661ddd1a12b40b9872`  
		Last Modified: Thu, 17 Oct 2024 01:18:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:92044a9e25c84f67cfda2ec3738c88858ae4926a3bff89fdb102aa8c83008a17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54118199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26022125b843dff54aa1c7b7ed44632c0aa12e5e174a466feb1cc0ca9e12969`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:51 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Thu, 17 Oct 2024 00:39:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:41:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4652ef0bcaa9f12c2246ab532cbbe42caf2e2e28f45cc6a97e28afa253a8ca2`  
		Last Modified: Thu, 17 Oct 2024 00:46:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:77130a7f1bf1d02eea7157cf86fe35d4c5ef382dd7d30ce281ecf0d4baf90b1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52158126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a3aa0651f57d18d2a378ed938209aa9aa44a5ef3936b5aee8d2333d5547ef2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:10:11 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Thu, 17 Oct 2024 01:10:17 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:16:22 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37056adead3149ed4af257697f9379e3f68824a4da5c3e2d7aa616459d68ac`  
		Last Modified: Thu, 17 Oct 2024 01:24:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:a8accf8993423ef819d4ba6318672425df1e76a4068260bb34dffb8f0c8df01c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57177048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43d653200a948aafb3858e823003ddd2e59db7539ef730d708022bac8d6e57f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:05 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Thu, 17 Oct 2024 01:19:08 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:21:01 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1988c42eada8f9fab0b0aaf03c4955afe5b85d6035da0dc99e4285952362f3`  
		Last Modified: Thu, 17 Oct 2024 01:24:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:7f880126ce35bd4adb2f91229d3088003be752269375fb8f42ec9c5773b5e1ee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51562910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85c0f34d59c87b644d0a42142e91f047d904a597799f54da163b78adb11de73`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:12 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Thu, 17 Oct 2024 01:09:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:13:41 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6de782ee8b4c5756743904bd15450218e40770be24a8f60c4cd322e6188c45f`  
		Last Modified: Thu, 17 Oct 2024 01:19:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:e9875609be1bf2c1989850646b58e62a8cae03c6c8927a27997484212487eb24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52852203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cb54f2759623153887a332dbf54a0ed54237d9522f900560c24f60c63c9dbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:33 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Thu, 17 Oct 2024 01:46:35 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:49:18 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78af0b69a3452155d0c37eeb885c9766e751076754f37cd9d9fedef23fd9166`  
		Last Modified: Thu, 17 Oct 2024 01:52:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
