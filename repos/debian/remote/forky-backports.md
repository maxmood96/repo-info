## `debian:forky-backports`

```console
$ docker pull debian@sha256:0ef55387228ddbc853b2d7f5073282dd2d1faf086bf70c6ff4f58e96e251c3d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:6f9bfcad409e32deaaf6bcd03849029eeba73f70606b73c3f6862cf079bdaf81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49759358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e8dcd8f6ac21cab8667fc001b1d4e594fb2cb6108b14b54562dc7b98851d49`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7671d30ee0069a32147537eef1beaae52a71b59148743b8ebecaf97652901808`  
		Last Modified: Tue, 21 Oct 2025 00:19:29 GMT  
		Size: 49.8 MB (49759136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c064a8b519523f573059baa2c2c50945222987b3ef35877f466884a5d6efbc75`  
		Last Modified: Tue, 21 Oct 2025 01:16:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dbb796ee358872fb4542ceafddcc509674ca97585827e33879c454ea0766020a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6274995e0a7274cbe1f578cf65305de2f6d39d2126fa8ded3ff0b763bde4f778`

```dockerfile
```

-	Layers:
	-	`sha256:9538aadf2bf4a2f66e78e2653f8c1cac0ca1d94c3ceab5d7d031b6571987ca92`  
		Last Modified: Tue, 21 Oct 2025 09:24:19 GMT  
		Size: 3.2 MB (3164889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce227353310c4f79d9d87667f10e9ed30d7ba48a4d1af0748cc57c33755cfdf5`  
		Last Modified: Tue, 21 Oct 2025 09:24:20 GMT  
		Size: 5.8 KB (5821 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ec92a2726cf5b4b5f6b65a1d7eef9531517e595a22892258393f602d7d29da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46030658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a3493baaa9b9b3de60f6a50b7acc9cd0a394898575bdb52b3f02f725dfdb35`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8d985114d6343216c46b3706ffd32abaa547ef65adf34aac773cf8677bc44aa8`  
		Last Modified: Tue, 21 Oct 2025 00:20:38 GMT  
		Size: 46.0 MB (46030435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff772725a149a2e7533099afdfde9c7946a3f8f77f08810f23fd69b74310a9e`  
		Last Modified: Tue, 21 Oct 2025 01:16:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:17b1f312d7ff917076850810a5820a4a791aab715c60d3ff0a5bc834fd4a733f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc339f6bdd7f5e307369a8676f24f3a736cb9429f040f60de622baca9b10c61a`

```dockerfile
```

-	Layers:
	-	`sha256:6abadfd30d272aac3a4c1dc8d04a03942d1402f7e035ab7eef65e4ff5c42b713`  
		Last Modified: Tue, 21 Oct 2025 09:24:24 GMT  
		Size: 3.2 MB (3166263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e39ce805f240a0f83a9560353b6a0f8c1a55e1d593e286720830b2c2735a6e`  
		Last Modified: Tue, 21 Oct 2025 09:24:25 GMT  
		Size: 5.9 KB (5877 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:edd102df8967b8cb2b8f35c054af9dd6045577e8c2ff0a270243da36e4e04192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49888704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aae78dbe58ac1ecf6ffb42bae3a32caeaf8dcef8bafa82b284813b1bff518fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f6aed6c6f2efe803974216c59eb03806f2c41bc69dd9196f4b2f7cddd7e58f63`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 49.9 MB (49888482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8f28951c47682a4b994bae2daf3b8580a5205956789c9a91bcb2af863a91f1`  
		Last Modified: Tue, 21 Oct 2025 01:16:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ec968b92ad9a692d1d712e0f30562c22a1d85a3d890a79af0d52447487c9f333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447628ba8ed3ca55372f61f2c9983c1abbaf3cbe14dde7f096a10a75dc03d1f3`

```dockerfile
```

-	Layers:
	-	`sha256:bbd45c867a028e57dfb5d9b85de35147e82268f14b2dba8f7d1495a02040285b`  
		Last Modified: Tue, 21 Oct 2025 09:24:29 GMT  
		Size: 3.2 MB (3165732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:474f2ee5b2ef9abf47cbdf6060a0dc93dda6c4b2194afb6537bfc7d0d4ccc3a8`  
		Last Modified: Tue, 21 Oct 2025 09:24:30 GMT  
		Size: 5.9 KB (5888 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:3529283e29fef8e6c2d2eef998cb2a3fc52d0c5fab421dfcb1bb52f935e83f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51134625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cedf460f850cf7377f782800f101f288d87846405c09019ec671f79922645f6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bef87153a80d12c20903cc117b0638354009942edbd8ed3d2109a962622491ad`  
		Last Modified: Tue, 21 Oct 2025 00:21:54 GMT  
		Size: 51.1 MB (51134403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f8aa66e99c92b69da5df402c468a30928d4e0494bcea3611685a99d93bf1e`  
		Last Modified: Tue, 21 Oct 2025 01:17:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0ef7fcd086d93dddbdee9438e802a50c86b08ba6cb425a8dfc7e300ea9fff946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3167897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec988d35ca33d0cac7b99b36eb1da9f1545237cb4527381ef7bd4a872cbf815`

```dockerfile
```

-	Layers:
	-	`sha256:c2a7bdc6a557ef97d5c08f130090303b2850da3717cc275048547a4f9ae7777f`  
		Last Modified: Tue, 21 Oct 2025 09:24:34 GMT  
		Size: 3.2 MB (3162094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3e0ad5c054eeb4eaafd227c40ae4b6bef4acc37b4f3150d71e7fed7c63a8ce`  
		Last Modified: Tue, 21 Oct 2025 09:24:34 GMT  
		Size: 5.8 KB (5803 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:db3e0914d0b9a42275f06c96ab88d3a4f388fa3f0a39a61b19960c185f8d16c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54876019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641b50734414fcd79630a90c739048cf5f89e8e65976ef3579cb31640ec8672c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e7d4356e03351899ba9f4be32ba46e679bea4702bcfe72d9b6fe6e31094e1e6b`  
		Last Modified: Tue, 21 Oct 2025 00:20:47 GMT  
		Size: 54.9 MB (54875797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f8aa66e99c92b69da5df402c468a30928d4e0494bcea3611685a99d93bf1e`  
		Last Modified: Tue, 21 Oct 2025 01:17:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:50e5d6bd7ced01eb949aa097bc520b70d58538ffd6eb2a1623abb9bb3629995c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19445356f55d310b3c3d38d58b0039cce33ac934fc21168fb3d4b7b2b48ed4d8`

```dockerfile
```

-	Layers:
	-	`sha256:64c9398732898f20a356b762393364267abcef051026d24d79b4f2cf3c601d2b`  
		Last Modified: Tue, 21 Oct 2025 03:26:41 GMT  
		Size: 3.2 MB (3168396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a167b3c99972300dc801a1740ccfcc3fe10521e1cdbf59e9be7ec35694ec8eac`  
		Last Modified: Tue, 21 Oct 2025 03:26:42 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:bd31f1a0f9417d523d70b80bcda53cd4ee8979aa7b615ed1bbe4014a9d719306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46791348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6894dae8e8ab629861fb6dcec1059a67039f705015d549cc0dbf292809d4d6ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:17:59 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:81afe9ed9d72ebbd06999820f64e36aa62bc978725062b4cc32efc39c6a99213`  
		Last Modified: Tue, 04 Nov 2025 00:13:41 GMT  
		Size: 46.8 MB (46791125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf706f26189ec92bd8b1b973e142e9d62839cac2656e3c210a0f6c4338970682`  
		Last Modified: Tue, 04 Nov 2025 01:19:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:be7a7e5773769c10b18220a0d8629ff3406a6c62784bafaa265a047170012d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3360a9a5e9b7a38d0f536334ffffbd65592750ec06552934264dc3dc13843f`

```dockerfile
```

-	Layers:
	-	`sha256:1adb4e4fafdb387907e0316874c685c0e3f419ad26201ea9996d7f0bac4732f2`  
		Last Modified: Tue, 04 Nov 2025 07:28:28 GMT  
		Size: 3.1 MB (3121836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b5558d66ad2b4082167870128fd27e7e7a49869b27945952309683c0008e7b3`  
		Last Modified: Tue, 04 Nov 2025 07:28:28 GMT  
		Size: 5.8 KB (5803 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:da0021dde99c6942cbaca05874090c59cfe6380ecf66db9aaaea59a471229bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49621011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71496646729e3ee5f6420148b58bd7a5afb61c13066c1895e4131469674c32e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4c17c2477a00887cc596493d4aa463fcafb677435d66760d41166feb0acd2773`  
		Last Modified: Tue, 21 Oct 2025 00:22:26 GMT  
		Size: 49.6 MB (49620788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f29195d7a7e858a3f3f0ce3e2fc228048975901399a899415d0ea6ce17e765`  
		Last Modified: Tue, 21 Oct 2025 01:18:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:50d5d9e57fb78327d7c0d9eaa97224d7f53c637cbbadd460f37bb260a82ccffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d45d36c06f4ed5298caaf5bd8aa765be9ee4227ad5a7fdc0be0dbd010eff56`

```dockerfile
```

-	Layers:
	-	`sha256:db2a0d3a9e0fe8a950a94cb77f4488e76e888fdabd51ac37c352f59b4dbb6621`  
		Last Modified: Tue, 21 Oct 2025 06:24:15 GMT  
		Size: 3.2 MB (3166336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64444ede407510375577a3242df81498fce6e9e4a8c1ba39c3b0d5ae8c65ff6c`  
		Last Modified: Tue, 21 Oct 2025 06:24:15 GMT  
		Size: 5.8 KB (5821 bytes)  
		MIME: application/vnd.in-toto+json
