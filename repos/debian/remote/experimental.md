## `debian:experimental`

```console
$ docker pull debian@sha256:62bb876bc6902e3b9a5262c572399395ec09fbb39c263c1ca814a7571c7464eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:0114df8ae9820a46ae8b3533b83366327560332e95b1ba26fc25e16e21f142ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49311233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12bdaf588c57badb8fb0b4d06fb4dda45fd3199a8dc518bf16c6656a38335c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8d168639a251c13f5f08371bd60d971e2a53831a5b4b99c809c222159bbe1d8b`  
		Last Modified: Tue, 12 Aug 2025 20:45:13 GMT  
		Size: 49.3 MB (49311012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442a94d9934ef9a4b080074fc410ad8c41dbbb2f6feb12f9dd9c66686a816e76`  
		Last Modified: Tue, 12 Aug 2025 21:10:37 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:6603ad50ddd242f73e28fd67346645d96318c0281ccb7a127cc9a67a283511eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc0738da5a022bf846dc66069a94ad556fa9e78ec90a5cab4299536df797e94`

```dockerfile
```

-	Layers:
	-	`sha256:058adf0463771e4fd841f0f02e461e7163a906b29304715a829b2bbd30d292c2`  
		Last Modified: Tue, 12 Aug 2025 21:25:16 GMT  
		Size: 3.2 MB (3167917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc5e4c1d33f23769d13ccbebccbc3bc24e984116cb5e76afb70d1acfd70aa94c`  
		Last Modified: Tue, 12 Aug 2025 21:25:17 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:9e07d4b6d863fbcea9a9a6478385de7446800294554cc5483c6e265a1fb0a937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47481374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d863d4adb66eea247b1b5028d4d6815cf093be2e4f97224493e6541a53a9d0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'unstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:a88437252d820d808b38eb04e434ddf003a393401dc451ba5574b698de06f8db`  
		Last Modified: Tue, 12 Aug 2025 20:49:44 GMT  
		Size: 47.5 MB (47481154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd46a1df80fb6cc8c02f2b2aac12848d3fb5b03fa924fc3dcf58bb7e8702b21`  
		Last Modified: Tue, 12 Aug 2025 21:12:09 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:f7a6cae29f90912b827b75eedc302c4981197559ad7319b719691d71daa09bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2c1bab6db74f812e3541f25b657c9559c8b3d37b954c7a1ba1a97f33ff4f0e`

```dockerfile
```

-	Layers:
	-	`sha256:efc3710d483fea3a27ad268d6e12ffab5f1450f83f6e61384cb4d9fbe3d38288`  
		Last Modified: Tue, 12 Aug 2025 21:25:22 GMT  
		Size: 3.2 MB (3170879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e956052f2559d7ac1d02a51b68361634cde61a700d83de8110a2a4136133ae5`  
		Last Modified: Tue, 12 Aug 2025 21:25:22 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:b4c70eca1641cea24dbbab1b9b83f3916938417fdc1707c5088f7b39891e0b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45743520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548165c83e9214f1f573daa6bc6728caa1d02524f7407014737b2d5432240397`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:e174eed54b3c68481ebd1162d2f02f82e3dfeea277a575604f44b83beb0d95cd`  
		Last Modified: Tue, 12 Aug 2025 21:25:59 GMT  
		Size: 45.7 MB (45743300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9331e4526a2809969fec6ae08ab307876a4fa5098b64e920f6f557e6ab2159`  
		Last Modified: Tue, 12 Aug 2025 21:12:01 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:023d25afc954ee9e3cadb1b4cf113fc5a53510dd4cb09ad4289b71a10ca9631f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e33511ab166e83259bacd6b7eb7609e5e4e448b77d18e21bf3c0a43c59ff8e`

```dockerfile
```

-	Layers:
	-	`sha256:be1abf6e3a4d865d18b9fe75b286155a355f13f1b2c3a1c29e1823c64d6e08b3`  
		Last Modified: Tue, 12 Aug 2025 21:25:27 GMT  
		Size: 3.2 MB (3169299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bfffd342e9f19def6a491185bb76a8b74bffdd2d97adb62c367790bded9019b`  
		Last Modified: Tue, 12 Aug 2025 21:25:27 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c0b324607beec221f7ddc2bbb09f1e96c8e3e57bbc39ff909d09c4267e1868b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49665980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e1255f43de36367523558b0552332bbf2943fbffbc73f87df2edf29ad50cfe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:eb3a2c17920faa8b0952114b1b4829ab47f1f72f63b4d23b1027d046618b13d4`  
		Last Modified: Tue, 12 Aug 2025 22:12:58 GMT  
		Size: 49.7 MB (49665759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687b8291a6a989fff9ab7f44c5bda4a958c768b06051083ace97c18cbc07027a`  
		Last Modified: Wed, 13 Aug 2025 01:51:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:b547def95b9c9ba9275884992557a351b679a0fb8f0f47483784082310667438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01ba9a5f42fb9e06ff9e594d3e04380abef23fa7b3927dfbbdaf34b52113760`

```dockerfile
```

-	Layers:
	-	`sha256:de20d9288b85368d15332e927518689f7be291407d78957a0905f6418ee0624d`  
		Last Modified: Wed, 13 Aug 2025 03:24:02 GMT  
		Size: 3.2 MB (3169410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8722297f3bf85e7241199f09eabbc90698e2f61e77a05ba2f199d1af8b28f186`  
		Last Modified: Wed, 13 Aug 2025 03:24:03 GMT  
		Size: 6.2 KB (6224 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:51f7ce1f7a65df20b88152f094f6accef7d6de452464ba9c85cf1ef519d1fea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50819308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3ce2d15f134b21f11ff74a35fa698486d92a12f07bdd01a2a670c578ae02cd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:841571c928fcc7b519177ac970c4935a88b831117cb5b23b23a7c03f73d6ddd1`  
		Last Modified: Tue, 12 Aug 2025 20:44:58 GMT  
		Size: 50.8 MB (50819087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40c5a61a83722c2debb8558d6c7c4c1fa844704d486973c6d388fc86f55f6b9`  
		Last Modified: Tue, 12 Aug 2025 21:59:02 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:412eb322a6818e2fbcc01658d76f20c2cc3d316e7125383e1c8ccb7834c75349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bd38185f2736487b9fd032563127c7c5502451f07f83229b36b673460665a7`

```dockerfile
```

-	Layers:
	-	`sha256:2940e8cf32bc1fc5f2fcf700a3456569a2443cd0d563db7e387c73d51582028c`  
		Last Modified: Tue, 12 Aug 2025 21:25:32 GMT  
		Size: 3.2 MB (3165116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b516773d342d060b2ab1b68f28f65b40a81791a6545bd87c032f362edb526a1c`  
		Last Modified: Tue, 12 Aug 2025 21:25:32 GMT  
		Size: 6.1 KB (6120 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:5a60bee6386ee080c587934d4dff1535a8d1813ef2cc46d454b483bdeb19d944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49562509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0643d758e43d1b1c6b0c76d9fcdd210b4bb6c8e48fc8e5bfadf989b4bba7fb1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'unstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:9ce69fa10ac1213ded740b15ea82dc3df6ba39f87bf5e1a4c93c31b66e33194d`  
		Last Modified: Tue, 12 Aug 2025 20:48:05 GMT  
		Size: 49.6 MB (49562288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04c3d94bdef47844ba8bb27660337bfb57ed0fc39a389ec214a098fcaaf86c`  
		Last Modified: Tue, 12 Aug 2025 21:13:03 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:d564ac04609338844cccdd6b27287968d136e892e259845ec5549ee716645696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 KB (5977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289ab97a72c2eafaaa45bd5a64cb6d9a39ccb399d89c7732ec7a9a7958ce0976`

```dockerfile
```

-	Layers:
	-	`sha256:3cac051bccff6f3f215111535c1485fc51dd0376401f65da43f4ced03613527b`  
		Last Modified: Wed, 13 Aug 2025 00:24:46 GMT  
		Size: 6.0 KB (5977 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:d1552e829c1fe6cd448fa2d5e9d07c5e03877e24a0ba01ccb6ad237b00b52319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53147974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66765c5607ba7ec3e0d1aeb1a296ebe91245094bdc9e540bdd17c7bf9b7b1041`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:687391c95aeb26f00e49fdade9d76a9f981bdd50d9f017d664ad9d8cdbd644f9`  
		Last Modified: Wed, 13 Aug 2025 07:00:15 GMT  
		Size: 53.1 MB (53147753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f63af9362b6739f38e54eb687132cda65e71ac9cd9047fb0b39238b7260a7e4`  
		Last Modified: Wed, 13 Aug 2025 04:33:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:b7e92a51dbcbbb8baf5a77c0e01c6b76c81da4a8813d3fa6d8fb80a14226530a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb3bc719da865c966d0ce5eecd250f73425fccc4dd143627d80a378776db289`

```dockerfile
```

-	Layers:
	-	`sha256:f6c4931d3d70bd5cce807db7b15d6c485538c3ddfa948b8cb82dad48c6202f54`  
		Last Modified: Wed, 13 Aug 2025 06:24:01 GMT  
		Size: 3.2 MB (3171432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d89b0916d752d19b151c90e4a41211d8d19ca9519d99aaaba986130fc4435e2f`  
		Last Modified: Wed, 13 Aug 2025 06:24:02 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:13634370752fa850bb0a6882a32f9f80a423322e6bbb635bf844f077a000f6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47776783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270c6c0b2dd0204f131e3b88f7c23b33ecadf619283b477b076f7855640e9d53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:49905211581fe3e61537fd9efcf132c0adce7bb2392c9b012120b155453a504e`  
		Last Modified: Wed, 13 Aug 2025 07:00:15 GMT  
		Size: 47.8 MB (47776561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff468d20aea9d87e705a5ebb841265f164aac86014ee9715fe3f56ff5e68b2`  
		Last Modified: Wed, 13 Aug 2025 07:46:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:772baf43ca8d6604659403f6cd953829b01b01ecb336db7e5de75d1fcead3628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ff1a3d58ed6ea8e6782f2c97ebce23cdcbbfc6dcd1ff18fef04fb7e290ae61`

```dockerfile
```

-	Layers:
	-	`sha256:5d711f6f1fc5a077e7f394ba8560a973fcd6eeb5fd1e39d583065e93b648bff1`  
		Last Modified: Wed, 13 Aug 2025 09:24:05 GMT  
		Size: 3.2 MB (3160186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa476d480931b4b7d2f4336cceb429473a128dbb20d8de52ee81bd93b62eb398`  
		Last Modified: Wed, 13 Aug 2025 09:24:06 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:c1c22841502baff04b2fba50fc6a39a16ded946fe738e1ad16c12d1b11d7b67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49380900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee072a7395b732d1b7ff1f8d2b68ab7988ffc5fe5d2c3f520d2995198518b26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:3d1a1383fffab0d05429d49bbef0155bfa087b49637ff2aa894e4ba619b18f4f`  
		Last Modified: Tue, 12 Aug 2025 21:00:22 GMT  
		Size: 49.4 MB (49380680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d71634cdbe188ab11a206ade0be739217ebcd2a0dc9a39575f5d24a9449c688`  
		Last Modified: Tue, 12 Aug 2025 23:16:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:6ff758d48625fba7d4f33aab3a865ff97910e33a1c3a7455632d38a590c1742c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be9be02084b38d0d2b4e308f446a750ad23b0574d169cfd6992040449ae7a65`

```dockerfile
```

-	Layers:
	-	`sha256:e28085f33bf39266dbfb06466c7d95c2719e960a0d6154dee7e4a888ee2e8d2a`  
		Last Modified: Wed, 13 Aug 2025 00:24:51 GMT  
		Size: 3.2 MB (3169364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d474569cb02ba17af7ed076fba58eabe7ce33f771735dbcc8077c042999127`  
		Last Modified: Wed, 13 Aug 2025 00:24:52 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json
