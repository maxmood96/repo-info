## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:b1f26b0b04c18442f48eceed88043658b641d96d0f8b67894fd371e5b1f69ea0
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
$ docker pull buildpack-deps@sha256:2ecf8dda7f148b5e3929a2b9a784fdbab34a0214c6585b40ad942ba66b1384ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143101803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2787eee0a5e2473253978555bf527fbb5fdefbd5b9044a06de57b5431c64e572`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:57 GMT
ADD file:abae7408d5e68c3a696c708e7c3eb4b503251a424e5ebe4d3c7c8f10051a6619 in / 
# Wed, 31 Jan 2024 22:36:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cc8e35210c92074bcaff9b0f9819d85e3d2721df871a170c5ffb2c3ce4d09c7c`  
		Last Modified: Wed, 31 Jan 2024 22:42:59 GMT  
		Size: 52.3 MB (52332875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07c0201c5063233d0e99feaf8970507290ce7a55ac210fe179c16b81362a4f`  
		Last Modified: Wed, 31 Jan 2024 23:35:24 GMT  
		Size: 24.3 MB (24342957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b5ec6ffb24174c2e8d7b59efdd6b0613b5bcef62a7cde965c456ae6a2b2ea`  
		Last Modified: Wed, 31 Jan 2024 23:35:43 GMT  
		Size: 66.4 MB (66425971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fa0a7b3fc115eb7c50fdc121201b0f3cad61bc1aebe5431d723aa89c4276d81a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136729677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc1ccb440ba9cfc7dd732a50febaa76de48f748d05f381de5e076f2db2d8311`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:13 GMT
ADD file:725ca9c152b8f221c1a5076443ed29cba7986d6c966b43fd73aac368d929041d in / 
# Wed, 31 Jan 2024 22:45:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdf41145b61f2fe05b34d8a769d529be6a6c13f054b6766a073b0164aac73d70`  
		Last Modified: Wed, 31 Jan 2024 22:49:48 GMT  
		Size: 49.4 MB (49419338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e75a3924a431c17b198e9e491b482222fca726f808ebe04dd75f745c7b7d84`  
		Last Modified: Wed, 31 Jan 2024 23:24:59 GMT  
		Size: 23.2 MB (23225452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162728a10cded66e397f0df0db68b9dbb11c61c6b79d3baaa731a13664cf8521`  
		Last Modified: Wed, 31 Jan 2024 23:25:18 GMT  
		Size: 64.1 MB (64084887 bytes)  
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
$ docker pull buildpack-deps@sha256:e50e6e87ada960fe674558c4c969c3f5c2a4376120151969b5d92b92aa2ed593
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142792869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e52d22551e9b7307d6ecf5f5151565ec72517200d28b1ed52e08dec63b594a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:34 GMT
ADD file:2954a14564e68bbee21d166d50487168fb308da137db675f9c3d1d24d2c9b4a2 in / 
# Wed, 31 Jan 2024 22:45:35 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8940f7446dbd5a08b1ac5dffe6fc85a0d545f6a8c5d7a0b7df016fc1158b7544`  
		Last Modified: Wed, 31 Jan 2024 22:51:02 GMT  
		Size: 52.2 MB (52190514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13324137c7a63af842733695e996e1fa7fbb6093bf7dbfd84520ef280103dc2`  
		Last Modified: Wed, 31 Jan 2024 23:54:51 GMT  
		Size: 24.1 MB (24062519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa2cf8c96bc8d8d3f9a21a0e32a3a2e78e0e214cf8eabcf8557a33907fe41c6`  
		Last Modified: Wed, 31 Jan 2024 23:55:07 GMT  
		Size: 66.5 MB (66539836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e37db9b541825e0b461db7b1b3152315ff0ababb91262d5a28a073ce368abea0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146867067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b23f42a39184a2d5b358f89bda2622a92bb313cb551fac68e2da13ea220693`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:40:38 GMT
ADD file:7eeb9c69e51143f9785ae65d9c9acb80a1be34c1ca4af1f148948207f4ece89a in / 
# Wed, 31 Jan 2024 22:40:39 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 23:40:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f0db883d85c18095d81fccef71599ce9faa085ec0ca27cea8f5e7945eaf77bfb`  
		Last Modified: Wed, 31 Jan 2024 22:47:09 GMT  
		Size: 53.2 MB (53169190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6aca1d99661228a7d9a67498beb1fcbba9e34c189e857708ee6407afc3d4c8`  
		Last Modified: Wed, 31 Jan 2024 23:48:58 GMT  
		Size: 25.5 MB (25473219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ad4f66a2cd19b6eea3bc0f180db9669dac381b31d1500c7c9b561e5310599f`  
		Last Modified: Wed, 31 Jan 2024 23:49:21 GMT  
		Size: 68.2 MB (68224658 bytes)  
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
$ docker pull buildpack-deps@sha256:ff5d0793ef43078309ca6a97d67d7e0f26961d5f2a58fb16a9288192cd147631
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140231916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dca8ca1f900819fc3fd4311ddfad7e9713941b0ef695be38126286ae0de9f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:09:41 GMT
ADD file:6160baef03e5634654c9dd6cdc03f300cee1c2ba12b10e3671c9bb2433523516 in / 
# Wed, 31 Jan 2024 22:09:43 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 31 Jan 2024 22:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e28eb1ccd25078d7ab267e8a17d83df2a6586cf1f71efcece99a7073b9edc32a`  
		Last Modified: Wed, 31 Jan 2024 22:12:30 GMT  
		Size: 50.5 MB (50540387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75905d39d19c540825ac97bf21480b038b4f58b0bbbcf7bea92252e68fa46c59`  
		Last Modified: Wed, 31 Jan 2024 22:42:15 GMT  
		Size: 24.0 MB (23998512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f8b671531c36b200b6e84dd21a3c784a776685b99bb9638b337cfd52d06fb8`  
		Last Modified: Wed, 31 Jan 2024 22:43:30 GMT  
		Size: 65.7 MB (65693017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f65853fd4f580166d1d03cea84837b87e35ed3cd312174b15a8231df43afbafa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144764527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0e4cd715bf0a897de59bb4489f02b586036192e46f18e78aa6439127c639e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:08:13 GMT
ADD file:080442a095efb5073711680e1deba8957cf0f0b56df25b98ee50a762eb11be94 in / 
# Wed, 31 Jan 2024 23:08:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:36:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 01 Feb 2024 07:38:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:83efec03ab43dce66d67adfca29d07dc60c49e276fbb445b9c7dab67d2879a9e`  
		Last Modified: Wed, 31 Jan 2024 23:30:22 GMT  
		Size: 51.7 MB (51740575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b59c6ea325db8e64f6c4b414760d04f081ec43522fe919f0195bf650e7bfa`  
		Last Modified: Thu, 01 Feb 2024 08:20:54 GMT  
		Size: 25.5 MB (25488387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c0a5ccbf3d4c81b3650225ea3b2d9eae4bd38f2e909a10e6c82117a577b24`  
		Last Modified: Thu, 01 Feb 2024 08:21:22 GMT  
		Size: 67.5 MB (67535565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
