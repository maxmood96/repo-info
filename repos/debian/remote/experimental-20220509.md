## `debian:experimental-20220509`

```console
$ docker pull debian@sha256:030f201daea8d750a656bd95070597ad21b569a997ba4016c9fc63d873ccfcc5
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

### `debian:experimental-20220509` - linux; amd64

```console
$ docker pull debian@sha256:277e0a88f463ba1885122ebb9adb881e33bf707180bb0385b13a1bdc6fd284d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53147374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1482fe2c7cb52ea1190dce699b0244f7f4d4fed96a3d1d8b57428646625d85db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:22:45 GMT
ADD file:7eff711e1a70eb1d1484892b9709814001da8a37e00431a22c03764ef9f0a5c7 in / 
# Wed, 11 May 2022 01:22:46 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:22:56 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:74eb7a1f108de67c086990b41789af4c613fa1537617a0d1858f68b66ad33a4c`  
		Last Modified: Wed, 11 May 2022 01:29:54 GMT  
		Size: 53.1 MB (53147154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53993909c717e4d013c439601f248c53a4e43664b7b42dce7a7a630f30f5c5b`  
		Last Modified: Wed, 11 May 2022 01:30:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220509` - linux; arm variant v5

```console
$ docker pull debian@sha256:bddb06b0f6965ac4b7ded82ced103322547df94ecde0a7e6eeea612a9ea6d959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50940069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8b79f0bb68044d2ae1551b33743f9e106125cbeb6804cfaabb3a67ea6b8d53`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:57:31 GMT
ADD file:3b98d75470b5342f06179d466794e6a231be41b0a3d3c94b6ae0efbdcbb9a74c in / 
# Wed, 11 May 2022 00:57:32 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:58:04 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:be71d4ded79eb5a181be2fe43c5f3f8e0e79c48fcef2a4b538396eb809b84547`  
		Last Modified: Wed, 11 May 2022 01:15:47 GMT  
		Size: 50.9 MB (50939848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5c84c2be9c8faed852a449321696e10b06f0cb595e2ab1c0048bdfba46abb2`  
		Last Modified: Wed, 11 May 2022 01:16:27 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220509` - linux; arm variant v7

```console
$ docker pull debian@sha256:672848b8cb15ddda5c9bf46ad7b05c1bfa447ddb1ed6f555d38da0da35381cb8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48678526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f41bb242eb14c0b12594dca8354619a4a779504ff528e0ea245048e633f7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:56:41 GMT
ADD file:feaa047701029ef35f79de94e47613b9069921d84667ea4a3de1dfc6d195b1a8 in / 
# Wed, 11 May 2022 01:56:42 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:57:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b8663dc9a70b670066e8632337e01951b4f2400a973cb02548508d5b27b49da7`  
		Last Modified: Wed, 11 May 2022 02:13:53 GMT  
		Size: 48.7 MB (48678308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bf44f3121f10ba13592a83a999f3403e8ef1f432827bf29458b4280543b698`  
		Last Modified: Wed, 11 May 2022 02:14:31 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220509` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1852de7a47ca58d2d7b4be64829177aed754fad925d55d8b01b7c4990f380036
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52243056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e80dfe21709b69bbd3c2fd1590e030bb3a8d84f289092c515308187d32e9790`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:57 GMT
ADD file:fb7b0c7243ece3153eb6384652f30d9b27358cad7fe3cb9e7b9a5cce9c268453 in / 
# Wed, 11 May 2022 00:49:58 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:50:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a230e1d39c988e206018433051d04df8420485ea18f0101acf80feb46b9a266a`  
		Last Modified: Wed, 11 May 2022 00:58:58 GMT  
		Size: 52.2 MB (52242835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b332b7b85d000137009262d3ac041cf388eb697b76fbd5ba48587c6476c4c199`  
		Last Modified: Wed, 11 May 2022 00:59:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220509` - linux; 386

```console
$ docker pull debian@sha256:798208f046e907724674da5bb716987444e11fb331e1200221c4ab07c1740a1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54146183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57324c50dfac6a2df11d5f9bec06dab960f527e76a0ccab88ea74795d7e1af85`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:42:23 GMT
ADD file:7cc5f2c300a500df4182f1c15fa359f0c8fcdccd99f867f41de25a9b00631bf8 in / 
# Wed, 11 May 2022 01:42:23 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:42:38 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:453b928821b105cc2eb7dc2481b9a80b3f1c158a461a40ca9c66204adcb674c4`  
		Last Modified: Wed, 11 May 2022 01:51:59 GMT  
		Size: 54.1 MB (54145961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2f9cfa21f37c0625b89ce0f40556ed48b284d0e6540f0dedc657e8685e0fb`  
		Last Modified: Wed, 11 May 2022 01:52:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220509` - linux; mips64le

```console
$ docker pull debian@sha256:adab2ad28652930d9ba4f0bae9ec059621b659030641352b3d8c21562dbdb1a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52268589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befe5f0f6bb19eb516a22e3099ff692e9ab5aa73dfe1e4b2dbb7a084e694d0c1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:29:37 GMT
ADD file:abfd357a115291ca41c0c5f26dcb21b075edd22fd8fff1174885342ee2d6be6d in / 
# Wed, 11 May 2022 02:29:42 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:30:19 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3265dad9b102c21609195de4c7b031c477dc6fe8ac02054d782fc719ca14b6bf`  
		Last Modified: Wed, 11 May 2022 02:40:36 GMT  
		Size: 52.3 MB (52268366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ee714b46e31134f953f415a6bf5bf6fc29d12c1b99cb2052ee2287ca26c36d`  
		Last Modified: Wed, 11 May 2022 02:41:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220509` - linux; ppc64le

```console
$ docker pull debian@sha256:641484f562861b68f84b7331d6e83af90c90244d8fa08ac3434ccf94f6e42fab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57352616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2276562fa92512e728c3e81f9d92dceb3a31919289ed3f6918cc76db4d312fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:37:59 GMT
ADD file:d609df19ea9759b393191a81b6f3f7908587d527836d2da5da57be6553a7f269 in / 
# Wed, 11 May 2022 01:38:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:38:46 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:54515ce7c2170e51c7779447710a1e1f0f0e40fb39cc75ff772811675b7b2f39`  
		Last Modified: Wed, 11 May 2022 01:47:47 GMT  
		Size: 57.4 MB (57352393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7e563103939da01d611631d9c6042ac9ba8841d8b3f030c1e73f77b0faee1f`  
		Last Modified: Wed, 11 May 2022 01:48:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220509` - linux; riscv64

```console
$ docker pull debian@sha256:6a3edc349738b7b8ee1ef03b62a110d421608361d124b935715e220effbbe79a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49377941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf54f5c12ef8c1ac81e298f078d6a5527c58745721e7a2dd7929e74fc89da617`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:18:59 GMT
ADD file:7325edeeeaf5959d6f5659ad3230bcfccaf4d5c3ff57d3006bf46d1d1d7ce623 in / 
# Wed, 11 May 2022 01:19:02 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:22:38 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9be57321a5b75bf9029368d5064dd36539cd46296afd8b04bb83cb9c46cfe37d`  
		Last Modified: Wed, 11 May 2022 01:37:29 GMT  
		Size: 49.4 MB (49377715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82c54cfe4b4cc5c8f89cdc334fc315b35b169ca134d40f28b9b35ae9cdf5014`  
		Last Modified: Wed, 11 May 2022 01:40:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220509` - linux; s390x

```console
$ docker pull debian@sha256:cccf87d96d2c1148703f5273e381823288ba27d593603f71e2eb3bc23916954f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51688054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875295368d24895673e5302aaa9d88d70a19c642f3d9719d007665849b56759a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:46:48 GMT
ADD file:d2704396a92a0cdef0cb5b6ae09d1bfdfdbdec0258fac59fa2da4dc8a53ef1d6 in / 
# Wed, 11 May 2022 00:46:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:47:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6eb697af246a7462539f7ece8e90e15eac1398d7979c89cd545274e905977870`  
		Last Modified: Wed, 11 May 2022 00:52:46 GMT  
		Size: 51.7 MB (51687834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16c82a2b9271c8211bc180c13be2f917fbbcd836cc00da436e8ee23bbfc80ce`  
		Last Modified: Wed, 11 May 2022 00:53:04 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
