## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:6763a03f084f2c42319ef411cbb45f3356114507753840ef680826aca9c1c091
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

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6d6ba19df7ac34deaee2837c9989349bb222d5d8cd772c2eb08090a05b0404f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142722649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ee1b47cac952c9c05aa200b7d527b77f84c37804e50850b0d411f7b6d7b228`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a99bf11f4d755d4745d428a5f8e59469920e4fa2dbb6384cd2d8b4155e6ee0`  
		Last Modified: Sat, 30 Mar 2024 21:42:41 GMT  
		Size: 25.1 MB (25100684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da143e0f6d9787b0c89d6405a787ded9de6dcb65f3b9717f82da42f10ff997b6`  
		Last Modified: Sat, 30 Mar 2024 21:42:57 GMT  
		Size: 66.1 MB (66121672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

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

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0bcf0e6e53f87bdf060fe92e1ff43af0edfdcecdc7bf80642f4326d6c365ec6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130674564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3603e38a05a3732f16f7345c6d4a212bca05335fd34aa151adf86be572361f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:42 GMT
ADD file:0ac8f97579d9f7611b866966dd5fc34fcfa2144355ba39b31883284475bb2585 in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:24:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:25:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e8b88d91442c01c97d07c620eba463296206c34b7c84ca5b992728b1cf4bd11`  
		Last Modified: Sat, 30 Mar 2024 20:54:52 GMT  
		Size: 46.3 MB (46295373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30834b6bf99a6286a5001978342fbaa380b0ba46f9fb0df977b164e1e3bea295`  
		Last Modified: Sat, 30 Mar 2024 21:30:32 GMT  
		Size: 23.1 MB (23127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ba4b082de66bbca9897c8dba7f31512bba321ddd2a661347d670d910b4ef36`  
		Last Modified: Sat, 30 Mar 2024 21:30:50 GMT  
		Size: 61.3 MB (61251721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

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

### `buildpack-deps:sid-scm` - linux; 386

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

### `buildpack-deps:sid-scm` - linux; mips64le

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

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f503a33191cf930c854f6db9bbbb4869ccbec7ff1c51ddc9f7c6a23aa26244a4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154344195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cad6e11ebc7819d06808e304fd24f559ffdd6df84c9f1b35094beb99311b6c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:03 GMT
ADD file:2bc730d62ee0ff93ea46112c42f75f01e2e6d04449beaf198c5ae6fb388ddd07 in / 
# Sat, 30 Mar 2024 20:55:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:36:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b6224779f10a25b25659a091e0036b5df62f6e69a0c2fe4dc52a3341dae37615`  
		Last Modified: Sat, 30 Mar 2024 20:57:40 GMT  
		Size: 55.3 MB (55287220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe9d1bcfdfd6cc666707508081610ef2a537ca8a7a9e722c61d540ccb99bd4`  
		Last Modified: Sat, 30 Mar 2024 21:45:19 GMT  
		Size: 27.4 MB (27367674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95220faf903de5c246bc60d7f00054712c075484056449785d59c657e22436e`  
		Last Modified: Sat, 30 Mar 2024 21:45:39 GMT  
		Size: 71.7 MB (71689301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

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

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:58058792dbb38618b64512a4f523c0e2e7ea9bd12447bb2555e85a21fc99e831
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144622282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b467bd594b194ed628a97ca9f35ace2f08eff7d03179e6bb58a3f0701ebfee5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:09:57 GMT
ADD file:88316cf04f8a7fb87824a6416e9cdf67bcfbf1ca51c2f1bd006913b99521ffb8 in / 
# Sat, 30 Mar 2024 21:09:59 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b0f03a5ad6e4fa7361970002745be26e768ef9bff94fe3f4e4500b11e6b70280`  
		Last Modified: Sat, 30 Mar 2024 21:28:28 GMT  
		Size: 50.9 MB (50907174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1344a987a86b78ee9d1374a50e21ccd18dac28034899fdf4daa6f58aea995994`  
		Last Modified: Sun, 31 Mar 2024 00:08:08 GMT  
		Size: 26.3 MB (26291660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8b2bab401823952dea39f0a278dd656c849280f02e7b6f21ca4deddc0219d`  
		Last Modified: Sun, 31 Mar 2024 00:08:23 GMT  
		Size: 67.4 MB (67423448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
