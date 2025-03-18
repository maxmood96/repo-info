## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:1844532f09a8aed0bba308d72c15035a729cce6b926a04e3e9634bee839098a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:418da6ebd29e54ad451c3f9f088c078c1491eb8803b6852bd5cf439322024736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53741498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6509dab3912e7d1e96b262381905a0e0109add92680fbd25e67488be471d562`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9f6f2db2889f924228d5fed390d7eba39449af6612506c186d747d50a846dd99`  
		Last Modified: Mon, 17 Mar 2025 22:17:25 GMT  
		Size: 53.7 MB (53741274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1735572c370d776060931e94ad15682f857be3aba6f67af3d6179cc652859f3a`  
		Last Modified: Mon, 17 Mar 2025 23:12:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:922d9b1e3309b4d117d3963ba19ab3364869ebc8cfc620b65384cdfe724d73e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a342829a64446e67ddf5cef20dea500ce717967b5a14da086055922a241649`

```dockerfile
```

-	Layers:
	-	`sha256:c2150047e925b79a7a5af57c7bf896b37c7b8eedc9856142af323b5fd9e737e2`  
		Last Modified: Mon, 17 Mar 2025 23:12:16 GMT  
		Size: 3.9 MB (3917518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faccdbdccd98025ece698b43e11829b233dcdabe299bd0617c13eef318c364cf`  
		Last Modified: Mon, 17 Mar 2025 23:12:16 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:04ead8aaec727e618b3f78ce9e063bdd4be837ebc1ea55a05dd6bbfaa216d3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49026787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c07cd78e10a42bfb86380b6923ca613099ddaa3b1e68d361ec65c4585059529`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:64ad5fdf9dec07d65f645029017de735cab5c8afeef849d7e1606a02be0fc863`  
		Last Modified: Mon, 17 Mar 2025 22:19:47 GMT  
		Size: 49.0 MB (49026563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abbc00c21ef2dd578e3cd47f92f5c0666ebe39cde18467a1c11d7bcbe4de251`  
		Last Modified: Tue, 18 Mar 2025 07:20:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fe3e649a1f9eb3838660017d1ad244fd96ed21163908de3dd2366f4de985c4a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3b0090ffd27f44ea0ee8fc4f4169190cbcdf88fd1996a016d835053d80b5b5`

```dockerfile
```

-	Layers:
	-	`sha256:41629d0c0008e345ea4e1d985f55ba187f81dc114b194f692b031e31f8ff4524`  
		Last Modified: Tue, 18 Mar 2025 07:20:50 GMT  
		Size: 3.9 MB (3919080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc2ac4a925e65b89ab4501f01f16f3e1903171f627d32e4e37d4c42164ee363e`  
		Last Modified: Tue, 18 Mar 2025 07:20:49 GMT  
		Size: 5.9 KB (5903 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8a125ac1b6ab878ef72c22b7dfac6642d157d6c26a852db06415ef537c8bd024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52248615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2408a6d816560f90fa3e7f709d0948b8ea3c3a7aef536d9e1614838f1aaa0951`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:84138708d20723dfdd9b1f0f94e1c088851e4a632c49c4f2d1a69b64e6b95cef`  
		Last Modified: Mon, 17 Mar 2025 22:19:28 GMT  
		Size: 52.2 MB (52248391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890bedb4f0351e997e74ff82bba85eb45221f3d2c6540e710a6097a45c1467fe`  
		Last Modified: Tue, 18 Mar 2025 07:35:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2cc2cee49b355ff42125f030374fd576c1af5ffea4def6d8435f2e35415e41a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9ad399972dd95fa6c883963c32474246ef65280614075c6a8cdd2e857e4027`

```dockerfile
```

-	Layers:
	-	`sha256:20d378528dd1a83056515538733d8dccdcc0114b6294743fa5b72f19428382ac`  
		Last Modified: Tue, 18 Mar 2025 07:35:27 GMT  
		Size: 3.9 MB (3917098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd466da8c9a9e01285d0da18f5b1f633d00d8a933922b07ca422e56d6775e6c`  
		Last Modified: Tue, 18 Mar 2025 07:35:26 GMT  
		Size: 5.9 KB (5920 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:3f7be803d6c1db344f6b5428d7cf43880832d5f3b8f9793ab9e720b836a8ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54678841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f4319262792fbc03abc6d6360e6c0230e84c48bc91489e017a3c37a64ae6bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ff654f4f86bd5f54c9ea16833c0d64fd810ffbddd628768cae4d932256f0a126`  
		Last Modified: Mon, 17 Mar 2025 22:17:48 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8a58fa780a4d3a2a359bb93840b3a41b677d7f9875ab1afe3e4328e9f4eee`  
		Last Modified: Mon, 17 Mar 2025 23:24:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ae0856f11580c8aac11917d9c159914ce8aa3e5c0b7cda3db9e978ba2c753207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a19a02bfc14b942e4dc0fb4ecc1751da2d8619a6bc2335a342cd7dc34aa295f`

```dockerfile
```

-	Layers:
	-	`sha256:97d4b1eef6cb277d6d82f07a35884a87ba5944c1edbd5f30c5e156f456cfc62e`  
		Last Modified: Mon, 17 Mar 2025 23:24:57 GMT  
		Size: 3.9 MB (3914025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46d72cef649eb2020f513cc0c6d820f26aafd6f5c8a97b0f94074cf1192a45e1`  
		Last Modified: Mon, 17 Mar 2025 23:24:56 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
