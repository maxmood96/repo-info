## `debian:stable-backports`

```console
$ docker pull debian@sha256:dfe2323bf78626fed08992e223dfdbd2845a3a1b8afa47d97b7b908026f51057
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:e27cbf40526686db82c96f2ddf59b72ba37232b0f8a6ccd2571be733cd07ecd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49302325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87ef4bea12f416c7ae56fcd39336a7baf0367a0da87be3e369aa4866d0cf592`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 01:15:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8061bf05062d424c77b9489757e4e7fdd853c4d882ae0ab30ea6bace2f806dca`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a040fd9e4af166a6f1ed2091636d7391b46d1da40e5962b97f23ec068cfdf040`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:843d32519ec7c58492ce2719e1b635c27a281394b7a5ca1e8676aa4924e6b268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be57d28988bc9b9d6091a000c55e9a507137a7d6165375f26467a09a341b0877`

```dockerfile
```

-	Layers:
	-	`sha256:a17bf44d0b19b5c37e0d6bd75f5072cec0ef9edffb204d597aca1f01a57a9892`  
		Last Modified: Wed, 22 Apr 2026 01:15:33 GMT  
		Size: 3.2 MB (3170913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c0c3d963ae1b747ddeb3c05b097e6ef40d52ef375b94b69fd09deabe3293`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 5.8 KB (5783 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ac4829a698ed94ade872b28c546c62e63d0bb0faaebb112d5c5f1631aab34b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47461115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbc286b03098108d752af7d98d07ff10046c6abf66ae7a8385408aa5419311a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1775433600'
# Tue, 07 Apr 2026 01:32:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2702209661b24cae974413016a03ea6db38017a6d2d290ed0c75a4fb448d8391`  
		Last Modified: Tue, 07 Apr 2026 00:11:23 GMT  
		Size: 47.5 MB (47460894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01b944769790b27602ff65900e641b336ba809482be642665d58bbbc113088d`  
		Last Modified: Tue, 07 Apr 2026 01:32:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3b11a2d598d31f63ff157792818646b15154666a2a5d4adf66c33daba3f52609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b014e14422ede187dfc6a651c7dbd630c7554261b27d316003887daf89339d9`

```dockerfile
```

-	Layers:
	-	`sha256:5455ccae10847f43f45071061a5194e46c6e084a8a104a7886bf3b538d62331b`  
		Last Modified: Tue, 07 Apr 2026 01:32:57 GMT  
		Size: 3.2 MB (3173850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d71c1cc10643f6812d654b4f5cabb30463aa0ca36a9be29aef4871517fd62c`  
		Last Modified: Tue, 07 Apr 2026 01:32:56 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1c7d91fb0c6596fe379f400233233832483df67d2327ead817ab90c640f129fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45738420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6100bf48b3257e2b4176638f6877bf4b9fa19aa56a0683ac04d278bd351bc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 01:15:06 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:597e80ce2b6b93e238072fe4ac1a1e7773ffb2578b0fb5742e6c7bbe14f74f02`  
		Last Modified: Wed, 22 Apr 2026 00:16:58 GMT  
		Size: 45.7 MB (45738198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89251ade1fb45888ecf0ec3fd59e9fbdc018341c19565129140d6faa6bc92bc9`  
		Last Modified: Wed, 22 Apr 2026 01:15:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:18dcd81f0d769031ab31f3c09b100c93d365a6e29f15f748cb9954aa496fa396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b736ffd83cf4fed292fb5f1df0fac66e5c04f3e2715ff6c2f6968c0cb6a118`

```dockerfile
```

-	Layers:
	-	`sha256:4aefdcf566900cd6ddb1a3a49729e4eed2957417d047d66c3a3fefc0082bd77b`  
		Last Modified: Wed, 22 Apr 2026 01:15:13 GMT  
		Size: 3.2 MB (3172287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57df933c114fb0382c175258c0656d9c9bafaab243a34b0264428a41bf2c2414`  
		Last Modified: Wed, 22 Apr 2026 01:15:13 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b4dee84c8aa8998924692e02ad6c87abd3d37f99cc1592a15cef0a8f7cc6eb6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49669467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0489e7c98e19135f0fb4e4ef227ed5f701301ce437f9be54a143e981d052fbc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 01:15:08 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:af0f848eaad9dee8a2e444559611664d0d8d12cb61a4dac40d312ae66c50e2c9`  
		Last Modified: Wed, 22 Apr 2026 00:16:34 GMT  
		Size: 49.7 MB (49669244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bb2bb9f66c276cac70672f9bf517e569f846c1e2a54e2f50d5a80304ddc01a`  
		Last Modified: Wed, 22 Apr 2026 01:15:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:355ca21ed24b143b259b2736d358e2deab2164a26d3140b3556158ace712dad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af8874fad43e3be587828d18359db3670a7be5240cfcfdeb68b1db943ab47cf`

```dockerfile
```

-	Layers:
	-	`sha256:83a16ba041bc42c69eb2e3fc98f970007be18515a7c0c53383361df75beca695`  
		Last Modified: Wed, 22 Apr 2026 01:15:15 GMT  
		Size: 3.2 MB (3172394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b74f4337faee3260e1a485b0a1bb40690c0f62f5f383464e9a19453e4310553`  
		Last Modified: Wed, 22 Apr 2026 01:15:14 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:1450da02f572f223c4812a3734cd529eaf5901666afe467d17ad9aa7b6f0d855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50819310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b42ea22548bc857387107c0381c3f7d3ef179b44289ffff1b36bf6afb7aba67`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1775433600'
# Tue, 07 Apr 2026 01:16:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1a276381351d9ea931384be14f3ae40499268086568ac420762532808043a069`  
		Last Modified: Tue, 07 Apr 2026 00:11:44 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b48e540d0e3ca4adfe9c62156b2e2a2987987293f6e072b52da63cdb7ffac7`  
		Last Modified: Tue, 07 Apr 2026 01:16:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ff240dbd303b7e0c9536713353832952aeb504f58e32692aac855da13a387ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b2a66f827eba1c3a6ea5e01810b07f3d4bb67e32999000e577b6105f2ed1ca`

```dockerfile
```

-	Layers:
	-	`sha256:b2eee81d58f1f676770f813dd89d53a4ed865257cba5ac0d7c95ae9aab7852f0`  
		Last Modified: Tue, 07 Apr 2026 01:16:36 GMT  
		Size: 3.2 MB (3168115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6eb1422baa8559056086ec74c46257ead8ec8ea5bcd6e04160ba2c1c1b0e2d5`  
		Last Modified: Tue, 07 Apr 2026 01:16:35 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:103174f03c636b93944223538bac0cd9643c59a32e6b4e9885e4a36bc118862c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53118894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0bddd6c3c06e36513f92283588b9a419d5ed88869d0d68213f1ad5df7cae24`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1775433600'
# Tue, 07 Apr 2026 01:16:18 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:45068c0ed4eab27204fdf198c80ba649af7f9435f06024a6f12de0619823606e`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 53.1 MB (53118670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc75e64d9ccd508c8545f4e22eb7c8160babeab6ae0550a40fe1e16ca142cbb1`  
		Last Modified: Tue, 07 Apr 2026 01:16:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:256b2d6c72b89db7ceb2a7d0e43974e817b20490c4154f6b2a916fe2525ab4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ad0eee242d4529f3daf0983f28adca270de0a8ef978777410649a9558ea7b5`

```dockerfile
```

-	Layers:
	-	`sha256:bf5de9fc88653336476b0fdf5265d090e5d351590a3dca6251f13a4269a002a7`  
		Last Modified: Tue, 07 Apr 2026 01:16:47 GMT  
		Size: 3.2 MB (3174426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c1e18214504d06f6be8656002ca8221dfbd966d2c43dfbb993aae4a85451304`  
		Last Modified: Tue, 07 Apr 2026 01:16:46 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:19cf3940bb64ac7f6177dd980325133ffcddde1f08a4b7b38f2c3c902f836812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47792845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8ad5798b5e74fa6ccd99d32e242091b2a5d802926b242ae3b0068d00be7fb9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1775433600'
# Tue, 07 Apr 2026 02:29:22 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a12d00e95409028f3b20c7467d2a9a9ca00b0e2aa0537e3b9ed4b310fd1aa0bc`  
		Last Modified: Tue, 07 Apr 2026 01:47:18 GMT  
		Size: 47.8 MB (47792622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dbcba62b1eb01fbf44b9deffdb8f365b20c3301244b9748549a536de04af07`  
		Last Modified: Tue, 07 Apr 2026 02:30:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cf87418a2b77a641389833fca49597c00caf5b95a40864d1565c6081ba701272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b07a304003fe446a5273d6c09353eeb07b4e0b38e69d4befde0168231af7d7`

```dockerfile
```

-	Layers:
	-	`sha256:daac21cc625bd78479f7e0fc540ce57deb67964cbf61e08fce6ec2272d1694ee`  
		Last Modified: Tue, 07 Apr 2026 02:30:16 GMT  
		Size: 3.2 MB (3163238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b1ed34f2b372d469b72d65fdc4c49fbf22ad056b37e440af23371d09a2b2644`  
		Last Modified: Tue, 07 Apr 2026 02:30:16 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:cb69bb27e1784b223270c5eb34136c847f30689b4987b0b8b43936b24afa734a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49372328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b25a73a4ebf46ce6935092de7581eeb13d095777a415fec464efe7977ce7a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 01:14:01 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6e48cdb6e56d2da8434609565fc55b1a806cc98aab46cf8ceefa77c2e90fe7de`  
		Last Modified: Wed, 22 Apr 2026 00:16:36 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6cd79f2d4783c5b70372002098a86c9c5080a92616a06e71709a2f8b136bc7`  
		Last Modified: Wed, 22 Apr 2026 01:14:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dea9b57065a122b3a2603cfa2aab5fc6b4321506a07a07b3c47503afe7b824ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d531104d61605efe9e4315060c7a0dabe45a3fedc88903f8f0c26c32ffb548d4`

```dockerfile
```

-	Layers:
	-	`sha256:75bc71d903265100d1e737bed8cf8144a68429a60102e8e1de0721b03c1c120e`  
		Last Modified: Wed, 22 Apr 2026 01:14:13 GMT  
		Size: 3.2 MB (3172360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a086c9272db4981ce5b7bafc11785417f0d36b2fb3e8f9e462551132620b553`  
		Last Modified: Wed, 22 Apr 2026 01:14:12 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
