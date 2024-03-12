## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:776412b16d551dd416f940fd9fed3d124bd4ba874979e5d13a1f722227138c48
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
$ docker pull buildpack-deps@sha256:0bb071c1266f203b2041ca93497a739fe9d4349b7c7853cff4887a81e059f022
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142975626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdde92020438ebe73f96a17fc7307a7b413d194374d50b71e68efb8a6944608b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0416ce76c708a01d23d622188ae0a4c0552e5a29d07378826ce051a51a2fc61d`  
		Last Modified: Tue, 13 Feb 2024 01:33:47 GMT  
		Size: 24.2 MB (24170886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab94778b4f8d542570a58f18b952aac258e2970cab96fd361b214bfa16118b00`  
		Last Modified: Tue, 13 Feb 2024 01:34:04 GMT  
		Size: 66.5 MB (66468254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1cec2114b9fbc4843b5cf0b9c8fbaa74c4b4b83edaefe5346dfc5a2325eb6d89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136584148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f9fdbbebeb90640507c0fe9c9c7f94c49092e2b2457779acf670d041930ffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3a1cdabe4cc17ce6f55149b66ca7c16793fb014ff72d99cb1da643581eed76`  
		Last Modified: Tue, 13 Feb 2024 01:56:59 GMT  
		Size: 64.1 MB (64108591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:779fa01b9f5918a69716dbdf3d599dd12913476ec65cd9c5bc05a41183678baa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130757215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d298e5bd648d71e4c86864a1c66f3452d3e31f41781f27ee8a9c9d9a15fd7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78cb86ad182c3cf9cfed5742a1bbd6365a9bcb95a5f378a558088dbcfe7364a`  
		Last Modified: Tue, 13 Feb 2024 04:31:10 GMT  
		Size: 61.5 MB (61467747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2828cf65ed74a397e66e8fb3eee64bde5f30b20ff6c647bc0748dda91ba50370
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143297356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2904dfc2bc2f7f22ec601d0030925c6a14c76a586d20c697612925d4c9d3a53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:41 GMT
ADD file:1202a56d8723ce5bee3f68e3d9488cef88889fe8b2bb138cde766ff787577a7b in / 
# Tue, 12 Mar 2024 00:46:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8e7b106821c007c3c67e9a4d248bd2f87194491ad746f2aa752c5b0ba2fca099`  
		Last Modified: Tue, 12 Mar 2024 00:51:35 GMT  
		Size: 51.4 MB (51353263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa13c84a803d4b150b717babd5d0b89e39ce55a7c4c07cfbc3d34a5e4ce85a3`  
		Last Modified: Tue, 12 Mar 2024 01:37:43 GMT  
		Size: 25.4 MB (25434519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde6d0bb19e702e70dc6d3b44c7538729b197d5c5c229f8df55709b3de11f031`  
		Last Modified: Tue, 12 Mar 2024 01:37:59 GMT  
		Size: 66.5 MB (66509574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5c9106633d47775077bc4f62164c7fa00a7ee8d404348145e6f41c9cac5a2886
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146706781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c92dfca00a5b2fbf2cb1672a258505f21b5cf25b37447b3e807b9f6c27863d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992ae92ecc708d9f7dbc50c93a7a44033fbb23286817ad552428376a53b6b21`  
		Last Modified: Tue, 13 Feb 2024 01:33:35 GMT  
		Size: 25.3 MB (25291521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b34fbe23d33273890d47ce232e0ea3ecafabe7cd6f1eacdaed0132a34c12c8`  
		Last Modified: Tue, 13 Feb 2024 01:34:03 GMT  
		Size: 68.2 MB (68249193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:351c91be38a50c74c25edc544bd502d4f74e3b6de4654e5aad3ea980b4281238
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141303459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e68e0576b452fb51c345c98058dda8777da05598f125487b7fa516a3863973`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:07:17 GMT
ADD file:46b0dcd0e81e4f61221659b1260cc43869ec44a23c045f293f694b50a4ce89a8 in / 
# Tue, 13 Feb 2024 02:07:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba59fa1171a061c2b49e9de14015f71d0e00ec2a17b49ddcdd453a663a922bf7`  
		Last Modified: Tue, 13 Feb 2024 02:18:44 GMT  
		Size: 51.4 MB (51411523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11595e21bfcc750f6639cddb481d3bae82b987766fc917da9fdbb55241005776`  
		Last Modified: Tue, 13 Feb 2024 04:27:08 GMT  
		Size: 24.6 MB (24627275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6328e06fb256ea30715aa4016628a9149817a5fd5af519caa1fc97eed490e251`  
		Last Modified: Tue, 13 Feb 2024 04:28:01 GMT  
		Size: 65.3 MB (65264661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6a6262101470d5f902e746a0fd115dc08a5bffd3790d17e56b29e2d14069a3ef
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154459349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abb73597e516d0a2f1196348483cff4c2caa8d87ebf42ad3cfea2b1ce78864a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:17 GMT
ADD file:d19bcd45d866b0d48dac33521c067bfbc08e3a101f90daebd092f75f282f6aff in / 
# Tue, 13 Feb 2024 00:40:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:28:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:947f8d1be7548afd5382ff5b1b5c220ae7893fa7f2c8f135cf8967ae1d5d8b04`  
		Last Modified: Tue, 13 Feb 2024 00:45:58 GMT  
		Size: 56.2 MB (56237347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81019b4261c2b7655008e5d128bbae18fd5c794c1676de082ef06c6e9d52b2f8`  
		Last Modified: Tue, 13 Feb 2024 07:38:36 GMT  
		Size: 26.3 MB (26259832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a5c8875e799e5e279fbdd05c6f1210fc9492749ce7709449def06189f5a739`  
		Last Modified: Tue, 13 Feb 2024 07:38:56 GMT  
		Size: 72.0 MB (71962170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:152a5cbfa44cf71e3e69318c518f5dd28d8dbbcbe55be8def9fe5a694621dd00
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141027990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ea7a8dc3cc9e8e9699bee6e7550865e5641da7a9b5efcf20db31fc5caf51f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:08:51 GMT
ADD file:ad62fb7e744226b84b9b87b22c6b1e797cb2a179f4f2c7295e0db14b95dcd84a in / 
# Tue, 12 Mar 2024 01:08:54 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:30:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:32:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9c2efbfef38bc6f28418aabddc7ba24be7bed3ebbd2673ebc8db7533e9ae8c47`  
		Last Modified: Tue, 12 Mar 2024 01:11:24 GMT  
		Size: 49.7 MB (49682014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ab338dc4eeec296303efc67a955dedb7028ccf69f05896a788076dbc0a4108`  
		Last Modified: Tue, 12 Mar 2024 01:41:00 GMT  
		Size: 24.7 MB (24700091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca4553b75aacf6fefe0df7808ade0293c53b5a2b5926e00353a53712d08926`  
		Last Modified: Tue, 12 Mar 2024 01:42:04 GMT  
		Size: 66.6 MB (66645885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cdcb147cf298be69685f44453fc0886d5b00156f2a176a5ebd4c3af96ee77356
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144604922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc10f37875adb45d677b6de292e99fb4740b93d3444cb3b8c0f9450701015d0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:12 GMT
ADD file:4bc7c850cbec49616034f8ea4f54dd700feae8731e30f527142a4ae20f2089d9 in / 
# Tue, 13 Feb 2024 01:11:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:463755eaddfb5b742f8a2a82a7c2ebcfcdcdbcfcad5bc7a79a96f0c7ea3c590a`  
		Last Modified: Tue, 13 Feb 2024 01:31:31 GMT  
		Size: 51.7 MB (51742366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cc53fd314acb7fb481a8eae3a329f16695193f59a9f56c9e4806de6b5cf329`  
		Last Modified: Tue, 13 Feb 2024 02:59:42 GMT  
		Size: 25.3 MB (25307440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d71e89930040fcd5c9bab43bc590b577afe0564c16033af772417a01da471`  
		Last Modified: Tue, 13 Feb 2024 02:59:57 GMT  
		Size: 67.6 MB (67555116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
