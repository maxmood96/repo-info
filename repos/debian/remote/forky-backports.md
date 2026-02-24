## `debian:forky-backports`

```console
$ docker pull debian@sha256:cc7ea93d2e9a2667973693d6418f174d2e179efe9243a568bcbd98b7d092526f
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
$ docker pull debian@sha256:15fd40b52dac2d60e83ee6d896499cc6ea9068a5692710740d81080bdc2f95f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48677405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d59b2d4bd3863143afae767459bc2e9053c7adee29d46abf805cf914ca5038e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 18:51:40 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:501906f379a13fc3675791cbd6304f648074973affcb965be0bef8b0aaa34ab5`  
		Last Modified: Tue, 24 Feb 2026 18:43:03 GMT  
		Size: 48.7 MB (48677181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992c232695dcd016baa5453eaca3fef20cda3eed3a2214c98a86459957768ed4`  
		Last Modified: Tue, 24 Feb 2026 18:51:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e14d090d12268af039c2b74dec00be41866948ef904a30fc17f1e8188b4cb7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e809d480c9ce562210268dfc21c153494e7cd12d93e92fbb1f96aaef3526705a`

```dockerfile
```

-	Layers:
	-	`sha256:9c8beacad55a7165c508ce45bf1018a5f087fcc70c15ddf35216a9150ea9c8aa`  
		Last Modified: Tue, 24 Feb 2026 18:51:46 GMT  
		Size: 3.1 MB (3147560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e057de71f537587bd1ca11b407677dcfbd5d0a3b8eb50f2532a2bd82f50c94d1`  
		Last Modified: Tue, 24 Feb 2026 18:51:46 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:baa33b6bfd79fd2185f466a3f83b02c9c3a711195a5c534a6b0442866b167f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fafa4e0d3bf5181298b47563c04dc8bb866ba165dda37a010f129980af9407c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 18:54:08 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b74010850dba4ef4e0d65d4c6bda126a2de154bff6afcac42cad46a2cbe16fc5`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 45.7 MB (45653048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc218767e01528b20b10e68868583cca830a7cd6c10a9699bce02da6068f415b`  
		Last Modified: Tue, 24 Feb 2026 18:54:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:23052c55aafde9024392fe726870c77fdcdc2471bf11fdd5465783cf3a24c91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bad32570659cc5af00656bdc8a7e870fd3c4af4689f3b2b7b8acc92321b2b3f`

```dockerfile
```

-	Layers:
	-	`sha256:83ac4096736d120cd63875f6c4632dc8f3ef9cfe35eae7865d9547de5c055ea3`  
		Last Modified: Tue, 24 Feb 2026 18:54:15 GMT  
		Size: 3.1 MB (3148928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c2fbb9c742fb32cf818e231a14abbd7ea5d41b844e4f8c9b887a450861187b3`  
		Last Modified: Tue, 24 Feb 2026 18:54:15 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c1a4a3d2033bafaaa3d0c0aca5c56a6e4435187306ef088cc9108c1a20ab5311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48705249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65650fc400c0e351af13b17156f15361e3575998cad8368eb29eb6008a0de40`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 18:56:11 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:dc3ce43fbcc581a6cb3e0909e03d7e31c0ff1d4d76469e15d6610d1403f2a7e0`  
		Last Modified: Tue, 24 Feb 2026 18:42:39 GMT  
		Size: 48.7 MB (48705026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3e5ba22d4e6aa260333c0a80a1c7c1a9dd072222ea36d12395dd784e6d7522`  
		Last Modified: Tue, 24 Feb 2026 18:56:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:470e85771ac534322c93ca5cb34746231a4da5757c4e9ad028bc0d26741ce701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4612fc70baf3882d2a761a386d721ffd2f3fe97b554e136d97de2c39f9e375`

```dockerfile
```

-	Layers:
	-	`sha256:1a78e493d3f34834dcc1624904957909d029481b65360ee4917ec09aae021f39`  
		Last Modified: Tue, 24 Feb 2026 18:56:18 GMT  
		Size: 3.2 MB (3155608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57899e0c5c5aff180b4edc7d7efa01197f35cc9d4a2a4fe0da6575f07258cc65`  
		Last Modified: Tue, 24 Feb 2026 18:56:18 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:d33cd0f94e127567c0dd2197c13f63f1d6217765b50fc9a40f1766bb478475c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50012192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bd26b496b04c9efbcf5bb9ce92078d822151bb2eaad9dcd42e890b242c078`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 18:53:07 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:143f133830d056570eb26009a5886b146c40a6e16bbee60113f54a6baa1643eb`  
		Last Modified: Tue, 24 Feb 2026 18:42:19 GMT  
		Size: 50.0 MB (50011968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac59fe16f9f6a2419c2d9d7eaba394daa7dc70cb11dca133a45cfb347b8d157`  
		Last Modified: Tue, 24 Feb 2026 18:53:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6149abb216304d687ac8f487dfe0700d1bbf536e40788ebb3104a8e4b5ef393a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0c9e04b78277760a60250a3159b179c7738b5fbd432ca8585e414a915509ad`

```dockerfile
```

-	Layers:
	-	`sha256:6193eaa1caca04024196b3cf3e5bd01b8cb90daf96f86403bde5c516dc8ad36c`  
		Last Modified: Tue, 24 Feb 2026 18:53:13 GMT  
		Size: 3.1 MB (3144758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db6ff5adba9c6d7bdb76450cb2e462403cc2fce242f42f392bbe8f327fa9c87`  
		Last Modified: Tue, 24 Feb 2026 18:53:12 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:7abed68a94ebc261b61a40eb4d03970736216692af81ebc035cffb5299d31c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53642010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5c5ad3a40d10caecd32d3881f94b7cfe533c640ff62e4cd274f3d799b4d21b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 18:52:36 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f1e7241652efbb83270036a6221c3c25c51e9feb8307ee3c94f7e0d52832e1af`  
		Last Modified: Tue, 24 Feb 2026 18:42:31 GMT  
		Size: 53.6 MB (53641787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a3f747af7d60ea35f790f1f2c5422483d18e800eef4775fb2968a8d54d3c5b`  
		Last Modified: Tue, 24 Feb 2026 18:52:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:07966e7b7865d4e3580e3169acb892c9ee0ac67bb6b5f31a53987ab33f88804a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d08eaab9f6f63d4333dc1b8a92ab960675fb2f6d94bdaac5ebfab761a9ae6`

```dockerfile
```

-	Layers:
	-	`sha256:e9fa0ab7155c73e7a38b246e767b7139fd00868b62c19c1bd6b2a4b1231359b6`  
		Last Modified: Tue, 24 Feb 2026 18:52:59 GMT  
		Size: 3.2 MB (3151075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d25168e6815ef0dc975935cec9223018908d8bcf01d8ac43b29ec3dbb0bcc386`  
		Last Modified: Tue, 24 Feb 2026 18:52:59 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:03b77e14f7a70a7899371da74e75002f01115f625cff89b68b2f5343b8c6e0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46914629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c810a96d407cb4e46c28c9e428d54f1b174c2e245e5bef9e5dbff88c8eab897f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:04:51 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:db31b4401b1ad39bc8394e302320dc063e12e2c0464e6a8103701611daac2f3e`  
		Last Modified: Tue, 24 Feb 2026 18:43:31 GMT  
		Size: 46.9 MB (46914404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536c40acf87ca91e9d930e7f9c0af5c07c3cb52179aa09e078069072587fbbc1`  
		Last Modified: Tue, 24 Feb 2026 19:05:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2cd7aa93f1f3d976fc0e8c2d49c0e5bb3cf38d6bbe439b971b1c8edd0afa7656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca04cc9ddc0889c9244a8e487683902aefb05139f2cabf2731888d6c31c293f`

```dockerfile
```

-	Layers:
	-	`sha256:2aab76664099a245b136e04f329066f1d593a428200c9fb849e3fc35b79b5de9`  
		Last Modified: Tue, 24 Feb 2026 19:05:46 GMT  
		Size: 3.1 MB (3139070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da11b2271efd5f741399226473fde325d0d1647c6a19553675fe17c2a0847c5`  
		Last Modified: Tue, 24 Feb 2026 19:05:46 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:e327cc8d74df4e37e6974793b20eda8da1ae4fa2bff1fed09d9563d9b630681c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48448576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0446fff8f780a156b43115ddef9c6f930533fadf9ae842c6e215ee9250aad5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 18:52:50 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f21354992e07f04a7de86938f41ff3c72cb8dc33252e2b2320b4169695270de1`  
		Last Modified: Tue, 24 Feb 2026 18:41:36 GMT  
		Size: 48.4 MB (48448352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83f1c57690f86e69cd7fe37463b2c558debf2d68e7f3cda2f3028c62ce9629`  
		Last Modified: Tue, 24 Feb 2026 18:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0d9caadbf09067efe295db073dfef80f834522ca507fdbe4348481c9f70ca7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a23cee7f50c2e572b90dede117eb6a98b5db1e2d54486f3db39ad17b9640933`

```dockerfile
```

-	Layers:
	-	`sha256:100eeb30a9fd212c065fec7f7fd9f9c95678dbf08cf51f5bdb9cbcc562159f10`  
		Last Modified: Tue, 24 Feb 2026 18:53:05 GMT  
		Size: 3.1 MB (3149009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56615b1071eaa93864898ed7f8dea4fdc7eeb724f3a6447f33823e68fc20b5eb`  
		Last Modified: Tue, 24 Feb 2026 18:53:05 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
