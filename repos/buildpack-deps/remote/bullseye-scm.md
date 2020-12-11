## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:5d2721c238b82927e9d4d674c1d952ba259674c90dc59c6a3711c4f017325fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:dfff17c4317c954868c77bfbbe97680d7a0671789464e3dcf45d7fe05eb7fdd4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124785647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8771905bfeb983a2f7362dda3b3f6741c1d8eec4ed4d5ebae7e3ab244a98361`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:24 GMT
ADD file:fa865518757ef9e0af03796e7abd6cbfd59e20f5ae325422e41524615051a2d1 in / 
# Tue, 17 Nov 2020 20:20:24 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:27:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:27:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:28:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d004aa4da82e9e47169ac4cccf33df9b52bef6dda8aa5f7b0bcb03af34078173`  
		Last Modified: Tue, 17 Nov 2020 20:26:32 GMT  
		Size: 55.6 MB (55578105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5514b41a34cf855f2908da965f01f2b0f68fc62b29b9fb67811a07e7c61d16`  
		Last Modified: Wed, 18 Nov 2020 00:47:23 GMT  
		Size: 5.1 MB (5063216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3985bf4e3bf68c52363fd7853ecc6142b55501eb8457558d27ae10a0358e8907`  
		Last Modified: Wed, 18 Nov 2020 00:47:24 GMT  
		Size: 10.6 MB (10645972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f00fbcbbd3c3783e061ff8d861834c157f06601ed495383250dabb36682027`  
		Last Modified: Wed, 18 Nov 2020 00:47:43 GMT  
		Size: 53.5 MB (53498354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b01cb55a5adc9d935895d80f079e7d419bb7e1333639e9ce9df35376c0987704
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120364930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004de1c79142aa4b3421e80d01e033bdafe4933fe2bc1f929a96ac1af4e12935`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:07 GMT
ADD file:8b9117df3f1a986438250b725bc8ec117cf1caba2e6953cf9a870edbcda4c565 in / 
# Fri, 11 Dec 2020 02:03:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:37:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 02:38:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Dec 2020 02:39:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:69233e69b29a579de45732361ee762ae02ccbe96b0f2a09fc2a48a802a25b265`  
		Last Modified: Fri, 11 Dec 2020 02:13:31 GMT  
		Size: 51.1 MB (51053259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d208cbc2dd055b46a0eb797352719db7e40a64bb90bab94b3d64b5b3b1c4a6bf`  
		Last Modified: Fri, 11 Dec 2020 03:04:31 GMT  
		Size: 7.4 MB (7444057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8ae15eeacf7f92e597567cdb02de06832bdbbcbbc72e66d77dba4a1854f649`  
		Last Modified: Fri, 11 Dec 2020 03:04:34 GMT  
		Size: 10.3 MB (10335286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63c9e301bf107aaab041c8ea9ccf08104e472540b7fad385a3c0c9b14a93cb1`  
		Last Modified: Fri, 11 Dec 2020 03:05:00 GMT  
		Size: 51.5 MB (51532328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3e46f6097ba1c37048ff3714d4ca548456fd9342f7b9894f210a56e3dcc5e62e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115480434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b29b5a80f549e26353988678db64a0e23df6b4c3492270e233e361c3c4a452`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:22:18 GMT
ADD file:f1ca2b90268fd790612e08e0e01b5ea1b63749dbec2ebb79b37a6168e5e82815 in / 
# Fri, 11 Dec 2020 02:22:20 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 16:18:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 16:18:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Dec 2020 16:19:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3354b3972c3003db2792ea643d0250983d6938232305c0bd0b2f3f8ee458c9ca`  
		Last Modified: Fri, 11 Dec 2020 02:32:03 GMT  
		Size: 48.7 MB (48731592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32f0027df82d0578bcc2d43af7c68680af181d153ad76b785b97e3ffb1a53e8`  
		Last Modified: Fri, 11 Dec 2020 16:41:21 GMT  
		Size: 7.2 MB (7185940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce3f21be10a21df5869d3131ec5a4c6715acb9e45fe541b0050baa4013a18f0`  
		Last Modified: Fri, 11 Dec 2020 16:41:21 GMT  
		Size: 10.0 MB (9974110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cd80ba9b81350feb3d9ed853fd31625b9a1308882fe61f8cee95c338f871d7`  
		Last Modified: Fri, 11 Dec 2020 16:41:50 GMT  
		Size: 49.6 MB (49588792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:95e89345057992aaab57af0b073a6c54e728969f9cf54563cbf587eef98c7c09
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124339817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a821bed0379d899f377e19c33b478eb10e608fbda4ff1384b5c8428a9333d16d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:44:38 GMT
ADD file:8b5c11cc7a49f4bcd4f99db7d2c343338d9930a8254ed6527ec04ee8f41446d1 in / 
# Fri, 11 Dec 2020 02:44:40 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 18:48:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 18:48:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Dec 2020 18:49:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:452eaeaea0dc38e36d92c42c3301a9bf90cd1779fdbe05d762ba387c5823b66d`  
		Last Modified: Fri, 11 Dec 2020 02:51:52 GMT  
		Size: 52.0 MB (51961868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a365361933f85eda3c750d50aca8a81a4775d22e9d737de3c7c45bc6b95a3b1`  
		Last Modified: Fri, 11 Dec 2020 19:05:17 GMT  
		Size: 7.8 MB (7752728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e4be3f3b3a66559755e4f49afd8b36b637ff6ae027a2cad951ec7f639f34e8`  
		Last Modified: Fri, 11 Dec 2020 19:05:17 GMT  
		Size: 10.7 MB (10653887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e158b7afd9be64690545f136c376c415333a78b35c4794e659ac726aaa18955`  
		Last Modified: Fri, 11 Dec 2020 19:05:39 GMT  
		Size: 54.0 MB (53971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:112273b5796141d07de61def08f0ed046485c72266e3d2e98a0f2cc1a62f740d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127762353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da19a817a8d76b76bd6d6be3370876afac4eb49838e404ae319c22a60f7343ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:01 GMT
ADD file:df88ece8f6b35ea6811921d958952eb8431b76449597cb6d5151e88c62167964 in / 
# Tue, 17 Nov 2020 20:19:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:01:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:01:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 21:02:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d9137c9a05e5bbf8d80413499157abbe788cac975a7926ded72bd9ff285f7520`  
		Last Modified: Tue, 17 Nov 2020 20:25:46 GMT  
		Size: 56.7 MB (56728874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbd9994454c4b84708c2d9754f396aac9f662a7169c2322418210f8d161ac4d`  
		Last Modified: Tue, 17 Nov 2020 21:22:12 GMT  
		Size: 5.2 MB (5182817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87786a5db1b57a9ac7c14addd518c4d55f9ac878f951e8110866257d83d6d82c`  
		Last Modified: Tue, 17 Nov 2020 21:22:13 GMT  
		Size: 11.0 MB (11022570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88de8fd349f0d1c859351edc10905c5adca2e975f84e43d737a1933c7ee86944`  
		Last Modified: Tue, 17 Nov 2020 21:22:35 GMT  
		Size: 54.8 MB (54828092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0e3bc85ea4c775692bc283766353add81ea870ca87a34405d21ce36d6c4a61fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122479987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffab2120d2f5f553ba6252c116926942570e71ac5cfd80924900a920d949928`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:02:20 GMT
ADD file:1c9d3b0dae65df3d925c78ab44bc00642c930f3deef925694dc0c1a3213de35a in / 
# Fri, 11 Dec 2020 02:02:21 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:44:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 02:44:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Dec 2020 02:46:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ede4ac036d71d6e9539de8a220d9f79c46f7c9cb9bf53f8498188327ec302195`  
		Last Modified: Fri, 11 Dec 2020 02:08:06 GMT  
		Size: 51.8 MB (51829610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff97d6058f001d48012d3119e7be581954924dd50d584771418ffecb191be4d2`  
		Last Modified: Fri, 11 Dec 2020 02:58:53 GMT  
		Size: 7.4 MB (7410105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5e05d9ca9fe9992047f5f69faf9d8cc20423eba1ebf9226cd16e85d820255c`  
		Last Modified: Fri, 11 Dec 2020 02:58:54 GMT  
		Size: 10.7 MB (10656688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f67c25b93b905661111d2e1ac9d028619abd3d68daf06b9e2d83aae2342219`  
		Last Modified: Fri, 11 Dec 2020 02:59:45 GMT  
		Size: 52.6 MB (52583584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:54fc6c5a91780d4fff234cc0aee4e8810e62e414a8288d4f6efa89d22b9045d0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134964366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ef9a50d2a580be5b1343133cac66690d1e07b6d0efe167d1fe02700fca9bba`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:31:53 GMT
ADD file:9583240ab6aa83a5f964dedeba18905486e879b1839d8329fc20f91cfccdd8d1 in / 
# Fri, 11 Dec 2020 03:32:06 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 19:12:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:13:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Dec 2020 19:14:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:018083dcdb1846644d37fb03ece4c9beb51dcb25f9851d01fc02f63c6fb143cc`  
		Last Modified: Fri, 11 Dec 2020 03:40:16 GMT  
		Size: 57.1 MB (57079148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a764e770549a2e9fcf1a37155cdeabec6a1bbe84c9873e18d51d8d1c4b6228`  
		Last Modified: Fri, 11 Dec 2020 19:50:33 GMT  
		Size: 8.3 MB (8342665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e75b76e059bba32797a570fe56ef47061e3ab409a710a1e409d2f231adaea9`  
		Last Modified: Fri, 11 Dec 2020 19:50:30 GMT  
		Size: 11.4 MB (11421077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316286b554fff880f9be84885643662c6077dc4f49c3c6bbcdd4419ed1157d99`  
		Last Modified: Fri, 11 Dec 2020 19:50:59 GMT  
		Size: 58.1 MB (58121476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:daa773908a4543e14ecd9fd47e402bbc815ec6fd12b51ff8b80294b0e9fb956b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123073098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6485cea7a4c062a13671b7d834319daecb43cd9e20804d5d70f59ba241532064`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:11:03 GMT
ADD file:74a0f68651d74636caec45b24b97289c444300a4e20ead2e9dd4ecad9a89b149 in / 
# Fri, 11 Dec 2020 02:11:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 15:56:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 15:57:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Dec 2020 15:58:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8c1102ca26cfeafe4e6f6b885fc1f8b1c19daafd157e556c9eb528d215f3ec2a`  
		Last Modified: Fri, 11 Dec 2020 02:16:10 GMT  
		Size: 51.7 MB (51656809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5318fd9b9f903620dcea8eebe0d1b3e4c22fbc8b859c0bf46ac13755d1a52a`  
		Last Modified: Fri, 11 Dec 2020 16:14:25 GMT  
		Size: 7.6 MB (7565720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845cbfbba3746772baf57c643c9a8edde11b111c4a69407f278d0c47ace4f158`  
		Last Modified: Fri, 11 Dec 2020 16:14:26 GMT  
		Size: 10.5 MB (10525441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f79a56621b8c3834393733c04a12d896e7ec992d0f284d592926bb45255ae`  
		Last Modified: Fri, 11 Dec 2020 16:14:42 GMT  
		Size: 53.3 MB (53325128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
