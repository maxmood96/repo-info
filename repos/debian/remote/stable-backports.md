## `debian:stable-backports`

```console
$ docker pull debian@sha256:b9a79b695c460c06165f2be2d9cac9491d1c8ba04c48189c96f6eb2adcaa07a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:c2c3ca5c6b47b6ecfda9ec1e46f26552446ca21917dcffc652b57cdd1d21436d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48497432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9e7316453463f8756f8141518caee074b71bd5cf04593c4473daf98d7cc8db`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a6b0a2b36cf5dbee93ce274c2693aa21f80b7a2a10a3b27da07ce21160cf1395`  
		Last Modified: Tue, 03 Dec 2024 01:27:23 GMT  
		Size: 48.5 MB (48497211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b590762d3bc9edb33d9ece542f1d03aa74bf6e74b23ddfb47ad1451b8d9226d2`  
		Last Modified: Tue, 03 Dec 2024 02:13:39 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:379e7df2d7815f2c1ac6fafb03684ce84b3c78086a01de645535f99014c40e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3288a131e1945a70f87b3f803c8955c3a4afba2982410772d67cf2f06f1ef708`

```dockerfile
```

-	Layers:
	-	`sha256:35ab80a81e87fb7cc65b232d8b8b4987931eed3a3998f11b38998e451c5ee71c`  
		Last Modified: Tue, 03 Dec 2024 02:13:39 GMT  
		Size: 3.6 MB (3623030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a1c756f69889c8d0bb255d42bbd4b4ae8bb27a3eea69bbf03e4dc4e3cc9908`  
		Last Modified: Tue, 03 Dec 2024 02:13:39 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3038d25f4b2a44504b00ca2f9de7bbdfe6ed75cb71078375d1cb8bbd4d6d3343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46024598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fec8c07b803b470df153fcb86f87aaf94109e8e84ae73a9cb17872fa4885a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3a657e175756fcf652b5305876148a6afb342430a95ae362b1ab2bab9e5808fc`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 46.0 MB (46024378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82db1dd51fd8d2a742e756424bc42ac9e35759d584d6fbdcae9b4895abbe74d`  
		Last Modified: Tue, 03 Dec 2024 02:19:04 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:831b4f45d8232b552683e7ef012865d8c8406496f2988cedc25d9e490ad3f7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1c56c0cecda7223d7ef2650e463e40cbe6a6f2c651b341b4b77f081432b4ad`

```dockerfile
```

-	Layers:
	-	`sha256:fd66ed06337ba4c325f961ae858631a06e2a4754fe5f1b300b9f9ab7fd3e6f5d`  
		Last Modified: Tue, 03 Dec 2024 02:19:04 GMT  
		Size: 3.6 MB (3623230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b2507ea3328ace2f8bfb3b5b42d1e8dae1dc623c3d1110b960af42806a56af`  
		Last Modified: Tue, 03 Dec 2024 02:19:04 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:da8df59dedb8a6a0df1e22c73602deaa3f1f0ed4537043444bed366380715c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44200330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f907d75c5cef3df1b4939458d596ba9c3a590fceac557b657da2cb6bdb5f433e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5adf777e5876a10a4604c3eb5d34bf3fcd887bb64dacba041bf9b2171e2fe12e`  
		Last Modified: Tue, 03 Dec 2024 01:30:24 GMT  
		Size: 44.2 MB (44200107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e000c76307956119a8f2b5eb32c13a366df0e352e94d94049ce71a68cf268f`  
		Last Modified: Tue, 03 Dec 2024 02:19:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6152b8620eff8fde9b36e96a6b82a0d81dbcef135aaafbbb58feeb7a56785db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d59352b075e7154cb0ee19e6788bee744660cd401b9f8cc4d5be5f8634a19c`

```dockerfile
```

-	Layers:
	-	`sha256:154e85ec4884f1b127a01566a246c0075f4c545059c29a602bc13c15a3d4b13d`  
		Last Modified: Tue, 03 Dec 2024 02:19:42 GMT  
		Size: 3.6 MB (3625208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7174c548a0e2d1043e6912c17cefefeb6ec640b23e5d24876369598852c282`  
		Last Modified: Tue, 03 Dec 2024 02:19:42 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:dff19bb7aa0eb924a9935f2c6601dc2c38816fb1bf5e3417362513757acedccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48325904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fcc4725fb5a28f079b95db4e610a66f7f75dd07979d8ce8bcd6ed4f8eb9e43`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a36a8cb80772e4ec4d03f2b8a1eb01b17086964025be4ef9bc29c7428ed93a58`  
		Last Modified: Tue, 03 Dec 2024 01:31:48 GMT  
		Size: 48.3 MB (48325682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f378158400ea9e72e0b88bbcbdc5b7ac90860f3739f4456332ef4c440edf8f`  
		Last Modified: Tue, 03 Dec 2024 02:19:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2d5146f0603b83ad9c1fd5ddd7326dea4710bb083647be153914bcf236a9de83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf8a5d3714da272a72e1fa36674e8520a483e78b768740e6768c44263484f84`

```dockerfile
```

-	Layers:
	-	`sha256:ec3d666ac3c0b033ace3a3f37a37851ffe7fa3332a9843bab50b368b1bdcc086`  
		Last Modified: Tue, 03 Dec 2024 02:19:01 GMT  
		Size: 3.6 MB (3623244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7bd82caf3f7f9149a7fd72870b2049016ef0822b321f13bde92ba9156a9ad5c`  
		Last Modified: Tue, 03 Dec 2024 02:19:01 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:66dc3dd6c561f26c2123b3801df603ec8f12d4995acc5b90411617e6174a2d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d7d6d34db1150479f4e3eafb2ae9a2581a6c599482ae325fb95739513e43be`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:51cd9053e2e0bf47797771dc8e7368ed7866a527fda21ed67e30b7ead0b62afa`  
		Last Modified: Tue, 03 Dec 2024 01:27:19 GMT  
		Size: 49.5 MB (49476154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdadfb6f1adbfc4242d21d20923763399a6171a24efdfb4520ace0dcdca0e15`  
		Last Modified: Tue, 03 Dec 2024 02:13:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c6ee3417b26ddc0836b3e12dc027524ae24e76afa683eb36b8581702d792d4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043a08ee434c91a4fb26e7f965e1e151287477b75d068af256c079872535557`

```dockerfile
```

-	Layers:
	-	`sha256:0cb958aa8d9ad97a65c0905178a164c45dfd0f09a414472724e0689d70825bbe`  
		Last Modified: Tue, 03 Dec 2024 02:13:45 GMT  
		Size: 3.6 MB (3620190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21f1426f17a241b333ab8d9a743319d5e788f61ed09cb463bc62e48b869e058b`  
		Last Modified: Tue, 03 Dec 2024 02:13:45 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ee95f3cba1f5702b159efc713edf7bb6086a7e0eb7823e5502c02e634fcd552c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48772071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47185fd6456e3bbf9b497bb905585c3115e91e52638f534edd54c715a4f124c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'stable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6f3420a03270d5d97e9fb002aecbb5fd42aa8d1412822f78de222c03d88066a6`  
		Last Modified: Tue, 03 Dec 2024 01:29:25 GMT  
		Size: 48.8 MB (48771849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a064e90275089b36c4e0e660e3c11ae32ccb13167b5725ead1f56b819c611df`  
		Last Modified: Tue, 03 Dec 2024 02:18:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e894e63cb44a040d574d2fb716bb839eb7a722212bc88afd02a4bb9f5e88f4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a17100ee2c71e90e1b06c31b1177d54adce7e9f37f197fb8eab723a589b2f57`

```dockerfile
```

-	Layers:
	-	`sha256:c4eb64d1e64fe54044d94f389cd8fc8d0aab766b501899849d14e875339b4fed`  
		Last Modified: Tue, 03 Dec 2024 02:18:14 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:0820af549ae47b79fe306440f06dc8e7b8b6f6c3484831fb2271d5fc4ed92875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52328448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c400ebe9525dc914b8ba7b675d11d34c8e1dac30b13f7d51e6324aae1a39cf29`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:de2ead00c8fdffdc34fb9896fcaff87d790574b30c701dd3e2dc57eb720e4c32`  
		Last Modified: Tue, 03 Dec 2024 01:30:06 GMT  
		Size: 52.3 MB (52328225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c172bd73207a7d3b44a3dea79f2952d46984b270273f57b3d11c6fa8e7b1ff`  
		Last Modified: Tue, 03 Dec 2024 02:16:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e5b3cf93fc75eb85e6063e0e04bcbe61227937b5c9239616480a786a219687d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd0afe26b789405efca157fc3344fa15f128c2c8198de91b3c176d0a0f38c4f`

```dockerfile
```

-	Layers:
	-	`sha256:4406391a1401f5b4dad2b42675321b61e3ef1c6992f0d12df2676c7b4b01595c`  
		Last Modified: Tue, 03 Dec 2024 02:16:20 GMT  
		Size: 3.6 MB (3627289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744553dff058f90f8b9c1142466e41f1b3181d3b6b11b36296c221de8fc72d39`  
		Last Modified: Tue, 03 Dec 2024 02:16:19 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:b93ac5828597fc40007a677dfd86bea228236ec0b27b23c37780617be33f733d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47149990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059bfeb235f80616b35b482f9bf03f81958a57a26675e319a3c7571a14ed5edd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b226327b3f529403c43816564e1ef00f225fb0f12756e37bb5773b0f09b78623`  
		Last Modified: Tue, 03 Dec 2024 01:29:56 GMT  
		Size: 47.1 MB (47149768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ec3e4720991fc907ace260d033a905e8cf264e1fa62a4263beef7872be75c9`  
		Last Modified: Tue, 03 Dec 2024 02:14:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e41ac66c3a5d2ec384f497f260ef434e7ac71e716a361b4c2a7e09735e71e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16522c54ffe663e68abe3514dccc2fb6086a0ff40ec6a048dd9ff0ad5b0124bf`

```dockerfile
```

-	Layers:
	-	`sha256:67c3c83d42c8e0b812da588de0b331b1663ff4f9cbc5ed27402a754634ecb6ed`  
		Last Modified: Tue, 03 Dec 2024 02:14:04 GMT  
		Size: 3.6 MB (3622761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6960ebf4efceca16bc6a2dfa5909685f8a8259240e7875d95b20c59ed66a2d4`  
		Last Modified: Tue, 03 Dec 2024 02:14:04 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
