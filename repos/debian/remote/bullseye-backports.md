## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:21c0bd074d66826c9f88f36076b0d8fd850ca3a28c5309f686ef61e52dc0ce3f
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:f63d7a815453356280cececc3f97acbe0232fd8f738ccd97f8859ae631e15494
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55056848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857d8bdc3ef75d8f00b3dc6af0924e4447cda5623934db420408d44684608bf1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:00:01 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039714e08e0a02f4a8566df4fbe05ad66bf54bf2e237a5eb43217ee4e8fc49ac`  
		Last Modified: Wed, 16 Aug 2023 01:05:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:458d49a537bdea36b9d93e39f5176966a6d9e8f0ace107a163587db54ba91f73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52558358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c846818ea480fed11b86d179ff10a210c48b9b3f6caf71947d8fbe0c5d7116d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:48:40 GMT
ADD file:d044e64aab907424be649252b5ff1d9f5e8c9494db5b60c0e54f5962bfb73478 in / 
# Tue, 15 Aug 2023 23:48:40 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:48:43 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0b63bbf2e6f6026dfaed9cbedf777472a04812b7d291501b1d416e49e3ce885e`  
		Last Modified: Tue, 15 Aug 2023 23:51:54 GMT  
		Size: 52.6 MB (52558130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ed972dcf768d79ea214885479652118dde820681d8f215ff515e8bcc5e05d0`  
		Last Modified: Tue, 15 Aug 2023 23:52:06 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:be6c32177750a4e5f2a6012749760fb37208eca7fa890023f51720457719f147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50219722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec72da80d2786898b1c2a70c78bf6e10c9666fac7334eba4d55872410644380`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:17:21 GMT
ADD file:b529de8b48c1e507ad6f29320c3c5cd83d8d06fa66e8d89bb62faff62700e9f2 in / 
# Wed, 16 Aug 2023 00:17:22 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:17:25 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c53151c23650f086e15d3652b8a931fb4623765c0112e8adc74eb8853c8c9232`  
		Last Modified: Wed, 16 Aug 2023 00:21:46 GMT  
		Size: 50.2 MB (50219496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef85287085d5d2e9f166a9b1a21859a7de8cbb3180a7bcfc9ac312c25c8b845c`  
		Last Modified: Wed, 16 Aug 2023 00:21:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:84790e7b8cce5f965a387f677b28596b12725562cfce077d86ab26b021a95531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53705004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd740fa6283f98531c840c46200af0ab0806a0f2ea2a33caf46b096bf76f01d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:40:06 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b932f4b110190e63603d08b867acb4cbe6a38388d0e005a3b015d7ebee9c3d`  
		Last Modified: Tue, 15 Aug 2023 23:43:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:123e16c17b3c1eee93d6266eb06ba5e8f9790dee96c644b5f3cc1203425ee5e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56040745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d6ecf422f320ca7b48d77ab5b19ad64c3bd1d4f1c01ae8672321eac3fbc79b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:11 GMT
ADD file:efc88a19b31e68ca41f555bcc51338b0f135cbbd72b90637d8c73969d53addd2 in / 
# Tue, 15 Aug 2023 23:39:12 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:39:16 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:822e033fa7b169545d5890de01438a9dd87774ff938ff440e823a3ec3f73996d`  
		Last Modified: Tue, 15 Aug 2023 23:43:47 GMT  
		Size: 56.0 MB (56040520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc2fe42b0e9a26ad377ea6baa5e2dfa1baddf1c93f41d376f5b1e8bec48cdd6`  
		Last Modified: Tue, 15 Aug 2023 23:44:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:fc912db366d6c68c1272d7f6b25b2fc59dd87b283d144e7afa3f1e3f1fc61b3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53271791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cdfa4524eec2e9edb9a918bc287ebae072af48a1aa9dd05d69a033dcb07394`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:09:18 GMT
ADD file:c0b984cd41325dc5f83fb228f8b95bd38027d8860098ac574a960400eaf0d976 in / 
# Wed, 16 Aug 2023 00:09:23 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:09:36 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4a039678eb41cc8e7dbd73bbab533513108157d96943588a97c7fac7c940eaca`  
		Last Modified: Wed, 16 Aug 2023 00:20:18 GMT  
		Size: 53.3 MB (53271564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6857354ce38787ec4c5624de1352fde3fbce8bbd075cc668aaa7377aa284b3`  
		Last Modified: Wed, 16 Aug 2023 00:20:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b22ea7c3b9bc63442c3f74752d6dacf8c5516040fd06f9777fd9f94ea30c21f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58928660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa64c8fd55e3c075ee9d2e9592afdab4b262fa58297fad98ab62475b215c02d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:09:50 GMT
ADD file:23fe4ecb2d3d302e0df50109aee416120a138fad47d1614500f98b65fa288281 in / 
# Wed, 16 Aug 2023 01:09:54 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:10:01 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:148c97e5e41c60dd4fc440664aeee1e57ab7158b53ea7d1f9132198b3d35bc5e`  
		Last Modified: Wed, 16 Aug 2023 01:16:30 GMT  
		Size: 58.9 MB (58928436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c599ffab002305f821dba26baf2f48b824528bc53f57c877bcdcf0106db7525f`  
		Last Modified: Wed, 16 Aug 2023 01:16:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:d6cb9084545aa4fc460e26cfe167062bb4893185529e2ec7d6fd9f65c90fb511
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53290868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3cd499a4bc06dc62a198ccdece237bfb02f677b1a2902bee6786db4562ff5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:42:43 GMT
ADD file:021ebd89eb6b326058b4fc3aeca5d0d93925ed29a443618fedef034618e8f2db in / 
# Tue, 15 Aug 2023 23:42:48 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:42:54 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cf9beb6f1941863d1df3b7a9c4f925894662762a3ceeba920f164d9e8c8bab57`  
		Last Modified: Tue, 15 Aug 2023 23:48:07 GMT  
		Size: 53.3 MB (53290642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f845b7fb8b3daa9998e5465d601bf060be9cc9350c28f140ae7843312c83e0d`  
		Last Modified: Tue, 15 Aug 2023 23:48:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
