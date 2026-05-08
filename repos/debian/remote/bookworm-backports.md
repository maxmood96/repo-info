## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:d28be3bd7bf41429ced9ea95197b7c3e967a001657a74abe340a55f57f9fbeb9
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:40fcc1902a3f4f40ac28a68d5fb0acd37d78362a784c86517954f630b8b996ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48488854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0582ef4b639582a13b0565bedca464bbb8080f5da8442b1f5e7e34d11c975dca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:14:53 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704dcfc20539d2071021b0928d5463d8ec18b198fc26135bc5dbe126873ea552`  
		Last Modified: Wed, 22 Apr 2026 01:14:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b93cfcfce1061a489916288deab676843ae9e729bd5b5439f20ed63a3a1c597c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e19ab0e6d372081c8e79e47b6757d8656873dd3dd84af0099002df65060dd5b`

```dockerfile
```

-	Layers:
	-	`sha256:72cb221cac1d7dc32939cc821bedde8db003199254d4f2f7b04d341a1b273313`  
		Last Modified: Wed, 22 Apr 2026 01:15:00 GMT  
		Size: 3.7 MB (3734074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5132d060e7f07ace38bde82de2c1ab440473169bdab0ba3904597a37b1ded09`  
		Last Modified: Wed, 22 Apr 2026 01:14:59 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6fabf9571fba47d8345c071ec1c2c9a5b2a18aec8c9389dffe3ada05e356061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e592188d7d90c666b9d7d3d1e2a59dfacc144e268083b01f62723aec7b90af6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:15:07 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4c47739de5592cd0e20e88645e3c951f4f15c777c5919d72ffd47300390dc284`  
		Last Modified: Wed, 22 Apr 2026 00:15:32 GMT  
		Size: 46.0 MB (46021502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c651f1e3b994684f6cb745fe3b35717b106eb1bedfa08cbc09e1a311465c13b9`  
		Last Modified: Wed, 22 Apr 2026 01:15:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5f2dd87dd607c3d4ed4e528f348a91b7ac0396a45562a2370150244492348ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d76e40e02ba961f44d1b21f1a46a97af56ee2304090ad6b3cfaee0f65a1196`

```dockerfile
```

-	Layers:
	-	`sha256:da89371daf580aa3df0087f6de0ece98db0cd0f0d174be7ae4c1d72f4e476f02`  
		Last Modified: Wed, 22 Apr 2026 01:15:14 GMT  
		Size: 3.7 MB (3734275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:368a1a190e3e9c3cbec26a878ee288b2576558a3b3de08b926e88092544e0bf2`  
		Last Modified: Wed, 22 Apr 2026 01:15:14 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:220973eabc534591fa5337dc2b77cf0f133901d2e578a5d86f3ccc00523e6f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44207880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb222913ab4303ae31859fd0f720188db034b6009dbb1422b95c4c5498a4a83`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:14:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ecbc41b1ffa11c8aca5f55316103fdfd4fd622e29d09b9978a038fcfbe3c38`  
		Last Modified: Wed, 22 Apr 2026 01:14:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:21a053ba722afc9c2a3c189ab9bfc6533d340b227501b6681f4e336c6c8dbf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2729a3a7ff0b1507195805448a6fd97b7bbfc60c2179ac74402f9cd63d3f32a6`

```dockerfile
```

-	Layers:
	-	`sha256:4918a653f0fc4d455cfd73122f2be42ec1e7c0d14d92d3d81856c4c1722e838b`  
		Last Modified: Wed, 22 Apr 2026 01:14:33 GMT  
		Size: 3.7 MB (3736253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0b363f1f0b014b79c799cb3e35d686fd2441c74ff88f709819623e3145cbb0f`  
		Last Modified: Wed, 22 Apr 2026 01:14:33 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:da1a0be836c8b84a5417ab149b490c1bd16dc142f13cc61f12a5efeae7be6fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b46cba66d0a968abf1ff1cc47ed6463052558474f6216e2bd594f4accf5a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:14:38 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72a4f55194fd7bd6bc949b7c9f0f3a1b4f0ff21c67f42d855c34fccb0138365`  
		Last Modified: Wed, 22 Apr 2026 01:14:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:73840076b1274a9b44d5a61c65736c83c91bc1d8643e6c9f445b0f24429cb11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039e348aaa8ab07d84ef7bedd27f8ecb30ce3b7c4ceae5556cbd6ef09bbef973`

```dockerfile
```

-	Layers:
	-	`sha256:e75460ed71d34102c688dcd19a60db7f45b0feb7e84f8096191e30c3bc96d2da`  
		Last Modified: Wed, 22 Apr 2026 01:14:45 GMT  
		Size: 3.7 MB (3734289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e92b8f218bad77077cfc6819167cc97779bf26091e998fa25bc531b760cdaf`  
		Last Modified: Wed, 22 Apr 2026 01:14:45 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:18d5f8ad6e49186ff67de9c5a9bd75818dae37e2b6fdf8d9bf54f780fe14c6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6646b4d2b67307254869b39a403fab72fc081e60068c6e3ef3c669fc538988c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:15:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8953b02261fb91b1640549c4e03b1f808f9a62bad344549f2309ac6e969f2c`  
		Last Modified: Wed, 22 Apr 2026 01:15:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0a929494ab9e117b832730202f6be11fa9b83ecb6fb9c4fced19be786dd49cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d9be8d5110391afff3fb5aef8c1d192a450f5cc5ab3157e12e3ad9ecef8ca3`

```dockerfile
```

-	Layers:
	-	`sha256:a7d63248309a32b680c483b278d4b5f7e95b50292d66cff980b2c601b4052de2`  
		Last Modified: Wed, 22 Apr 2026 01:15:07 GMT  
		Size: 3.7 MB (3731270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee44635cbcf2ee054f30664813226cfca0815284cfbbbf4c623de2e4d3bf0f9b`  
		Last Modified: Wed, 22 Apr 2026 01:15:07 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:6e7f95b2b664bce7c3f4639413b352de88746e87ff164d3a2a0cef3a2ea96c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52680c1a4a4a16414509494a1301a7f533bcae3ce64fcb56f55dc3497da0125`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:14:13 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:08baa8fe1f531703c14c631b772a987ffc44ae832951ae77c2cf756cd9309b97`  
		Last Modified: Fri, 08 May 2026 18:19:35 GMT  
		Size: 48.8 MB (48782513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36704f77658acd30bd7e5a54d551f7f0996ddf866dcf55d9ae246360b944611d`  
		Last Modified: Fri, 08 May 2026 19:14:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:39031c439dac56a4b1f0bbcb0b054f4874e2acbbf3314c233c514996cba9c5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76acc529ee8b76620f011011f6cf16ad676d64d58aba6af759860388162d1034`

```dockerfile
```

-	Layers:
	-	`sha256:4dfeab2b67792179fbe9c8f8647104ed1e739320b038969ffb193432ca51c12c`  
		Last Modified: Fri, 08 May 2026 19:14:29 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d48db7917e15ae7148ad58bddd1d7c8b3a88c1d477e02efd0948ac7cadaed85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52336959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81c5f17b9e289d914d822a169f530f15b0b613a6a2c179b1bfa5e804959bee1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:13:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4276747f11131a9eab59c95513f57c241148d00240bd13de3ade97eaf8cdf0`  
		Last Modified: Wed, 22 Apr 2026 01:14:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:92b3b480f58dc74b757d015e541c0f314067e3bef3a5dce9ddaee0c9adeeb37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bf452c6aea06e3ef1dea9b4435a108f7b2c1895c2a3682f9a8e65018393ee8`

```dockerfile
```

-	Layers:
	-	`sha256:969f02eb0e1ccf6b64ca97d9b27a9ded2ef9d95addb86cf77cf0fe806d2b5782`  
		Last Modified: Wed, 22 Apr 2026 01:14:19 GMT  
		Size: 3.7 MB (3738432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa29987fb5b072fa65d7de50424ac8d80da4a20bc7bda2a9c154dd3be13de73c`  
		Last Modified: Wed, 22 Apr 2026 01:14:18 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:8136613527f18f03b543fb8e52b6dde5ab3363310bbedc9e4f6e6a060220e3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47148194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4adb743f4ce165c81bdd668134a25b6dfdb62a3e13c81661607a36e8dbc5618`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:14:01 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a27f74c8272ec3fe01116621131d155f567a643402bf3afc136c7e188aa06`  
		Last Modified: Wed, 22 Apr 2026 01:14:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b5fbc01b921cc4e80e597a92bab8840671880604314dc5b52c804095c31c3833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d1d7a4c3ca02381d180b038cc147fd7a84ab423bd71318c53048f3857c50e`

```dockerfile
```

-	Layers:
	-	`sha256:5630cab3b5a6363ec8fad7a1a197dcabeb8cc1df16c37bff81ad91209a50a039`  
		Last Modified: Wed, 22 Apr 2026 01:14:13 GMT  
		Size: 3.7 MB (3730912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3415ee064c3c9252bce1f9d8d00092c6b7c92e726c1ff5c856e8ef9e17011cb6`  
		Last Modified: Wed, 22 Apr 2026 01:14:13 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json
