## `debian:stable-backports`

```console
$ docker pull debian@sha256:da70d1fb017512f5c88c7781b90f30ec38ad785c5c4f6f44ef5d3b977c872d95
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
$ docker pull debian@sha256:7fb596a4373e6035f0fb9fea20c8a698c7d86cf1e9557836eced8b740e752310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49298057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b174ee7da68c30591231a50df090d9019d60ef3ed4080d2897879c23f39d82b5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1775433600'
# Tue, 07 Apr 2026 01:16:52 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7278849ec4822a1f503b14378b86a3f2f6c343e7284462c9cf8875869e8ab383`  
		Last Modified: Tue, 07 Apr 2026 00:11:17 GMT  
		Size: 49.3 MB (49297835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bacaff060bdf9cc235cd306025bac157fc3d0d281e40c4d752d6158d3e3110`  
		Last Modified: Tue, 07 Apr 2026 01:16:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cd49779dd5007a03fb0bda4cae32980832950fb871eed9fb3a38b3423db80bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1cb429d56aab1df3c302d7104b947f4bcd81c254175ebc8ae3237edfa7033c`

```dockerfile
```

-	Layers:
	-	`sha256:10263b13d276c933ed32d80ba5050adb2bbee0ec03f927ac161c7152a10a466c`  
		Last Modified: Tue, 07 Apr 2026 01:16:58 GMT  
		Size: 3.2 MB (3170913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3358b12c2ddcaec438f4b10a04784edd05a2f26f4cad5695feb3900cb729ed9`  
		Last Modified: Tue, 07 Apr 2026 01:16:58 GMT  
		Size: 5.8 KB (5784 bytes)  
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
$ docker pull debian@sha256:404a1b155bdd77cfdd6eb44b943043cdda7d8b7dcc6ced9d5829c39fb30e31d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45733219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47285eaa9e0651afb2cc6b32bcfa57a8278703fa4ab708688627692673395fc1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1775433600'
# Tue, 07 Apr 2026 01:15:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2a71761f5c5b417f0f7dbd670162ecf8fbd045e16bf41e32201ce92ebd2f3571`  
		Last Modified: Tue, 07 Apr 2026 00:59:49 GMT  
		Size: 45.7 MB (45732997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78152e3edf9e686388e26c1c1a817a428e5cb78e6f40d2c5412f9c4e6d99c15`  
		Last Modified: Tue, 07 Apr 2026 01:16:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cdf61de18ce605f03f247a24c48ffe5c96e82200499ca3874fbba98dd2e82dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670f790ea085e139a8f2839b915eefbae95cd8553dc60badf09c300687aedfe3`

```dockerfile
```

-	Layers:
	-	`sha256:92f837c345dd63900aa6596d9e7582bea680bfd333c62911cd02b3bcfec17ec5`  
		Last Modified: Tue, 07 Apr 2026 01:16:04 GMT  
		Size: 3.2 MB (3172287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:608999a863cf43c09dc2b975b25857420beb903a3c848804c453d367d489f5a4`  
		Last Modified: Tue, 07 Apr 2026 01:16:04 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3d18ec66af4bdb1da3d9d61deebd10f4e0fa7c21e13db19aabc72d0f410c2ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49665479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a506938cfd22b41110703a1f0410615601fad767b2c53f52d91ccc8f87ed6c38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1775433600'
# Tue, 07 Apr 2026 01:16:13 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8d7cd5f6eb41754eb4ccaf7765c15797902f122902467c89c7a75d825e3bdc9a`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f75932f6982a1c10b0829ea76659e845041933864e0972bb1ba72986c7e462`  
		Last Modified: Tue, 07 Apr 2026 01:16:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:53ed4af7cc0ed52c1ba8fc8c2a7c463a5d74ec371753e327cdad1da2f12162b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33307750aa6aee6499375a0d957352596347bbfe53b16fc37bbfd2d281c832ae`

```dockerfile
```

-	Layers:
	-	`sha256:964827d128281bf8f77762faffe3db294c1c20a54a1cd55f9277ed2f391799b0`  
		Last Modified: Tue, 07 Apr 2026 01:16:19 GMT  
		Size: 3.2 MB (3172394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b94bd32a4f32a63bbe77cf67bdda172c7abb6ed6bad19717e377120e157eba35`  
		Last Modified: Tue, 07 Apr 2026 01:16:19 GMT  
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
$ docker pull debian@sha256:2b623469da8f03f98f2edf03a40df091423851cdeeaa9fd1d0c2e41c1ec98b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49365331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7824f3da78696b31553f35f58de45e8880e5c4270f823173dd4d9a1d484612a4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1775433600'
# Tue, 07 Apr 2026 01:15:58 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a69cebdd8de4f9dd975cffdec21fe8e58c44320100c9ecec5e1e34d761e872bf`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 49.4 MB (49365107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5a6f991f137793e310250d9b748d024ffbfd7335492d4c17b87629773a8115`  
		Last Modified: Tue, 07 Apr 2026 01:16:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:73457bdb03c7f73fcef86e12a52ca53c9efc1aac51f6ff99f7222ad9378c49b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997c808aa4ad500ffd2c24f6d69b7cc4c7421c57b8f2e404d9584cb43d60fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:2e3f8f8f1d9bcb7807d08173370135e30402cbdc843304563a6d5e9658bdfc15`  
		Last Modified: Tue, 07 Apr 2026 01:16:17 GMT  
		Size: 3.2 MB (3172360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6914c20c56efaa23aabc87b37ce2c3156d4391d456a17acbb0b461d1c612438`  
		Last Modified: Tue, 07 Apr 2026 01:16:16 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
