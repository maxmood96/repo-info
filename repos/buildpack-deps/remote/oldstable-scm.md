## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:bf17003795f6d4636c58e901f9d621e668279cb2e9a391c3cd39a75b9657763c
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e8e625f4969cc834325843bb85a11c0736551d1dd5b2910d02ec9d7981417377
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110596973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797765de7a324f1dd848875af327ef4fbf5c64a332dc159fc5d6e60874ce12dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:23:35 GMT
ADD file:82e0eb87c6ff97b66f86c9fee44884c4cf1b08f5721f36878fc7a15a125b5079 in / 
# Wed, 13 May 2020 21:23:35 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6ce7b04634a37b5c20274b3cc1469490cb28f734448d2c84d01454465418e1f`  
		Last Modified: Wed, 13 May 2020 21:29:57 GMT  
		Size: 45.4 MB (45375936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99828f061d94e903ecb427fa486d6f5876932a98b7bbe2dbeaf26d1b7a4d52c`  
		Last Modified: Wed, 13 May 2020 22:48:42 GMT  
		Size: 10.8 MB (10797470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c850eee83158cd6c3f9a0c3a52202356cce4782a6c3e17f69786722711814e11`  
		Last Modified: Wed, 13 May 2020 22:48:41 GMT  
		Size: 4.3 MB (4340177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdf93eb77fd0efd6548185bf7c7f4fa03ea8a9c9dda06ca7a07b20f5eefbfb9`  
		Last Modified: Wed, 13 May 2020 22:49:00 GMT  
		Size: 50.1 MB (50083390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6583603c8b004b9b9b94bc8b61f59a8227b01934496563dbe37600aa2bc0b101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106399377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c832ebe030c5bfaad5571ec23d07e9b6d84a68030d18d460b2a805e6074945`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:54:56 GMT
ADD file:85da223f359bde63cb0354ad866044074595630104ae55a1790b83f209585e48 in / 
# Wed, 13 May 2020 21:55:00 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:48:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:48:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:49:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e24629b52a5049ace3da69cc30167057bc65b6c050c9fe405d45685d76f1dd5`  
		Last Modified: Wed, 13 May 2020 22:03:01 GMT  
		Size: 44.1 MB (44067816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d758908a0acec534a104fc28eac5f46f7cff0b2e7d72e3d10a141c322ccc13c`  
		Last Modified: Wed, 13 May 2020 22:59:50 GMT  
		Size: 9.9 MB (9866753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccfd03f2512eb54a2aac699e7339f04dd979d0d314217d9c5522916b9b1095e`  
		Last Modified: Wed, 13 May 2020 22:59:48 GMT  
		Size: 4.2 MB (4159121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f673ada185ba56e8d7f1984fd7d09160290af02c98aad30c66617c23b100bc00`  
		Last Modified: Wed, 13 May 2020 23:00:12 GMT  
		Size: 48.3 MB (48305687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:aa44c9115156a9dc22e8e8ad8292cac55a0d8927475736e40642cc6b12591fa3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101931278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325b5c2f65c6ec37ab10f53a8a481e950b0624f81cbc8beb2d69048dd4f8a472`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:13 GMT
ADD file:af00fcaffcce2a55b74d080d33cbc9ce5bcf91faf659b887f508c06803fa64bd in / 
# Thu, 23 Apr 2020 01:07:15 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:23:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:23:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:24:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4168e46f368afa15fa660f5197fb2946df81a85078c82e37a76d2610fb3999f1`  
		Last Modified: Thu, 23 Apr 2020 01:14:13 GMT  
		Size: 42.1 MB (42101192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bc0e3bfcb00266e5034f08dae24b7862a41a069b0db0c68beb50e66983e602`  
		Last Modified: Thu, 23 Apr 2020 04:34:11 GMT  
		Size: 9.5 MB (9498287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3461f3bce5656c429f5d3faee144de5778a7f01ecd08241211c4badd34a7197b`  
		Last Modified: Thu, 23 Apr 2020 04:34:09 GMT  
		Size: 3.9 MB (3918722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2c88136aac9941bfddb6eed51d8f03cc96ee12d1164f9edf450f6ff914e414`  
		Last Modified: Thu, 23 Apr 2020 04:34:41 GMT  
		Size: 46.4 MB (46413077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d2d5efbe95b78462edec381abcd34718665cf8d7617945e28da481e457709f54
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105036255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368aee20debdb765a73bfab3a928e9f8a09a0a4ae0f0da87a88c02a09dbaa0dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:47:38 GMT
ADD file:e7776aac0b87be303e31e5947db89f835a4e17175e339ec23becf5fe4a9548a5 in / 
# Wed, 13 May 2020 21:47:41 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:32:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0480c895dd1d5b237cb931426f18706cbe8dac16e19ed583f3010f3655094efa`  
		Last Modified: Wed, 13 May 2020 21:56:03 GMT  
		Size: 43.2 MB (43158976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cf6474b5cce4b1c7c8d54d2c80e8db074f4c5d89471a009859e0c318ac7d76`  
		Last Modified: Wed, 13 May 2020 22:42:35 GMT  
		Size: 9.7 MB (9748540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f97c7d6d20cb6dbf105d3e25bea385e4b74876e9fcd4cbd49ac0e5b30c69c80`  
		Last Modified: Wed, 13 May 2020 22:42:34 GMT  
		Size: 4.1 MB (4094379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3166282442cd611f517b83932715119560eac9ad53b1356b6377568687f87a2a`  
		Last Modified: Wed, 13 May 2020 22:42:58 GMT  
		Size: 48.0 MB (48034360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:27c4bfa6ff5167e47803d8d6b1a7e382819727f3a249d47086bd6927b8fa405c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113090434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a329466851527b55ef42f015654ca5e57929af82f7898fde05257ed83ff14f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:41:58 GMT
ADD file:8306146558afbef9f6d47f7f076c52ab05fd05f1bcb39f7ff213202cd94dcd5f in / 
# Thu, 23 Apr 2020 00:41:59 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:55:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:56:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:56:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1486d1a476351a4d6b262062475bfc82bdeb3819a9b7a2f74f0f5a1e40d8ba98`  
		Last Modified: Thu, 23 Apr 2020 00:47:14 GMT  
		Size: 46.1 MB (46094994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb50803a47d4388a509a1c5fb643910f2bb60969080edae785733965267e167e`  
		Last Modified: Thu, 23 Apr 2020 02:04:12 GMT  
		Size: 10.8 MB (10818201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d191d704104098ba0e67efadfd9701aca063fcac4e1fa6fbafdf93de71d289`  
		Last Modified: Thu, 23 Apr 2020 02:04:10 GMT  
		Size: 4.6 MB (4561465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be907f8a7062232bc7eb1afb884e007e9c0c4d024c36a2f2d8ac09a177b3f19`  
		Last Modified: Thu, 23 Apr 2020 02:04:34 GMT  
		Size: 51.6 MB (51615774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3c2857f1e551e4673617cdeaaa67f06557c0d65256708be20c99430432eea83e
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108745439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14445b7142c2d533bab6a4d9bd82f16fca629607ca6676ce38591096d8a2c0ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:12:30 GMT
ADD file:076cd21ba96c7d91a0af4f716c8309a9b092cbbcd4c11f5ead2e2a91dae43736 in / 
# Thu, 23 Apr 2020 00:12:31 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:00:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:00:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:02:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3535f2056d5540d877f08809fd21e68e9db2ecaa1af00cb85b4522a16c35e414`  
		Last Modified: Thu, 23 Apr 2020 00:22:41 GMT  
		Size: 45.0 MB (45048818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e3b44e91d14a9d07b503cf60d0ed04ee5d11eebacef157dabfa2c6d4a62fed`  
		Last Modified: Thu, 23 Apr 2020 01:17:13 GMT  
		Size: 9.8 MB (9826234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecb2ad4ea35a7a01e57dfa74ff5af3cdcfad24105d385a7b475a3d0a9e9f4e1`  
		Last Modified: Thu, 23 Apr 2020 01:17:10 GMT  
		Size: 4.4 MB (4394838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b206fda6aa600e14c689d94764f50425c38308c250f177746840c0618364fe90`  
		Last Modified: Thu, 23 Apr 2020 01:18:05 GMT  
		Size: 49.5 MB (49475549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0ab2c266378bd2a744942599bd988b7fa1cc3ae405862850c132ec9228b2ba47
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110026299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49822f92ff2b7ae176e9150311435f6f22669fdcf26dfeeb63caa263df47c3d9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:41:48 GMT
ADD file:b7acf2b2b981f87e5f10fe000e64273a621d414c7434c4168273a1639751a765 in / 
# Thu, 23 Apr 2020 00:41:52 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 02:11:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 02:12:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4cde65f7be4b1cfe64760c957dd5bd9fcb4d8704337ab159a9e83eae83a02b4c`  
		Last Modified: Thu, 23 Apr 2020 00:54:57 GMT  
		Size: 45.6 MB (45646096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc277ea268a02dce4b6c95c60f39a5735b07bbc2bb2eb883d1833f97c83877`  
		Last Modified: Thu, 23 Apr 2020 02:28:16 GMT  
		Size: 10.0 MB (10002410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c03e97e8a114fd2155b807671cf9f573cd6d3d01aa7c301a26d8249ea6f84a`  
		Last Modified: Thu, 23 Apr 2020 02:28:14 GMT  
		Size: 4.3 MB (4296683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cae94e17fa6dafc744e871ffe091f16bd6dc516d23edb6242e063247a308a11`  
		Last Modified: Thu, 23 Apr 2020 02:28:55 GMT  
		Size: 50.1 MB (50081110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:10d7ad57461578de472af15cc7e041415b559c4d83f84676d087d5c48394a932
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110442091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfc571f2635047825ecca94e7131f84d3b95cfd70bbb3a896494c83e608005f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:44:18 GMT
ADD file:80db5381a461bb249455c6e92a06f91a777c0d8db654106cc55f91d6252c3c44 in / 
# Wed, 13 May 2020 21:44:20 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:43:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:44:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:44:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dd38adf1f4e3b358b79e0f6559fa135ec376d7abbcc3f8bf0b62a2d19d972cbc`  
		Last Modified: Wed, 13 May 2020 21:48:31 GMT  
		Size: 45.2 MB (45232705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b7499c91144099ccb386aa415835bab026fb0216cd29e9e2b0ef701d9f9edc`  
		Last Modified: Wed, 13 May 2020 22:50:12 GMT  
		Size: 10.3 MB (10325615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89032869e1382e045958dbcc66285bcdc50c4540833a40f19b218759847548a5`  
		Last Modified: Wed, 13 May 2020 22:50:11 GMT  
		Size: 4.4 MB (4372600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40a216015c652fe4455523b0c4b2447eb65f5f5c502d88b116fe834e2041e7c`  
		Last Modified: Wed, 13 May 2020 22:50:26 GMT  
		Size: 50.5 MB (50511171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
