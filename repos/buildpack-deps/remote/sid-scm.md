## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:82fa26cfc995d50826b0fcb0176af623a7c1d9f01a02845783eaf3462a43d65f
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
$ docker pull buildpack-deps@sha256:bc770f8215593410866c545b078b6c734690c704829b84e484ac261f8397c17d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130893443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a112abeca93d31b15a585b5d5c6f6b83020c1b10c0e0cfab3638ce8a249c272`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:58 GMT
ADD file:bd90d0f1ca5c36a5e1904d7ae20530c307bdd6b9e95969d77a5ddfcc2a05a5a3 in / 
# Wed, 31 Jan 2024 22:46:00 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:52:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 02:53:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fc855b34c99f9eb7f5014e33574cd598c0da1401f1cd9ed077eb716baeb3d1ff`  
		Last Modified: Wed, 31 Jan 2024 22:51:47 GMT  
		Size: 46.9 MB (46917561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8997f9632816c43b708f24c452298dc5fde9a90004e67d10ed7447bdb4a31f27`  
		Last Modified: Thu, 01 Feb 2024 03:01:45 GMT  
		Size: 22.5 MB (22529982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82d5c17bde538214384a501538668ef9f5559e9cda83e4b7913d622823ccc1a`  
		Last Modified: Thu, 01 Feb 2024 03:02:04 GMT  
		Size: 61.4 MB (61445900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4c705bda8f8f91e639cf3638fc33c9feb0ee0193c9dde109b78bbe6a45204325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142647850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd40f6dc2d9a57c3494b8c18be9c992dbdee27bbb8e85d2653ee05954ba2f66c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:26 GMT
ADD file:88085ab115a08b9d412def1f9fea5d59c60a8e26965f72639d8199179230cb86 in / 
# Tue, 13 Feb 2024 00:42:26 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:42:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:84e6541c14eb2246826ed0d079d915b03d190721bc05675c66f459f0cc97e40b`  
		Last Modified: Tue, 13 Feb 2024 00:47:37 GMT  
		Size: 52.2 MB (52195661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb51a1adc81a562b48092b8b5446a6aea6604838e971db7945e6af747f8414c`  
		Last Modified: Tue, 13 Feb 2024 01:49:18 GMT  
		Size: 23.9 MB (23885814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313a023dd2178b52531ace278aad9cfe2b7b237ef6b56c93424eefb6724d585`  
		Last Modified: Tue, 13 Feb 2024 01:49:39 GMT  
		Size: 66.6 MB (66566375 bytes)  
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
$ docker pull buildpack-deps@sha256:fc0825bd389a6489fc62e1ac0b9edc1d57ac46cd5b0c4a6e7e6b5857d473b845
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141447777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec64eb59a353b81dcaa6ca4fa3f268d8126a1a2499682b25aab14231ad0d51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:21 GMT
ADD file:6a1dcc04909356575c7d849b10872921731a30bccddfb53ba49ae8626652a273 in / 
# Wed, 31 Jan 2024 22:30:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5822a20b82218747f0844b39d5a436f6742aead15996aa69a1122f629a606a97`  
		Last Modified: Wed, 31 Jan 2024 22:41:46 GMT  
		Size: 51.4 MB (51406564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9405e8efef456596dc19eee13f772439ed44169eb80706ffd1e8a0fcba3d098`  
		Last Modified: Thu, 01 Feb 2024 07:51:55 GMT  
		Size: 24.8 MB (24805195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bae2c96b6133a9c62aa17246799e040dbce8e2ce06213bc63d1ec7c2e221ca`  
		Last Modified: Thu, 01 Feb 2024 07:52:48 GMT  
		Size: 65.2 MB (65236018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3c35af313037569737d47ff9054cd1f7f9bf415d6f8d94534a166f11b0c03fbf
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154615907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6077912799958be3a58ab47c99949b783e864b50458ceaea23470245b2608a13`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:54 GMT
ADD file:f008ab9b7b25339989d465f43537a36c24dcbbbb95ea5f9105efe84e51aaad98 in / 
# Wed, 31 Jan 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:37:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5f53c7509b33e66b5a3e300443a4b78d8837e78de409ef9b1ffe22b6466bc615`  
		Last Modified: Wed, 31 Jan 2024 22:36:21 GMT  
		Size: 56.2 MB (56237850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a6dd7bc6acc476ce97457472306d643ea33de119f6cda8771ff78ed990a98e`  
		Last Modified: Wed, 31 Jan 2024 23:50:06 GMT  
		Size: 26.4 MB (26440984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770bfff2a14e6e587d4c11641dfff4fc47965b3e5a5be2c00940d05089da4f95`  
		Last Modified: Wed, 31 Jan 2024 23:50:28 GMT  
		Size: 71.9 MB (71937073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8cddfb384ed7eda6cf63effa0216f3b88205274484e895ec8d600f7a47555ec5
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140072371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af13fdd86228575c0423c9cc3a2a23c756cf4d2d71c5b4f8d912ea669bf54afe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:16 GMT
ADD file:b421fdf9092f4ec73d99564dd5502ef1d3668a7a691ba3bf1dbac96a04dc4a5e in / 
# Tue, 13 Feb 2024 01:09:18 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dd7397a9685010df855591550ae6ac222e43aafe4aa8f629b13f53ec98a94bff`  
		Last Modified: Tue, 13 Feb 2024 01:12:06 GMT  
		Size: 50.5 MB (50535650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37f9252bfe79456c9018c3962c3bb12a6b36262f5780411de6623ccf1a0df7a`  
		Last Modified: Tue, 13 Feb 2024 01:41:30 GMT  
		Size: 23.8 MB (23822159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759b918e35db2dd593162c00a042bb80cc9bea4f8643a193ebb8f688356fa5d4`  
		Last Modified: Tue, 13 Feb 2024 01:42:44 GMT  
		Size: 65.7 MB (65714562 bytes)  
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
