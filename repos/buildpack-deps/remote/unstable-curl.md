## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:041108ff27509033882d8121b80b41f55b6275854ac73f55d8555bf2a6d118e0
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d522acdb043d5cbb3f6d4283fb097a8866b98a2191046b0428f1d681eaf3b945
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76969859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95511780c74a23f8bd83bb404a073bdd9048a6937e226d9924937117bcf2d48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:52:30 GMT
ADD file:7fec587617b78a81cacf7bfcdeac3b9e90b4135c4c242e80b5ea34f57d221168 in / 
# Wed, 10 Apr 2024 01:52:31 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a999d56b72e8c3f4b4c87318c15dcb947ac03342db6e04cfeab945b70473ad0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72928169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0ceb50c9ddb6b90628541790d6f575aa32aa7192bc327b4d73924eb785435d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:50:32 GMT
ADD file:4a9afbefe640815ceed7c04b5539d7c65f79afb1c50420641fb90ea84d9456ee in / 
# Wed, 10 Apr 2024 00:50:33 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:47:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:99f71903987fbe81008b2e459492477e0d5780681fc3704c361329385ae1332d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69747471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e029b1e5863b99aaeb53a082282a7baa8e432118521318e38c3a92ab9008900`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:00:33 GMT
ADD file:b651a9e79740799ad0cf7f17474e58eefdc73e4611a56f8f166422f38c62fa53 in / 
# Wed, 10 Apr 2024 01:00:34 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:51:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:beefa2ded7ef51612db5ec825b62b529563e4038d95f33767a7827d28d65f101
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77083124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f853bfc9fb4d2bd9214e0a8c434905db38c97ace674a62731792bc126c7815f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:31 GMT
ADD file:69ea41e74fa7a7601d1adbbdf992359f0c16c551447466cb4aaeac1914dc2377 in / 
# Wed, 10 Apr 2024 00:41:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:74929914d3bf10218eb443a53cc62f0b5fb36e1301de240c2bbd8b13afc9a56d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78962352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44bb9946109d8a8a928e49dd2cfae0f798c7674d9810df9203d3e51781103fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:52 GMT
ADD file:e239896f7b5e011b6d0233f2b19722dd4ed9b477a41df953ada860d9292309a9 in / 
# Wed, 10 Apr 2024 00:58:53 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:59:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aa1551ec75fa2e9c2e1970c5f0cf8c95e50b19638484e38cd439a1ae005100e7`  
		Last Modified: Wed, 10 Apr 2024 01:05:22 GMT  
		Size: 52.5 MB (52545296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d841d60f045a27d1521cf79ab6870b8315e8707b3fac64ae28185661bb2e97`  
		Last Modified: Wed, 10 Apr 2024 08:09:44 GMT  
		Size: 26.4 MB (26417056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2a17a6d4765a053dec30b05093a1e573b7012502927498451d1f8fa9683c8944
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76495596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529960e0128aac19e0c0dd2913610608f913b9702e3ac13f7f25657b999f45db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:13:28 GMT
ADD file:6c115df8d41d96a6520599c767a96584736ea315fb4abba16fba15c638d24338 in / 
# Wed, 10 Apr 2024 01:13:34 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6b337f2d29cf3d5aea69862db4f9452dc2c952aad643e9b732cd86bf32e8ec80`  
		Last Modified: Wed, 10 Apr 2024 01:25:24 GMT  
		Size: 50.8 MB (50814629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8436a21eadc6f17429cdcebf42555b9f09eb6d5cb3805750aca63ad51a6b8294`  
		Last Modified: Wed, 10 Apr 2024 15:52:53 GMT  
		Size: 25.7 MB (25680967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:01c5f0441d130fbb6d1f4013e20b3347f2e57f67d0f55ece57ab56afb52eb5fb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83047814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd97258808ea315f8cdce007ef3217655a02585cc22547513db29e9930513bc5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:40 GMT
ADD file:b4d76c20a1ef31eb6916914baa486e040481cfc4a1f2464b19f7a54de07a7414 in / 
# Wed, 10 Apr 2024 01:27:43 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:46:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:73717050aefb6e48ba2e4e077bbd31fad43d7f31f02911571c01a6df4b1ad72d
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74845046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c671d2001d6cc9e8d6303772f118203bb6371094293cebd7a6af64f329996a4b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:08:58 GMT
ADD file:cf8b9266fc4180144feb816ff584ba8b6b03b244743764b117ff119f451aa497 in / 
# Wed, 10 Apr 2024 01:09:00 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:30:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:78bed5a98c967569b0c5ef829b62e4038276031cda33a8c1cda34d575fe1bc23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77565470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183bdfc6ba18ec47e5ca68d9496a805abe0e55d8527f86ad1717da7beec2ee30`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:25:52 GMT
ADD file:90e106baf8019819d61f3875a3695b4ee1f0f47f890bc23db62485c13c0badfd in / 
# Wed, 10 Apr 2024 01:25:56 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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
