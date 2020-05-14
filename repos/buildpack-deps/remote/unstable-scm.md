## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:1c7686e7cd10ccdd37d83504f31b020b013027d378b2f7b359ed5fec89848bed
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c09d42a4140e52df1a8de0c321fcad4e86ec0224f76f4fbdba09ad65e997fbc2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125443464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72cc1ef3b4dd3f150fbe712a73467b66fd2f6c9e58e7d1ad8bc7c557b67716b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:22:30 GMT
ADD file:1b99a100214a4a86a413bf6a826c70d07fee06a8c4e6d1f3ed1550fb08f9818e in / 
# Wed, 13 May 2020 21:22:30 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:37:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:37:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:37:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:268c82fb25093fc20c25872a9f96ca2bef121a19a81a91079b62afb96b725135`  
		Last Modified: Wed, 13 May 2020 21:28:35 GMT  
		Size: 51.4 MB (51390987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a426d8c659d27b64d66f82bd62c2bb3dccd6560447f354396111cb0c27bc0e8f`  
		Last Modified: Wed, 13 May 2020 22:47:30 GMT  
		Size: 7.9 MB (7934296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ac7ef969a4b66cfe2e8dae9867620b1821ab5b3d64e9e37b0a3ca56f574a44`  
		Last Modified: Wed, 13 May 2020 22:47:30 GMT  
		Size: 10.5 MB (10463093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f137f68410074c0abacbce781d17f5b40e894982fa38e5f1cf1edb52c3274181`  
		Last Modified: Wed, 13 May 2020 22:47:51 GMT  
		Size: 55.7 MB (55655088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1856dca6a14251166d0d563a682db7bfbdd0511413c9885996b8e10e259587c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120325618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a621801a834d707768d2048ae37ac2d61987f1040fac0c2cb24290cd368f6cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:53:19 GMT
ADD file:b96a79161ef28394a61231962b6b094cc6d55101ffa9e159bca48da52498c02f in / 
# Wed, 13 May 2020 21:53:23 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:43:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:43:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e01d6f3a75b2bb37376867eda5418ce8818270da85f9e637bc0f8131b3c49c32`  
		Last Modified: Wed, 13 May 2020 22:01:43 GMT  
		Size: 49.4 MB (49359537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4060fe458be3ad9bb5734b9386b2be633e551438da5fa5933a3caf2eef1d3084`  
		Last Modified: Wed, 13 May 2020 22:58:05 GMT  
		Size: 7.5 MB (7514215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e846164403fa17ac3349dfde468323e0107f2f131933333cec4baa962c230c`  
		Last Modified: Wed, 13 May 2020 22:58:05 GMT  
		Size: 10.2 MB (10157674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3205e486be95e4ba1ae8b2d22f6ad94505d38726a1f4f4c6cef0287bcfc053`  
		Last Modified: Wed, 13 May 2020 22:58:38 GMT  
		Size: 53.3 MB (53294192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f0dd34d43c68930cf5bb89b18ba628d94d7deb505b594581f1389375f09e0d7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115670965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602273a0e69e87a35ab1c47dfc3363a5d3ba765fddbb1182a8dab3821c5af6e8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:05:52 GMT
ADD file:465fed22a1d7f049dd801ccbefcbf7935f5c5f16afe77b6b85ec70d29f68c29a in / 
# Thu, 23 Apr 2020 01:05:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:19:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:19:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb14aff5b9321076d299a3cbc700d0f2230140c74e6d1556733e1f8a03e877e`  
		Last Modified: Thu, 23 Apr 2020 01:13:09 GMT  
		Size: 47.7 MB (47659080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9435f19640aaff696311982d6c431b3aaf1673d5f2f94be3106dc7fed67539b3`  
		Last Modified: Thu, 23 Apr 2020 04:32:42 GMT  
		Size: 7.3 MB (7257375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27313d2b2136e2d0cc017a27c4974044c01dbfdfd2f863ba921839d87686147e`  
		Last Modified: Thu, 23 Apr 2020 04:32:42 GMT  
		Size: 9.7 MB (9672965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1d15e346be4952d2bfeeaa0a5c2b14e01c0f703d6ca46ef995a185e3465efc`  
		Last Modified: Thu, 23 Apr 2020 04:33:06 GMT  
		Size: 51.1 MB (51081545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e3ba12e2235d011e4f880e849a32e67a1afde170328f47a247878a10b1bb5267
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124399187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee784a6fb5c1a9b7355bbbca5e59aad03af09ffb015da1b89212b1595b0e0eb2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:45:26 GMT
ADD file:22517e10f0b5d2760fafa2367b5a187d7ecef96291f15a746c24bfa50f756219 in / 
# Wed, 13 May 2020 21:45:29 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:27:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:28:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:28:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ad0025dc69d6f0241b2f5b614e96cef6e1fd54c9ef07b726338235b4766714ea`  
		Last Modified: Wed, 13 May 2020 21:54:40 GMT  
		Size: 50.3 MB (50328664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de8e099b34fe681d2134dc5800a33dcf2d66893cc852ada1704e600b8e46fac`  
		Last Modified: Wed, 13 May 2020 22:41:03 GMT  
		Size: 7.8 MB (7809465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2735cc8b188a094edcf282e931946b14d50022e973d985f72d13b23f3a1a810`  
		Last Modified: Wed, 13 May 2020 22:41:04 GMT  
		Size: 10.5 MB (10459849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c718f2ae452283da0b15ae79d609faee60fe428710fa0ad565afc8198c9f8a`  
		Last Modified: Wed, 13 May 2020 22:41:27 GMT  
		Size: 55.8 MB (55801209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e27a60a0a17a94274ff5ec656aec95e9b91c140b4f9eff455f68bfaf6814b9c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129411621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec484b6d9ab84cfd7ddb42cdb8d8335cfeba49403992a500c11031196b7b3519`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:41:06 GMT
ADD file:5651707cdeb4825b44f6e8cca314dc9b453dbc8c9eb87d4235235b6f6065edd9 in / 
# Thu, 23 Apr 2020 00:41:07 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:53:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:53:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:54:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6b90db2302f3b878a7e51a668d323ec00b33326362c4983e10df2b689e081dcc`  
		Last Modified: Thu, 23 Apr 2020 00:46:19 GMT  
		Size: 53.1 MB (53123711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce77e9469d5af64bf3279f4b449bc6a887436148b9e1690295858e67ff72aaa`  
		Last Modified: Thu, 23 Apr 2020 02:02:44 GMT  
		Size: 8.1 MB (8112210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea37667c03d37033a105606940d504f39ee410a6c8103822b0079326b905c448`  
		Last Modified: Thu, 23 Apr 2020 02:02:44 GMT  
		Size: 10.7 MB (10657220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c990c61d17e4dd94174396267f80a8189c9884fbbc6d7385359954821f14a9c5`  
		Last Modified: Thu, 23 Apr 2020 02:03:06 GMT  
		Size: 57.5 MB (57518480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c210941f60dd7b8389604195924be8bd9be46ddd7d8ee7ba1b85a79ef7ab8ce7
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123079536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e278b7bfe0e5085045fd0431298878eab8be225375ac2a180f4f64376c29a47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:11:00 GMT
ADD file:66d4b8806942796ca49e31a046824a633333dba393126281f5c12e26efea8e7f in / 
# Thu, 23 Apr 2020 00:11:01 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:56:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:56:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:57:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e50f308fab9e31aebf27548f07771af5a99a609ac88a60bbf74cd4f85125c24f`  
		Last Modified: Thu, 23 Apr 2020 00:19:59 GMT  
		Size: 50.7 MB (50696153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81374d42ab3f43b1e9a01bc0af60264f1036fe997a6abb2a98e309bef8774229`  
		Last Modified: Thu, 23 Apr 2020 01:13:33 GMT  
		Size: 7.5 MB (7461350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f82f88069fa53135d2819a8aa2d5e279767bf7aaf186c38c0b84e09717b63d7`  
		Last Modified: Thu, 23 Apr 2020 01:13:34 GMT  
		Size: 10.3 MB (10324460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0a1c2f8318544a7575e0094d5dceea034ae91f430e4404b8d5eec3a37b90`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 54.6 MB (54597573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47514cd12706f5649ef0c492ea69d02d591dd2b5b835163441cca8911ccaebdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136238088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b06a61df7e2bff8f4bf48743a4240ecc8a6635307d2edb86bc9fa83b7f4e7b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:38:45 GMT
ADD file:d55bd2bc22fb060f41d4316af4a741b519580bd2eaf76cbbbf9e3b88355447eb in / 
# Thu, 23 Apr 2020 00:38:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:59:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 02:00:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 02:02:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1757960a31f3d7e8a61f52b30d276d1605aa71eec0c10f82c131db13d7402512`  
		Last Modified: Thu, 23 Apr 2020 00:52:17 GMT  
		Size: 55.9 MB (55855455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6563142de6e877d15e44abd8c25bfd401d3b30ad60789123881110c1b09c3973`  
		Last Modified: Thu, 23 Apr 2020 02:26:04 GMT  
		Size: 8.4 MB (8357037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8308c7f5986dc304d470a4bb73bbf6316be522707269361fee59307548cc763`  
		Last Modified: Thu, 23 Apr 2020 02:26:04 GMT  
		Size: 11.0 MB (10975930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3548c6fd949381bbdfaf54bfbac4ddccdce7a765b0656dee4776b58726b776cc`  
		Last Modified: Thu, 23 Apr 2020 02:26:43 GMT  
		Size: 61.0 MB (61049666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:627d77fb802fa50c5e03bcff10a5732fa83965d5c509a77e6def014682041fa5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122848692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823f552524fe2196e0bbe3c6cce298774bd4c51908cc824c5eae939314e768e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:22 GMT
ADD file:e7473e4f1acf1308ed319dfcc667696c733d4173125423a8f1b2c67039e5f498 in / 
# Wed, 13 May 2020 21:43:24 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:42:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:42:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:42:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23e07cfb1ab58da76b3f9f0fdc8f5c154643a262a86037b7b6d1c26b5959a166`  
		Last Modified: Wed, 13 May 2020 21:47:43 GMT  
		Size: 50.0 MB (50002084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e62641450b73095b82a741ceaf6d58012156b7f78bf4f67b73575fb15b7a03`  
		Last Modified: Wed, 13 May 2020 22:49:18 GMT  
		Size: 7.6 MB (7600546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f55d4f91dc718f22796b06fd0faf568f26113eb77e940c765216272c8262472`  
		Last Modified: Wed, 13 May 2020 22:49:24 GMT  
		Size: 10.3 MB (10347816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4524f47c96e9e169805caad967eaff45bbd160c819137b91ec0a64201132afa`  
		Last Modified: Wed, 13 May 2020 22:49:38 GMT  
		Size: 54.9 MB (54898246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
