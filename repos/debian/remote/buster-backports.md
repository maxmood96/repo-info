## `debian:buster-backports`

```console
$ docker pull debian@sha256:f6ee9c98458aba79441eb4cfba8282145fcc50e5de7d2ab5825f257e207b3078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:77ba988d4f876abf86c615c4c8ac0a7705ada95e4615c89580f30087e06470fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50447964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d4d659a63a1d67038f74772d83a8bffd8e5fb22b1462f1d1aab02fc797cd06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 01:44:06 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa2814ff3db73b71da97af63bd15cc964e7cd761db5fea54ff563e5e24d65f9`  
		Last Modified: Tue, 25 Oct 2022 01:48:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c19f2d0f63b4eddcc792fffcc3011c69268411fb2390b9d34aafd4521c830a73
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32364a727be1c1be5b2dd08a0e7b4a3d0ee669c74771990d2c45713c1c41cad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:44 GMT
ADD file:68e8c9a779cffc9968c1d577e6367eb14306b9cb1ef195c63c2def986afcec06 in / 
# Tue, 25 Oct 2022 03:14:45 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:14:53 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a96a0f5b8ad36dd704fa61a4d79f60b2467017919db6ccc83b23de2d450aa97c`  
		Last Modified: Tue, 25 Oct 2022 03:21:42 GMT  
		Size: 45.9 MB (45916231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd095880eb2d87a40daac65be08cc1e5ac13dc1cb803dd8ab29d0fc2ae2f6d0`  
		Last Modified: Tue, 25 Oct 2022 03:22:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5835253cbc60bb9dcde155d7f5aad707a520cf15ca1013b32fc97b505a201f22
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49233503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25f8ab393aa997f81d845d59b2ff0eb661abd239af7df9fb2f63b8bf6ed519e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:07 GMT
ADD file:21afa32c0395cc5046d09741d6821d21cfd9b77bce46ebcfc8fd9aca57c73648 in / 
# Tue, 25 Oct 2022 05:46:08 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:46:10 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3ba81f4c3c21f92780061ee116827d64ac4edbcd02b056845c2aaa3097b730ed`  
		Last Modified: Tue, 25 Oct 2022 05:49:24 GMT  
		Size: 49.2 MB (49233280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff84250025571feea5ea26445a5a990b676f31941bcdc04ab69c5eebdde57777`  
		Last Modified: Tue, 25 Oct 2022 05:49:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:18eff1815f0dc495a351387ee5b19e273a48bac6cb39dddfb49957e59bd85e38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51208165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccdece0bf4325cc51e96409574f5c038c88e05e6d0d793a0f98bfa541d055f82`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:47 GMT
ADD file:7e14d4afa5499129c959c5ae5dc270e2fa04659c2c9b0527094cda3494c02d0f in / 
# Tue, 25 Oct 2022 02:22:47 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:22:54 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:76a731c42f665e7334a622f65117ef9389e97a878b7c74bb4a10dfe9cdb296c6`  
		Last Modified: Tue, 25 Oct 2022 02:28:50 GMT  
		Size: 51.2 MB (51207943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef3a34b1eb366aa2eb4180121b9a6ff3d217d0fcb3f0948a98b77c347af03e0`  
		Last Modified: Tue, 25 Oct 2022 02:29:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
