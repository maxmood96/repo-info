## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:0dc92a5ce78a9769440b75146afcb4d3fd582892f7c21cc8652f60c4e59e1712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1cf4b7fc09e47bd48176254fd8b634e4cdc17669c448bf9f4641511ebdb74fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145505465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1933c140f19ff4ea7d54f8752e5a3800d5a20892facf0cebdf62875ddb7ce0be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:52:30 GMT
ADD file:7fec587617b78a81cacf7bfcdeac3b9e90b4135c4c242e80b5ea34f57d221168 in / 
# Wed, 10 Apr 2024 01:52:31 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 05:30:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9c331a6d36afda0d91938277ed86b71e85bfb5904bb0efa434e13d0991817c34`  
		Last Modified: Wed, 10 Apr 2024 01:58:18 GMT  
		Size: 51.7 MB (51735884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbc54dabf654d02139eee6023952ef9722f71eccc8835cd61dd4f574adcea59`  
		Last Modified: Wed, 10 Apr 2024 05:37:54 GMT  
		Size: 25.2 MB (25233975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f084187fa2b14471c0826c24248ca716aaf99049ade3cc30674118bd1a7fd2`  
		Last Modified: Wed, 10 Apr 2024 05:38:11 GMT  
		Size: 68.5 MB (68535606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:14c04925c198205cb83c60c62cba3cb68bc5b77605fd986adfaab24e3df0bca8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139126084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768fdb90eec70b8eff7e710e9dc8c99a5d2c30bdf0760d2e371951c31ca6ae61`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:50:32 GMT
ADD file:4a9afbefe640815ceed7c04b5539d7c65f79afb1c50420641fb90ea84d9456ee in / 
# Wed, 10 Apr 2024 00:50:33 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:47:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:435c81b262aa45b615a98b5b08f6124900f0a2f8c1b016424864ba2f1ed5bea0`  
		Last Modified: Wed, 10 Apr 2024 00:56:32 GMT  
		Size: 48.9 MB (48901894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1396417efc6e373a240285f028c909e31f5fb9efd13378c97dd450e23ed90a97`  
		Last Modified: Wed, 10 Apr 2024 04:57:34 GMT  
		Size: 24.0 MB (24026275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76004e4bc491beba63b8855446407f9a2d7d9e8296c8b5bc053170acc6c366d3`  
		Last Modified: Wed, 10 Apr 2024 04:57:55 GMT  
		Size: 66.2 MB (66197915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:24e70c6793cfae64c3d80567463f0a4716a93d0f4d48c9deca211ae3cb38e52f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133193849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a0e47824eb2d6f42860c05bc6742fcac37bc72495f01f2d21c14620766817b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:00:33 GMT
ADD file:b651a9e79740799ad0cf7f17474e58eefdc73e4611a56f8f166422f38c62fa53 in / 
# Wed, 10 Apr 2024 01:00:34 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:51:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 06:51:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bb537406eccf44a062d659169f21696e8c3000511c07deaf7acadb77364db29`  
		Last Modified: Wed, 10 Apr 2024 01:07:36 GMT  
		Size: 46.5 MB (46488213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa8bb32b6a8fa1654a8654ec8498eee6b8f5a14412626a85c0b6aa2517664a5`  
		Last Modified: Wed, 10 Apr 2024 07:03:37 GMT  
		Size: 23.3 MB (23259258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1684840457534f3c616560bbb71c0c6d2ccd3a666f6246ee27b8175ce907e517`  
		Last Modified: Wed, 10 Apr 2024 07:04:01 GMT  
		Size: 63.4 MB (63446378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9bb18cbf41e25eadee3137cd7ec713850b0322ee3a21a89be1ca3b7d2d1c2f0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145785621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfca5e6ae94f30516a0322c676df4fa472b1e71a32b5eccbef0688b076526613`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:31 GMT
ADD file:69ea41e74fa7a7601d1adbbdf992359f0c16c551447466cb4aaeac1914dc2377 in / 
# Wed, 10 Apr 2024 00:41:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:de2b6ae488daf95901751cee985416dfee51a36f7f9f15e60031279618e00a20`  
		Last Modified: Wed, 10 Apr 2024 00:46:49 GMT  
		Size: 52.1 MB (52136998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5adedb09bcdae19c9c078aeaa62769929c3099af358e94efbac1473c079342b`  
		Last Modified: Wed, 10 Apr 2024 04:34:38 GMT  
		Size: 24.9 MB (24946126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324a0d5b61d3a348879655c04f5c1126df0827ea0ca894a127660c330ef8602e`  
		Last Modified: Wed, 10 Apr 2024 04:34:54 GMT  
		Size: 68.7 MB (68702497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d18fa777ebc7ea2e073e4bffda4c47de7132dd54b9fd9b1e58690f087de5d3a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146443487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b170d882dbbd60c1068d13fd4cadcf7e8399258e2290a48999a461dd9f1ca2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:47 GMT
ADD file:5c0cc8b80773608ad255427432daa6a4ea6c6d1257178c16e9fde71fe5f2c803 in / 
# Sat, 30 Mar 2024 20:51:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c8e6f721d25b23e18d050c75bbf87b16883b01f37acac5142a881b7006f7696`  
		Last Modified: Sat, 30 Mar 2024 20:54:19 GMT  
		Size: 52.3 MB (52279241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d21e3778f3e12a5abf7a2295be5a05142eaad46fa3793baaf32a4f9d5145082`  
		Last Modified: Sat, 30 Mar 2024 21:21:23 GMT  
		Size: 26.3 MB (26288009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a15da4ef836ff60f9c28ef8b15ef8794d788a67c0a3d58b61d51a0e65213a7`  
		Last Modified: Sat, 30 Mar 2024 21:21:45 GMT  
		Size: 67.9 MB (67876237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6c77a5529a0384f610cc4238b7086ad705e14f1fc79c382bfafca81d6c957a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141304358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41ad8fc978f8d2925c94540c6b5928f5e0e55c43ab6d99a9e02b26e17a9b10b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:54:42 GMT
ADD file:3fab027e6d739287e4b7349292c885c809a65c14845b5d292aebb3844ce27682 in / 
# Sat, 30 Mar 2024 20:54:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cbe55b4cce02b94dd21e3b65d94bdb65a4b1119288ec18dec4cbfe762dc19adc`  
		Last Modified: Sat, 30 Mar 2024 21:01:00 GMT  
		Size: 50.6 MB (50600834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f963513fde292fd81669591d3906b0da2c957d9712fccfa5e3456c15942a0`  
		Last Modified: Sat, 30 Mar 2024 21:46:20 GMT  
		Size: 25.6 MB (25551593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70614ded1d05fb936c73b08a0c6dfe5d84789dc9d8bd520b58fc90ed5d9fc8a2`  
		Last Modified: Sat, 30 Mar 2024 21:47:10 GMT  
		Size: 65.2 MB (65151931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c44526114f46d15cb3f755e9e9a8df22db57f3248d2f7cb2f47849245ec38a0e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157291135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2f8e3d07b215f1ebf7a5d6d72aaa52edce9d42ebe3bfb13c6b28fbce41dbe2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:40 GMT
ADD file:b4d76c20a1ef31eb6916914baa486e040481cfc4a1f2464b19f7a54de07a7414 in / 
# Wed, 10 Apr 2024 01:27:43 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:46:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 06:49:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:149ef7b943fcf6c968df7da67a0cab193a9c8b879654558231f5a04b02ace929`  
		Last Modified: Wed, 10 Apr 2024 01:33:03 GMT  
		Size: 55.6 MB (55558752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23863b8ea71766628fe06ba3262e6ca0ca1b9427125763d73844952a82e439f7`  
		Last Modified: Wed, 10 Apr 2024 07:18:52 GMT  
		Size: 27.5 MB (27489062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0af6beb4c1564ee27dcd22b51d140012207437010746dbe861c9858b7791414`  
		Last Modified: Wed, 10 Apr 2024 07:19:13 GMT  
		Size: 74.2 MB (74243321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a73fc886602408a3d34d34c4105b53b05286a7e00b62ae1f72028abfef3039d6
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142821949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97da67fcb719578fc81020c41c51228bdcbcf5866752eaebb2877bd1ac932d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:08:58 GMT
ADD file:cf8b9266fc4180144feb816ff584ba8b6b03b244743764b117ff119f451aa497 in / 
# Wed, 10 Apr 2024 01:09:00 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:30:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 01:32:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8bfd6a26c3a37b6a00ea3d238fb8eed745384d2bb98efaff22428174a68f6a1`  
		Last Modified: Wed, 10 Apr 2024 01:11:44 GMT  
		Size: 49.9 MB (49941022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a180df00bec725b09dac77cce3dc37d1d711ae817d8b4a36f2aa34d8d552ed`  
		Last Modified: Wed, 10 Apr 2024 01:39:42 GMT  
		Size: 24.9 MB (24904024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce99732b9cfa4521c0ab9070c5af6f235f8b3d7977ca84c4ec174dba2588aa`  
		Last Modified: Wed, 10 Apr 2024 01:40:47 GMT  
		Size: 68.0 MB (67976903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:74e5364d267d204134c99e90a6c82002adb87b9958c892c3eb83b04992b3d9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147568789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f4805f472e2b89ec381f5b0318fdc057106d59699e1d7997cec1e83d85a259`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:25:52 GMT
ADD file:90e106baf8019819d61f3875a3695b4ee1f0f47f890bc23db62485c13c0badfd in / 
# Wed, 10 Apr 2024 01:25:56 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 07:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:111a73d2cd21eab548d0ffddc9bb5a4d0a8616f2cef311480858e7b83b040f90`  
		Last Modified: Wed, 10 Apr 2024 01:49:40 GMT  
		Size: 51.1 MB (51141422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ceb5aa4e39ffe287fe10a3493d2f4d5523e68aa7a2824b810a3822bd3b198`  
		Last Modified: Wed, 10 Apr 2024 07:32:48 GMT  
		Size: 26.4 MB (26424048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b51be5a8b279e9d858406806bb10f22ba19f1e529f4b8e300e3603f1323af1`  
		Last Modified: Wed, 10 Apr 2024 07:33:05 GMT  
		Size: 70.0 MB (70003319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
