## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:ff73bf8cd7d96872785619595d038c8e90ab5786e95ca0db16a5c27284f81a77
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fcd2d9099030515aeb5f83284ea996ae70d3574b8de265661ba1588d8489f94e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76675832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d4f4ca2cb7f034ff1f539af0a06830aa81a5a5e14c3794a84b0555e6c905ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:57 GMT
ADD file:abae7408d5e68c3a696c708e7c3eb4b503251a424e5ebe4d3c7c8f10051a6619 in / 
# Wed, 31 Jan 2024 22:36:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c42c8819f1fa5380b5b5e29f8eeddea27f524d09fbb64332095004705f0460ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72644790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eb54c99b149e0581f2727767ac3ce54802736c5425f8c87727e63dbe142a3d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:13 GMT
ADD file:725ca9c152b8f221c1a5076443ed29cba7986d6c966b43fd73aac368d929041d in / 
# Wed, 31 Jan 2024 22:45:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:86da99842ef26b82eff6b152da87b23b444361d86d4e7cd96a1d151e750276e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69447543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fdeba4944fe5bb9db1d931e3cc152318179a31a7382a4285d42ab8c210832f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:58 GMT
ADD file:bd90d0f1ca5c36a5e1904d7ae20530c307bdd6b9e95969d77a5ddfcc2a05a5a3 in / 
# Wed, 31 Jan 2024 22:46:00 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:52:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bbcba588bae85846e7d7335a4c37d794d121dab50f2eaccf1d778091ef4e6eb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76253033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54f8f75ddf41d7078ffa54e5fbcad654c7c81735fd749c2cea562553fb8bbbe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:34 GMT
ADD file:2954a14564e68bbee21d166d50487168fb308da137db675f9c3d1d24d2c9b4a2 in / 
# Wed, 31 Jan 2024 22:45:35 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:19d121e6ee2ce272210391657681ae25a7c00d30e41d137892c7790612a10927
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78642409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67d6b14ca1804b8f79826bb27046b3153b9e1ed115fbb9dc111dfc1075d88c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:40:38 GMT
ADD file:7eeb9c69e51143f9785ae65d9c9acb80a1be34c1ca4af1f148948207f4ece89a in / 
# Wed, 31 Jan 2024 22:40:39 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0601797f655badef54dea4e87ffb29a3e9a2a09155df555d06c88ab5b847d341
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76211759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e4ffeaebf0041f02568ffcb40e3a846aa3a0acb73791de9b7af6605ee20780`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:21 GMT
ADD file:6a1dcc04909356575c7d849b10872921731a30bccddfb53ba49ae8626652a273 in / 
# Wed, 31 Jan 2024 22:30:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1ac4a3ad5d3bf651112f8d660acb7a620a7346ff12038a0ceb051e0de5756051
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82678834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358460f8c89c426b007de7787673a61b110055b4cce49e7dcbe9ee092809d47f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:54 GMT
ADD file:f008ab9b7b25339989d465f43537a36c24dcbbbb95ea5f9105efe84e51aaad98 in / 
# Wed, 31 Jan 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:36:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:67f8a76b0939dba6d21780840fb30310d54991ca90634b51cffd416e2d344f96
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74538899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c61be68605628329917168d49371cd583ba1bd6dd4a9ce99295025f2cdd03a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:09:41 GMT
ADD file:6160baef03e5634654c9dd6cdc03f300cee1c2ba12b10e3671c9bb2433523516 in / 
# Wed, 31 Jan 2024 22:09:43 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9e9c35bf4ff5560030b773a4313e74303ca9abc4f76733b51c2cceab24ed61db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77228962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59015da23604a0123e6c648008596096a38231cbd08df796981592e8967ce82a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:08:13 GMT
ADD file:080442a095efb5073711680e1deba8957cf0f0b56df25b98ee50a762eb11be94 in / 
# Wed, 31 Jan 2024 23:08:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:36:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
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
