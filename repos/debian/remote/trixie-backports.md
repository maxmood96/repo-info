## `debian:trixie-backports`

```console
$ docker pull debian@sha256:d67b3010c7652f25ea4156b19f606214f94725aaff2c22485a54c843defdfdd6
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:752b4e0bdf01cf7907fde43530f6d9e6d068ed8cec98d816751c246ec030f079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49302326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795ed6ff827a3e204f7c6c360f89f651d8492fff2818159e32d9b3e016d4eca9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:42 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd1d07a6249c8164bc3082d8c3100384f8c52525cd3a576c1f820ce4d60db3`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d8e1dbbc77b83e570589bfc38a1674c19bbf2d6d92e2d6342127e5e3f8fa9845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c0be88e123244069045ef00800307a069ce64e51fa47c91411226f4d481338`

```dockerfile
```

-	Layers:
	-	`sha256:123cce6ce36f55e69c7baf09e7fdf69f4c791ef298df6afd3f63ce08e1699a06`  
		Last Modified: Wed, 22 Apr 2026 01:15:49 GMT  
		Size: 3.2 MB (3170913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf84d24d8928cd05f088331824113282c864469f521ef7a60a5d374ac89ac31f`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 5.8 KB (5783 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:09f555a1ab1e357b7702c791a9dd0103bf11e0d5f75f12bda45329c8a67353f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47466329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf16e177ef8483097a8d477bba3407f71eff5f02c2d23e2039cd3a17b3d8f657`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:47 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2a20d1d425bc7f9412bd28183d8c6af38f835b7563f035cf6476381816d73dd3`  
		Last Modified: Wed, 22 Apr 2026 00:16:22 GMT  
		Size: 47.5 MB (47466106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9239d8bf030a29c085fa1a5772ff048e9e591cce0cc98cd73e864823fba187a8`  
		Last Modified: Wed, 22 Apr 2026 01:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4d38733858e60c6d78d0e92c5322e3dd3de9c53d8053e13c4a8b8505ec0ec04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337f8b11aaf15fe23797c7b5fba18ede4bcc2a72a8cb99a13639dfe66c5ed0d6`

```dockerfile
```

-	Layers:
	-	`sha256:89d063d7847d13c25ae8e53736ffff6443fe48662a5b1b73b0b9bad367f88ee9`  
		Last Modified: Wed, 22 Apr 2026 01:15:54 GMT  
		Size: 3.2 MB (3173850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:463191a93c0648f68cc679787000b96298fc65ac2d0c1578e2475ac109455a06`  
		Last Modified: Wed, 22 Apr 2026 01:15:54 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a2ead23cd07ced5392c1db37de136924fb5a9307a18e3046dbd1891a769d706a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45738417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bec21c6979752e09a8876dcd28189b4daddb1f4d49acd2a28e9e0e3a3493d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:49 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62605cfe66216afd10bd4da40aacdc9d0f446a8c533c96f90c123dde8ddd5b7a`  
		Last Modified: Wed, 22 Apr 2026 01:15:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b65931098e001c744b2f4e28e8dbd491ca40409b4b06b8bddb6e8428b9de7066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644e42ebe9f71828c6006c90d13c8941930d7f4a4597a836547a24d3edf38274`

```dockerfile
```

-	Layers:
	-	`sha256:8b8acb2c027f7bdff8dde5ffbaae0c031fef20be7f69d8b0622e0fe05f29d4e5`  
		Last Modified: Wed, 22 Apr 2026 01:15:56 GMT  
		Size: 3.2 MB (3172287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4af60bbdf31ebd2e6637490bf741a3a97395ef309ff019bf1d75b5d7dd8d34`  
		Last Modified: Wed, 22 Apr 2026 01:15:56 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4836b2c12ff767086abdf07aea722678b46c78923b3f8ac9f14d670d6aa1db3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49669469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a210c63042af955b16ba2a5e4fea3465099ee6dd6d833fac0388959efdb0e58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:14:55 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662da7c9b759849f09861842faed2a945baadbce03bf1a9ea65943f34a7013dc`  
		Last Modified: Wed, 22 Apr 2026 01:15:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d90191e4cdb9912c373b13ed103f67d303e54ee3aa7f5dbebacbfbac45e8ab22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df808af76eff7944f8a663108d7421b05ddb29ba1e129b5a3865b6ddefaeb3d`

```dockerfile
```

-	Layers:
	-	`sha256:134acbd8e280f1c8ad3268bc77512a349af2ac43ca21e8a1d2e01ba2fe25ff7c`  
		Last Modified: Wed, 22 Apr 2026 01:15:02 GMT  
		Size: 3.2 MB (3172394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792ce9b167833e208ed4199e8e894e734f58ff580eea73ec601f4e0e4a2875f5`  
		Last Modified: Wed, 22 Apr 2026 01:15:01 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:f5e6cdf97a5d7e7a419043f07ff53bcdd1af3f0b45c9d8f4ef39e1952020a2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50825581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b23f829e6860a58d5512b75351448cfb06841b76f742304211c7044b05b93f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:50 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62605cfe66216afd10bd4da40aacdc9d0f446a8c533c96f90c123dde8ddd5b7a`  
		Last Modified: Wed, 22 Apr 2026 01:15:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:75357cd262f72785e78351ab6f8cea45d9e48d250512b486c089c825a12f4ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d182b31239216518f464253041da5083c38077430598a9bf12d19f80c9a1e6f`

```dockerfile
```

-	Layers:
	-	`sha256:3e309bd445c1d3bac4e18555216c5d2a2d54ce6670980a9437ea6438605b9b41`  
		Last Modified: Wed, 22 Apr 2026 01:15:57 GMT  
		Size: 3.2 MB (3168115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1f47600c8e4f1ce1b5460e0660e67017df1c02fcf671644b44b9f49eb46a71`  
		Last Modified: Wed, 22 Apr 2026 01:15:56 GMT  
		Size: 5.8 KB (5766 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:8e9f86df7bdda4d87668d402180885f72c903131c20fdeb5bf443a751338adf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53123207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f8102a8809160166d3e84868c882949d5664cec5b48b9507515729e6354219`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:16:04 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c9cbe5350f17b8cdc2a3c3aba8a66dc5f0a994b9da37063c3030c1c25f74d`  
		Last Modified: Wed, 22 Apr 2026 01:16:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bafe786b686607b09cc4ddfd83a4d084a6050c33e3e2acddc6ba322eafa1d085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d5c9da125cfc285d62d927c6d840b39a1c29f4730dc8decb02a04d791d1a3f`

```dockerfile
```

-	Layers:
	-	`sha256:2f78650ecd1a170aa4ff242ca601b21ea962196e77f51bc6548615c50af56a02`  
		Last Modified: Wed, 22 Apr 2026 01:16:26 GMT  
		Size: 3.2 MB (3174426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f397437f9ee85a51cf8603dd8e12e067e71262af23b42d0530cfd24786e2e7`  
		Last Modified: Wed, 22 Apr 2026 01:16:26 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:12958450b181a40a831421b5e879ecc31c05d84f1a0c34fec20bdaee632177dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca59481aabf06cc0b4a5118a4fb45b7bc7a3430ae802e44336d6daa2e593ceb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 06:01:36 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0c89056b1a32f4449f98665686aa354cc42579d832e5ee4d84260d617afd7c`  
		Last Modified: Wed, 22 Apr 2026 06:02:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:84a8d662b8ae4952e567382cebac85abf321042a96b37296a9197c3df730bd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6606ec302d310ffc7238c69988d1e701310c3e480a1718f8731a466c9d3a7d6e`

```dockerfile
```

-	Layers:
	-	`sha256:7e988e9ecc776fb0302191297756f7fd497c1ff486a73553b1f2dbbdcb4205f7`  
		Last Modified: Wed, 22 Apr 2026 06:02:30 GMT  
		Size: 3.2 MB (3163238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c83edabc2b7ca35a71b09b03f5d205b90f703af0b303e9cfa68dde89a0a617e0`  
		Last Modified: Wed, 22 Apr 2026 06:02:30 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:57170629bb2c0935859468ebb6ae576f20a11dd13af07ab9e793aac4a350ba85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49372329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf466befb3ef61831caf9b45052b7c39634a23e85820c566239113d8fe91aff7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:14:36 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5653c2a2ae826aeda11c931196627567a732bd4f4d7dbfd6b121302a53cb1470`  
		Last Modified: Wed, 22 Apr 2026 01:14:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:34c23b2734e2a7fc3f804e97cf68804e7664faed0e63c095dce335b0237c9a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5206c3d8cd1f4a865160c5e9ffec12a739790c9260f0cf73e80c45af306b7813`

```dockerfile
```

-	Layers:
	-	`sha256:e253eb60b3492d142473155d0efdbf19bccfd83c4c88783aa8b96921d034d744`  
		Last Modified: Wed, 22 Apr 2026 01:14:47 GMT  
		Size: 3.2 MB (3172360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c2528043a551a647f21807ee7c9ddaf813f10cec867610cbe38557e8313235d`  
		Last Modified: Wed, 22 Apr 2026 01:14:47 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
