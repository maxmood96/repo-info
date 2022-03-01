## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:c61a02401856cd4756334a2384e8d8a95ce1126296b31b9288b4b3bd08a1d8e6
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:d77ac54ab63f87ac47d9ce54afaed85d96f3c9b562314e754875e12278558f15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55764346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87877f7fac7228bfc248a62dafc1261a22b04b4d5b010265eb14307b19e2e765`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:12:48 GMT
ADD file:ba00d13bcd1098159b17d28658733d14360751081a0ff0ae5e599ea2b24d8bfb in / 
# Tue, 01 Mar 2022 02:12:49 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:12:52 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4e0d8da139e3fe03100d4937bc5abe5a82000a26ba213987f21c101384e663b3`  
		Last Modified: Tue, 01 Mar 2022 02:18:16 GMT  
		Size: 55.8 MB (55764122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2def9bda7d83558cbfb637a8aa7e86d436f6f2debaeca660610f31b1eb2da9c8`  
		Last Modified: Tue, 01 Mar 2022 02:18:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4ac8dc09182427892d0d3a7c94c547614d664555cf783d6b878c6020738b2830
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53159617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afd98624741da45981acede7160c2df2cbbeb705bb00430caf7101b51ddcf51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:15 GMT
ADD file:1c7800709331eb899ffb3adab213dd035f158fbb5682366917ca9b29bca0df53 in / 
# Tue, 01 Mar 2022 02:01:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:01:28 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:73894112358cdc16a19d6f8dc64e5d28dbe24c82ac6079e97e3750913f71a9bd`  
		Last Modified: Tue, 01 Mar 2022 02:16:26 GMT  
		Size: 53.2 MB (53159389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff5f6c4d13af1aa8adbf64b34af0a314e7f75ef43c56eb392cb9e814cf38abd`  
		Last Modified: Tue, 01 Mar 2022 02:16:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:53806f3963fc5067250230034daac2a5f68ad379caf556c3f3c9b82ed07bd2f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50787800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97ae462949f7d9fd5ef825dc647ae940a6727d94cded219100eb46f559a5648`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:09 GMT
ADD file:b4dba23a3881b51ce93a5fac275db003c57e88fc4534625e4c57917ee7d15dad in / 
# Tue, 01 Mar 2022 02:01:10 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:01:22 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bac975da179fd2ec964b1f0a2374ae27456aefbe28014e1301872aaa7a545619`  
		Last Modified: Tue, 01 Mar 2022 02:17:11 GMT  
		Size: 50.8 MB (50787576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2075773539869dbf9cc838de4588d8a5340c2cdb0c2051544b5346e9964c6b4`  
		Last Modified: Tue, 01 Mar 2022 02:17:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3bd7bde2fc3a7ed7a6cf7655bb811dbadc780def39bf8992f2578d1da1b0af3d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54704722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206e757fcba65f69a925f8497db02d20bfb5cac383be7eabd99f315063ebddab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:10:47 GMT
ADD file:6cc6cb40b70acca2462997590c41a6b84b7434e382c9b14ee43a22dcd7981979 in / 
# Tue, 01 Mar 2022 02:10:47 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:10:53 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4ef7b4e27074d58d976b796a4f016999e5977498dbef83e6266727f3bedc89af`  
		Last Modified: Tue, 01 Mar 2022 02:17:12 GMT  
		Size: 54.7 MB (54704495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e96fa3bf9bd9232cd6e32a45d41c0de49d8db218aceb0ff4a63a089f6948937`  
		Last Modified: Tue, 01 Mar 2022 02:17:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:48ac162059ec3ed1489f20b0d4aaf2c5c53d82ead093ade8dd60c25bf5ba445e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56800472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01447e81c5e5f1474bb956db0f77479bc83189af9390e65e8cd42a7290456d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:44 GMT
ADD file:2e2ec9677737b8bd29e3af438e4f72a00e4024d7771df47c835bc532f3955901 in / 
# Tue, 01 Mar 2022 02:06:44 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:06:49 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:86f9569b4496bcb71f9a06eca983db008f228f89df9115b51deb7ba67bce86ba`  
		Last Modified: Tue, 01 Mar 2022 02:14:26 GMT  
		Size: 56.8 MB (56800248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cea9fe87138b04062a1985f8f29892143d69c8026db10918d2651b720465b0a`  
		Last Modified: Tue, 01 Mar 2022 02:14:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:37cfdbcb1d66c8794bc1648b63a9d80d4c02d8fa8875e0a739321b2aa67a5c45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54412516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4604e3d0a99b602f0a81f29fdab81bea75f07adb93bb2c84b843d0f807aef1ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:16 GMT
ADD file:205e6fa10b349b94cd09f9ab81d41ac5b9cc551f15798915ab0db37a758e13ed in / 
# Tue, 01 Mar 2022 02:01:16 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:01:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f016bfd811ef5b25e78858421fa083872f3db557018c6de8e9e19a3db5d69e73`  
		Last Modified: Tue, 01 Mar 2022 02:10:17 GMT  
		Size: 54.4 MB (54412288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6f3d5abd9fca3a24e814f7844e5016697bd2bd1dfeb8b2ab8ad77cc9ad5c3b`  
		Last Modified: Tue, 01 Mar 2022 02:10:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:0967b1b92084db484d1c46ca7e8fdefbea3be377c808787d48fa4ff10a3e36b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60166592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c09aaa6951f8437367f3d3ac7957f5d21c39ed60b3f082a3c9c61c2365dc33`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:22 GMT
ADD file:08a06b615cc3142b45e95ffc03be0940c1aed49581fdb5c3a45d69c9ba65fcdf in / 
# Tue, 01 Mar 2022 02:03:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:03:44 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e0578def7e304114d931a4e4be85f40364b30cf0228e8360d7ec9d82b30f2519`  
		Last Modified: Tue, 01 Mar 2022 02:13:53 GMT  
		Size: 60.2 MB (60166365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a15be72c5ab6bccf0091b672119083b3dbc679fff4c0fd90488cd37a5efbe1`  
		Last Modified: Tue, 01 Mar 2022 02:14:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:76648c35410f84185517204c9910ce799f18028e2a9ce385c3067fdd0775dd4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54007417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3c8e8bf1203d179bd050aed6ea01a4aaafb0ad0ad7f534f9acfbec7022ecbe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:03 GMT
ADD file:97ccc226b81c90fe178edd1d68832f3a504aa1ef983753f12fed36e4fa09c796 in / 
# Tue, 01 Mar 2022 02:01:10 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:01:18 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d7c29f1e9903c84021327567eb513269c7f0b92b6f050037783556a33deac133`  
		Last Modified: Tue, 01 Mar 2022 02:06:47 GMT  
		Size: 54.0 MB (54007195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d680b722903142b8d82713648085e96bcb52fb50b0c34e3adf66c54b017d300`  
		Last Modified: Tue, 01 Mar 2022 02:06:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
